---
title: 'INapSoHConstructor 介面 (NapProtocol .h) '
description: Sha 用來建立 SoHRequests，以及由 Shv 用來建立 SoHResponses。
ms.assetid: ad79c80a-3003-4465-b350-77890c217d63
keywords:
- INapSoHConstructor 介面 NAP
- INapSoHConstructor 介面 NAP，描述
topic_type:
- apiref
api_name:
- INapSoHConstructor
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 546a6d3b4ec262fdd725af24211338e848b2b848
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103933977"
---
# <a name="inapsohconstructor-interface"></a><span data-ttu-id="3f40c-105">INapSoHConstructor 介面</span><span class="sxs-lookup"><span data-stu-id="3f40c-105">INapSoHConstructor interface</span></span>

> [!Note]  
> <span data-ttu-id="3f40c-106">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="3f40c-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="3f40c-107">**INapSoHConstructor** 會提供方法，讓 sha 用來建立 [**SoHRequests**](/windows/win32/api/naptypes/ns-naptypes-soh) ，並由 Shv 用來建立 **SoHResponses**。</span><span class="sxs-lookup"><span data-stu-id="3f40c-107">The **INapSoHConstructor** provides methods that are used by SHAs to construct [**SoHRequests**](/windows/win32/api/naptypes/ns-naptypes-soh) and by SHVs to construct **SoHResponses**.</span></span>

## <a name="members"></a><span data-ttu-id="3f40c-108">成員</span><span class="sxs-lookup"><span data-stu-id="3f40c-108">Members</span></span>

<span data-ttu-id="3f40c-109">**INapSoHConstructor** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="3f40c-109">The **INapSoHConstructor** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="3f40c-110">**INapSoHConstructor** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="3f40c-110">**INapSoHConstructor** also has these types of members:</span></span>

-   [<span data-ttu-id="3f40c-111">方法</span><span class="sxs-lookup"><span data-stu-id="3f40c-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="3f40c-112">方法</span><span class="sxs-lookup"><span data-stu-id="3f40c-112">Methods</span></span>

<span data-ttu-id="3f40c-113">**INapSoHConstructor** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="3f40c-113">The **INapSoHConstructor** interface has these methods.</span></span>



| <span data-ttu-id="3f40c-114">方法</span><span class="sxs-lookup"><span data-stu-id="3f40c-114">Method</span></span>                                                                                   | <span data-ttu-id="3f40c-115">描述</span><span class="sxs-lookup"><span data-stu-id="3f40c-115">Description</span></span>                                         |
|:-----------------------------------------------------------------------------------------|:----------------------------------------------------|
| [<span data-ttu-id="3f40c-116">**INapSoHConstructor::AppendAttribute**</span><span class="sxs-lookup"><span data-stu-id="3f40c-116">**INapSoHConstructor::AppendAttribute**</span></span>](inapsohconstructor-appendattribute-method.md) | <span data-ttu-id="3f40c-117">將 TLV 新增至 SoH 緩衝區的結尾。</span><span class="sxs-lookup"><span data-stu-id="3f40c-117">Adds a TLV to the end of the SoH buffer.</span></span><br/> |
| [<span data-ttu-id="3f40c-118">**INapSoHConstructor::GetSoH**</span><span class="sxs-lookup"><span data-stu-id="3f40c-118">**INapSoHConstructor::GetSoH**</span></span>](inapsohconstructor-getsoh-method.md)                   | <span data-ttu-id="3f40c-119">抓取已建造的 SoH 封包。</span><span class="sxs-lookup"><span data-stu-id="3f40c-119">Retrieves the constructed SoH packet.</span></span><br/>    |
| [<span data-ttu-id="3f40c-120">**INapSoHConstructor：： Initialize**</span><span class="sxs-lookup"><span data-stu-id="3f40c-120">**INapSoHConstructor::Initialize**</span></span>](inapsohconstructor-initialize-method.md)           | <span data-ttu-id="3f40c-121">初始化 SoH 封包。</span><span class="sxs-lookup"><span data-stu-id="3f40c-121">Initializes the SoH packet.</span></span><br/>              |
| [<span data-ttu-id="3f40c-122">**INapSoHConstructor：： Validate**</span><span class="sxs-lookup"><span data-stu-id="3f40c-122">**INapSoHConstructor::Validate**</span></span>](inapsohconstructor-validate-method.md)               | <span data-ttu-id="3f40c-123">檢查 SoH 封包的有效性。</span><span class="sxs-lookup"><span data-stu-id="3f40c-123">Checks the validity of the SoH packet.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="3f40c-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="3f40c-124">Requirements</span></span>



| <span data-ttu-id="3f40c-125">需求</span><span class="sxs-lookup"><span data-stu-id="3f40c-125">Requirement</span></span> | <span data-ttu-id="3f40c-126">值</span><span class="sxs-lookup"><span data-stu-id="3f40c-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f40c-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3f40c-127">Minimum supported client</span></span><br/> | <span data-ttu-id="3f40c-128">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3f40c-128">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="3f40c-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3f40c-129">Minimum supported server</span></span><br/> | <span data-ttu-id="3f40c-130">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3f40c-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="3f40c-131">標頭</span><span class="sxs-lookup"><span data-stu-id="3f40c-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="3f40c-132"><dt>NapProtocol。h</dt></span><span class="sxs-lookup"><span data-stu-id="3f40c-132"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="3f40c-133">Idl</span><span class="sxs-lookup"><span data-stu-id="3f40c-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3f40c-134"><dt>NapProtocol .idl</dt></span><span class="sxs-lookup"><span data-stu-id="3f40c-134"><dt>NapProtocol.idl</dt></span></span> </dl> |
| <span data-ttu-id="3f40c-135">DLL</span><span class="sxs-lookup"><span data-stu-id="3f40c-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3f40c-136"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3f40c-136"><dt>Qutil.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="3f40c-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3f40c-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f40c-138">NAP 介面</span><span class="sxs-lookup"><span data-stu-id="3f40c-138">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="3f40c-139">NAP 參考</span><span class="sxs-lookup"><span data-stu-id="3f40c-139">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

