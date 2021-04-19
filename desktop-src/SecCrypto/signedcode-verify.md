---
description: 確認簽署程式碼上的 Authenticode 簽章。
ms.assetid: eecd692d-6b20-4644-a3d9-fba07ee667d7
title: SignedCode Verify 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.Verify
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2ad9ad2cdbf9c8b7970f50446bba0da7a3afdcd4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994874"
---
# <a name="signedcodeverify-method"></a><span data-ttu-id="c3c66-103">SignedCode Verify 方法</span><span class="sxs-lookup"><span data-stu-id="c3c66-103">SignedCode.Verify method</span></span>

<span data-ttu-id="c3c66-104">\[[ **驗證** ] 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="c3c66-104">\[The **Verify** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="c3c66-105">相反地，請使用平台叫用服務 (PInvoke) 呼叫 WIN32 API [**SignerSignEx**](signersignex.md)、 [**SignerTimeStampEx**](signertimestampex.md)和 [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) 函式，以使用 Authenticode 數位簽章簽署內容。</span><span class="sxs-lookup"><span data-stu-id="c3c66-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md), and [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) functions to sign content with an Authenticode digital signature.</span></span> <span data-ttu-id="c3c66-106">如需 PInvoke 的詳細資訊，請參閱 [平台叫用教學](https://msdn.microsoft.com/library/aa288468.aspx)課程。</span><span class="sxs-lookup"><span data-stu-id="c3c66-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="c3c66-107">[.Net 和 cryptoapi Via p/invoke：第1部分](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5)和[.net，以及透過 p/invoke](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6)叫用的 cryptoapi：[利用 CAPICOM 和 p/invoke 擴充 .net 密碼](/previous-versions/ms867087(v=msdn.10))編譯的第二部分，可能也很有用。\]</span><span class="sxs-lookup"><span data-stu-id="c3c66-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="c3c66-108">**Verify** 方法會驗證已簽署程式碼上的 Authenticode 簽章。</span><span class="sxs-lookup"><span data-stu-id="c3c66-108">The **Verify** method verifies the Authenticode signature on the signed code.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3c66-109">語法</span><span class="sxs-lookup"><span data-stu-id="c3c66-109">Syntax</span></span>


```VB
SignedCode.Verify( _
  [ ByVal bUIAllowed ] _
)
```



## <a name="parameters"></a><span data-ttu-id="c3c66-110">參數</span><span class="sxs-lookup"><span data-stu-id="c3c66-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3c66-111">*bUIAllowed* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="c3c66-111">*bUIAllowed* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c3c66-112">指定是否使用對話方塊來驗證簽章的布林值。</span><span class="sxs-lookup"><span data-stu-id="c3c66-112">A Boolean value that specifies whether a dialog box is used to verify the signature.</span></span> <span data-ttu-id="c3c66-113">若為 true，則會產生對話方塊，以判斷程式碼是否受信任。</span><span class="sxs-lookup"><span data-stu-id="c3c66-113">If true, a dialog box is generated to determine whether the code is trusted.</span></span> <span data-ttu-id="c3c66-114">預設值為 false。</span><span class="sxs-lookup"><span data-stu-id="c3c66-114">The default value is false.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3c66-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="c3c66-115">Return value</span></span>

<span data-ttu-id="c3c66-116">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="c3c66-116">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3c66-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="c3c66-117">Requirements</span></span>



| <span data-ttu-id="c3c66-118">需求</span><span class="sxs-lookup"><span data-stu-id="c3c66-118">Requirement</span></span> | <span data-ttu-id="c3c66-119">值</span><span class="sxs-lookup"><span data-stu-id="c3c66-119">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c3c66-120">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="c3c66-120">Redistributable</span></span><br/> | <span data-ttu-id="c3c66-121">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="c3c66-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="c3c66-122">DLL</span><span class="sxs-lookup"><span data-stu-id="c3c66-122">DLL</span></span><br/>             | <dl> <span data-ttu-id="c3c66-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c3c66-123"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3c66-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c3c66-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3c66-125">**SignedCode**</span><span class="sxs-lookup"><span data-stu-id="c3c66-125">**SignedCode**</span></span>](signedcode.md)
</dt> </dl>

 

 
