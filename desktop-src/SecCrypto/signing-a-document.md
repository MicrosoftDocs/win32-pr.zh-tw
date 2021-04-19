---
description: 簽章的標準用途是簽署文字，並將該帶正負號的文字儲存至檔案。 簽署的文字也可透過網際網路傳送。 簽署的訊息是 PKCS \# 7 格式。
ms.assetid: 67a36123-4fce-4d40-83c3-b9668221276b
title: 簽署檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ce1754cdfa1e89c23525474bae880dc2809c242
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971988"
---
# <a name="signing-a-document"></a><span data-ttu-id="f2c2e-105">簽署檔</span><span class="sxs-lookup"><span data-stu-id="f2c2e-105">Signing a Document</span></span>

<span data-ttu-id="f2c2e-106">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="f2c2e-106">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="f2c2e-107">相反地，請使用 .NET Framework 來執行安全性功能。</span><span class="sxs-lookup"><span data-stu-id="f2c2e-107">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="f2c2e-108">如需詳細資訊，請參閱 [使用 CAPICOM 的替代方案](alternatives-to-using-capicom.md)。\]</span><span class="sxs-lookup"><span data-stu-id="f2c2e-108">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="f2c2e-109">簽章的標準用途是簽署文字，並將該帶正負號的文字儲存至檔案。</span><span class="sxs-lookup"><span data-stu-id="f2c2e-109">A standard use of a signature is to sign a text and save that signed text to a file.</span></span> <span data-ttu-id="f2c2e-110">簽署的文字也可透過網際網路傳送。</span><span class="sxs-lookup"><span data-stu-id="f2c2e-110">The signed text could also be sent over the Internet.</span></span> <span data-ttu-id="f2c2e-111">簽署的訊息是 PKCS \# 7 格式。</span><span class="sxs-lookup"><span data-stu-id="f2c2e-111">The signed message is in PKCS \#7 format.</span></span>

<span data-ttu-id="f2c2e-112">在此範例中，會針對卸離的內容建立簽章， (當內容未隨附于簽章) 時。</span><span class="sxs-lookup"><span data-stu-id="f2c2e-112">In this example, the signature is created for detached content (when the content is not included with the signature).</span></span> <span data-ttu-id="f2c2e-113">如果簽章的收件者有一份完整的帶正負號文字，最常使用卸離的簽章。</span><span class="sxs-lookup"><span data-stu-id="f2c2e-113">A detached signature would most often be used if the recipient of the signature has a copy of the exact signed text.</span></span> <span data-ttu-id="f2c2e-114">在下列範例中，會將原始訊息和卸離的簽章寫入個別的檔案。</span><span class="sxs-lookup"><span data-stu-id="f2c2e-114">In the example below, the original message and the detached signature are written to separate files.</span></span>

<span data-ttu-id="f2c2e-115">在任何的 CAPICOM 錯誤中 **，會傳回** 負數值的負數值。</span><span class="sxs-lookup"><span data-stu-id="f2c2e-115">On any CAPICOM error, a negative decimal value of **Err.Number** is returned.</span></span> <span data-ttu-id="f2c2e-116">如需詳細資訊，請參閱 [**CAPICOM \_ 錯誤碼 \_**](capicom-error-code.md)。</span><span class="sxs-lookup"><span data-stu-id="f2c2e-116">For more information, see [**CAPICOM\_ERROR\_CODE**](capicom-error-code.md).</span></span> <span data-ttu-id="f2c2e-117">如需有關 **錯誤** 之正十進位值的詳細資訊，請參閱 winerror.h。</span><span class="sxs-lookup"><span data-stu-id="f2c2e-117">For information about positive decimal values of **Err.Number**, see Winerror.h.</span></span>

