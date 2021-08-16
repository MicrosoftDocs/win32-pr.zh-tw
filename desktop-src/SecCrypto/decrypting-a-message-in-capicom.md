---
description: 這個副程式會採用密碼字串來產生會話加密金鑰，以及要從中讀取加密訊息的檔案名。 所有參數都會依值傳遞至副程式。
ms.assetid: 70f23d93-2bca-419b-9de7-e52ce4fb1350
title: 在 CAPICOM 中解密訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 744878378fbe2791e66151e451029be8adde2435b451d540196a1082c4e005f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117767756"
---
# <a name="decrypting-a-message-in-capicom"></a>在 CAPICOM 中解密訊息

\[CAPICOM 是僅限32位的元件，可供下列作業系統使用： Windows Server 2008、Windows Vista 和 Windows XP。 相反地，請使用 .NET Framework 來執行安全性功能。 如需詳細資訊，請參閱 [使用 CAPICOM 的替代方案](alternatives-to-using-capicom.md)。\]

這個副程式會採用密碼字串來產生會話加密金鑰，以及要從中讀取加密訊息的檔案名。 所有參數都會依值傳遞至副程式。

> [!Note]  
> CAPICOM 不支援 PKCS \# 7 a 內容類型，但會使用非標準的 ASN 結構來進行 a。 因此，只有 CAPICOM 才能解密 CAPICOM a 物件。

 

如果解密失敗，則會檢查 **Err** 值，以判斷錯誤是否是因為使用不符合用來加密訊息之密碼的密碼所造成。 在此情況下， \_ \_ 會傳回不正確的資料錯誤。

在任何的 CAPICOM 錯誤中 **，會傳回** 負數值的負數值。 如需詳細資訊，請參閱 [**CAPICOM \_ 錯誤碼 \_**](capicom-error-code.md)。 如需有關 **錯誤** 之正十進位值的詳細資訊，請參閱 winerror.h。


```VB
Sub DecryptMessage(ByVal hidden As String, ByVal filename As String)
On Error goto ErrorHandler

'Declare an EncryptedData object

Dim message As New EncryptedData

'Declare a string variable to hold the encrypted message.
Dim encrypted As String

' Open an input file and read in the encrypted message
Open filename For Input As #1
Input #1, encrypted
Close #1

' If a message was read in (the length of the input string is 
' greater than 0), set the password and decrypt the message.
If Len(encrypted) > 0 then
    ' Set the password used to generate the key
    ' used to decrypt the message. If the password
    ' not the same as the password used when the message
    ' was encrypted, decryption will fail.
    ' The algorithm name and key length set in the encrypting
    ' process are automatically used to decrypt the message. 
    message.SetSecret hidden
    message.Decrypt encrypted
    ' Display the decrypted message.
    MsgBox message.Content
else
    msgbox "No encrypted message was read in.
endif

' Release the EncryptedData object and exit the subroutine.
Set message = Nothing
Exit Sub

ErrorHandler:
If Err.Number > 0 Then
    MsgBox "Visual Basic error found:" & Err.Description
Else
'    Check for a bad password error.
    If Err.Number = -2146893819 Then
        MsgBox "Error. The password may not be correct."
    Else
        MsgBox "CAPICOM error found : " & Err.Number
    End If
End If
End Sub
```



 

 



