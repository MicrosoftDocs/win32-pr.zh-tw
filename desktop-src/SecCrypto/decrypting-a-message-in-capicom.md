---
description: 這個副程式會採用密碼字串來產生會話加密金鑰，以及要從中讀取加密訊息的檔案名。 所有參數都會依值傳遞至副程式。
ms.assetid: 70f23d93-2bca-419b-9de7-e52ce4fb1350
title: 在 CAPICOM 中解密訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba984bad7d9289eaf89725e9598a4330f16b49ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983489"
---
# <a name="decrypting-a-message-in-capicom"></a><span data-ttu-id="e013c-104">在 CAPICOM 中解密訊息</span><span class="sxs-lookup"><span data-stu-id="e013c-104">Decrypting a Message in CAPICOM</span></span>

<span data-ttu-id="e013c-105">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="e013c-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="e013c-106">相反地，請使用 .NET Framework 來執行安全性功能。</span><span class="sxs-lookup"><span data-stu-id="e013c-106">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="e013c-107">如需詳細資訊，請參閱 [使用 CAPICOM 的替代方案](alternatives-to-using-capicom.md)。\]</span><span class="sxs-lookup"><span data-stu-id="e013c-107">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="e013c-108">這個副程式會採用密碼字串來產生會話加密金鑰，以及要從中讀取加密訊息的檔案名。</span><span class="sxs-lookup"><span data-stu-id="e013c-108">This subroutine take a password string to be used to generate a session encryption key, and the name of a file from which an encrypted message will be read.</span></span> <span data-ttu-id="e013c-109">所有參數都會依值傳遞至副程式。</span><span class="sxs-lookup"><span data-stu-id="e013c-109">All parameters are passed into the subroutine by values.</span></span>

> [!Note]  
> <span data-ttu-id="e013c-110">CAPICOM 不支援 PKCS \# 7 a 內容類型，但會使用非標準的 ASN 結構來進行 a。</span><span class="sxs-lookup"><span data-stu-id="e013c-110">CAPICOM does not support the PKCS \#7 EncryptedData content type but uses a nonstandard ASN structure for EncryptedData.</span></span> <span data-ttu-id="e013c-111">因此，只有 CAPICOM 才能解密 CAPICOM a 物件。</span><span class="sxs-lookup"><span data-stu-id="e013c-111">Therefore, only CAPICOM can decrypt a CAPICOM EncryptedData object.</span></span>

 

<span data-ttu-id="e013c-112">如果解密失敗，則會檢查 **Err** 值，以判斷錯誤是否是因為使用不符合用來加密訊息之密碼的密碼所造成。</span><span class="sxs-lookup"><span data-stu-id="e013c-112">If decryption fails, the **Err.Number** value is checked to determine whether the error was caused by the use of a password that did not match the password used to encrypt the message.</span></span> <span data-ttu-id="e013c-113">在此情況下， \_ \_ 會傳回不正確的資料錯誤。</span><span class="sxs-lookup"><span data-stu-id="e013c-113">In this case, the NTE\_BAD\_DATA error is returned.</span></span>

<span data-ttu-id="e013c-114">在任何的 CAPICOM 錯誤中 **，會傳回** 負數值的負數值。</span><span class="sxs-lookup"><span data-stu-id="e013c-114">On any CAPICOM error, a negative decimal value of **Err.Number** is returned.</span></span> <span data-ttu-id="e013c-115">如需詳細資訊，請參閱 [**CAPICOM \_ 錯誤碼 \_**](capicom-error-code.md)。</span><span class="sxs-lookup"><span data-stu-id="e013c-115">For more information, see [**CAPICOM\_ERROR\_CODE**](capicom-error-code.md).</span></span> <span data-ttu-id="e013c-116">如需有關 **錯誤** 之正十進位值的詳細資訊，請參閱 winerror.h。</span><span class="sxs-lookup"><span data-stu-id="e013c-116">For information about positive decimal values of **Err.Number**, see Winerror.h.</span></span>


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



 

 



