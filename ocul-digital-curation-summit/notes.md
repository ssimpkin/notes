#Introduction
###Nick Ruest, York  

What could we preserve? What rights do we have to the data (in the case of GIS data, maybe not). What's within scope?  
What can our infrastructure support? (size, type) -- jpeg derivatives, tiff masters, etc. Need to budget for equipment and storage.  

Once you've IDed which objects to preserve:  

Preservation action plan for different types of objects. These include preferred formats. Policy should be consistent and predictable and based on a plan!  

Planning steps:  
* What is your general approach (preservation strategic plan -- what do we care about? what are our considerations? Includes ways to evaluate fixity.)
* What tools are available (archival formats, format normalization, integrity monitoring)
* How do we apply said tools (use cases, write a spec)  

Other considerations: are there different levels of preservation we can offer? For example, WAV and FLAC can be fully preserved, MP3s preserved at the bit-level.  

Another document is the digital preservation implementation plan. Includes guidelines for naming files, fixity checking schedule and methods, as well as preservation levels (bit-level, full, none, etc.)  

Audience vote: let's look at a preservation action plan for audio content at York. This includes content formats, what a SIP submission includes, how files will be described (MODS), FITS datastream upon ingest. Includes information on what's not included, any normalization or metadata normalization, as well as acceptable formats for full-level preservation.  

Parting thoughts: ethos of open source software -- release early, release often. Preservation documentation is all in github in markdown for editing and to allow contributors to submit pull requests.  

#Project management for digitization programs: implementing sustainable projects
###Jess Posgate and Loren Fantin, Our Digital World  

Always keep your objectives and mission in mind. 4 Ws and 1 H. Need to identify the objects but also the priorities. Who's your audience? How are you going to do it?  

Breaking it down: the project plan  

* Putting together the plan or proposal (integration, scale, budget)
* What you need to get the job done (equipment, staff)
* Your digital collection (standards, technology, display)  

Projects should be part of larger program plans.  

Digitization is not just scanning! Must consider all stages in the process, risks, contingencies, etc. Going through this process will also allow you to consider the workflow.   
Typical project expenses:  
* 50% staffing
* 20% outsourcing
* 20% software, hosting, user interface
* 8% equipment
* 2% promotion  

To start budgeting for staffing, consider tasks and time required per task/per item. Total = number of items x hours x salary.  

Digitization equipment  

* Hardware (for 2D or 3D objects, conversion devices for AV materials)
* Software (image editing, OCR, audio editing, video editing)

Digital files - need to make sure you have consistent policies/guidelines on naming conventions and chosen metadata schemas. Good file names are under 32 characters to prevent truncation. Storage (master files, vs. web/derivatives), hosting != storage, storage options (server, hard drives, DVD -- consider lifecycles), LOCKSS.  

Evaluation and assessment - regular internal reports and tracking documents. Documentation!  

Metadata application profiles are very important. Let your staff know which metadata elements have to be used, how fields should be completed, which ones can be repeated, etc. Better & smarter metadata will be able to do more later on. Example of KML "smart data" that might allow mapping applications later on.  

Rights and copyright - determine copyright status of EVERY object (ownership versus copyright). In-house tracking (copyright status, copyright owner, donor, permissions, etc. Include as part of the metadata record.) _Copyright status should be displayed as part of the record, as well as attribution information_. Have policies in place - be proactive, not reactive. Think about how you can use existing creative commons licenses for filtering/faceting and clarity for end-users.  

The user community experience - online communities can be defined many different ways and discovery happens in many different spaces. Who are you trying to reach? Consider capturing and indexing comments that people leave in digital spaces - people may tell their stories or provide background information about the content.  

Cultural heritage projects can also be crowdsourced. Want to keep "smart data" in mind (creative commons licenses, geodata). Our Digital World has a copyright FAQ and project management resources on their site.  

#Digitization project management in practice
##Sara Allain, Ryerson (but talking about UTSC)  

Project: digitize hundreds of images. Mission to facilitate digital access to select archival collections related to UTSC's 50th anniversary. June-August 2014. Had YCW funding to hire an MI/MLIS graduate student (Rachel Pisani). Had previously developed digitization standards, purchased equipment, and UTSC owned copyright. UTSC photographic services collection ~10,000 prints, negatives and slides. Loosely described and arranged by subject. Didn't do all 10,000 - selected several hundred. Also had 2 librarians and 2 work study students.  

Rachel did a collection inventory and basic one-line descriptions. Prioritized good candidates for digitization on a spreadsheet. Converted spreadsheet to MODSXML using Open Refine. Work study students scanned the images following standards (600 dpi, full-colour TIFFs).  

