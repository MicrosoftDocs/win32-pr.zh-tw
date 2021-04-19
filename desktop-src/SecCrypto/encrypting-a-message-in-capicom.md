---
description: 這個副程式會取得要加密的字串、要用來產生加密金鑰的密碼字串，以及將寫入加密訊息的檔案名。
ms.assetid: 9ad3199a-bca1-4990-80da-80744e349047
title: 在 CAPICOM 中加密訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8039586736c09673644cacc90759e8d5f25b6e1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980592"
---
# <a name="encrypting-a-message-in-capicom"></a>在 CAPICOM 中加密訊息

\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。 相反地，請使用 .NET Framework 來執行安全性功能。 如需詳細資訊，請參閱 [使用 CAPICOM 的替代方案](alternatives-to-using-capicom.md)。\]

這個副程式會取得要加密的字串、要用來產生加密金鑰的密碼字串，以及將寫入加密訊息的檔案名。 所有參數都會依值傳遞至副程式。 若要解密訊息，必須使用相同的密碼字串。 如果遺失密碼，則無法將文字解密。 如果非預期的收件者取得密碼存取權，則會遺失訊息的隱私權。

> [!Note]  
> CAPICOM 不支援 PKCS \# 7 a 內容類型，但會使用非標準的 ASN 結構來進行 a。 因此，只有 CAPICOM 才能解密 CAPICOM a 物件。

 

在任何 CAPICOM 錯誤上，會傳回 **Err** 屬性的負小數值。 如需詳細資訊，請參閱 [**CAPICOM \_ 錯誤碼 \_**](capicom-error-code.md)。 如需有關 **錯誤** 之正十進位值的詳細資訊，請參閱 winerror.h。


```VB
Sub EncryptMessage(ByVal TobeEncrypted As String, ByVal hidden _
    As String, ByVal filename As String)

    On Error GoTo ErrorHandler

    ' Declare and initialize an EncryptedData object.
    ' Algorithm.Name and KeyLength do not need to be set.

    Dim message As New EncryptedData
    message.Content = Tobeencrypted
    message.SetSecret(hidden)
    ' Optionally, the encryption algorithm and key length can be set.
    ' If these properties are not set, the default algorithm and key 
    ' length are used.
    ' Information about the algorithm and key length is saved with 
    ' the encrypted string and the individual decrypting the message
    ' does not need to set these properties.

    message.Algorithm.Name = CAPICOM_ENCRYPTION_ALGORITHM_DES

    ' Declare the string that will hold the encrypted message.

    Dim encryptedmessage As String

    ' Encrypt the message storing the result in the encryptedmessage
    ' string.
    encryptedmessage = message.Encrypt

    ' Optionally, check the length of the encrypted string to 
    ' make sure that the encrypt method worked. 

    If Len(encryptedmessage) < 1 Then
        MsgBox("no message encrypted. ")
    Else
        MsgBox(" Message is " & Len(encryptedmessage) & " characters")

        ' Open an output file and write the encrypted message to the
        ' file. The file is not opened if there is no message
        ' to write.
    Open filename For Output As #1
    Write #1, encryptedmessage
    Close #1
        MsgBox("Encrypted message written to file ")
    End If

    ' Release the EncryptedData object.
    message = Nothing

    Exit Sub

ErrorHandler:
    If Err.Number > 0 Then
        MsgBox("Visual Basic error found:" & Err.Description)
    Else
        MsgBox("CAPICOM error found : " & Err.Number)
    End If
End Sub
```



 

 



