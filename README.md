# LucidChartSoftware
LucidChart Software is a Class Diagrams software for Bitbucket, an automated feature that makes class diagrams from repositories. 

# Goal: 
The process of creating class diagrams can create more problems than it solves, and it takes hours of tedious work to build the diagram initially, and the diagram is only useful as long as you keep it up to date. If there is a team of engineers adding and changing code daily, class diagrams just have not been practical. To create way to remove the tedium and generate class diagrams directly from source code.
# Overview: 
My friends and I decided to create a solution, a software called LucidChart and with the help of Atlassian (founder of Bitbucket), we were able to further the LucidChart to become an built-out feature for Bitbucket.
This Bitbucket add-on allows you to automatically generate UML class diagrams from your code repository. Once generated, these diagrams are available to everyone with read access to the repository, and you can:
1	Click class members within your diagram and jump directly to their definitions in the source code.
2	Update your diagram in one click when you push new code.
3	Open a copy of the diagram in Lucidchart if you want to make changes or share it outside of Bitbucket 
Whether you work alone or on a team, you can see your entire project architecture, including class dependencies and relationships, at a glance. The add-on currently works best with Java, with limited support for C++, C#, ObjectiveC, Go, and Python, and Ruby. 
We used ctags to extract symbol information from source code. From there, we created a dependency graph and turn it into a Lucidchart diagram. Finally, we used the hierarchy layout in Lucidchart to space out the elements perfectly, even for large diagrams. This add-on was developed using Atlassian Connect for Bitbucket Cloud. We were also able to try out the new API Proxy feature and save hours of development time. Let Lucidchart do the hard work. LucidChart is a powerful software that reduces time spent on mapping out classes, architecture, structures of code. 
# Tools: 
Built with Scala, JavaScript, Bitbucket, Atlassian-Connect, Bitbucket-Api-Proxy, C++, C#, ObjectiveC, Go, and Python, and Ruby


Relate
http://lucidchartsoftware.github.io/relate/

Build Status Maven Version Join the chat at https://gitter.im/lucidchartsoftware/relate

Relate is a lightweight, blazingly fast database access layer for Scala that abstracts the idiosyncricies of the JDBC while keeping complete control over the SQL.


# Install
```javascript
libraryDependencies += "com.lucidchart" %% "relate" % "<version>" `

# Examples 
```javascript
 val ids =  Seq(1, 2, 3)
sql"SELECT email FROM users WHERE id in ($ids)".asMap { row => 
  row.long("id") -> row.string("email")
}
```

```javascript 
val id = 4
val email = "github@lucidchart.com"
sql"INSERT INTO users VALUES ($id, $email)".execute() 
```



