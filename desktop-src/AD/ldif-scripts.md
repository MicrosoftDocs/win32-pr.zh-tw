---
title: LDIF 腳本
description: " (LDIF) 的 LDAP 資料交換格式是一種網際網路工程任務推動小組， (IETF) 標準，定義如何在使用 LDAP 服務提供者的目錄伺服器之間匯入和匯出目錄資料。"
ms.assetid: a87d0d34-96c0-4cef-a38e-30a7e2291a7a
ms.tgt_platform: multiple
keywords:
- LDIF 腳本 Active Directory
- LDIF 腳本 Active Directory、關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ad45c51fc16b3c19c3e59f4cfba2e006d4df900c20ce7ddc1b801478a22982c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118187082"
---
# <a name="ldif-scripts"></a>LDIF 腳本

 (LDIF) 的 LDAP 資料交換格式是一種網際網路工程任務推動小組， (IETF) 標準，定義如何在使用 LDAP 服務提供者的目錄伺服器之間匯入和匯出目錄資料。 Windows 2000 和 Windows Server 2003 都包含命令列公用程式 LDIFDE，可用來使用 LDIF 檔案將目錄物件匯入 Active Directory Domain Services。 LDIFDE 可讓您將篩選準則設定為特定字串，以搜尋 Active Directory Domain Services 中的目錄物件，並將其列為可供架構系統管理員輕鬆讀取的 LDIF 檔案。

匯入 Unicode 檔案時，如果檔案的開頭包含 Unicode 識別碼，LDIFDE 會將該檔案匯入為 Unicode。 如果您想要在檔案開頭沒有包含 Unicode 識別碼時將檔案匯入為 Unicode，您可以使用-u 參數，強制將它匯入為 Unicode。

匯出檔案的預設模式為 ANSI。 如果有 Unicode 專案，則會轉換成基底64格式。 若要將檔案匯出成 Unicode 格式，請使用-u 參數。

當加入的屬性之間有相依性時，LDIF 檔案必須套用架構變更。 例如，您應該在對應的上一頁連結屬性之前加入轉寄連結屬性。 您也必須在新增相依于 LDIF 腳本稍早新增之屬性或類別的類別之前，更新架構快取。 如需詳細資訊，請參閱下列程式碼範例。

請注意，對於二進位值，您必須將值編碼為 base64。 Base64 編碼是在 IETF RFC 2045，第6.8 節中定義。

