---
layout: post
author: Sophie Goldman
excerpt_separator: <!--more-->
title: Encoding the Lending Library
---

### Motivation and Background
For this digital tools assignment, I was interested in encoding a document that contained informational data, such as records or lists. I also hoped to find a source that contained many attributes within one record. While searching the Princeton University Library collections for potential documents, I came across the [Sylvia Beach Papers](https://findingaids.princeton.edu/catalog/C0108) and the accompanying [Shakespeare and Company Project](https://shakespeareandco.princeton.edu/) by Princeton's Center for Digital Humanities.  Sylvia Beach (1887 - 1962) owned and ran the Shakespeare and Company bookstore and lending library in Paris, France, serving members of European and American literary communities from 1919 to 1941. The Shakespeare and Company Project maintains a database of the books, members, and documents related to the library, using materials sourced from the Sylvia Beach collections. I was drawn to the lending library cards, which were used to document each library member's borrowed materials. These cards contained many of the attributes I was hoping to tag, including names, addresses, book titles, and dates. Additionally, the layout of the cards led me to consider interesting questions on how to encode their contents using XML.

<!--more-->

### Ellen Wright
Through the Shakespeare and Company Project website, I selected the collection of [all cards associated with Ellen Wright](https://shakespeareandco.princeton.edu/members/wright-ellen/cards/0d89fdbb-a48a-4bfa-8690-c53234d02331/),  an American living in Paris with her husband, the acclaimed African-American author Richard Wright. There are two cards associated with Wright, pictured below:

![Front of Card 1](https://iiif.princeton.edu/loris/figgy_prod/13%2Fe8%2F39%2F13e839f94ac344f7bc0a5793c5c4df80%2Fintermediate_file.jp2/full/450,/0/default.jpg)

![Front of Card 2](https://iiif.princeton.edu/loris/figgy_prod/93%2Fdd%2F4d%2F93dd4d3a5fa048ed8e88685bd2df1e0c%2Fintermediate_file.jp2/full/450,/0/default.jpg)

Though there is overlap between the information on the two cards, I chose to encode them both. I did not encode the backs of the cards, as the first card is blank on the reverse, and the other side of second card is an advertisement from the Princeton Bank and Trust Company.

### Important Elements
When encoding these cards, I began by identifying the key items that formed the basis of the borrowing records: the borrow date, the book title, and the return date. I also encoded the heading on the top of each card, which contained the library member's name and home address. Another key aspect of these cards were the other library members mentioned, many of whom were accomplished authors themselves, such as Richard Wright and Gertrude Stein. Finally, I noted that the handwritten text on each card changed color multiple times, a result of the process by which the card was updated over the span of months each time Wright borrowed or returned books. Though the particular colors used may not have much significance, they provide evidence for the ways the card changed over time. 

I used the transcriptions of book titles and dates on the Shakespeare and Company Project database to confirm my reading of the cards. However, as I wanted to encode the card in full, I also had to parse the notes and other markings on each card.

### The XML Encoding

``` <div type='all-lending-library-cards'>
	<div type="lending-library-card">
		<side type="front">
			<heading>
				<text color="blue">
					<member-name>Mrs Richard WRIGHT</member-name>
					<address>14 rue M. le Prince, Paris VI</address>
				</text>
			</heading>
			<borrowing-record>
				<text color="blue">
					<date-start>Sept 19 1949</date-start>
					<title>The Pasquier Chronicles</title>
					<date-end>Oct 26</date-end>
					<title>Christine</title>
					<date-end>Oct 26</date-end>
					<title>Lafcadio's Adventures</title>
					<date-end>Oct 26</date-end>
					<date-start>Oct 26</date-start>
					<title>The Gambler</title>
					<date-end>Dec 10</date-end>
					<title>Walter Rathenau his life and work by	
						<author>Count Harry Kessler</author>
						<publication-info>(
							<publisher>Gerald Howe Ltd</publisher>
							<address>23 Soho Square London</address>
							<year>1929</year>
							)
						</publication-info>
					</title>
					<note>O.P. to send to
						<member-name>Richard Wright</member-name>
					</note>
				</text>
				<text color='black'>
					<note>returned			
						<date-end>June 1952</date-end>
						By
						<member-name>R. W.</member-name>
					</note>
				</text>
				<text color="blue">
					<date-start>Dec 13</date-start>
					<title>Middle of the Journey</title>
					<date-end>Dec 19</date-end>
					<note>
						<circled>
							<member-name>Ellen Wright</member-name>
							<unclear>pg 81 to SB</unclear>
						</circled>
					</note>
					<title>Heidegger</title>
					<date-start>Dec 19</date-start>
					<title>Party Going</title>
				</text>
				<text color='light-blue'>
					<date-end>Jan 9</date-end>
				</text>
				<text color='blue'>
					<title>Goodbye to all that</title>
				</text>
				<text color='light-blue'>
					<date-end>Jan 9</date-end>
					<date-start>Jan 9</date-start>
				</text>
				<text color='black'>
					<unclear>19--</unclear>
				</text>
				<text color='light-blue'>
					<title>Little Women - Little Women Married</title>
				</text>
				<text color='blue'>
					<date-end>Feb 4</date-end>
				</text>
				<text color='light-blue'>
					<title>Mr Norris Changes Trains</title>
				</text>
				<text color='blue'>
					<date-end>Feb 4</date-end>
				</text>
				<text color='black'>
					<date-start>Nov 3 1946</date-start>
					<title>A Serial Universe</title>
					<note>returned</note>
					<note>(Composition
						<member-name>Gertrude Stein</member-name>
						. gave copy to
						<member-name>R W</member-name>)
					</note>
					<date-start>June 20 1946</date-start>
					<title>The Negro in our History</title>
					<title>Proletarian Literature</title>
				</text>
			</borrowing-record>
		</side>
		<side type="reverse"></side>
	</div>
	<div type="lending-library-card">
		<side type="front">
			<heading>
				<text color="purple">
					<member-name>Ellen Wright</member-name>
				</text>
				<text color="black">
					<address>14 rue M. le Prince</address>
				</text>
			</heading>
			<borrowing-record>
				<text color="purple">
					<date-start>Sept 19 1949</date-start>
					<title>The Pasquier Chronicles</title>
				</text>
				<text color="blue">
					<date-end>Oct 26</date-end>
				</text>
				<text color="purple">
					<strikethrough>
						<title>The Close</title>
					</strikethrough>
					<title>Christine</title>
				</text>
				<text color="blue">
					<date-end>Oct 26 1949</date-end>
				</text>
				<text color="purple">
					<title>Lafcadio's Adventures</title>
				</text>
				<text color="blue">
					<date-end>Oct 26 1949</date-end>
					<date-start>Oct 26 1949</date-start>
					<title>The Gambler</title>
					<date-start>Oct 26</date-start>
					<title>Walter Rathenau his life &amp; work by
						
						<author>Count Harry Kessler</author>
						<publication-info>
							<publisher>Gerald Howe Ltd</publisher>
							<address>23 Soho Square London</address>
							<year>1929</year>
						</publication-info>
					</title>
				</text>
				<text color="faded-blue">
					<note>
						<unclear>Also wants	
							<author>Christina</author>
						</unclear>
						&amp;	
						<author>Morand's</author>
						Books
					</note>
				</text>
			</borrowing-record>
		</side>
		<side type="reverse"/>
	</div>
</div>
```
