# Node-SELECT-INSER-UPDATE-DELETE-Connection-
/MySQL Query.txt



--------------------------------------------------------------------------------------------------------
 SQL Insert Command Query
--------------------------
var mysql = require('mysql2');  
  var con = mysql.createConnection({  
    host: "localhost",  
    user: "root",  
    password: "",  
    database: "akash1"  
    });  
    con.connect(function(err) {  
    if (err) throw err;  
    console.log("Connected!");  
    var sql = `INSERT INTO login (id, username, password) VALUES (null, 'Dhongi BABA','BSDK')`;  
       con.query(sql, function (err, result) {  
      if (err) throw err;  
      console.log("1 record inserted");  
  }); 
  }); 
  });

--------------------------------------------------------------------------------------------------------
  SQL DELETE Command Query 
------------------------------
  app.get('/delete', function (req, res) {  

  var mysql = require('mysql2');  
  var con = mysql.createConnection({  
    host: "localhost",  
    user: "root",  
    password: "",  
    database: "akash1"  
    });  
    con.connect(function(err) {  
    if (err) throw err;  
    console.log("Connected!");  
    var sql = `DELETE FROM login WHERE id=18`;  
    con.query(sql, function (err, result) {  
    if (err) throw err;  
    console.log("Number of records deleted: ");   
}); 
}); 
  });
----------------------------------------------------------------------------------------------------------
  SQL SELECT Command Query 
------------------------------
app.get('/select', function (req, res) {  

  var mysql = require('mysql2');  
  var con = mysql.createConnection({  
    host: "localhost",  
    user: "root",  
    password: "",  
    database: "akash1"  
    });  
    con.connect(function(err) {  
    if (err) throw err;  
    console.log("Connected!");  
    var sql = `SELECT * FROM login `;  
       con.query(sql, function (err, result) {  
      if (err) throw err;  
      console.log("1 record inserted");  
      res.send(result) ;
}); 
}); 
  });

--------------------------------------------------------------------------------------------------------
  SQL UPDATE Command Query 
------------------------------
  app.get('/update', function (req, res) {  

  var mysql = require('mysql2');  
  var con = mysql.createConnection({  
    host: "localhost",  
    user: "root",  
    password: "",  
    database: "akash1"  
    });  
    con.connect(function(err) {  
    if (err) throw err;  
    console.log("Connected!");  
var sql = `UPDATE login SET username = 'Deepak Jadhav' WHERE id=3`;  
con.query(sql, function (err, result) {  
if (err) throw err;  
console.log(" record(s) updated"); 
}); 
}); 
  });

----------------------------------------------------------------------------------------------------------
