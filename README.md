ScriptCs.EasyHttp
=================

A scriptcs script pack for performing very easy and declarative http requests in your scripts with no boilerplate code needed.

Using this script pack you can write very simple scripts similar to this:


	public class Notification
	{
		public string Message {get; set;}
		public string SenderName {get; set;}
	}
	var notificationToSend = new Notification { Message = "Merry christmas!", SenderName = "Santa"};
	var http = Require<EasyHttp>();
	var result = http.PostJson("http://your.site.com/api/notification", notificationToSend);
	Console.WriteLine("Response status code: " + result.StatusCode);


The script pack also has the Json.NET namespace available so you can make use of different Json.NET serialization possibilities (e.g. [JsonIgnore]) to suit your needs. 
