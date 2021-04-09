---
title: 'IBackgroundCopyManager 介面 (>deliveryoptimization .h) '
description: 建立傳送作業、抓取包含佇列中之作業的列舉值物件，以及從佇列中取出個別的作業。
ms.assetid: EA7CB5CE-5E95-4C6D-8026-4B8375EE216A
keywords:
- IBackgroundCopyManager 介面
- IBackgroundCopyManager 介面，說明
topic_type:
- apiref
api_name:
- IBackgroundCopyManager
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6fa752398c0849c987e2a28b804e65a8361e15b0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934498"
---
# <a name="ibackgroundcopymanager-interface"></a><span data-ttu-id="c95eb-105">IBackgroundCopyManager 介面</span><span class="sxs-lookup"><span data-stu-id="c95eb-105">IBackgroundCopyManager interface</span></span>

<span data-ttu-id="c95eb-106">建立傳送作業、抓取包含佇列中之作業的列舉值物件，以及從佇列中取出個別的作業。</span><span class="sxs-lookup"><span data-stu-id="c95eb-106">Creates transfer jobs, retrieves an enumerator object that contains the jobs in the queue, and retrieves individual jobs from the queue.</span></span>

## <a name="members"></a><span data-ttu-id="c95eb-107">成員</span><span class="sxs-lookup"><span data-stu-id="c95eb-107">Members</span></span>

<span data-ttu-id="c95eb-108">**IBackgroundCopyManager** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="c95eb-108">The **IBackgroundCopyManager** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="c95eb-109">**IBackgroundCopyManager** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="c95eb-109">**IBackgroundCopyManager** also has these types of members:</span></span>

-   [<span data-ttu-id="c95eb-110">方法</span><span class="sxs-lookup"><span data-stu-id="c95eb-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c95eb-111">方法</span><span class="sxs-lookup"><span data-stu-id="c95eb-111">Methods</span></span>

<span data-ttu-id="c95eb-112">**IBackgroundCopyManager** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="c95eb-112">The **IBackgroundCopyManager** interface has these methods.</span></span>



| <span data-ttu-id="c95eb-113">方法</span><span class="sxs-lookup"><span data-stu-id="c95eb-113">Method</span></span>                                                | <span data-ttu-id="c95eb-114">描述</span><span class="sxs-lookup"><span data-stu-id="c95eb-114">Description</span></span>                                          |
|:------------------------------------------------------|:-----------------------------------------------------|
| [<span data-ttu-id="c95eb-115">**>batchclient.joboperations.createjob**</span><span class="sxs-lookup"><span data-stu-id="c95eb-115">**CreateJob**</span></span>](ibackgroundcopymanager-createjob.md) | <span data-ttu-id="c95eb-116">建立傳送工作。</span><span class="sxs-lookup"><span data-stu-id="c95eb-116">Creates a transfer job.</span></span><br/>                   |
| [<span data-ttu-id="c95eb-117">**GetJob**</span><span class="sxs-lookup"><span data-stu-id="c95eb-117">**GetJob**</span></span>](ibackgroundcopymanager-getjob.md)       | <span data-ttu-id="c95eb-118">從佇列中取出指定的工作。</span><span class="sxs-lookup"><span data-stu-id="c95eb-118">Retrieves a specified job from the queue.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c95eb-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="c95eb-119">Requirements</span></span>



| <span data-ttu-id="c95eb-120">需求</span><span class="sxs-lookup"><span data-stu-id="c95eb-120">Requirement</span></span> | <span data-ttu-id="c95eb-121">值</span><span class="sxs-lookup"><span data-stu-id="c95eb-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c95eb-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c95eb-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c95eb-123">Windows 10， \[ 僅限1709版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c95eb-123">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c95eb-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c95eb-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c95eb-125">僅限 Windows Server，版本 1709 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c95eb-125">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="c95eb-126">標頭</span><span class="sxs-lookup"><span data-stu-id="c95eb-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="c95eb-127"><dt>>deliveryoptimization。h</dt></span><span class="sxs-lookup"><span data-stu-id="c95eb-127"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="c95eb-128">Idl</span><span class="sxs-lookup"><span data-stu-id="c95eb-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c95eb-129"><dt>>deliveryoptimization .idl</dt></span><span class="sxs-lookup"><span data-stu-id="c95eb-129"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="c95eb-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="c95eb-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="c95eb-131"><dt>Dosvc .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c95eb-131"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="c95eb-132">DLL</span><span class="sxs-lookup"><span data-stu-id="c95eb-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c95eb-133"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c95eb-133"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="c95eb-134">IID</span><span class="sxs-lookup"><span data-stu-id="c95eb-134">IID</span></span><br/>                      | <span data-ttu-id="c95eb-135">IID_IBackgroundCopyManager 定義為5CE34C0D-0DC9-4C1F-897C-DAA1B78CEE7C</span><span class="sxs-lookup"><span data-stu-id="c95eb-135">IID_IBackgroundCopyManager is defined as 5CE34C0D-0DC9-4C1F-897C-DAA1B78CEE7C</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="c95eb-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c95eb-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c95eb-137">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="c95eb-137">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> </dl>

 

