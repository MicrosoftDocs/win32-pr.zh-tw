---
description: 檔可由一個以上的簽署者簽署。
ms.assetid: f81cbf7b-317d-4fab-9b30-88b6c6576db8
title: Cosigning 檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa06cbbc95dc0fe558c6e704bd18102e80221dbc
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106974781"
---
# <a name="cosigning-a-document"></a><span data-ttu-id="c2989-103">Cosigning 檔</span><span class="sxs-lookup"><span data-stu-id="c2989-103">Cosigning a Document</span></span>

<span data-ttu-id="c2989-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="c2989-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="c2989-105">相反地，請使用 .NET Framework 來執行安全性功能。</span><span class="sxs-lookup"><span data-stu-id="c2989-105">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="c2989-106">如需詳細資訊，請參閱 [使用 CAPICOM 的替代方案](alternatives-to-using-capicom.md)。\]</span><span class="sxs-lookup"><span data-stu-id="c2989-106">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="c2989-107">檔可由一個以上的簽署者簽署。</span><span class="sxs-lookup"><span data-stu-id="c2989-107">A document can be signed by more than one signer.</span></span> <span data-ttu-id="c2989-108">例如，當兩個或更多方簽署合約或支出報表時，就會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="c2989-108">This happens when, for instance, two or more parties sign a contract or an expense report.</span></span> <span data-ttu-id="c2989-109">在下列範例中，已簽署的檔是由第二位簽署者所接收。</span><span class="sxs-lookup"><span data-stu-id="c2989-109">In the following example, a document already signed is received by a second signer.</span></span> <span data-ttu-id="c2989-110">這個簽署者會使用 [**CoSign**](signeddata-cosign.md) 方法，將其他簽章附加至檔。</span><span class="sxs-lookup"><span data-stu-id="c2989-110">This signer uses the [**CoSign**](signeddata-cosign.md) method to attach an additional signature to the document.</span></span>

<span data-ttu-id="c2989-111">如果發生任何 CAPICOM 錯誤，則會在 **Err** 屬性中傳回負數值。</span><span class="sxs-lookup"><span data-stu-id="c2989-111">If any CAPICOM error occurs, a negative value is returned in the **Err.Number** property.</span></span> <span data-ttu-id="c2989-112">如需有關 CAPICOM 錯誤碼的詳細資訊，請參閱 [**capicom \_ 錯誤碼 \_**](capicom-error-code.md)。</span><span class="sxs-lookup"><span data-stu-id="c2989-112">For more information about CAPICOM error codes, see [**CAPICOM\_ERROR\_CODE**](capicom-error-code.md).</span></span> <span data-ttu-id="c2989-113">如果 **Err** 屬性中的錯誤碼是正值，則錯誤是 Windows 錯誤。</span><span class="sxs-lookup"><span data-stu-id="c2989-113">If the error code in the **Err.Number** property is a positive value, then the error is a Windows error.</span></span> <span data-ttu-id="c2989-114">如需 Windows 錯誤碼的詳細資訊，請參閱 Winerror.h。</span><span class="sxs-lookup"><span data-stu-id="c2989-114">For information about Windows error codes, see Winerror.h.</span></span>

> [!Note]
> <span data-ttu-id="c2989-115">Cosigning 檔時，也需要 cosigner 擁有具有 [*私密金鑰*](../secgloss/p-gly.md)的可用 [*憑證*](../secgloss/c-gly.md)，才能建立簽章。</span><span class="sxs-lookup"><span data-stu-id="c2989-115">Cosigning a document also requires that the cosigner have an available [*certificate*](../secgloss/c-gly.md) with a [*private key*](../secgloss/p-gly.md) to create the signature.</span></span> <span data-ttu-id="c2989-116">如果未在 [**Sign**](signeddata-sign.md) 方法的呼叫中指定簽署者，且在 \_ 具有相關私密金鑰的 CAPICOM MY 存放區中沒有憑證 \_ ，則方法會失敗。</span><span class="sxs-lookup"><span data-stu-id="c2989-116">If a signer is not specified in the call of the [**Sign**](signeddata-sign.md) method and there is no certificate in CAPICOM\_MY\_STORE with an associated private key, the method fails.</span></span> <span data-ttu-id="c2989-117">如果在具有相關私密金鑰的 CAPICOM MY STORE 中只有一個憑證 \_ \_ ，則會使用該金鑰和憑證。</span><span class="sxs-lookup"><span data-stu-id="c2989-117">If there is one and only one certificate in CAPICOM\_MY\_STORE with an associated private key, that key and certificate are used.</span></span> <span data-ttu-id="c2989-118">如果有一個以上的可用憑證，則會顯示提示，讓使用者選擇所需的憑證。</span><span class="sxs-lookup"><span data-stu-id="c2989-118">If there is more than one usable certificate, a prompt is displayed to allow the user to choose the desired certificate.</span></span>
> 
> <span data-ttu-id="c2989-119">如果在 web 應用程式中使用 [**CoSign**](signeddata-cosign.md) 方法，則在使用該簽署者的私密金鑰建立簽章之前，一律會顯示提示以取得使用者的許可權。</span><span class="sxs-lookup"><span data-stu-id="c2989-119">If the [**CoSign**](signeddata-cosign.md) method is used in a web-based application, a prompt is always displayed to get the user's permission before a signature is created by using that signer's private key.</span></span>

 

<span data-ttu-id="c2989-120">在下列範例中，包含要簽署之檔的檔案，以及該檔的目前簽章都會被讀取、簽章為 cosigned，而新的簽章會寫入檔案。</span><span class="sxs-lookup"><span data-stu-id="c2989-120">In the following example, files that contain the document to be signed and the current signatures on that document are read, the signature is cosigned, and the new signature is written to a file.</span></span> <span data-ttu-id="c2989-121">此範例會使用已中斷連結的簽章，並將資料簽章和簽章放在不同的檔案中。</span><span class="sxs-lookup"><span data-stu-id="c2989-121">The example uses a detached signature with the data signed and the signature in separate files.</span></span>


```VB
Sub CoSignContent(ByVal InputFile1Name As String, ByVal _
    InputFile2Name As String, ByVal OutputFileName As String)

    On Error GoTo ErrorHandler
    Dim c As String
    Dim s As String
    Dim CS As String
    Dim Signobj As New SignedData
    Open InputFile1Name for Input as #1
    Input #1, s
    Close #1
    Open InputFileName2 for input as #2
    Input #2, c 
    Close #2

    Signobj.Content = c
    Signobj.Verify(s)
    CS = Signobj.CoSign
    Open OutputFileName for output as #3
    Write #3, CS
    Close # 3
    Signobj = Nothing
    MsgBox("Cosign finished. Cosignature saved to a file.")
    Exit Sub
ErrorHandler:
    If err.number > 0 Then
        MsgBox("Visual Basic error found:" & err.description)
    Else
        MsgBox("CAPICOM error found : " & err.number)
    End If
End Sub
```



 

 