Open Refine produces a giant XML file for the whole collection, but Islandora wants one XML file and one image per item. XML::Twig fixes this. Batch ingested into Islandora. Now online! Yay! Important to define what success means for your project. Learning moment: emphasizing regular communication means being prepared for and flexibly adapting to changes to project scope and implementation. [Project is here!](http://uoft.me/utsc-photos)  

#Linked data in digital curation
###Jenny Jing, Queen's

Three layers: interface and web layer (PHP, JS, HTML, etc. Drupal or WP for publishing), system/admin layer (shell scripting, configuration, maintenance, etc. Various OSes and editing tools), and data/databases (holds content). Different technologies and skills required for each. Linked data can help users discover the content, no matter where it is.  

To be considered linked data, it must be structured (choose an ontology, i.e. Schema.org), it must have a URI, and must have relationships structured as triples (subject-relationship-object). Humans are able to tell the difference between a book written by Bill Gates versus a book about Bill Gates - how can computers make this distinction? Linked data can define these relationships.  

Linked data can help (1) bring traffic through Schema.org, (2) make data reusable by other web applications, (3) apply authority control as subject headings with URLS - don't have to pay vendors (4) BIBFRAME to edit records faster.  

How could we use it? Apply structured data to HTML using attributes (Schema.org). In digital curation (see Linked Data for Libraries project, IRs, Digital Asset Management). 

#Digital curation tools
###Gabriela Mircea, McMaster

* Depositing and ingesting digital objects (computing and manipulating metadata, data transfer and deposit, metadata extraction, normalization and migration, web archiving)
* Archving and preserving information packages
* Managing and administering repositories

Many tools! Gabriela's presentation went through tools used for different parts of the DCC cycle, including Atom, Curator's Workbench, Fits, Xena for normalization. Refer to slides!  

McMaster has created a digital curation workstation with a bunch of drives to handle various media (zip, jaz, etc.) BitCurator to extract digital materials from removable media in ways that generate metadata. BitCurator is a collection of software and utilities developped by a consortium of schools.  

#Archivematica
###Jeremy Heil, Queen's

City of Vancouver chose Archivematica, had several criteria for selection: compliance with OAIS, ingests a wide variety of digital objects, stores objects securely, addresses reservation planning, provides logging to demonstrate preservation actions, open source, flexibility to add new features, scalability for large acquisitions.  

Open Archival Information System (OAIS): SIPs and AIPs and DIPs.  

* SIP: Submission information package - acquired and submitted to system
* AIP: what is preserved in OAIS
* DIP: what is provided to end-users.

SIPs have to be massaged a bit to enter the system, for fixity, etc. These are ingested an converted to AIPs and DIPs. Can do either/or, both at same time if needed, etc.  

SIP contains original documents, captured metadata, checksums, added metadata. Information at the point of capture.  

AIP contains METS/PREMIS and ZIP file containing: original records, normalized versions from preservation and access, preservation metadata.  

DIP contains normalized versions of records for access, descriptive metadata.  

Admin options include the ability to quarantine transfers (can specify length of time if so), can link to Atom, DSpace, or CONTENTdm for DIPs. Failure report will identify problems. Preservation planning menu: Format information taken from format registries. Might have preferred tools to manage format rules.  

Archivematica can be used to enable digital preservation of your IR.  

Demonstration of transferring some sample content from Artefactual. Choose format, add name, accession number if present, etc. Actions: approve transfer (creates unique id, completes microservices, red lines indicate having to do something), create SIP, normalize, etc, etc. 

#Islandora
###Nick Ruest (York) & Kirsta Stapelfeldt (UTSC)

Islandora the project, Islandora the software, Islandora the community. We're getting the condensed version of Islandora Camp content.  

Islandora Foundation: 1 full-time staff member, lots of members and collaborators. Foundation holds events and are the stewards for the codebase.  

The software: holds whatever content types you want, as long as you can model them. Fedora the repository, not Fedora the OS. On top is Islandora the integration layer, on top of that is Drupal.  

Fedora Commons doesn't work like a hierarchy, it's more like a graph. Objects can be linked together. 

Everything is an object, with datastreams that connect objects together. Drupal was different roles, which each have their set of CRUD permissions which are defined in an XML file.  

Permissions can be really granular. Can hide content to select audiences but make the description available, can limit to certain groups of users, etc. Doesn't force openness.  

Drupal's plug-ins are called modules, and there are thousands of these. Islandora leverages this concept to create "solution pack" modules that address different needs. For example, audio , image, warc, etc. Some solution packs:

* Collections solution pack enables you to have collections, including the root collection.
* Audio solution pack takes in an audio format, normalizes it, gives you an mp3 derivative, and allows you to play it back on your site.
* Book for book objects, includes Tesseract for OCR
* Image annotation
* Compound object to relate different objects (for instance, both sides of a postcard can be separate objects that are shown together, can also use for supplementary information for theses, etc.)
* Basic and large image solution packs (large image one includes a zoomable viewer)
* Newspaper solution pack to organize serials, provides in-text highlighting
* PDF
* Video to allow streaming. Can also link out to streaming server.
* Web ARChive solution pack to store warcs, could do a wayback machine-type thing to see previous versions of pages.

Many opportunities to get involved in interest groups. Big community effort. Documentation needs work - contribute if you can. Community is quite active and there are training opportunities at Islandora Camps. First all-volunteer release was in May 2014. Committed to doing these every 6 months. Meeting minutes are all public. Lots of testers in the room. Yay testers and everyone involved in the release! IRC channel and mailing list if you have questions.  

Learning from other communities: Archivematica has a file format registry. Islandora group are looking at incorporating this and working with them. Development is ongoing, lots of things coming up.  







