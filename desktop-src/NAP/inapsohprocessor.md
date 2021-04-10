---
title: 'INapSoHProcessor 介面 (NapProtocol .h) '
description: Sha 用來處理 SoHResponses 和 Shv 的內容，以處理 SoHRequests 的內容。
ms.assetid: c2dd71ca-a4dd-44d2-81ab-b83e90599a2f
keywords:
- INapSoHProcessor 介面 NAP
- INapSoHProcessor 介面 NAP，描述
topic_type:
- apiref
api_name:
- INapSoHProcessor
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c43abf137bb267468deeb9d4bd47546275ba6c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024620"
---
# <a name="inapsohprocessor-interface"></a><span data-ttu-id="17108-105">INapSoHProcessor 介面</span><span class="sxs-lookup"><span data-stu-id="17108-105">INapSoHProcessor interface</span></span>

> [!Note]  
> <span data-ttu-id="17108-106">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="17108-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="17108-107">**INapSoHProcessor** 會提供方法，讓 sha 用來處理 [**SoHResponses**](/windows/win32/api/naptypes/ns-naptypes-soh)的內容，以及由 shv 處理 **SoHRequests** 內容。</span><span class="sxs-lookup"><span data-stu-id="17108-107">The **INapSoHProcessor** provides methods that are used by SHAs to process the contents of [**SoHResponses**](/windows/win32/api/naptypes/ns-naptypes-soh) and by SHVs to process the contents of **SoHRequests**.</span></span>

## <a name="members"></a><span data-ttu-id="17108-108">成員</span><span class="sxs-lookup"><span data-stu-id="17108-108">Members</span></span>

<span data-ttu-id="17108-109">**INapSoHProcessor** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="17108-109">The **INapSoHProcessor** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="17108-110">**INapSoHProcessor** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="17108-110">**INapSoHProcessor** also has these types of members:</span></span>

-   [<span data-ttu-id="17108-111">方法</span><span class="sxs-lookup"><span data-stu-id="17108-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="17108-112">方法</span><span class="sxs-lookup"><span data-stu-id="17108-112">Methods</span></span>

<span data-ttu-id="17108-113">**INapSoHProcessor** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="17108-113">The **INapSoHProcessor** interface has these methods.</span></span>



| <span data-ttu-id="17108-114">方法</span><span class="sxs-lookup"><span data-stu-id="17108-114">Method</span></span>                                                                                           | <span data-ttu-id="17108-115">描述</span><span class="sxs-lookup"><span data-stu-id="17108-115">Description</span></span>                                                                           |
|:-------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [<span data-ttu-id="17108-116">**INapSoHProcessor::FindNextAttribute**</span><span class="sxs-lookup"><span data-stu-id="17108-116">**INapSoHProcessor::FindNextAttribute**</span></span>](inapsohprocessor-findnextattribute-method.md)         | <span data-ttu-id="17108-117">尋找下一個 SoH 封包屬性的位置索引。</span><span class="sxs-lookup"><span data-stu-id="17108-117">Finds the location index of the next SoH packet attribute.</span></span><br/>                 |
| [<span data-ttu-id="17108-118">**INapSoHProcessor：： GetAttribute**</span><span class="sxs-lookup"><span data-stu-id="17108-118">**INapSoHProcessor::GetAttribute**</span></span>](inapsohprocessor-getattribute-method.md)                   | <span data-ttu-id="17108-119">抓取屬性型別和值。</span><span class="sxs-lookup"><span data-stu-id="17108-119">Retrieves the attribute type and value.</span></span><br/>                                    |
| [<span data-ttu-id="17108-120">**INapSoHProcessor::GetNumberOfAttributes**</span><span class="sxs-lookup"><span data-stu-id="17108-120">**INapSoHProcessor::GetNumberOfAttributes**</span></span>](inapsohprocessor-getnumberofattributes-method.md) | <span data-ttu-id="17108-121">捕獲 SoH 中包含的屬性數目。</span><span class="sxs-lookup"><span data-stu-id="17108-121">Retrieves the number of attributes contained in the SoH.</span></span><br/>                   |
| [<span data-ttu-id="17108-122">**INapSoHProcessor：： Initialize**</span><span class="sxs-lookup"><span data-stu-id="17108-122">**INapSoHProcessor::Initialize**</span></span>](inapsohprocessor-initialize-method.md)                       | <span data-ttu-id="17108-123">初始化 SoH 通訊協定封包和 NAP 系統以進行內容處理。</span><span class="sxs-lookup"><span data-stu-id="17108-123">Initializes the SoH protocol packet and NAP System for content processing.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="17108-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="17108-124">Requirements</span></span>



| <span data-ttu-id="17108-125">需求</span><span class="sxs-lookup"><span data-stu-id="17108-125">Requirement</span></span> | <span data-ttu-id="17108-126">值</span><span class="sxs-lookup"><span data-stu-id="17108-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="17108-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="17108-127">Minimum supported client</span></span><br/> | <span data-ttu-id="17108-128">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="17108-128">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="17108-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="17108-129">Minimum supported server</span></span><br/> | <span data-ttu-id="17108-130">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="17108-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="17108-131">標頭</span><span class="sxs-lookup"><span data-stu-id="17108-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="17108-132"><dt>NapProtocol。h</dt></span><span class="sxs-lookup"><span data-stu-id="17108-132"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="17108-133">Idl</span><span class="sxs-lookup"><span data-stu-id="17108-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="17108-134"><dt>NapProtocol .idl</dt></span><span class="sxs-lookup"><span data-stu-id="17108-134"><dt>NapProtocol.idl</dt></span></span> </dl> |
| <span data-ttu-id="17108-135">DLL</span><span class="sxs-lookup"><span data-stu-id="17108-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17108-136"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17108-136"><dt>Qutil.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="17108-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="17108-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17108-138">NAP 介面</span><span class="sxs-lookup"><span data-stu-id="17108-138">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="17108-139">NAP 參考</span><span class="sxs-lookup"><span data-stu-id="17108-139">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

