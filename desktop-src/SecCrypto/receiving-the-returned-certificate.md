---
description: 說明應用程式如何接收憑證。
ms.assetid: 7f87dcf5-b434-4f63-abcd-6873831d22bc
title: 接收傳回的憑證
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 73853250c581e460360f5490defc0c94e76e5be3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979352"
---
# <a name="receiving-the-returned-certificate"></a>接收傳回的憑證

當憑證授權單位單位 (CA) 驗證要求者的身分識別資訊，並且滿足要求者為私密金鑰的擁有者，且該要求者的相關資料正確時，CA 就會建立 x.509 憑證、簽署它、將其封裝為任何其他必要的憑證 (例如，在訊息中) CA 本身的憑證，然後將訊息傳送給要求者。 此訊息可以是 PKCS \# 7 訊息或 cmc 回應 (V2 範本會導致 CMC 回應) 。

接收應用程式會將訊息傳遞給憑證註冊控制項。 憑證註冊控制項接著會開啟訊息並將憑證解壓縮。 系統會以對話方塊提示使用者，詢問使用者是否會接受「根」存放區中的自我簽署憑證。 如果使用者接受根憑證，則憑證的其餘部分 (除了要求者的憑證) ，都會放在「CA」存放區中。 要求者的憑證會放在 [**MyStoreName**](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_mystorename) 屬性中要求者所指定的憑證存放區中。

下列範例示範如何在網頁中使用 Visual Basic Scripting Edition (VBScript) 和 HTML 來接收和儲存傳回的憑證。


```VB
<HTML>
<TITLE>Certificate Enrollment Acceptance HTML Page
</TITLE>

<OBJECT  classid="clsid:127698E4-E730-4E5C-A2b1-21490A70C8A1"
    CODEBASE="xenroll.dll"
    id=IControl >
</OBJECT>

<SCRIPT language="VBScript">

<!--

Option Explicit 

'Accept the certificate subroutine.

Sub AcceptCertSub

On Error Resume Next

' Get the issued certificate.
' The following value, "PKCS7", represents the received message. 
' Actually, this value must be supplied through the design of
' the receiving application.
' A possible implementation is as follows: after using 
' ICertRequest.Submit to submit the PKCS #10, call 
' ICertRequest.GetLastStatus to confirm successful certificate 
' creation, and then call ICertRequest.GetCertificate to retrieve 
' the certificate.

document.result.result.value = "PKCS7"

    Call IControl.AcceptPKCS7(document.result.result.value)

    If err.Number = 0 Then
        navigate "..\done.htm"
    Else
        Alert "Error: " & Hex(err)
    End If

    End sub

    ' Decline the certificate sub-routine.
    Sub NoAcceptCertSub
    navigate "..\notdone.htm"
    End sub
-->
</SCRIPT>
</BODY>
</HTML>
```



 

 
