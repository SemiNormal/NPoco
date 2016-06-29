Getting Started
===============

NPoco is installed via nuget using the following command::

    PM> Install-Package NPoco 

Your first query
================

.. code-block:: csharp

  public class User 
  {
      public int UserId { get;set; }
      public string Email { get;set; }
  }
  
  using (IDatabase db = new Database("connStringName")) 
  {
      List<User> users = db.Fetch<User>("select userId, email from users");
  }
