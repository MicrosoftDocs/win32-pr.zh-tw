---
title: 'IBackgroundCopyJob5 介面 (>deliveryoptimization .h) '
description: 您可以使用此介面來查詢或設定工作的數個選擇性行為。
ms.assetid: C4706E10-40E6-489B-9772-59D581781038
keywords:
- IBackgroundCopyJob5 介面
- IBackgroundCopyJob5 介面，說明
topic_type:
- apiref
api_name:
- IBackgroundCopyJob5
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e76898f7bbfe4d4dc34aec035b842e6671091630
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105324"
---
# <a name="ibackgroundcopyjob5-interface"></a><span data-ttu-id="eeeee-105">IBackgroundCopyJob5 介面</span><span class="sxs-lookup"><span data-stu-id="eeeee-105">IBackgroundCopyJob5 interface</span></span>

<span data-ttu-id="eeeee-106">您可以使用此介面來查詢或設定工作的數個選擇性行為。</span><span class="sxs-lookup"><span data-stu-id="eeeee-106">Use this interface to query or set several optional behaviors of a job.</span></span>

<span data-ttu-id="eeeee-107">若要取得這個介面，請使用做為介面識別碼來呼叫 **IBackgroundCopyJob：： QueryInterface** 方法 `__uuidof(IBackgroundCopyJob5)` 。</span><span class="sxs-lookup"><span data-stu-id="eeeee-107">To get this interface, call the **IBackgroundCopyJob::QueryInterface** method using `__uuidof(IBackgroundCopyJob5)` as the interface identifier.</span></span>

## <a name="members"></a><span data-ttu-id="eeeee-108">成員</span><span class="sxs-lookup"><span data-stu-id="eeeee-108">Members</span></span>

<span data-ttu-id="eeeee-109">**IBackgroundCopyJob5** 介面繼承自 [**IBackgroundCopyJob**](ibackgroundcopyjob-.md)。</span><span class="sxs-lookup"><span data-stu-id="eeeee-109">The **IBackgroundCopyJob5** interface inherits from [**IBackgroundCopyJob**](ibackgroundcopyjob-.md).</span></span> <span data-ttu-id="eeeee-110">**IBackgroundCopyJob5** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="eeeee-110">**IBackgroundCopyJob5** also has these types of members:</span></span>

-   [<span data-ttu-id="eeeee-111">方法</span><span class="sxs-lookup"><span data-stu-id="eeeee-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="eeeee-112">方法</span><span class="sxs-lookup"><span data-stu-id="eeeee-112">Methods</span></span>

<span data-ttu-id="eeeee-113">**IBackgroundCopyJob5** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="eeeee-113">The **IBackgroundCopyJob5** interface has these methods.</span></span>



| <span data-ttu-id="eeeee-114">方法</span><span class="sxs-lookup"><span data-stu-id="eeeee-114">Method</span></span>                                                 | <span data-ttu-id="eeeee-115">描述</span><span class="sxs-lookup"><span data-stu-id="eeeee-115">Description</span></span>                                                |
|:-------------------------------------------------------|:-----------------------------------------------------------|
| [<span data-ttu-id="eeeee-116">**GetProperty**</span><span class="sxs-lookup"><span data-stu-id="eeeee-116">**GetProperty**</span></span>](ibackgroundcopyjob5-getproperty.md) | <span data-ttu-id="eeeee-117">用來取得作業屬性的泛型方法。</span><span class="sxs-lookup"><span data-stu-id="eeeee-117">A generic method for getting DO job properties.</span></span><br/> |
| [<span data-ttu-id="eeeee-118">**SetProperty**</span><span class="sxs-lookup"><span data-stu-id="eeeee-118">**SetProperty**</span></span>](ibackgroundcopyjob5-setproperty.md) | <span data-ttu-id="eeeee-119">設定 DO 作業屬性的泛型方法。</span><span class="sxs-lookup"><span data-stu-id="eeeee-119">A generic method for setting DO job properties.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="eeeee-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="eeeee-120">Requirements</span></span>



| <span data-ttu-id="eeeee-121">需求</span><span class="sxs-lookup"><span data-stu-id="eeeee-121">Requirement</span></span> | <span data-ttu-id="eeeee-122">值</span><span class="sxs-lookup"><span data-stu-id="eeeee-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eeeee-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="eeeee-123">Minimum supported client</span></span><br/> | <span data-ttu-id="eeeee-124">Windows 10， \[ 僅限1709版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eeeee-124">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="eeeee-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="eeeee-125">Minimum supported server</span></span><br/> | <span data-ttu-id="eeeee-126">僅限 Windows Server，版本 1709 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eeeee-126">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="eeeee-127">標頭</span><span class="sxs-lookup"><span data-stu-id="eeeee-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="eeeee-128"><dt>>deliveryoptimization。h</dt></span><span class="sxs-lookup"><span data-stu-id="eeeee-128"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="eeeee-129">Idl</span><span class="sxs-lookup"><span data-stu-id="eeeee-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="eeeee-130"><dt>>deliveryoptimization .idl</dt></span><span class="sxs-lookup"><span data-stu-id="eeeee-130"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="eeeee-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="eeeee-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="eeeee-132"><dt>Dosvc .lib</dt></span><span class="sxs-lookup"><span data-stu-id="eeeee-132"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="eeeee-133">DLL</span><span class="sxs-lookup"><span data-stu-id="eeeee-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eeeee-134"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eeeee-134"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="eeeee-135">IID</span><span class="sxs-lookup"><span data-stu-id="eeeee-135">IID</span></span><br/>                      | <span data-ttu-id="eeeee-136">IID_IBackgroundCopyJob5 定義為 E847030C-BBBA-4657-AF6D-484AA42BF1FE</span><span class="sxs-lookup"><span data-stu-id="eeeee-136">IID_IBackgroundCopyJob5 is defined as E847030C-BBBA-4657-AF6D-484AA42BF1FE</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="eeeee-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eeeee-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eeeee-138">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="eeeee-138">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> </dl>

 

 





