---
description: 建立 Authenticode 數位簽章，並簽署 SignedCode 中指定的可執行檔。
ms.assetid: db17be29-35ec-4468-b5cc-5ba64c4cf3fb
title: SignedCode. Sign 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.Sign
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 36e5c813b997ae452d44764ed88f51b273c75528
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996232"
---
# <a name="signedcodesign-method"></a><span data-ttu-id="b2f15-103">SignedCode. Sign 方法</span><span class="sxs-lookup"><span data-stu-id="b2f15-103">SignedCode.Sign method</span></span>

<span data-ttu-id="b2f15-104">\[**Sign** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="b2f15-104">\[The **Sign** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b2f15-105">相反地，請使用平台叫用服務 (PInvoke) 呼叫 WIN32 API [**SignerSignEx**](signersignex.md)、 [**SignerTimeStampEx**](signertimestampex.md)和 [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) 函式，以使用 Authenticode 數位簽章簽署內容。</span><span class="sxs-lookup"><span data-stu-id="b2f15-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md), and [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) functions to sign content with an Authenticode digital signature.</span></span> <span data-ttu-id="b2f15-106">如需 PInvoke 的詳細資訊，請參閱 [平台叫用教學](https://msdn.microsoft.com/library/aa288468.aspx)課程。</span><span class="sxs-lookup"><span data-stu-id="b2f15-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="b2f15-107">[.Net 和 cryptoapi Via p/invoke：第1部分](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5)和[.net，以及透過 p/invoke](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6)叫用的 cryptoapi：[利用 CAPICOM 和 p/invoke 擴充 .net 密碼](/previous-versions/ms867087(v=msdn.10))編譯的第二部分，可能也很有用。\]</span><span class="sxs-lookup"><span data-stu-id="b2f15-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="b2f15-108">**Sign** 方法會建立 Authenticode 數位簽章，並簽署 [**SignedCode**](signedcode-filename.md)中指定的可執行檔。</span><span class="sxs-lookup"><span data-stu-id="b2f15-108">The **Sign** method creates an Authenticode digital signature and signs the executable file specified in the [**SignedCode.FileName**](signedcode-filename.md) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2f15-109">語法</span><span class="sxs-lookup"><span data-stu-id="b2f15-109">Syntax</span></span>


```VB
SignedCode.Sign( _
  [ ByVal Signer ] _
)
```



## <a name="parameters"></a><span data-ttu-id="b2f15-110">參數</span><span class="sxs-lookup"><span data-stu-id="b2f15-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2f15-111">*簽署者* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="b2f15-111">*Signer* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b2f15-112">[**簽署者**](signer.md)物件，該物件可存取用來簽署程式碼的憑證私密金鑰。</span><span class="sxs-lookup"><span data-stu-id="b2f15-112">A [**Signer**](signer.md) object that has access to the private key of the certificate used to sign the code.</span></span> <span data-ttu-id="b2f15-113">預設值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="b2f15-113">The default value is **Null**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2f15-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="b2f15-114">Return value</span></span>

<span data-ttu-id="b2f15-115">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="b2f15-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2f15-116">備註</span><span class="sxs-lookup"><span data-stu-id="b2f15-116">Remarks</span></span>

<span data-ttu-id="b2f15-117">在呼叫 **Sign** 方法之前，必須在 [**FileName**](signedcode-filename.md) 屬性中指定包含程式碼的檔案。</span><span class="sxs-lookup"><span data-stu-id="b2f15-117">Before the **Sign** method is called, the file that contains the code must be specified in the [**FileName**](signedcode-filename.md) property.</span></span>

<span data-ttu-id="b2f15-118">如果可執行檔已經簽署，這個方法會覆寫現有的簽章。</span><span class="sxs-lookup"><span data-stu-id="b2f15-118">If the executable file is already signed, this method overwrites the existing signature.</span></span>

<span data-ttu-id="b2f15-119">下列結果適用于 *簽署者* 參數值：</span><span class="sxs-lookup"><span data-stu-id="b2f15-119">The following results apply to the *Signer* parameter value:</span></span>

-   <span data-ttu-id="b2f15-120">如果 *簽署者* 參數不是 **Null**，這個方法會使用相關聯憑證所指向的私密金鑰來加密簽章。</span><span class="sxs-lookup"><span data-stu-id="b2f15-120">If the *Signer* parameter is not **NULL**, this method uses the private key pointed to by the associated certificate to encrypt the signature.</span></span> <span data-ttu-id="b2f15-121">如果憑證所指向的私密金鑰無法使用，方法將會失敗。</span><span class="sxs-lookup"><span data-stu-id="b2f15-121">If the private key pointed to by the certificate is not available, the method fails.</span></span>
-   <span data-ttu-id="b2f15-122">如果 *簽署者* 參數為 **Null** ，而且目前使用者的存放區中只有一個憑證可 \_ 存取具有程式碼簽署功能的私密金鑰，則會使用該憑證來建立簽章。</span><span class="sxs-lookup"><span data-stu-id="b2f15-122">If the *Signer* parameter is **NULL** and there is exactly one certificate in the CURRENT\_USER MY store that has access to a private key with code signing capability, that certificate is used to create the signature.</span></span>
-   <span data-ttu-id="b2f15-123">如果 *簽署者* 參數為 **Null**， [**EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) 屬性值為 true，而且目前使用者的存放區中有一個以上的憑證具有 \_ 程式碼簽署功能的可用私密金鑰，則會出現一個對話方塊，讓使用者選取所要使用的憑證。</span><span class="sxs-lookup"><span data-stu-id="b2f15-123">If the *Signer* parameter is **NULL**, the [**Settings.EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) property value is true, and there is more than one certificate in the CURRENT\_USER MY store with an available private key with code signing capability, a dialog box appears that allows the user to select which certificate is used.</span></span>
-   <span data-ttu-id="b2f15-124">如果 *簽署者* 參數為 **Null** ，而且 [**EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) 屬性為 false，則方法會失敗。</span><span class="sxs-lookup"><span data-stu-id="b2f15-124">If the *Signer* parameter is **NULL** and the [**Settings.EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) property is false, the method fails.</span></span>
-   <span data-ttu-id="b2f15-125">如果 *簽署者* 參數為 **Null** ，而且目前使用者的存放區中沒有具有 \_ 程式碼簽署功能之可用私密金鑰的憑證，則該方法會失敗。</span><span class="sxs-lookup"><span data-stu-id="b2f15-125">If the *Signer* parameter is **NULL** and there are no certificates in the CURRENT\_USER MY store with an available private key with code signing capability, the method fails.</span></span>

<span data-ttu-id="b2f15-126">這個方法會使用 SHA-1 雜湊演算法。</span><span class="sxs-lookup"><span data-stu-id="b2f15-126">This method uses the SHA-1 hashing algorithm.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2f15-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="b2f15-127">Requirements</span></span>



| <span data-ttu-id="b2f15-128">需求</span><span class="sxs-lookup"><span data-stu-id="b2f15-128">Requirement</span></span> | <span data-ttu-id="b2f15-129">值</span><span class="sxs-lookup"><span data-stu-id="b2f15-129">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b2f15-130">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="b2f15-130">Redistributable</span></span><br/> | <span data-ttu-id="b2f15-131">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="b2f15-131">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="b2f15-132">DLL</span><span class="sxs-lookup"><span data-stu-id="b2f15-132">DLL</span></span><br/>             | <dl> <span data-ttu-id="b2f15-133"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b2f15-133"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
