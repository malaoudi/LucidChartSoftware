# LucidChartSoftware 
An add on feature to Bitbucket that automatically generates interactive diagrams and maps out classes in a source code. It can naviagte across the source code, imports/segments/files and between members and functions.  
# Goal: 
Class diagrams provide a valuable overview of source code—with these diagrams, developers don’t have to jump between files and read thousands of lines of text to learn the system or find where they need to implement new code. Yet, many engineers learn how to create UML class diagrams in school and then never use them again. Even at Lucid, where they build tools for visual communication, they haven’t created class diagrams to document our software. Why? <br/>
The process of creating class diagrams can create more problems than it solves, and it takes hours of tedious work to build the diagram
initially, and the diagram is only useful as long as you keep it up to date. If there is a team of engineers adding and changing code daily, class
diagrams just have not been practical. To create way to remove the tedium and generate class diagrams directly from source code.
# Overview: 
LucidChart is n built-out feature for Bitbucket. This Bitbucket add-on allows you to automatically generate UML class diagrams from your code repository. Once generated, these diagrams are
available to everyone with read access to the repository, and you can:<br/>
• Click class members within your diagram and jump directly to their definitions in the source code.<br/>
• Update your diagram in one click when you push new code.<br/>
• Open a copy of the diagram in Lucidchart if you want to make changes or share it outside of Bitbucket
Whether you work alone or on a team, you can see your entire project architecture, including class dependencies and relationships, at a glance.
The add-on currently works best with Java, with limited support for C++, C#, ObjectiveC, Go, and Python, and Ruby.
We used ctags to extract symbol information from source code. From there, a dependency graph was created and turn it into a Lucidchart diagram.
Finally, the hierarchy layout was used in Lucidchart to space out the elements perfectly, even for large diagrams. This add-on was developed
using Atlassian Connect for Bitbucket Cloud. The new API Proxy feature saved hours of development time. Let
Lucidchart do the hard work. LucidChart is a powerful software that reduces time spent on mapping out classes, architecture, structures of code.
# Tools: 
Built with Scala, JavaScript, Bitbucket, Atlassian-Connect, Bitbucket-Api-Proxy, C++, C#, ObjectiveC, Go, and Python, and Ruby

# Relate
http://lucidsoftwarechart.github.io/relate/

[![Build Status](https://travis-ci.org/lucidsoftware/relate.svg)](https://travis-ci.org/lucidsoftware/relate)
[![Maven Version](https://img.shields.io/maven-central/v/com.lucidchart/relate_2.12.svg)](https://search.maven.org/#search%7Cga%7C1%7Cg%3A%22com.lucidchart%22%20AND%20a%3A%22relate_2.12%22)
[![Join the chat at https://gitter.im/lucidchartsoftware/relate](https://badges.gitter.im/lucidsoftware/relate.svg)](https://gitter.im/lucidsoftware/relate?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

Relate is a lightweight, blazingly fast database access layer for Scala that abstracts the idiosyncricies of the JDBC while keeping complete control over the SQL.

## Install

```scala
libraryDependencies += "com.lucidchart" %% "relate" % "<version>"
```

## Examples

```scala
val ids = Seq(1, 2, 3)
sql"SELECT email FROM users WHERE id in ($ids)".asMap { row =>
  row.long("id") -> row.string("email")
}
```

```scala
val id = 4
val email = "github@lucidchart.com"
sql"INSERT INTO users VALUES ($id, $email)".execute()
```

# Demonstration
www.vimeo.com/230209219


