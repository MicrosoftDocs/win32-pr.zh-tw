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
# <a name="encrypting-a-message-in-capicom"></a><span data-ttu-id="fbc3f-103">在 CAPICOM 中加密訊息</span><span class="sxs-lookup"><span data-stu-id="fbc3f-103">Encrypting a Message in CAPICOM</span></span>

<span data-ttu-id="fbc3f-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="fbc3f-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="fbc3f-105">相反地，請使用 .NET Framework 來執行安全性功能。</span><span class="sxs-lookup"><span data-stu-id="fbc3f-105">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="fbc3f-106">如需詳細資訊，請參閱 [使用 CAPICOM 的替代方案](alternatives-to-using-capicom.md)。\]</span><span class="sxs-lookup"><span data-stu-id="fbc3f-106">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="fbc3f-107">這個副程式會取得要加密的字串、要用來產生加密金鑰的密碼字串，以及將寫入加密訊息的檔案名。</span><span class="sxs-lookup"><span data-stu-id="fbc3f-107">This subroutine takes a string to be encrypted, a password string to be used to generate an encryption key, and the name of a file where the encrypted message will be written.</span></span> <span data-ttu-id="fbc3f-108">所有參數都會依值傳遞至副程式。</span><span class="sxs-lookup"><span data-stu-id="fbc3f-108">All parameters are passed into the subroutine by values.</span></span> <span data-ttu-id="fbc3f-109">若要解密訊息，必須使用相同的密碼字串。</span><span class="sxs-lookup"><span data-stu-id="fbc3f-109">To decrypt the message, the same password string must be used.</span></span> <span data-ttu-id="fbc3f-110">如果遺失密碼，則無法將文字解密。</span><span class="sxs-lookup"><span data-stu-id="fbc3f-110">If the password is lost, the text cannot be decrypted.</span></span> <span data-ttu-id="fbc3f-111">如果非預期的收件者取得密碼存取權，則會遺失訊息的隱私權。</span><span class="sxs-lookup"><span data-stu-id="fbc3f-111">The privacy of the message is lost if an unintended recipient gains access to the password.</span></span>

> [!Note]  
> <span data-ttu-id="fbc3f-112">CAPICOM 不支援 PKCS \# 7 a 內容類型，但會使用非標準的 ASN 結構來進行 a。</span><span class="sxs-lookup"><span data-stu-id="fbc3f-112">CAPICOM does not support the PKCS \#7 EncryptedData content type but uses a nonstandard ASN structure for EncryptedData.</span></span> <span data-ttu-id="fbc3f-113">因此，只有 CAPICOM 才能解密 CAPICOM a 物件。</span><span class="sxs-lookup"><span data-stu-id="fbc3f-113">As a result, only CAPICOM can decrypt a CAPICOM EncryptedData object.</span></span>

 

<span data-ttu-id="fbc3f-114">在任何 CAPICOM 錯誤上，會傳回 **Err** 屬性的負小數值。</span><span class="sxs-lookup"><span data-stu-id="fbc3f-114">On any CAPICOM error, a negative decimal value of the **Err.Number** property is returned.</span></span> <span data-ttu-id="fbc3f-115">如需詳細資訊，請參閱 [**CAPICOM \_ 錯誤碼 \_**](capicom-error-code.md)。</span><span class="sxs-lookup"><span data-stu-id="fbc3f-115">For more information, see [**CAPICOM\_ERROR\_CODE**](capicom-error-code.md).</span></span> <span data-ttu-id="fbc3f-116">如需有關 **錯誤** 之正十進位值的詳細資訊，請參閱 winerror.h。</span><span class="sxs-lookup"><span data-stu-id="fbc3f-116">For information about positive decimal values of **Err.Number**, see Winerror.h.</span></span>


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



 

 



