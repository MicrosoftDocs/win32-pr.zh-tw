---
description: 設定或抓取已簽署的可執行檔之描述的 URL。
ms.assetid: 854c76fb-5cb3-4200-bab0-fa3fa5bd3abe
title: SignedCode. DescriptionURL 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.DescriptionURL
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 628d176595031f2b87b9fcb5f58ff81838d49be8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106975983"
---
# <a name="signedcodedescriptionurl-property"></a><span data-ttu-id="248d6-103">SignedCode. DescriptionURL 屬性</span><span class="sxs-lookup"><span data-stu-id="248d6-103">SignedCode.DescriptionURL property</span></span>

<span data-ttu-id="248d6-104">\[**DescriptionURL** 屬性可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="248d6-104">\[The **DescriptionURL** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="248d6-105">相反地，請使用平台叫用服務 (PInvoke) 呼叫 WIN32 API [**SignerSignEx**](signersignex.md)、 [**SignerTimeStampEx**](signertimestampex.md)和 [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) 函式，以使用 Authenticode 數位簽章簽署內容。</span><span class="sxs-lookup"><span data-stu-id="248d6-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md), and [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) functions to sign content with an Authenticode digital signature.</span></span> <span data-ttu-id="248d6-106">如需 PInvoke 的詳細資訊，請參閱 [平台叫用教學](https://msdn.microsoft.com/library/aa288468.aspx)課程。</span><span class="sxs-lookup"><span data-stu-id="248d6-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="248d6-107">[.Net 和 cryptoapi Via p/invoke：第1部分](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5)和[.net，以及透過 p/invoke](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6)叫用的 cryptoapi：[利用 CAPICOM 和 p/invoke 擴充 .net 密碼](/previous-versions/ms867087(v=msdn.10))編譯的第二部分，可能也很有用。\]</span><span class="sxs-lookup"><span data-stu-id="248d6-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="248d6-108">**DescriptionURL** 屬性會設定或抓取已簽署的可執行檔之描述的 URL。</span><span class="sxs-lookup"><span data-stu-id="248d6-108">The **DescriptionURL** property sets or retrieves the URL of a description of the signed executable file.</span></span>

## <a name="syntax"></a><span data-ttu-id="248d6-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="248d6-109">Syntax</span></span>


```VB
SignedCode.DescriptionURL As String
```



## <a name="property-value"></a><span data-ttu-id="248d6-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="248d6-110">Property value</span></span>

<span data-ttu-id="248d6-111">已簽署可執行檔之描述的 URL。</span><span class="sxs-lookup"><span data-stu-id="248d6-111">The URL of a description of the signed executable file.</span></span>

## <a name="remarks"></a><span data-ttu-id="248d6-112">備註</span><span class="sxs-lookup"><span data-stu-id="248d6-112">Remarks</span></span>

<span data-ttu-id="248d6-113">**DescriptionURL** 是出現在 [Authenticode 驗證] 對話方塊連結中之 [**描述**](signedcode-description.md)的 URL。</span><span class="sxs-lookup"><span data-stu-id="248d6-113">The **DescriptionURL** is the URL to which the [**Description**](signedcode-description.md) that appears in the Authenticode verification dialog box links.</span></span> <span data-ttu-id="248d6-114">如果此屬性為 **Null**，則 **描述** 不會作為連結運作。</span><span class="sxs-lookup"><span data-stu-id="248d6-114">If this property is **NULL**, the **Description** does not function as a link.</span></span>

## <a name="requirements"></a><span data-ttu-id="248d6-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="248d6-115">Requirements</span></span>



| <span data-ttu-id="248d6-116">需求</span><span class="sxs-lookup"><span data-stu-id="248d6-116">Requirement</span></span> | <span data-ttu-id="248d6-117">值</span><span class="sxs-lookup"><span data-stu-id="248d6-117">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="248d6-118">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="248d6-118">Redistributable</span></span><br/> | <span data-ttu-id="248d6-119">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="248d6-119">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="248d6-120">DLL</span><span class="sxs-lookup"><span data-stu-id="248d6-120">DLL</span></span><br/>             | <dl> <span data-ttu-id="248d6-121"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="248d6-121"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="248d6-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="248d6-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="248d6-123">**SignedCode**</span><span class="sxs-lookup"><span data-stu-id="248d6-123">**SignedCode**</span></span>](signedcode.md)
</dt> </dl>

 

 
