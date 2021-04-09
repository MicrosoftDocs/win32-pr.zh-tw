---
description: 若要解密封裝的訊息，收件者會比對來自 My store 的憑證，該憑證具有可用的私密金鑰與封包訊息中的憑證。
ms.assetid: 536f9977-102c-4df9-9d07-97b4b434b845
title: 接收封包的資料訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d32276193e8fd03904aed1ad626cd3ed241c654
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852087"
---
# <a name="receiving-an-enveloped-data-message"></a>接收封包的資料訊息

\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。 相反地，請使用 .NET Framework 來執行安全性功能。 如需詳細資訊，請參閱 [使用 CAPICOM 的替代方案](alternatives-to-using-capicom.md)。\]

若要解密封裝的訊息，收件者會比對來自 My store 的憑證，該 [*憑證*](../secgloss/c-gly.md) 具有可用的私密金鑰與封包訊息中的憑證。 如果找到相符的，則會解密與該憑證相關聯的加密金鑰，並使用解密的金鑰來解密封包訊息。 沒有具有可用私密金鑰之相符憑證的訊息收件者無法解密訊息。

在接下來的範例中，會將檔案名傳遞到副程式中，該檔案會開啟，並在中讀取封包訊息。 然後解密封包訊息。 使用封包訊息中的憑證比對使用者憑證、解密加密金鑰以及最後解密訊息的步驟，全都是在幕後完成。 如果找不到憑證相符或解密失敗，就會引發錯誤。

在任何的 CAPICOM 錯誤中 **，會傳回** 負數值的負數值。 如需詳細資訊，請參閱 [**CAPICOM \_ 錯誤碼 \_**](capicom-error-code.md)。 如需有關 **錯誤** 之正十進位值的詳細資訊，請參閱 winerror.h。


```VB
Sub ReceiveMessage(ByVal InFile As String)
On Error GoTo ErrorHandler

'Declare an EnvelopedData object

Dim Envmessage As New EnvelopedData

'Declare a string variable to hold the encrypted message.

Dim Encrypted As String

' Open an input file and read in the encrypted message
Open InFile For Input As #1
Input #1, Encrypted
Close #1

' If the length of the input string is greater than 0, 
' an encrypted message string is available. Decrypt the message.
' Note: to decrypt the message, a certificate with access to
' a user's private key must be available, and that certificate must
' match one of the certificates in the Recipients collection of 
' certificates.
If Len(Encrypted) > 0 Then
    ' Receive and decrypt the message
    Envmessage.Decrypt encrypted
    
    ' Display the decrypted message.
    MsgBox Envmessage.Content
Else
    MsgBox "No enveloped message was read in."
End If
' Release the EncryptedData object.
Set Envmessage = Nothing
Exit Sub

ErrorHandler:
If Err.Number > 0 Then
    MsgBox "Visual Basic error found:" & Err.Description
Else
    MsgBox "CAPICOM error found : " & Err.Number
End If
End Sub
```



 

 
