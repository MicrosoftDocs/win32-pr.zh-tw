---
title: IDeliveryOptimizationJob2 介面
description: 深入瞭解： IDeliveryOptimizationJob2 介面
keywords:
- IDeliveryOptimizationJob2 介面
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob2
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2019
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 13f5a32b4ddccc203bcae7d6674c4713069355cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970928"
---
# <a name="ideliveryoptimizationjob2-interface"></a><span data-ttu-id="609e2-104">IDeliveryOptimizationJob2 介面</span><span class="sxs-lookup"><span data-stu-id="609e2-104">IDeliveryOptimizationJob2 interface</span></span>

<span data-ttu-id="609e2-105">IDeliveryOptimizationJob2 可讓您將單一檔案新增至下載作業，並立即取出檔案。</span><span class="sxs-lookup"><span data-stu-id="609e2-105">The IDeliveryOptimizationJob2 enables adding a single file to the download job, and retrieving the file immediately.</span></span> <span data-ttu-id="609e2-106">這個介面也支援設定和取得選擇性的工作屬性。</span><span class="sxs-lookup"><span data-stu-id="609e2-106">This interface also supports setting and getting optional job properties.</span></span>

## <a name="members"></a><span data-ttu-id="609e2-107">成員</span><span class="sxs-lookup"><span data-stu-id="609e2-107">Members</span></span>

<span data-ttu-id="609e2-108">**IDeliveryOptimizationJob2** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="609e2-108">The **IDeliveryOptimizationJob2** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="609e2-109">**IDeliveryOptimizationJob2** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="609e2-109">**IDeliveryOptimizationJob2** also has these types of members:</span></span>

- [<span data-ttu-id="609e2-110">方法</span><span class="sxs-lookup"><span data-stu-id="609e2-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="609e2-111">方法</span><span class="sxs-lookup"><span data-stu-id="609e2-111">Methods</span></span>

<span data-ttu-id="609e2-112">**IDeliveryOptimizationJob2** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="609e2-112">The **IDeliveryOptimizationJob2** interface has these methods.</span></span>

| <span data-ttu-id="609e2-113">方法</span><span class="sxs-lookup"><span data-stu-id="609e2-113">Method</span></span>                                              | <span data-ttu-id="609e2-114">描述</span><span class="sxs-lookup"><span data-stu-id="609e2-114">Description</span></span>                                                          |
|:----------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="609e2-115">**AddFile**</span><span class="sxs-lookup"><span data-stu-id="609e2-115">**AddFile**</span></span>](ideliveryoptimizationjob2-addfile.md) | <span data-ttu-id="609e2-116">AddFile 方法會將單一檔案新增至現有的作業。</span><span class="sxs-lookup"><span data-stu-id="609e2-116">The AddFile method adds a single file to an existing DO job.</span></span>         |
| [<span data-ttu-id="609e2-117">**GetProperty**</span><span class="sxs-lookup"><span data-stu-id="609e2-117">**GetProperty**</span></span>](ideliveryoptimizationjob2-getproperty.md) | <span data-ttu-id="609e2-118">AddFile 方法會將單一檔案新增至現有的作業。</span><span class="sxs-lookup"><span data-stu-id="609e2-118">The AddFile method adds a single file to an existing DO job.</span></span> |
| [<span data-ttu-id="609e2-119">**SetProperty**</span><span class="sxs-lookup"><span data-stu-id="609e2-119">**SetProperty**</span></span>](ideliveryoptimizationjob2-setproperty.md) | <span data-ttu-id="609e2-120">未使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="609e2-120">This method is unused.</span></span>                                       |

## <a name="requirements"></a><span data-ttu-id="609e2-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="609e2-121">Requirements</span></span>

| <span data-ttu-id="609e2-122">需求</span><span class="sxs-lookup"><span data-stu-id="609e2-122">Requirement</span></span> | <span data-ttu-id="609e2-123">值</span><span class="sxs-lookup"><span data-stu-id="609e2-123">Value</span></span> |
|--------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="609e2-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="609e2-124">Minimum supported client</span></span> | <span data-ttu-id="609e2-125">Windows 10， \[ 僅限1803版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="609e2-125">Windows 10, version 1803 \[desktop apps only\]</span></span>                                   |
| <span data-ttu-id="609e2-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="609e2-126">Minimum supported server</span></span> | <span data-ttu-id="609e2-127">僅限 Windows Server，版本 1709 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="609e2-127">Windows Server, version 1709 \[desktop apps only\]</span></span>                               |
| <span data-ttu-id="609e2-128">標頭</span><span class="sxs-lookup"><span data-stu-id="609e2-128">Header</span></span>                   | <span data-ttu-id="609e2-129">>deliveryoptimization。h</span><span class="sxs-lookup"><span data-stu-id="609e2-129">Deliveryoptimization.h</span></span>                                                           |
| <span data-ttu-id="609e2-130">Idl</span><span class="sxs-lookup"><span data-stu-id="609e2-130">IDL</span></span>                      | <span data-ttu-id="609e2-131">>deliveryoptimization .idl</span><span class="sxs-lookup"><span data-stu-id="609e2-131">DeliveryOptimization.idl</span></span>                                                         |
| <span data-ttu-id="609e2-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="609e2-132">Library</span></span>                  | <span data-ttu-id="609e2-133">Dosvc .lib</span><span class="sxs-lookup"><span data-stu-id="609e2-133">Dosvc.lib</span></span>                                                                        |
| <span data-ttu-id="609e2-134">DLL</span><span class="sxs-lookup"><span data-stu-id="609e2-134">DLL</span></span>                      | <span data-ttu-id="609e2-135">Dosvc.dll</span><span class="sxs-lookup"><span data-stu-id="609e2-135">Dosvc.dll</span></span>                                                                        |
| <span data-ttu-id="609e2-136">IID</span><span class="sxs-lookup"><span data-stu-id="609e2-136">IID</span></span>                      | <span data-ttu-id="609e2-137">IID_IDeliveryOptimizationJob2 定義為18995A26-BF59-4ABE-9F8B-D5092D5A2405</span><span class="sxs-lookup"><span data-stu-id="609e2-137">IID_IDeliveryOptimizationJob2 is defined as 18995A26-BF59-4ABE-9F8B-D5092D5A2405</span></span> |