如需 LDIF 檔案格式的詳細資訊，請參閱網際網路工程任務推動小組網站上 [的 LDAP 資料交換格式 (LDIF) -技術規格](https://www.ietf.org/rfc/rfc2849.txt) (RFC 2849) 。

## <a name="ntds-specific-ldif-changetypes"></a>特定 NTDS 的 LDIF changetypes

最好是使用 ntdsSchema changetypes， \* 而不是呼叫 ldifde-k。 Ldifde 的-k 選項會忽略一組較大的 LDAP 錯誤。 已忽略錯誤的完整清單如下所示：

-   物件已經是群組的成員。
-   如果要匯入的物件沒有其他屬性，則物件類別違規 (表示指定的物件類別不存在) 。
-   物件已經存在 (**LDAP \_ 已經 \_ 存在**) 
-   條件約束違規 (**LDAP \_ 條件約束 \_ 違規**) 
-   屬性或值已存在 (**LDAP \_ 屬性 \_ 或 \_ 值 \_ 存在**) 
-   沒有此類物件 (**LDAP \_ 沒有 \_ 這類 \_ 物件**) 

下列 changetypes 是特別針對架構升級作業而設計的。



| Changetype                      | Description                                                                                                                                                                                                                                                                              |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ntdsSchemaAdd**<br/>    | **ntdsSchemaAdd** 對應于 LDIF 檔案中的 **add** 。 唯一的差別在於，如果物件已經存在於架構中， **ntdsSchemaAdd** 會讓 ldifde 略過 **加入** 作業。 已忽略 (**LDAP \_ 已 \_ 存在** 。 ) <br/>                                   |
| **ntdsSchemaModify**<br/> | **ntdsSchemaModify** 對應于 LDIF 檔案中的 **modify** 。 唯一的差別在於，如果在架構中找不到物件， **ntdsSchemaModify** 會讓 ldifde 略過 **修改** 作業。  (**LDAP \_ 不會忽略 \_ 這類 \_ 物件** 。 ) <br/>                        |
| **ntdsSchemaDelete**<br/> | **ntdsSchemaDelete** 對應至 LDIF 檔案中的 **delete** 。 唯一的差別在於，如果在架構中找不到物件， **ntdsSchemaDelete** 會讓 ldifde 略過 **刪除** 作業。  (**LDAP \_ 不會忽略 \_ 這類 \_ 物件** 。 ) <br/>                        |
| **ntdsSchemaModRdn**<br/> | **ntdsSchemaModRdn** 對應至 LDIF 檔案中的 **modrdn** 。 唯一的差別在於，如果在架構中找不到物件， **ntdsSchemaModRdn** 會讓 ldifde 略過修改相關的分辨名稱作業。  (**LDAP \_ 不會忽略 \_ 這類 \_ 物件** 。 ) <br/> |



 

## <a name="example"></a>範例

下列程式碼範例包含：

-   Myschemaext 是包含新屬性和類別的 LDIF 腳本。 請注意，這個檔案是從 Lgetattcls.vbs 產生之檔案的修改版本。 另外也請注意， **我的測試屬性-dn-fl** 屬性已移至我的 **測試-屬性-dn-BL** ，因為 (我的測試 **-屬性-dn-BL**) 的後置連結 (**我的測試屬性-dn-FL**) 的轉寄連結。 此外， **schemaUpdateNow** 操作屬性是在兩個地方設定來觸發架構快取的更新，讓相依的屬性和類別可用於在腳本中加入這兩個類別。
    > [!Note]  
    > 如需有關 linkID：語句中識別碼來源的詳細資訊，請參閱主題 [取得連結識別碼](obtaining-a-link-id.md) 。

     

-   Lgetattcls.vbs 是一個 VBScript 檔案，它會產生用來作為 Myschemaext 起點的 LDIF 腳本。 請注意，目前的架構路徑會取代為 CN = Schema，CN = Configuration，DC = myorg，DC = com。 您可以取代 DC = myorg，DC = com，以反映在 LDIF 腳本中發佈 (DN) 的辨別名稱，確保 LSETATTCLS.VBS 反映其 **sFromDN** 中的變更，以便在套用 LDIF 腳本時取代正確的 DN。 另外也請注意，腳本會使用前置詞來尋找您也應定義的類別和屬性，並使用所有類別和屬性的前置詞。 如需詳細資訊，請參閱 [命名屬性和類別](naming-attributes-and-classes.md)。 此外，腳本只會將 **attributeSchema** 和 **classSchema** 物件的必要屬性輸出至 LDIF 檔案。
-   Lsetattcls.vbs 是 VBScript 檔案，它會使用 Myschemaext .ldf 腳本在腳本中加入新的屬性和類別。 確定可以在執行腳本之前，先將架構主機寫入。

## <a name="myschemaextldf"></a>MYSCHEMAEXT.LDF

``` syntax
dn: CN=My-Test-Attribute-CaseExactString,CN=Schema,CN=Configuration,DC=myorg,DC=com
changetype: add
adminDisplayName: My-Test-Attribute-CaseExactString
attributeID: 1.2.840.113556.1.4.7000.159.24.10.65
attributeSyntax: 2.5.5.3
cn: My-Test-Attribute-CaseExactString
description: Test attribute of syntax CaseExactString used to show how to add a CaseExactString attribute.
isMemberOfPartialAttributeSet: FALSE
isSingleValued: TRUE
lDAPDisplayName: myTestAttributeCaseExactString
distinguishedName: CN=My-Test-Attribute-CaseExactString,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectCategory: CN=Attribute-Schema,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectClass: attributeSchema
oMSyntax: 27
name: My-Test-Attribute-CaseExactString
schemaIDGUID:: 6ASznA3W0hGBpwDAT7mMGg==
searchFlags: 0
 
dn: CN=My-Test-Attribute-DN-FL,CN=Schema,CN=Configuration,DC=myorg,DC=com
changetype: add
adminDisplayName: My-Test-Attribute-DN-FL
attributeID: 1.2.840.113556.1.4.7000.159.24.10.614
attributeSyntax: 2.5.5.1
cn: My-Test-Attribute-DN-FL
description: Test forward link attribute of syntax DN used to show how to add a forward link attribute. Back link is My-Test-Attribute-DN-BL.
isMemberOfPartialAttributeSet: FALSE
isSingleValued: TRUE
lDAPDisplayName: myTestAttributeDNFL
linkID: 1.2.840.113556.1.2.50
distinguishedName: CN=My-Test-Attribute-DN-FL,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectCategory: CN=Attribute-Schema,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectClass: attributeSchema
oMObjectClass:: KwwCh3McAIVK
oMSyntax: 127
rangeLower: 0
rangeUpper: 257
name: My-Test-Attribute-DN-FL
schemaIDGUID:: YGLudffa0hGLEwDAT7mMGg==
searchFlags: 0
 
dn: CN=My-Test-Attribute-DN-BL,CN=Schema,CN=Configuration,DC=myorg,DC=com
changetype: add
adminDisplayName: My-Test-Attribute-DN-BL
attributeID: 1.2.840.113556.1.4.7000.159.24.10.615
attributeSyntax: 2.5.5.1
cn: My-Test-Attribute-DN-BL
description: Test back link attribute of syntax DN used to show how to add a back link attribute. Forward link is My-Test-Attribute-DN-FL.
isMemberOfPartialAttributeSet: FALSE
isSingleValued: TRUE
lDAPDisplayName: myTestAttributeDNBL
linkID: 1.2.840.113556.6.1234
distinguishedName: CN=My-Test-Attribute-DN-BL,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectCategory: CN=Attribute-Schema,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectClass: attributeSchema
oMObjectClass:: KwwCh3McAIVK
oMSyntax: 127
rangeLower: 0
rangeUpper: 257
name: My-Test-Attribute-DN-BL
schemaIDGUID:: jFfbhffa0hGLEwDAT7mMGg==
searchFlags: 0
 
dn: CN=My-Test-Attribute-DN-Regular,CN=Schema,CN=Configuration,DC=myorg,DC=com
changetype: add
adminDisplayName: My-Test-Attribute-DN-Regular
attributeID: 1.2.840.113556.1.4.7000.159.24.10.613
attributeSyntax: 2.5.5.12
cn: My-Test-Attribute-DN-Regular
description: Test attribute of syntax DN used to show how to add a DN attribute.
isMemberOfPartialAttributeSet: FALSE
isSingleValued: TRUE
lDAPDisplayName: myTestAttributeDNRegular
distinguishedName: CN=My-Test-Attribute-DN-Regular,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectCategory: CN=Attribute-Schema,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectClass: attributeSchema
oMObjectClass:: KwwCh3McAIVK
oMSyntax: 64
rangeLower: 0
rangeUpper: 257
name: My-Test-Attribute-DN-Regular
schemaIDGUID:: 5QSznA3W0hGBpwDAT7mMGg==
searchFlags: 0
 
dn: CN=My-Test-Attribute-DNString,CN=Schema,CN=Configuration,DC=myorg,DC=com
changetype: add
adminDisplayName: My-Test-Attribute-DNString
attributeID: 1.2.840.113556.1.4.7000.159.24.10.611
attributeSyntax: 2.5.5.14
cn: My-Test-Attribute-DNString
description: Test attribute of syntax DNString used to show how to add a DNString attribute.
isMemberOfPartialAttributeSet: FALSE
isSingleValued: TRUE
lDAPDisplayName: myTestAttributeDNString
distinguishedName: CN=My-Test-Attribute-DNString,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectCategory: CN=Attribute-Schema,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectClass: attributeSchema
oMObjectClass:: KoZIhvcUAQEBDA==
oMSyntax: 127
rangeLower: 1
rangeUpper: 64
name: My-Test-Attribute-DNString
schemaIDGUID:: 5ASznA3W0hGBpwDAT7mMGg==
searchFlags: 0

DN:
changetype: modify
add: schemaUpdateNow
schemaUpdateNow: 1
-
 
dn: CN=My-Test-Auxiliary-Class1,CN=Schema,CN=Configuration,DC=Fabrikam,DC=com
changetype: add
adminDisplayName: My-Test-Auxiliary-Class1
description: Test class used to show how to add an auxiliary class.
objectCategory: CN=Class-Schema,CN=Schema,CN=Configuration,DC=Fabrikam,DC=com
objectClass: classSchema
lDAPDisplayName: myTestAuxiliaryClass1
governsID: 1.2.840.113556.1.4.7000.159.24.10.611.11
instanceType: 4
objectClassCategory: 3
schemaIDGUID:: mmsxdsXb0hGL0AAA+HW2YA==
subClassOf: Top
mayContain: my-Test-Attribute-DNString
mustContain: description
 
DN:
changetype: modify
add: schemaUpdateNow
schemaUpdateNow: 1
-
 
dn: CN=My-Test-Structural-Class1,CN=Schema,CN=Configuration,DC=Fabrikam,DC=com
changetype: add
adminDisplayName: My-Test-Structural-Class1
auxiliaryClass: myTestAuxiliaryClass1
defaultHidingValue: FALSE
defaultObjectCategory: CN=Organizational-Unit,CN=Schema,CN=Configuration,DC=Fabrikam,DC=com
defaultSecurityDescriptor: D:(A;;RPWPCRCCDCLCLOLORCWOWDSDDTDTSW;;;DA)(A;;RPWPCRCCDCLCLORCWOWDSDDTSW;;;SY)(A;;RPLCLORC;;;AU)
admindescription: Test class used to show how to add a structure class.
objectCategory: CN=Class-Schema,CN=Schema,CN=Configuration,DC=Fabrikam,DC=com
objectClass: classSchema
lDAPDisplayName: myTestStructuralClass1
governsID: 1.2.840.113556.1.4.7000.159.24.10.611.12
mayContain: myTestAttributeDNFL
mayContain: wWWHomePage
mustContain: url
instanceType: 4
objectClassCategory: 1
possSuperiors: organizationalUnit
rDNAttID: ou
schemaIDGUID:: 1HsnsL7b0hGL0AAA+HW2YA==
subClassOf: organizationalUnit
 
DN:
changetype: modify
add: schemaUpdateNow
schemaUpdateNow: 1
-
```

## <a name="lgetattclsvbs"></a>LGETATTCLS.VBS


```VB
On Error Resume Next
 
'''''''''''''''''''
' Bind to the rootDSE
'''''''''''''''''''
sPrefix = "LDAP://"
Set root= GetObject(sPrefix & "rootDSE")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method"
End If
 
'''''''''''''''''''
' Get the DN for the Schema
'''''''''''''''''''
sSchema = root.Get("schemaNamingContext")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on Get method"
End If
 
'''''''''''''''''''
' Bind to the Schema container
'''''''''''''''''''
Set Schema= GetObject(sPrefix & sSchema )
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method to bind to Schema"
End If
''''''''''''''''''''
' Read the fsmoRoleOwner attribute to see which server is the schema master.
''''''''''''''''''''
sMaster = Schema.Get("fsmoRoleOwner")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on IADs::Get method for fsmoRoleOwner"
End If
''''''''''''''''''''
' fsmoRoleOwner attribute returns the nTDSDSA object.
' The parent is the server object.
' Bind to NTDSDSA object and get parent
''''''''''''''''''''
Set NTDS = GetObject(sPrefix & sMaster)
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method for NTDS"
End If
sServer = NTDS.Parent
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on IADs::get_Parent method"
End If
''''''''''''''''''''
' Bind to server object and get the
' reference to the computer object.
''''''''''''''''''''
Set Server = GetObject(sServer)
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method for " & sServer
End If
'''''''''''''''''''''
' Display the DN for the computer object.
'''''''''''''''''''''
sComputerDNSName = Server.Get("DNSHostName")
strText = "Schema Master has the following DNS Name: "& sComputerDNSName
WScript.echo strText
 
sFile = "myschemaext1.ldf"
sFromDN = sSchema
sToDN = "CN=Schema,CN=Configuration,DC=myorg,DC=com"
sAttrPrefix = "My-Test"
sFilter = "(&((cn=" & sAttrPrefix & "*)(|(objectCategory=classSchema)_
(objectCategory=attributeSchema))))"
sRetAttr = "dn,adminDescription,adminDisplayName,governsID,cn,mayContain,_
mustContain,systemMayContain,systemMustContain,lDAPDisplayName,_
objectClassCategory,distinguishedName,objectCategory,objectClass,_
possSuperiors,systemPossSuperiors,subClassOf,defaultObjectCategory,_
name,schemaIDGUID,auxiliaryClass,auxiliaryClass,systemAuxiliaryClass,_
description,defaultHidingValue,rDNAttId,defaultSecurityDescriptor,_
attributeID,attributeSecurityGUID,attributeSyntax,_
isMemberOfPartialAttributeSet,isSingleValued,mAPIID,oMSyntax,rangeLower,_
rangeUpper,searchFlags,oMObjectClass,linkID"
 
' Add flag rootDN.
sCommand = "ldifde -d " & sSchema 
sCommand = sCommand & " -c " & sFromDN & " " & sToDN
' Add flag schema master.
sCommand = sCommand & " -s " & sComputerDNSName
' Add flag filename.
sCommand = sCommand & " -f " & sFile
' Add flag filter to search for attributes.
sCommand = sCommand & " -r " & sFilter
' Add flag for attributes to return.
sCommand = sCommand & " -l " & sRetAttr
 
WScript.echo sCommand
Set WshShell = Wscript.CreateObject("Wscript.Shell")
WshShell.Run (sCommand)
 
 
''''''''''''''''''''
' Display subroutines
''''''''''''''''''''
 
Sub BailOnFailure(ErrNum, ErrText) strText = "Error 0x"_
 & Hex(ErrNum) & " " & ErrText
    MsgBox strText, vbInformation, "ADSI Error"
    WScript.Quit
End Sub
```



## <a name="lsetattclsvbs"></a>LSETATTCLS.VBS


```VB
On Error Resume Next
 
'''''''''''''''''''
' Bind to the rootDSE
'''''''''''''''''''
sPrefix = "LDAP://"
Set root= GetObject(sPrefix & "rootDSE")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method"
End If
 
'''''''''''''''''''
' Get the DN for the Schema
'''''''''''''''''''
sSchema = root.Get("schemaNamingContext")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on Get method"
End If
 
'''''''''''''''''''
' Bind to the Schema container
'''''''''''''''''''
Set Schema= GetObject(sPrefix & sSchema )
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method to bind to Schema"
End If
''''''''''''''''''''''''''''''''''''''
' Read the fsmoRoleOwner attribute to see which server is the schema master.
''''''''''''''''''''''''''''''''''''''
sMaster = Schema.Get("fsmoRoleOwner")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on IADs::Get method for fsmoRoleOwner"
End If
'''''''''''''''''''''''''''
' fsmoRoleOwner attribute returns the nTDSDSA object.
' The parent is the server object.
' Bind to NTDSDSA object and get parent
'''''''''''''''''''''''''''
Set NTDS = GetObject(sPrefix & sMaster)
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method for NTDS"
End If
sServer = NTDS.Parent
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on IADs::get_Parent method"
End If
''''''''''''''''''''''''
' Bind to server object
' and get the reference to the computer object.
''''''''''''''''''''''''
Set Server = GetObject(sServer)
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method for " & sServer
End If
sComputer = Server.Get("serverReference")
'''''''''''''''''''''
' Display the DN for the computer object.
'''''''''''''''''''''
sComputerDNSName = Server.Get("DNSHostName")
' strText = "Schema Master has the following DN: "& sComputer
strText = "Schema Master has the following DNS Name: "& sComputerDNSName
WScript.echo strText
 
sFile = "myschemaext.ldf"
sFromDN = "CN=Schema,CN=Configuration,DC=myorg,DC=com"
sToDN = sSchema
' Add flag replace fromDN with ToDN.
sCommand = "ldifde -i -k -c " & sFromDN & " " & sToDN
' Add flag schema master.
sCommand = sCommand & " -s " & sComputerDNSName
'Add flag filename.
sCommand = sCommand & " -f " & sFile
' Add flag filter to search for my attributes.
 
WScript.echo sCommand
Set WshShell = Wscript.CreateObject("Wscript.Shell")
WshShell.Run (sCommand)
 
 
''''''''''''''''''''
' Display subroutines
''''''''''''''''''''
 
Sub BailOnFailure(ErrNum, ErrText)    strText = "Error 0x" & Hex(ErrNum) & " " & ErrText
    MsgBox strText, vbInformation, "ADSI Error"
    WScript.Quit
End Sub
```



 

 





