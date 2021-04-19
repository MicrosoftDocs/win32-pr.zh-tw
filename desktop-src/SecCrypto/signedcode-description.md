---
description: 設定或抓取已簽署之可執行檔的描述。
ms.assetid: 39ce37bd-fe3e-4195-a132-93f3743f7370
title: SignedCode。 Description 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.Description
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b5783dd5e662aed33722a1c587bfcdc3cab76c78
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990267"
---
# <a name="signedcodedescription-property"></a><span data-ttu-id="98d52-103">SignedCode。 Description 屬性</span><span class="sxs-lookup"><span data-stu-id="98d52-103">SignedCode.Description property</span></span>

<span data-ttu-id="98d52-104">\[[ **描述** ] 屬性可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="98d52-104">\[The **Description** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="98d52-105">相反地，請使用平台叫用服務 (PInvoke) 呼叫 WIN32 API [**SignerSignEx**](signersignex.md)、 [**SignerTimeStampEx**](signertimestampex.md)和 [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) 函式，以使用 Authenticode 數位簽章簽署內容。</span><span class="sxs-lookup"><span data-stu-id="98d52-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md), and [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) functions to sign content with an Authenticode digital signature.</span></span> <span data-ttu-id="98d52-106">如需 PInvoke 的詳細資訊，請參閱 [平台叫用教學](https://msdn.microsoft.com/library/aa288468.aspx)課程。</span><span class="sxs-lookup"><span data-stu-id="98d52-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="98d52-107">[.Net 和 cryptoapi Via p/invoke：第1部分](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5)和[.net，以及透過 p/invoke](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6)叫用的 cryptoapi：[利用 CAPICOM 和 p/invoke 擴充 .net 密碼](/previous-versions/ms867087(v=msdn.10))編譯的第二部分，可能也很有用。\]</span><span class="sxs-lookup"><span data-stu-id="98d52-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="98d52-108">**Description** 屬性會設定或抓取已簽署之可執行檔的描述。</span><span class="sxs-lookup"><span data-stu-id="98d52-108">The **Description** property sets or retrieves the description of the signed executable file.</span></span>

## <a name="syntax"></a><span data-ttu-id="98d52-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="98d52-109">Syntax</span></span>


```VB
SignedCode.Description As String
```



## <a name="property-value"></a><span data-ttu-id="98d52-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="98d52-110">Property value</span></span>

<span data-ttu-id="98d52-111">已簽署之可執行檔的描述。</span><span class="sxs-lookup"><span data-stu-id="98d52-111">The description of the signed executable file.</span></span>

## <a name="remarks"></a><span data-ttu-id="98d52-112">備註</span><span class="sxs-lookup"><span data-stu-id="98d52-112">Remarks</span></span>

<span data-ttu-id="98d52-113">描述是出現在 [Authenticode 驗證] 對話方塊中的文字。</span><span class="sxs-lookup"><span data-stu-id="98d52-113">The description is the text that appears in the Authenticode verification dialog box.</span></span> <span data-ttu-id="98d52-114">文字應該會描述已簽署的可執行檔。</span><span class="sxs-lookup"><span data-stu-id="98d52-114">The text should describe the signed executable file.</span></span> <span data-ttu-id="98d52-115">如果此屬性為 **Null**，對話方塊會顯示可執行檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="98d52-115">If this property is **NULL**, the dialog box displays the name of the executable file.</span></span>

## <a name="requirements"></a><span data-ttu-id="98d52-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="98d52-116">Requirements</span></span>



| <span data-ttu-id="98d52-117">需求</span><span class="sxs-lookup"><span data-stu-id="98d52-117">Requirement</span></span> | <span data-ttu-id="98d52-118">值</span><span class="sxs-lookup"><span data-stu-id="98d52-118">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="98d52-119">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="98d52-119">Redistributable</span></span><br/> | <span data-ttu-id="98d52-120">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="98d52-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="98d52-121">DLL</span><span class="sxs-lookup"><span data-stu-id="98d52-121">DLL</span></span><br/>             | <dl> <span data-ttu-id="98d52-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98d52-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98d52-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="98d52-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98d52-124">**SignedCode**</span><span class="sxs-lookup"><span data-stu-id="98d52-124">**SignedCode**</span></span>](signedcode.md)
</dt> </dl>

 

 
