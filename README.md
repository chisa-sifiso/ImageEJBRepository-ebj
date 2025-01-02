<h1>Image Management EJB Project</h1>

<p>This project is an Enterprise Java Beans (EJB) application designed to manage image entities. The application is built using Java Persistence API (JPA) to handle the persistence of image data, including storing image metadata and binary content.</p>

<h2>Project Structure</h2>

<p>The project follows a structured package organization:</p>

<ul>
  <li><strong>za.ac.tut.model</strong>: Contains the <code>Image</code> entity class that represents an image with attributes like <code>id</code>, <code>name</code>, and <code>image_source</code>.</li>
  <li><strong>za.ac.tut.bl</strong>: Includes the business logic classes, such as <code>AbstractFacade</code>, <code>ImageFacade</code>, and <code>ImageFacadeLocal</code> for handling image-related operations.</li>
</ul>

<h2>Features</h2>

<ul>
  <li><strong>Image Entity:</strong> The <code>Image</code> class is a JPA entity that represents an image stored in the database.</li>
  <li><strong>CRUD Operations:</strong> Provides basic Create, Read, Update, and Delete (CRUD) operations for managing images in the database.</li>
  <li><strong>Binary Image Storage:</strong> Stores image data as binary content (byte array) in the database using the <code>@Lob</code> annotation.</li>
</ul>

<h2>Getting Started</h2>

<h3>Prerequisites</h3>

<ul>
  <li>Java Development Kit (JDK) 8 or higher</li>
  <li>Java EE-compatible application server (e.g., GlassFish, WildFly)</li>
  <li>NetBeans or another IDE with EJB support</li>
  <li>MySQL or another relational database for persistence</li>
</ul>

<h3>Installation</h3>

<ol>
 
  
  <li>Open the project in your preferred IDE.</li>
  
  <li>Configure the database connection in <code>persistence.xml</code> to match your database settings.</li>
  
  <li>Deploy the application on a Java EE-compatible server.</li>
</ol>

<h2>Usage</h2>

<p>This application can be used for managing images in a database through an EJB-based architecture. You can integrate this backend with a frontend application to provide an interface for uploading and managing images.</p>

<h3>Example Code</h3>

<p>Here's an example of how to use the <code>ImageFacade</code> to add a new image:</p>

<pre><code>
@Inject
private ImageFacade imageFacade;

public void addImage(String name, byte[] data) {
    Image image = new Image(name, data);
    imageFacade.create(image);
}
</code></pre>

<h2>Contributing</h2>

<p>Contributions are welcome! Please fork the repository and submit a pull request.</p>

<h2>License</h2>

<p>This project is licensed under the MIT License - see the <code>LICENSE</code> file for details.</p>
<p>Developed by Sifiso Vinjwa </p>
<h2>Contact</h2>


<p>For any inquiries or issues, please reach out to the project maintainer at <a href="mailto:your-email@example.com">sifisovinjwa1@gmail.com</a>.</p>
