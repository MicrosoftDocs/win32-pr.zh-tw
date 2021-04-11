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
# <a name="receiving-an-enveloped-data-message"></a><span data-ttu-id="e1a6c-103">接收封包的資料訊息</span><span class="sxs-lookup"><span data-stu-id="e1a6c-103">Receiving an Enveloped Data Message</span></span>

<span data-ttu-id="e1a6c-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="e1a6c-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="e1a6c-105">相反地，請使用 .NET Framework 來執行安全性功能。</span><span class="sxs-lookup"><span data-stu-id="e1a6c-105">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="e1a6c-106">如需詳細資訊，請參閱 [使用 CAPICOM 的替代方案](alternatives-to-using-capicom.md)。\]</span><span class="sxs-lookup"><span data-stu-id="e1a6c-106">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="e1a6c-107">若要解密封裝的訊息，收件者會比對來自 My store 的憑證，該 [*憑證*](../secgloss/c-gly.md) 具有可用的私密金鑰與封包訊息中的憑證。</span><span class="sxs-lookup"><span data-stu-id="e1a6c-107">To decrypt an enveloped message, the recipient matches a [*certificate*](../secgloss/c-gly.md) from the My store that has an available private key with a certificate in the enveloped message.</span></span> <span data-ttu-id="e1a6c-108">如果找到相符的，則會解密與該憑證相關聯的加密金鑰，並使用解密的金鑰來解密封包訊息。</span><span class="sxs-lookup"><span data-stu-id="e1a6c-108">If a match is found, the encrypted key associated with that certificate is decrypted and that decrypted key is used to decrypt the enveloped message.</span></span> <span data-ttu-id="e1a6c-109">沒有具有可用私密金鑰之相符憑證的訊息收件者無法解密訊息。</span><span class="sxs-lookup"><span data-stu-id="e1a6c-109">A message recipient that does not have a matching certificate with an available private key cannot decrypt the message.</span></span>

<span data-ttu-id="e1a6c-110">在接下來的範例中，會將檔案名傳遞到副程式中，該檔案會開啟，並在中讀取封包訊息。</span><span class="sxs-lookup"><span data-stu-id="e1a6c-110">In the example that follows, a file name is passed into the subroutine, that file is opened and an enveloped message is read in.</span></span> <span data-ttu-id="e1a6c-111">然後解密封包訊息。</span><span class="sxs-lookup"><span data-stu-id="e1a6c-111">The enveloped message is then decrypted.</span></span> <span data-ttu-id="e1a6c-112">使用封包訊息中的憑證比對使用者憑證、解密加密金鑰以及最後解密訊息的步驟，全都是在幕後完成。</span><span class="sxs-lookup"><span data-stu-id="e1a6c-112">The steps of matching a user certificate with a certificate in the enveloped message, of decrypting the encryption key, and finally of decrypting the message are all done behind the scenes.</span></span> <span data-ttu-id="e1a6c-113">如果找不到憑證相符或解密失敗，就會引發錯誤。</span><span class="sxs-lookup"><span data-stu-id="e1a6c-113">An error is raised if a certificate match is not found or if the decryption fails.</span></span>

<span data-ttu-id="e1a6c-114">在任何的 CAPICOM 錯誤中 **，會傳回** 負數值的負數值。</span><span class="sxs-lookup"><span data-stu-id="e1a6c-114">On any CAPICOM error, a negative decimal value of **Err.Number** is returned.</span></span> <span data-ttu-id="e1a6c-115">如需詳細資訊，請參閱 [**CAPICOM \_ 錯誤碼 \_**](capicom-error-code.md)。</span><span class="sxs-lookup"><span data-stu-id="e1a6c-115">For more information, see [**CAPICOM\_ERROR\_CODE**](capicom-error-code.md).</span></span> <span data-ttu-id="e1a6c-116">如需有關 **錯誤** 之正十進位值的詳細資訊，請參閱 winerror.h。</span><span class="sxs-lookup"><span data-stu-id="e1a6c-116">For information about positive decimal values of **Err.Number**, see Winerror.h.</span></span>


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



 

 
