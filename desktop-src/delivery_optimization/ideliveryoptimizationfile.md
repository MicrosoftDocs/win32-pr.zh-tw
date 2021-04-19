---
title: IDeliveryOptimizationFile 介面
description: 執行 IDeliveryOptimizationFile 介面，以識別特定檔案的狀態。
ms.assetid: 4D1D82E1-B39C-4634-A0B7-BC4322796AB2
keywords:
- IDeliveryOptimizationFile 介面
- IDeliveryOptimizationFile 介面，說明
topic_type:
- apiref
api_name:
- IDeliveryOptimizationFile
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2b86434f4be2f7d14ae46f4af92784c1be4fd1aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968548"
---
# <a name="ideliveryoptimizationfile-interface"></a><span data-ttu-id="88abd-105">IDeliveryOptimizationFile 介面</span><span class="sxs-lookup"><span data-stu-id="88abd-105">IDeliveryOptimizationFile interface</span></span>

<span data-ttu-id="88abd-106">執行 **IDeliveryOptimizationFile** 介面，以識別特定檔案的狀態。</span><span class="sxs-lookup"><span data-stu-id="88abd-106">Implement the **IDeliveryOptimizationFile** interface to identify the status of a specific file.</span></span>

## <a name="members"></a><span data-ttu-id="88abd-107">成員</span><span class="sxs-lookup"><span data-stu-id="88abd-107">Members</span></span>

<span data-ttu-id="88abd-108">**IDeliveryOptimizationFile** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="88abd-108">The **IDeliveryOptimizationFile** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="88abd-109">**IDeliveryOptimizationFile** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="88abd-109">**IDeliveryOptimizationFile** also has these types of members:</span></span>

-   [<span data-ttu-id="88abd-110">方法</span><span class="sxs-lookup"><span data-stu-id="88abd-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="88abd-111">方法</span><span class="sxs-lookup"><span data-stu-id="88abd-111">Methods</span></span>

<span data-ttu-id="88abd-112">**IDeliveryOptimizationFile** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="88abd-112">The **IDeliveryOptimizationFile** interface has these methods.</span></span>



| <span data-ttu-id="88abd-113">方法</span><span class="sxs-lookup"><span data-stu-id="88abd-113">Method</span></span>                                                 | <span data-ttu-id="88abd-114">描述</span><span class="sxs-lookup"><span data-stu-id="88abd-114">Description</span></span>                                                       |
|:-------------------------------------------------------|:------------------------------------------------------------------|
| [<span data-ttu-id="88abd-115">**GetStats**</span><span class="sxs-lookup"><span data-stu-id="88abd-115">**GetStats**</span></span>](ideliveryoptimizationfile-getstats.md) | <span data-ttu-id="88abd-116">傳回特定檔案的下載和上傳統計資料。</span><span class="sxs-lookup"><span data-stu-id="88abd-116">Returns download and upload stats for a specific file.</span></span><br/> |

## <a name="requirements"></a><span data-ttu-id="88abd-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="88abd-117">Requirements</span></span>

| <span data-ttu-id="88abd-118">需求</span><span class="sxs-lookup"><span data-stu-id="88abd-118">Requirement</span></span> | <span data-ttu-id="88abd-119">值</span><span class="sxs-lookup"><span data-stu-id="88abd-119">Value</span></span> |
|-------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="88abd-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="88abd-120">Minimum supported client</span></span>      | <span data-ttu-id="88abd-121">Windows 10， \[ 僅限1709版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="88abd-121">Windows 10, version 1709 \[desktop apps only\]</span></span>                                   |
| <span data-ttu-id="88abd-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="88abd-122">Minimum supported server</span></span>      | <span data-ttu-id="88abd-123">僅限 Windows Server，版本 1709 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="88abd-123">Windows Server, version 1709 \[desktop apps only\]</span></span>                               |
| <span data-ttu-id="88abd-124">標頭</span><span class="sxs-lookup"><span data-stu-id="88abd-124">Header</span></span>                        | <span data-ttu-id="88abd-125">>deliveryoptimization。h</span><span class="sxs-lookup"><span data-stu-id="88abd-125">Deliveryoptimization.h</span></span>                                                           |
| <span data-ttu-id="88abd-126">Idl</span><span class="sxs-lookup"><span data-stu-id="88abd-126">IDL</span></span>                           | <span data-ttu-id="88abd-127">>deliveryoptimization .idl</span><span class="sxs-lookup"><span data-stu-id="88abd-127">DeliveryOptimization.idl</span></span>                                                         |
| <span data-ttu-id="88abd-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="88abd-128">Library</span></span>                       | <span data-ttu-id="88abd-129">Dosvc .lib</span><span class="sxs-lookup"><span data-stu-id="88abd-129">Dosvc.lib</span></span>                                                                        |
| <span data-ttu-id="88abd-130">DLL</span><span class="sxs-lookup"><span data-stu-id="88abd-130">DLL</span></span>                           | <span data-ttu-id="88abd-131">Dosvc.dll</span><span class="sxs-lookup"><span data-stu-id="88abd-131">Dosvc.dll</span></span>                                                                        |
| <span data-ttu-id="88abd-132">IID</span><span class="sxs-lookup"><span data-stu-id="88abd-132">IID</span></span>                           | <span data-ttu-id="88abd-133">IID_IDeliveryOptimizationFile 定義為 B76B9699-E99E-4101-803F-A20E325D93E2</span><span class="sxs-lookup"><span data-stu-id="88abd-133">IID_IDeliveryOptimizationFile is defined as B76B9699-E99E-4101-803F-A20E325D93E2</span></span> |
