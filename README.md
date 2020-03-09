# java-code

package lab.aiub;

public class Document {
	String a;
	String t;
	int n=0;
	
	public Document(String a, String t) {
		super();
		this.a = a;
		this.t = t;
	}
	public Document() {
		super();
	}
	@Override
	public String toString() {
		return "Document [a=" + a + ", t=" + t + "]";
	}
	void createCopies (int n)
	{
		this.n=this.n+n;
		
	}
	void sellCopies (int n)
	{
		
		if (n>this.n)
		{
			System.out.println("Number of available copies = 0");
		}
		else 
			this.n=this.n-n;
	}
	String getAuthor()
	{
		return a;
	}
	String getTitle()
	{
		return t;
	}
	int getCopies()
	{
		return n;
	}
	
}

package lab.aiub;

public class TestDocument {
	
    public static void main(String[] args) {
       Document d1 = new Document("Mario Rossi", "My first document");
       System.out.println(d1);
       d1.createCopies(10);
       d1.sellCopies(5);
       System.out.println(d1);
       System.out.println("Information on the document:");
       System.out.println("Author: " + d1.getAuthor());
       System.out.println("Title:  " + d1.getTitle());
       System.out.println("Copies: " + d1.getCopies());
    }
}

