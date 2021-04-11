---
description: 當收到簽署的檔時，可以檢查簽章或簽章的有效性。
ms.assetid: 088915d8-768c-4378-a9dd-9347a428aff9
title: 驗證檔上的簽章
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f2886edcb9629011ddf1a0b5fb45a12a11f0556
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849457"
---
# <a name="verifying-the-signature-on-a-document"></a><span data-ttu-id="6516c-103">驗證檔上的簽章</span><span class="sxs-lookup"><span data-stu-id="6516c-103">Verifying the Signature on a Document</span></span>

<span data-ttu-id="6516c-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="6516c-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="6516c-105">相反地，請使用 .NET Framework 來執行安全性功能。</span><span class="sxs-lookup"><span data-stu-id="6516c-105">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="6516c-106">如需詳細資訊，請參閱 [使用 CAPICOM 的替代方案](alternatives-to-using-capicom.md)。\]</span><span class="sxs-lookup"><span data-stu-id="6516c-106">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="6516c-107">當收到簽署的檔時，可以檢查簽章或簽章的有效性。</span><span class="sxs-lookup"><span data-stu-id="6516c-107">When a signed document is received, the validity of the signature or signatures can be checked.</span></span> <span data-ttu-id="6516c-108">簽章可以檢查：</span><span class="sxs-lookup"><span data-stu-id="6516c-108">A signature can be checked for:</span></span>

-   <span data-ttu-id="6516c-109">簽章雜湊的有效性</span><span class="sxs-lookup"><span data-stu-id="6516c-109">Validity of the signature hash</span></span>
-   <span data-ttu-id="6516c-110">簽署者憑證的有效性</span><span class="sxs-lookup"><span data-stu-id="6516c-110">Validity of the signer's certificate</span></span>

<span data-ttu-id="6516c-111">簽章 [*雜湊*](../secgloss/h-gly.md)會使用簽署者 [*憑證*](../secgloss/c-gly.md)上找到之簽署者的 [*公開金鑰*](../secgloss/p-gly.md)進行解密，並納入為簽章的一部分。</span><span class="sxs-lookup"><span data-stu-id="6516c-111">The signature [*hash*](../secgloss/h-gly.md) is decrypted using the [*public key*](../secgloss/p-gly.md) of the signer found on the signer's [*certificate*](../secgloss/c-gly.md), included as part of the signature.</span></span> <span data-ttu-id="6516c-112">如果解密簽章符合原始檔案的新雜湊，則簽章是由與用來解密雜湊的公開金鑰相關聯之私密金鑰的擁有者所建立。</span><span class="sxs-lookup"><span data-stu-id="6516c-112">If the decrypted signature matches a new hash of the original document, the signature was created by the owner of the private key associated with the public key used to decrypt the hash.</span></span> <span data-ttu-id="6516c-113">此外，簽章所依據的檔，一定不會在建立簽章之後變更。</span><span class="sxs-lookup"><span data-stu-id="6516c-113">In addition, the document that the signature is based on is guaranteed not to have been changed after the signature was created.</span></span>

<span data-ttu-id="6516c-114">提供公開金鑰和簽署者身分識別的憑證也可以檢查是否有效，包括是否已撤銷憑證、憑證是否過期，或是憑證是否由受信任的憑證簽發者所發出。</span><span class="sxs-lookup"><span data-stu-id="6516c-114">The certificate that provided the public key and the identity of the signer can also be checked for validity including such issues as whether the certificate has been revoked, whether the certificate is out of date, or whether the certificate was issued by a trusted certificate issuer.</span></span>

<span data-ttu-id="6516c-115">在下列範例中，會在檔案和簽章中讀取已簽署的內容和 **SignedData** 物件，並檢查用來建立簽章之憑證的有效性。</span><span class="sxs-lookup"><span data-stu-id="6516c-115">In the following example, the content signed and the **SignedData** object are read in from a file and the signature and the validity of the certificate used to create the signature are checked.</span></span>

> [!Note]  
> <span data-ttu-id="6516c-116">如果簽章未以密碼編譯有效，或簽署者的憑證無效，則會引發例外狀況，而且驗證程式必須處理例外狀況。</span><span class="sxs-lookup"><span data-stu-id="6516c-116">If the signature is not cryptographically valid or the certificate of the signer is not valid, an exception is raised and the verifying program must handle the exception.</span></span> <span data-ttu-id="6516c-117">在任何的 CAPICOM 錯誤中 **，會傳回** 負數值的負數值。</span><span class="sxs-lookup"><span data-stu-id="6516c-117">On any CAPICOM error, a negative decimal value of **Err.Number** is returned.</span></span> <span data-ttu-id="6516c-118">如需詳細資訊，請參閱 [**CAPICOM \_ 錯誤碼 \_**](capicom-error-code.md)。</span><span class="sxs-lookup"><span data-stu-id="6516c-118">For more information, see [**CAPICOM\_ERROR\_CODE**](capicom-error-code.md).</span></span> <span data-ttu-id="6516c-119">如需有關 **錯誤** 之正十進位值的詳細資訊，請參閱 winerror.h。</span><span class="sxs-lookup"><span data-stu-id="6516c-119">For information about positive decimal values of **Err.Number**, see Winerror.h.</span></span>

 


```VB
Sub VerifySig(ByVal FileToVerify As String, ByVal FileBase As String)
On Error GoTo ErrorHandler

Dim sdContent As String
Dim sdCheck As String
Dim mySD As SignedData
Set mySD = New SignedData

' Open a file and read the signature.
Open FileToVerify For Input As #1
Input #1, sdCheck
Close #1

' Open a file and input the plaintext content that was signed.
Open FileBase For Input As #2
Input #2, sdContent
Close #1

' Set the detached content upon which the signature is based.
mySD.Content = sdContent

' Verify the detached signature.
On Error Resume Next
    mySD.Verify sdCheck, True
If Err.Number <> 0 Then
    MsgBox "Signature verification failed. " & Err.Description
Else
    MsgBox "Verification complete."
End If

' Release the SignedData object.
Set mySD = Nothing

Exit Sub
ErrorHandler:
    If Err.Number > 0 Then
        MsgBox "Visual Basic error found: " & Err.Description
    Else
        MsgBox "CAPICOM error found: " & Hex(Err.Number)
    End If
End Sub

```



 

 
