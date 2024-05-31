# xLongSignDB

## INSTRUCTIONS FOR DOWNLOADING xLongSignDB 
1) [Download license agreement](https://bidalab.eps.uam.es/static/licenses/xLongSignDB_License.pdf), send by email one signed and scanned copy to **atvs@uam.es** according to the instructions given in point 2.
 
 
2) Send an email to **atvs@uam.es**, as follows:

   *Subject:* **[DATABASE download: xLongSignDB ]**

   Body: Your name, e-mail, telephone number, organization, postal mail, purpose for which you will use the database, time and date at which you sent the email with the signed license agreement.
 

3) Once the email copy of the license agreement has been received at ATVS, you will receive an email with a username, a password, and a time slot to download the database.
 

4) [Download the database](https://bidalab.eps.uam.es/listdatabases?id=xLongSignDB#page), for which you will need to provide the authentication information given in step 4. After you finish the download, please notify by email to **atvs@uam.es** that you have successfully completed the transaction.
 

5) For more information, please contact: **atvs@uam.es**


## DESCRIPTION OF xLongSignDB 

The dataset comprises the on-line signature data of the 29 common users to the BiosecurID and the Biosecure databases. These two signature subsets were acquired in a 15 month time span and present some unique features that make them especially suited for aging evaluation of on-line signature recognition systems [IET2019]. The general time distribution of the different sessions of the database is shown in Fig. 1.

![](http://atvs.ii.uam.es/atvs/xLongSignDB.jpg )
Figure 1. General time diagram of the different acquisition sessions that form the xLongSignDB.


#### __The BiosecurID Signature Subset [PAA2010]__

It comprises 16 original signatures per user (29 users).

Samples were captured in 4 separate acquisition sessions (named S1, S2, S3 and S4 in Fig. 1).

The sessions were captured leaving a two month interval between them, in a controlled and supervised office-like scenario.

Users were asked to sign on a piece of paper, inside a grid that marked the valid signing space, using an inking pen. The paper was placed on the Wacom Intuos 3 pen tablet that captured the time signals of each signature at a 100Hz sampling rate (trajectory functions x and y with an accuracy of 0.25mm, pressure function p with a precision of 1024 pressure levels, and azimuth and altitute angles). All the dynamic information is stored in separate text files following the format used in the first Signature Verification Competition, SVC.


#### __The Biosecure Signature Subset [PAMI2010]__
This dataset was captured 6 months after the BiosecurID acquisition campaign had finished (the time sequence of the two databases is shown in Fig. 1).

It comprises 30 original signatures per user (same 29 users as the BiosecurID subset) distributed in two acquisition sessions separated three months (named S5 and S6 in Fig. 1).

The 15 original samples corresponding to each session were captured in three groups of 5 consecutive signatures with an interval of around 15 minutes between groups (named in Fig. 1 S.5.1-2-3 and S.6.1-2-3, respectively).

The signature dataset was designed to be fully compatible with the BiosecurID one. The acquisition scenario and protocol are almost identical: as in the BiosecurID case, users had to sign using an inking pen on a piece of paper with a restricted space, placed over the Wacom Intuos 3 pen tablet. The dynamic information stored is the same as in BiosecurID and following also the SVC format.


#### FILES FORMAT
The signatures are stored in text files following the format of the 2004 Signature Verification Competition (SVC), where:

+ ROW 1: it just contains one entry with the number of sampled points of the signature (N).

+ ROWS 2 to (N+1): represents the y coordinate.

  + COLUMN 1: represents the x coordinate.

  + COLUMN 2: represents the y coordinate.

  + COLUMN 3: this is a synthetic timestamp (it may be neglected).

  + COLUMN 4: indicates the penups. It is 0 where p=0, and 1 otherwise.

  + COLUMN 5: this is the azimuth angle.

  + COLUMN 6: this is the altitude angle.

  + COLUMN 7: represents the pressure (p) function.
  
  
#### FILES NOMENCLATURE
The nomenclature followed to name the signature files is as follows: XXXX_sgYY.svc

+ XXXX: is the number of the user [1001, 1002, ... , 1029]

+ YY: is the number of the sample [1, 2, ... , 46]

The correspondence between signatures is as follows: XXXX_sgYY.svc

+ Signatures 1-4: S1 (1st session of BiosecurID)

+ Signatures 5-8: S2 (2nd session of BiosecurID)

+ Signatures 9-12: S3 (3rd session of BiosecurID)

+ Signatures 13-16: S4 (4th session of BiosecurID)

+ Signatures 17-31: S5 (1st session of Biosecure)

+ Signatures 32-46: S6 (2nd session of Biosecure)


#### REFERENCES
For further information on the database and on different applications where it has been used, we refer the reader to (all these articles are publicly available in the [publications](http://atvs.ii.uam.es/atvs/listpublications.do) section of the ATVS group webpage.)
+ [IET2019] R. Tolosana, R. Vera-Rodriguez, J. Fierrez and J. Ortega-Garcia, “Reducing the Template Aging Effect in On-Line Signature Biometrics”, IET Biometrics, 2019.

+ [PONE2013] J.Galbally, M. Martinez-Diaz and Julian Fierrez, "[Aging in Biometrics: An Experimental Analysis on On-Line Signature](https://bidalab.eps.uam.es/static/files/2013_PLOSone_AgeingSignature_Galbally_Published.pdf)", PLOS ONE, Vol. 8, n. 7, 2013 ([DOI](http://dx.plos.org/10.1371/journal.pone.0069897)).

+ [PAA2010] J. Fierrez, J. Galbally, J. Ortega-Garcia, M. R. Freire, F. Alonso-Fernandez, D. Ramos, D. T. Toledano, J. Gonzalez-Rodriguez, J. A. Siguenza, J. Garrido-Salas, E. Anguiano, G. Gonzalez-de-Rivera, R. Ribalda, M. Faundez-Zanuy, J. A. Ortega, V. Cardeñoso-Payo, A. Viloria, C. E. Vivaracho, Q. I. Moro, J. J. Igarza, J. Sanchez, I. Hernaez, C. Orrite-Uruñuela, F. Martinez-Contreras and J. J. Gracia-Roche, "[BiosecurID: A Multimodal Biometric Database](https://bidalab.eps.uam.es/static/files/2009_PAA_BiosecurID_Fierrez.pdf)", Pattern Analysis and Applications, Vol. 13, n. 2, pp. 235-246, 2010.

+ [PAMI2010] J. Ortega-Garcia, J. Fierrez, F. Alonso-Fernandez, J. Galbally, M. Freire, J. Gonzalez-Rodriguez, C.Garcia-Mateo, J.-L.Alba-Castro, E.Gonzalez-Agulla, E.Otero-Muras, S.Garcia-Salicetti, L.Allano, B.Ly-Van, B.Dorizzi, J.Kittler, T.Bourlai, N.Poh, F.Deravi, M.Ng, M.Fairhurst, J.Hennebert, A.Humm, M.Tistarelli, L.Brodo, J.Richiardi, A.Drygajlo, H.Ganster, F.M.Sukno, S.-K.Pavani, A.Frangi, L.Akarun and A.Savran, "[The Multi-Scenario Multi-Environment BioSecure Multimodal Database (BMDB)](https://bidalab.eps.uam.es/static/files/2010_PAMI_BMDM_Ortega.pdf)", IEEE Trans. on Pattern Analysis and Machine Intelligence, Vol. 32, n. 6, pp. 1097-1111, 2010.

Please remember to reference articles [IET2019] and [PONE2013] on any work made public, whatever the form, based directly or indirectly on any part of the xLongSignDB.
