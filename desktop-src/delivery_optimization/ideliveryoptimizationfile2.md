---
title: IDeliveryOptimizationFile2 介面
description: IDeliveryOptimizationFile2 支援設定和取得選用的檔案屬性。
keywords:
- IDeliveryOptimizationFile2 介面
- IDeliveryOptimizationFile2 介面，說明
topic_type:
- apiref
api_name:
- IDeliveryOptimizationFile2
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a45efd821116b24e883ec29d494a1d588559f57a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024865"
---
# <a name="ideliveryoptimizationfile2-interface"></a><span data-ttu-id="74e62-105">IDeliveryOptimizationFile2 介面</span><span class="sxs-lookup"><span data-stu-id="74e62-105">IDeliveryOptimizationFile2 interface</span></span>

<span data-ttu-id="74e62-106">**IDeliveryOptimizationFile2** 支援設定和取得選用的檔案屬性。</span><span class="sxs-lookup"><span data-stu-id="74e62-106">The **IDeliveryOptimizationFile2** supports setting and getting optional file properties.</span></span> 

## <a name="members"></a><span data-ttu-id="74e62-107">成員</span><span class="sxs-lookup"><span data-stu-id="74e62-107">Members</span></span>

<span data-ttu-id="74e62-108">**IDeliveryOptimizationFile2** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="74e62-108">The **IDeliveryOptimizationFile2** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="74e62-109">**IDeliveryOptimizationFile2** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="74e62-109">**IDeliveryOptimizationFile2** also has these types of members:</span></span>

- [<span data-ttu-id="74e62-110">方法</span><span class="sxs-lookup"><span data-stu-id="74e62-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="74e62-111">方法</span><span class="sxs-lookup"><span data-stu-id="74e62-111">Methods</span></span>

<span data-ttu-id="74e62-112">**IDeliveryOptimizationFile2** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="74e62-112">The **IDeliveryOptimizationFile2** interface has these methods.</span></span>

| <span data-ttu-id="74e62-113">方法</span><span class="sxs-lookup"><span data-stu-id="74e62-113">Method</span></span>                                                 | <span data-ttu-id="74e62-114">描述</span><span class="sxs-lookup"><span data-stu-id="74e62-114">Description</span></span>                                                  |
|:-------------------------------------------------------|:-------------------------------------------------------------|
| [<span data-ttu-id="74e62-115">**GetProperty**</span><span class="sxs-lookup"><span data-stu-id="74e62-115">**GetProperty**</span></span>](ideliveryoptimizationfile2-getproperty.md)  | <span data-ttu-id="74e62-116">這個方法會傳回 DO 檔案的單一屬性。</span><span class="sxs-lookup"><span data-stu-id="74e62-116">This method returns a single property of the DO file.</span></span> |
| [<span data-ttu-id="74e62-117">**SetProperty**</span><span class="sxs-lookup"><span data-stu-id="74e62-117">**SetProperty**</span></span>](ideliveryoptimizationfile2-setproperty.md)  | <span data-ttu-id="74e62-118">這個方法會設定 DO 檔案的單一屬性。</span><span class="sxs-lookup"><span data-stu-id="74e62-118">This method sets a single property of the DO file.</span></span>    |

## <a name="requirements"></a><span data-ttu-id="74e62-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="74e62-119">Requirements</span></span>

| <span data-ttu-id="74e62-120">需求</span><span class="sxs-lookup"><span data-stu-id="74e62-120">Requirement</span></span> | <span data-ttu-id="74e62-121">值</span><span class="sxs-lookup"><span data-stu-id="74e62-121">Value</span></span> |
|-------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="74e62-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="74e62-122">Minimum supported client</span></span>      | <span data-ttu-id="74e62-123">Windows 10， \[ 僅限1803版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="74e62-123">Windows 10, version 1803 \[desktop apps only\]</span></span>                                    |
| <span data-ttu-id="74e62-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="74e62-124">Minimum supported server</span></span>      | <span data-ttu-id="74e62-125">僅限 Windows Server，版本 1709 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="74e62-125">Windows Server, version 1709 \[desktop apps only\]</span></span>                                |
| <span data-ttu-id="74e62-126">標頭</span><span class="sxs-lookup"><span data-stu-id="74e62-126">Header</span></span>                        | <span data-ttu-id="74e62-127">>deliveryoptimization。h</span><span class="sxs-lookup"><span data-stu-id="74e62-127">Deliveryoptimization.h</span></span>                                                            |
| <span data-ttu-id="74e62-128">Idl</span><span class="sxs-lookup"><span data-stu-id="74e62-128">IDL</span></span>                           | <span data-ttu-id="74e62-129">>deliveryoptimization .idl</span><span class="sxs-lookup"><span data-stu-id="74e62-129">DeliveryOptimization.idl</span></span>                                                          |
| <span data-ttu-id="74e62-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="74e62-130">Library</span></span>                       | <span data-ttu-id="74e62-131">Dosvc .lib</span><span class="sxs-lookup"><span data-stu-id="74e62-131">Dosvc.lib</span></span>                                                                         |
| <span data-ttu-id="74e62-132">DLL</span><span class="sxs-lookup"><span data-stu-id="74e62-132">DLL</span></span>                           | <span data-ttu-id="74e62-133">Dosvc.dll</span><span class="sxs-lookup"><span data-stu-id="74e62-133">Dosvc.dll</span></span>                                                                         |
| <span data-ttu-id="74e62-134">IID</span><span class="sxs-lookup"><span data-stu-id="74e62-134">IID</span></span>                           | <span data-ttu-id="74e62-135">IID_IDeliveryOptimizationFile2 定義為3A87296F-6EC2-4126-AB29-E3F8DC4CC390</span><span class="sxs-lookup"><span data-stu-id="74e62-135">IID_IDeliveryOptimizationFile2 is defined as 3A87296F-6EC2-4126-AB29-E3F8DC4CC390</span></span> |
