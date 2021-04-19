---
description: 在 SignedCode 中指定的已簽署可執行檔上建立 Authenticode 時間戳記簽章。
ms.assetid: 8f4c9901-b509-4e4c-82f9-a802b0896a11
title: SignedCode Timestamp 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.Timestamp
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 1b0f4478e4ece5188a96257a8a1dcc9722caa140
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987116"
---
# <a name="signedcodetimestamp-method"></a><span data-ttu-id="0808e-103">SignedCode Timestamp 方法</span><span class="sxs-lookup"><span data-stu-id="0808e-103">SignedCode.Timestamp method</span></span>

<span data-ttu-id="0808e-104">\[Timestamp 方法可用於 [需求 **]** 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="0808e-104">\[The **Timestamp** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="0808e-105">相反地，請使用平台叫用服務 (PInvoke) 呼叫 WIN32 API [**SignerSignEx**](signersignex.md)、 [**SignerTimeStampEx**](signertimestampex.md)和 [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) 函式，以使用 Authenticode 數位簽章簽署內容。</span><span class="sxs-lookup"><span data-stu-id="0808e-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md), and [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) functions to sign content with an Authenticode digital signature.</span></span> <span data-ttu-id="0808e-106">如需 PInvoke 的詳細資訊，請參閱 [平台叫用教學](https://msdn.microsoft.com/library/aa288468.aspx)課程。</span><span class="sxs-lookup"><span data-stu-id="0808e-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="0808e-107">[.Net 和 cryptoapi Via p/invoke：第1部分](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5)和[.net，以及透過 p/invoke](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6)叫用的 cryptoapi：[利用 CAPICOM 和 p/invoke 擴充 .net 密碼](/previous-versions/ms867087(v=msdn.10))編譯的第二部分，可能也很有用。\]</span><span class="sxs-lookup"><span data-stu-id="0808e-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="0808e-108">**Timestamp** 方法會在 **SignedCode** 中指定的已簽署可執行檔上建立 Authenticode 時間戳記簽章。</span><span class="sxs-lookup"><span data-stu-id="0808e-108">The **Timestamp** method creates an Authenticode time stamp signature on the signed executable file specified in the **SignedCode.FileName** property.</span></span> <span data-ttu-id="0808e-109">這個時間戳記是由時間戳記授權單位所執行之已簽署可執行檔的計數器簽章。</span><span class="sxs-lookup"><span data-stu-id="0808e-109">This time stamp is a counter signature on the signed executable file that is performed by a time stamp authority.</span></span>

## <a name="syntax"></a><span data-ttu-id="0808e-110">語法</span><span class="sxs-lookup"><span data-stu-id="0808e-110">Syntax</span></span>


```VB
SignedCode.Timestamp( _
  ByVal URL _
)
```



## <a name="parameters"></a><span data-ttu-id="0808e-111">參數</span><span class="sxs-lookup"><span data-stu-id="0808e-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0808e-112">*URL* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0808e-112">*URL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0808e-113">字串，包含時間戳記伺服器的 URL。</span><span class="sxs-lookup"><span data-stu-id="0808e-113">A string that contains the URL of the time stamp server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0808e-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="0808e-114">Return value</span></span>

<span data-ttu-id="0808e-115">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="0808e-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0808e-116">備註</span><span class="sxs-lookup"><span data-stu-id="0808e-116">Remarks</span></span>

<span data-ttu-id="0808e-117">時間戳記會藉由確認可執行檔是否在時間戳記時簽署，來擴充憑證的有效性。</span><span class="sxs-lookup"><span data-stu-id="0808e-117">A time stamp extends the validity of a certificate by verifying that the executable file was signed at the time that it was time stamped.</span></span>

<span data-ttu-id="0808e-118">在呼叫這個方法之前，必須在 **SignedCode** 中指定要加上時間戳記的已簽署可執行檔，而且必須呼叫 [**SignedCode**](signedcode-sign.md) 方法來簽署可執行檔。</span><span class="sxs-lookup"><span data-stu-id="0808e-118">Before this method can be called, the signed executable file to be time stamped must be specified in the **SignedCode.FileName** property, and the [**SignedCode.Sign**](signedcode-sign.md) method must be called to sign the executable file.</span></span>

<span data-ttu-id="0808e-119">如果已簽署的可執行檔已加上時間戳記，這個方法會覆寫現有的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="0808e-119">If the signed executable file is already time stamped, this method overwrites the existing time stamp.</span></span>

## <a name="requirements"></a><span data-ttu-id="0808e-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="0808e-120">Requirements</span></span>



| <span data-ttu-id="0808e-121">需求</span><span class="sxs-lookup"><span data-stu-id="0808e-121">Requirement</span></span> | <span data-ttu-id="0808e-122">值</span><span class="sxs-lookup"><span data-stu-id="0808e-122">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0808e-123">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="0808e-123">Redistributable</span></span><br/> | <span data-ttu-id="0808e-124">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="0808e-124">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="0808e-125">DLL</span><span class="sxs-lookup"><span data-stu-id="0808e-125">DLL</span></span><br/>             | <dl> <span data-ttu-id="0808e-126"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0808e-126"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0808e-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0808e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0808e-128">**SignedCode**</span><span class="sxs-lookup"><span data-stu-id="0808e-128">**SignedCode**</span></span>](signedcode.md)
</dt> </dl>

 

 
