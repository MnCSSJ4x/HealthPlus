# HealthPlus - An End To End HIS Application For Busy Doctors

**Contributors**

> **_Karanjit Saha_**\
> [LinkedIn](https://www.linkedin.com/in/karanjit-saha-65a02122b/)\
> [GitHub](https://github.com/KaranjitSaha)

> **_Chinthan Chandra_**\
> [LinkedIn](https://www.linkedin.com/in/chinthanchandra/)\
> [GitHub](https://github.com/Chinthan23)

> **_Darshak Jivrajani_**\
> [LinkedIn](https://www.linkedin.com/in/darshak-jivrajani-296475227/)\
> [GitHub](https://github.com/Darshak11)

> **_Monjoy Narayan Choudhury_**\
> [LinkedIn](https://www.linkedin.com/in/monjoy-narayan-choudhury-a424b3200/)\
> [GitHub](https://github.com/MnCSSJ4x)

> **_Tejas Sharma_**\
> [LinkedIn](https://www.linkedin.com/in/tejassharma15/)\
> [GitHub](https://github.com/Tejsharma15)

<h2>Scope of the product</h2>

The aim of the project is to build a Hospital Information System which
is primarily for the ease of use for the doctor.

<h2>High Level Requirements</h2>

> 1\. **Registration Desk Worker**: General hospital registration desk
> work like: Adding new patient, As-signing doctors, Updating patient
> information, Reassigning doctors, Removing patients and some other
> functionalities.
>
> 2\. **Doctor**: We use a tablet app to accommodate on-duty doctors who
> will be on the move when the use case of the HIS is realized, using
> which he will be able to add logs using different input methods (pen
> input), can update patient, can update prescription and in general any
> other requirements a doctor has while reviewing a patient.
>
> 3\. **Shift Manager/Head Nurse**: The HIS will be used by the head
> nurse to obtain patient logs, discharge patients, update patient logs,
> change severity, update prescriptions, and some other day-to-day tasks
> of a head nurse in the hospital.
>
> 4\. **Pharmacist**: The pharmacist will be able to access patient
> prescriptions using the HIS.
>
> 5\. **Nurse**: Nurse will have a tablet app with the arguments for it
> similar to a doctor but with a lower access level to that of a doctor.

<h2>Use Case(s)</h2>

> **Use Case Diagram for Doctor -**
>
> ![](vertopal_c5f67f4f10f14c9ab9e59323c57b0c7a/media/image3.png)

> **Use Case Diagram for Nurse -**
>
> ![](vertopal_c5f67f4f10f14c9ab9e59323c57b0c7a/media/image4.png)

> **Use Case Diagram for Head Nurse -**
>
> ![](vertopal_c5f67f4f10f14c9ab9e59323c57b0c7a/media/image5.png)

> **Use Case Diagram for Admission Desk User -**
>
> ![](vertopal_c5f67f4f10f14c9ab9e59323c57b0c7a/media/image6.png)

> **Use Case Diagram for Pharmacist -**
>
> ![](vertopal_c5f67f4f10f14c9ab9e59323c57b0c7a/media/image7.png)

<h2>System Architecture</h2>

> ![](vertopal_c5f67f4f10f14c9ab9e59323c57b0c7a/media/image2.png)

> Keeping in mind the requirements and functionalities to be
> implemented, we have decided to follow a micro-services architecture.
> The backend software can be split into 3 services -
>
> 1\. **EMR Service** - This service has the responsibility to handle
> patient records.
>
> 2\. **Dashboard Service** - This service is responsible to handle
> dashboard related features for the actors involved - doctor, nurse,
> admission desk user, pharmacist.
>
> 3\. **Admin Service** - This service is for the admin who has control
> over the system. It provides functionality like adding/removing an
> employee.
>
> Apart from this, we have an **authentication and authorization
> service** and an **API-Gateway**. Incoming requests are sent to the
> API Gateway, which will call the authentication and authorization
> module. Upon authenticating and authorizing the user, the gateway
> routes the request to the appropriate service.

<h2>Database Schema</h2>

> ![](vertopal_c5f67f4f10f14c9ab9e59323c57b0c7a/media/image1.png)

<h2> UI Design</h2>

**Registration Desk**

Home Screen
![](vertopal_c5f67f4f10f14c9ab9e59323c57b0c7a/media/image10.png)

![](vertopal_c5f67f4f10f14c9ab9e59323c57b0c7a/media/image11.png)

Login

![](vertopal_c5f67f4f10f14c9ab9e59323c57b0c7a/media/image12.png)

Landing

![](vertopal_c5f67f4f10f14c9ab9e59323c57b0c7a/media/image13.png)

Registration Desk view for patients registered
![](vertopal_c5f67f4f10f14c9ab9e59323c57b0c7a/media/image18.png)

Registration Desk can now allocate consultations to doctors.
![](vertopal_c5f67f4f10f14c9ab9e59323c57b0c7a/media/image19.png)

Viewing Patient Details
![](vertopal_c5f67f4f10f14c9ab9e59323c57b0c7a/media/image15.png)

**Tablet Application**

Shift Managers View on Android Tablet
![](vertopal_c5f67f4f10f14c9ab9e59323c57b0c7a/media/image16.png)

Viewing Admitted Patient Details on an Android Tablet
![](vertopal_c5f67f4f10f14c9ab9e59323c57b0c7a/media/image17.png)

Nurse View for Nurses on Tablet
![](vertopal_c5f67f4f10f14c9ab9e59323c57b0c7a/media/image21.png)

Nurse details modal
![](vertopal_c5f67f4f10f14c9ab9e59323c57b0c7a/media/image22.png)

Attending Patient
![](vertopal_c5f67f4f10f14c9ab9e59323c57b0c7a/media/image26.png)

Editing Prescription
![](vertopal_c5f67f4f10f14c9ab9e59323c57b0c7a/media/image25.png)

**Pharmacists**

Editing Prescription
![](vertopal_c5f67f4f10f14c9ab9e59323c57b0c7a/media/image27.png)

**Shift Manager**

Viewing Logs
![](vertopal_c5f67f4f10f14c9ab9e59323c57b0c7a/media/image28.png)

<h2>Security and Technical Safeguards</h2>

**Securing Patient Data with Spring Security and Custom Verifications**

The Hospital Information System (HIS) prioritizes the security and
privacy of sensitive patient data. To achieve this, Spring Security, a
mature framework for authentication and authorization, was meticulously
integrated into the system's architecture. This section delves into the
technical details of how Spring Security was implemented alongside a
custom verification layer to establish a robust access control system.

Spring Security leverages a modular approach, allowing for the
configuration of various security aspects. We utilized Spring Security's
core features like:

> • Authentication: We adopted a token-based authentication mechanism
> (e.g., JWT) to manage user sessions. Users login with their
> credentials, and upon successful verification, a token is issued
> containing user information and role claims. Subsequent requests
> include this token within the authorization header, enabling Spring
> Security to validate the user's identity and role.
>
> • Authorization: RBAC was implemented using Spring Security's
> '@PreAuthorize' annotation or method-level security configuration.
> Developers directly specify the required role for accessing a
> particular API or functionality within the system. Spring Security
> intercepts the request and verifies if the user's associated role
> grants them the necessary permission. Additionally, Spring Security
> provides granular control through its own permission and authority
> mechanisms, allowing for the creation of fine-grained access controls
> based on specific functionalities within the system.

Beyond standard role-based access control, a custom verification layer
was developed to further enhance security. This layer intercepts
authenticated requests and performs additional checks before granting
access to specific APIs or functionalities within the HIS. Here's how
the custom verification layer operates:

> • User Status Check: The layer retrieves user information from an
> external user management system (e.g., HR database) and verifies if
> the user's account is active within the hospital system. This ensures
> that even a user with valid credentials and a designated role cannot
> access the system if their employment status has been terminated or
> their account deactivated.
>
> • Data/Service Access Restriction: The verification layer can be
> extended to incorporate additional access control rules based on
> specific data or services being accessed. This can involve checking
> the user's department affiliation, patient location, or other relevant
> criteria. For instance, a nurse might only have access to view medical
> records for patients assigned to their specific ward. This granular
> control ensures that users can only access data and functionalities
> relevant to their assigned duties and responsibilities.

By integrating Spring Security with a custom verification layer, the HIS
establishes a multi-layered security approach. This ensures that only
authorized users with active accounts can access the system, and further
restricts access based on user roles and potentially even departmental
affiliations or patient location. This comprehensive approach safeguards
sensitive patient data and minimizes the risk of unauthorized access.

<h2> Tech Stack Used </h2>

> For WebApp we use the following frontend framework:
>
> 1\. React as the base framework for frontend. The reasons were the
> familiarity of the team members and the extensive documentation
> present.
>
> 2\. Recoil: As a state management library for having a
> uniform state handling mechanism which is not possible with
> react-context.
>
> 3\. Tailwind.css: As the CSS library. This helps in writing shorthand
> CSS inline while rescuing us from the curse of naming CSS classes
> while it becomes significantly easier to convert tailwind CSS
> statements to regular CSS statements which would be required while
> implementing the same design system in react native.
>
> 4\. React-Router: For routing-related queries.

> For the TabletApp we use the following frameworks:
>
> 1.  React Native as our familiarity with react can help us prototype screens faster than using other libraries.
> 2.  React Navigation: which is the equivalent of React-routers for native. In this, we are using the native stack navigator.

> Backend Implementation Details:
> Our backend leverages Spring Boot for constructing various APIs and ensuring a robust, multi-layered security architecture. Additionally, we've integrated Java's Jasypt library to encrypt sensitive user data, enhancing the security of our system. For graphic processing, particularly SVG images and other formats, we utilize Apache Batik libraries, which support our needs for handling complex visual data.

> Database Configuration:
> We utilize MySQL as our database solution to store hospital records and user data efficiently. The connection between our backend and the MySQL database is facilitated through the JDBC driver, ensuring reliable data management and integration.

<h2>Codebase</h2>

**Backend**

> • [EMR Service](https://github.com/Tejsharma15/MedicalRecordService)
>
> • [Authentication Service](https://github.com/Darshak11/HIS)
>
> • [Dashboard Service](https://github.com/Darshak11/HIS-Authentication)

**Frontend**

> • [Tablet Application](https://github.com/MnCSSJ4x/tabletApp)
>
> • [Registration Desk Web Application](https://github.com/MnCSSJ4x/his-registration-desk-frontend)

**API Documentation**

Available on [Postman](https://documenter.getpostman.com/view/21648989/2sA2rCV2H4).