<span data-ttu-id="f2c2e-118">建立簽章會使用簽署人的 [*私密金鑰*](../secgloss/p-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="f2c2e-118">Creating a signature uses the signer's [*private key*](../secgloss/p-gly.md).</span></span> <span data-ttu-id="f2c2e-119">只有當簽署者的憑證有相關聯的私密金鑰可供使用時，才能建立簽章。</span><span class="sxs-lookup"><span data-stu-id="f2c2e-119">A signature can only be created if the signer's certificate with an associated private key is available.</span></span> <span data-ttu-id="f2c2e-120">這個 **Sign** 方法的範例不會指定簽署人。</span><span class="sxs-lookup"><span data-stu-id="f2c2e-120">This example of the **Sign** method does not specify a signer.</span></span> <span data-ttu-id="f2c2e-121">如果未指定簽署者，且在 **CAPICOM 我的 \_ \_ 存放區** 中沒有任何憑證有相關聯的私密金鑰，則 **Sign** 方法會失敗。</span><span class="sxs-lookup"><span data-stu-id="f2c2e-121">If a signer is not specified and no certificate in **CAPICOM\_MY\_STORE** has an associated private key, the **Sign** method fails.</span></span> <span data-ttu-id="f2c2e-122">如果 **CAPICOM \_ MY \_ STORE** 中只有一個憑證有相關聯的私密金鑰，則會使用該憑證與其私密金鑰來建立簽章。</span><span class="sxs-lookup"><span data-stu-id="f2c2e-122">If one and only one certificate in **CAPICOM\_MY\_STORE** has an associated private key, that certificate and its private key is used to create the signature.</span></span> <span data-ttu-id="f2c2e-123">如果 [ **CAPICOM \_ MY \_ STORE** ] 存放區中有一個以上的憑證有相關聯的私密金鑰，就會出現一個對話方塊，使用者可以選擇要用來建立簽章的憑證。</span><span class="sxs-lookup"><span data-stu-id="f2c2e-123">If more than one certificate in the **CAPICOM\_MY\_STORE** store has an associated private key, a dialog box appears and the user can choose the certificate to be used to create the signature.</span></span>

<span data-ttu-id="f2c2e-124">當 web 應用程式使用 **Sign** 方法時，一律會顯示提示，並且需要使用者的許可權，才能建立使用該簽署者之私密金鑰的簽章。</span><span class="sxs-lookup"><span data-stu-id="f2c2e-124">When a web-based application uses the **Sign** method, a prompt is always displayed and the user's permission is required before a signature that uses that signer's private key is created.</span></span>


```VB
Sub Signfile(ByVal InputFileName As String, _
    ByVal OutputFileName As String)
    
    On Error GoTo ErrorHandler
    Dim c As String
    Dim s As String
    Dim MyStore As New Store
    Dim Signobj As New SignedData
    Dim Signer As New Signer

    ' NOTE: the name 'Attribute' is not a unique name
    ' and must be preceded by 'CAPICOM.'
    Dim SigningTime As New CAPICOM.Attribute

    ' Open the MY store and retrieve the first certificate from the
    ' Store. The signing operation will only work if this
    ' certificate is valid and has access to the signer's private key.
    MyStore.Open CAPICOM_CURRENT_USER_STORE, "MY", _
        CAPICOM_STORE_OPEN_READ_ONLY
    Signer.Certificate = MyStore.Certificates.Item(1)

    ' Open the input file and read the content to be signed from
    ' the file.
    Open App.Path & "\" & InputFileName For Input As #1
    Input #1, c
    Close #1
    
    ' Set the content to be signed.
    Signobj.Content = c

    ' Save the time the data was signed as a signer attribute.
    SigningTime.Name = CAPICOM_AUTHENTICATED_ATTRIBUTE_SIGNING_TIME
    SigningTime.Value = Now
    Signer.AuthenticatedAttributes.Add SigningTime

    ' Sign the content using the signer's private key.
    ' The 'True' parameter indicates that the content signed is not
    ' included in the signature string.
    s = Signobj.Sign(Signer, True)

    Open App.Path & "\" & OutputFileName For Output As #2
    Write #2, s
    Close #2

    MsgBox ("Signature done - Saved to file" & OutputFileName)
    Set Signobj = Nothing
    Set MyStore = Nothing
    Set Signer = Nothing
    Set SigningTime = Nothing

    Exit Sub

ErrorHandler:
    If Err.Number > 0 Then
        MsgBox ("Visual Basic error found:" & Err.Description)
    Else
        MsgBox ("CAPICOM error found : " & Err.Number)
    End If
End Sub
```



## <a name="related-topics"></a><span data-ttu-id="f2c2e-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="f2c2e-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2c2e-126">**Store. Open**</span><span class="sxs-lookup"><span data-stu-id="f2c2e-126">**Store.Open**</span></span>](store-open.md)
</dt> <dt>

[<span data-ttu-id="f2c2e-127">**簽署者憑證**</span><span class="sxs-lookup"><span data-stu-id="f2c2e-127">**Signer.Certificate**</span></span>](signer-certificate.md)
</dt> <dt>

[<span data-ttu-id="f2c2e-128">**屬性**</span><span class="sxs-lookup"><span data-stu-id="f2c2e-128">**Attribute**</span></span>](attribute.md)
</dt> <dt>

[<span data-ttu-id="f2c2e-129">**SignedData**</span><span class="sxs-lookup"><span data-stu-id="f2c2e-129">**SignedData**</span></span>](signeddata.md)
</dt> </dl>

 

 
