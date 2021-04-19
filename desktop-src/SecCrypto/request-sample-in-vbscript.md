---
description: 下列 VBScript 範例程式碼示範憑證註冊控制項如何與 CCertRequest 物件搭配使用，以建立並提交憑證要求。
ms.assetid: be1bc66a-7bc5-4369-9344-168af53fdfb9
title: VBScript 中的要求範例
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 12e14507f0bb27e7bc8caba605158a70f5e08ac4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985103"
---
# <a name="request-sample-in-vbscript"></a><span data-ttu-id="d4a29-103">VBScript 中的要求範例</span><span class="sxs-lookup"><span data-stu-id="d4a29-103">Request Sample in VBScript</span></span>

<span data-ttu-id="d4a29-104">下列 VBScript 範例程式碼示範憑證註冊控制項如何與 CCertRequest 物件搭配使用，以建立並提交 [*憑證要求*](../secgloss/c-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="d4a29-104">The following VBScript sample code shows how the Certificate Enrollment Control can be used with the CCertRequest object to create and submit a [*certificate request*](../secgloss/c-gly.md).</span></span>


```VB
<HTML>
<HEAD>
<TITLE>VBScript Certificate Enrollment Control Sample
</TITLE>
<OBJECT classid="clsid:127698E4-E730-4E5C-A2b1-21490A70C8A1"
    codebase="xenroll.dll"
    id=Enroll >
</OBJECT>
<OBJECT classid="clsid:98AFF3F0-5524-11D0-8812-00A0C903B83C"
    codebase="certcli.dll"
    id=Request >
</OBJECT>
<BR>
Certificate Enrollment Control Request Sample
<BR>
<BR>

<SCRIPT language="VBScript">
<!--
' Declare the distinguished name variable.
Dim strDN

' Declare the request variable.
Dim strReq

' Declare a local variable for request disposition.
Dim nDisp

' Enable error handling.
On Error Resume Next

' Declare constants used by CertRequest object.
const CR_IN_BASE64 = &H1
const CR_IN_PKCS10 = &H100

' Build the DN.
strDN =  "CN=UserName" _
      & ",OU=UserUnit" _
      & ",O=UserOrg" _
      & ",L=UserCity" _
      & ",S=WA" _
      & ",C=US"

' Attempt to use the control, in this case, to create a PKCS #10.
MsgBox("Creating PKCS #10 " & strDN)
strReq = Enroll.createPKCS10( strDN, "1.3.6.1.4.1.311.2.1.21")
' If above line failed, Err.Number will not be 0.
if ( Err.Number <> 0 ) then
    MsgBox("Error in call to createPKCS10 " & Err.Number)
    err.clear
else
    MsgBox("Submitting request " & strReq)
    nDisp = Request.Submit( CR_IN_BASE64 OR CR_IN_PKCS10, _
                            strReq, _
                            "", _
                            "Machine\CertAuth")
    ' If the preceding line failed, Err.Number will not be 0.
    if ( Err.Number <> 0 ) then
        MsgBox("Error in Request Submit " & Err.Number)
        err.clear
    else
        MsgBox("Submitted certificate; disposition = " & nDisp)
    end if

end if
-->
</SCRIPT>
<BR>
</HEAD>
</HTML>
```



 

 
