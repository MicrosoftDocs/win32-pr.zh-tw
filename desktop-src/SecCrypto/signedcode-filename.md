---
description: FileName 屬性會設定或抓取可執行檔的路徑。 這是預設屬性。
ms.assetid: 2d2ea87b-86db-40b4-b052-8503beafa08c
title: SignedCode FileName 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.FileName
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e6e31e57376f987b2b5cb47e5e6bd8a0d5e85fba
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995099"
---
# <a name="signedcodefilename-property"></a><span data-ttu-id="74e1c-104">SignedCode FileName 屬性</span><span class="sxs-lookup"><span data-stu-id="74e1c-104">SignedCode.FileName property</span></span>

<span data-ttu-id="74e1c-105">\[[ **檔案名** ] 屬性可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="74e1c-105">\[The **FileName** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="74e1c-106">相反地，請使用平台叫用服務 (PInvoke) 呼叫 WIN32 API [**SignerSignEx**](signersignex.md)、 [**SignerTimeStampEx**](signertimestampex.md)和 [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) 函式，以使用 Authenticode 數位簽章簽署內容。</span><span class="sxs-lookup"><span data-stu-id="74e1c-106">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md), and [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) functions to sign content with an Authenticode digital signature.</span></span> <span data-ttu-id="74e1c-107">如需 PInvoke 的詳細資訊，請參閱 [平台叫用教學](https://msdn.microsoft.com/library/aa288468.aspx)課程。</span><span class="sxs-lookup"><span data-stu-id="74e1c-107">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="74e1c-108">[.Net 和 cryptoapi Via p/invoke：第1部分](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5)和[.net，以及透過 p/invoke](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6)叫用的 cryptoapi：[利用 CAPICOM 和 p/invoke 擴充 .net 密碼](/previous-versions/ms867087(v=msdn.10))編譯的第二部分，可能也很有用。\]</span><span class="sxs-lookup"><span data-stu-id="74e1c-108">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="74e1c-109">**FileName** 屬性會設定或抓取可執行檔的路徑。</span><span class="sxs-lookup"><span data-stu-id="74e1c-109">The **FileName** property sets or retrieves the path to the executable file.</span></span> <span data-ttu-id="74e1c-110">這是預設屬性。</span><span class="sxs-lookup"><span data-stu-id="74e1c-110">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="74e1c-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="74e1c-111">Syntax</span></span>


```VB
SignedCode.FileName As String
```



## <a name="property-value"></a><span data-ttu-id="74e1c-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="74e1c-112">Property value</span></span>

<span data-ttu-id="74e1c-113">可執行檔路徑。</span><span class="sxs-lookup"><span data-stu-id="74e1c-113">The path to the executable file.</span></span>

## <a name="remarks"></a><span data-ttu-id="74e1c-114">備註</span><span class="sxs-lookup"><span data-stu-id="74e1c-114">Remarks</span></span>

<span data-ttu-id="74e1c-115">如果已修改 **FileName** 屬性的值，則會重設整個 [**SignedCode**](signedcode.md) 物件的狀態。</span><span class="sxs-lookup"><span data-stu-id="74e1c-115">If the value of the **FileName** property is modified, the state of the entire [**SignedCode**](signedcode.md) object is reset.</span></span>

## <a name="requirements"></a><span data-ttu-id="74e1c-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="74e1c-116">Requirements</span></span>



| <span data-ttu-id="74e1c-117">需求</span><span class="sxs-lookup"><span data-stu-id="74e1c-117">Requirement</span></span> | <span data-ttu-id="74e1c-118">值</span><span class="sxs-lookup"><span data-stu-id="74e1c-118">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="74e1c-119">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="74e1c-119">Redistributable</span></span><br/> | <span data-ttu-id="74e1c-120">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="74e1c-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="74e1c-121">DLL</span><span class="sxs-lookup"><span data-stu-id="74e1c-121">DLL</span></span><br/>             | <dl> <span data-ttu-id="74e1c-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="74e1c-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74e1c-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="74e1c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74e1c-124">**SignedCode**</span><span class="sxs-lookup"><span data-stu-id="74e1c-124">**SignedCode**</span></span>](signedcode.md)
</dt> </dl>

 

 
