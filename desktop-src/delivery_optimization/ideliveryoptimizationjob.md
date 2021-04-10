---
title: 'IDeliveryOptimizationJob 介面 (>deliveryoptimization .h) '
description: 使用 IDeliveryOptimizationJob 介面下載檔案範圍。
ms.assetid: 7549F3B2-47E9-44DA-BD9C-AEFB0C36FF15
keywords:
- IDeliveryOptimizationJob 介面
- IDeliveryOptimizationJob 介面，說明
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6ee2ce35b8089e9b05b7291f535361e39140f856
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103655"
---
# <a name="ideliveryoptimizationjob-interface"></a><span data-ttu-id="0179d-105">IDeliveryOptimizationJob 介面</span><span class="sxs-lookup"><span data-stu-id="0179d-105">IDeliveryOptimizationJob interface</span></span>

<span data-ttu-id="0179d-106">使用 **IDeliveryOptimizationJob** 介面下載檔案範圍。</span><span class="sxs-lookup"><span data-stu-id="0179d-106">Use the **IDeliveryOptimizationJob** interface to download ranges of a file.</span></span>

## <a name="members"></a><span data-ttu-id="0179d-107">成員</span><span class="sxs-lookup"><span data-stu-id="0179d-107">Members</span></span>

<span data-ttu-id="0179d-108">**IDeliveryOptimizationJob** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="0179d-108">The **IDeliveryOptimizationJob** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="0179d-109">**IDeliveryOptimizationJob** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="0179d-109">**IDeliveryOptimizationJob** also has these types of members:</span></span>

- [<span data-ttu-id="0179d-110">方法</span><span class="sxs-lookup"><span data-stu-id="0179d-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="0179d-111">方法</span><span class="sxs-lookup"><span data-stu-id="0179d-111">Methods</span></span>

<span data-ttu-id="0179d-112">**IDeliveryOptimizationJob** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="0179d-112">The **IDeliveryOptimizationJob** interface has these methods.</span></span>



| <span data-ttu-id="0179d-113">方法</span><span class="sxs-lookup"><span data-stu-id="0179d-113">Method</span></span>                                                                  | <span data-ttu-id="0179d-114">描述</span><span class="sxs-lookup"><span data-stu-id="0179d-114">Description</span></span>                                                                                         |
|:------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0179d-115">**AddFileWithRanges**</span><span class="sxs-lookup"><span data-stu-id="0179d-115">**AddFileWithRanges**</span></span>](ideliveryoptimizationjob-addfilewithranges.md) | <span data-ttu-id="0179d-116">將檔案新增至下載作業，並指定您想要下載的檔案範圍。</span><span class="sxs-lookup"><span data-stu-id="0179d-116">Adds a file to a download job and specifies the ranges of the file you want to download.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="0179d-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="0179d-117">Requirements</span></span>



| <span data-ttu-id="0179d-118">需求</span><span class="sxs-lookup"><span data-stu-id="0179d-118">Requirement</span></span> | <span data-ttu-id="0179d-119">值</span><span class="sxs-lookup"><span data-stu-id="0179d-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0179d-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0179d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0179d-121">Windows 10， \[ 僅限1709版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0179d-121">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="0179d-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0179d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0179d-123">僅限 Windows Server，版本 1709 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0179d-123">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="0179d-124">標頭</span><span class="sxs-lookup"><span data-stu-id="0179d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0179d-125"><dt>>deliveryoptimization。h</dt></span><span class="sxs-lookup"><span data-stu-id="0179d-125"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="0179d-126">Idl</span><span class="sxs-lookup"><span data-stu-id="0179d-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0179d-127"><dt>>deliveryoptimization .idl</dt></span><span class="sxs-lookup"><span data-stu-id="0179d-127"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="0179d-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="0179d-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="0179d-129"><dt>Dosvc .lib</dt></span><span class="sxs-lookup"><span data-stu-id="0179d-129"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="0179d-130">DLL</span><span class="sxs-lookup"><span data-stu-id="0179d-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0179d-131"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0179d-131"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="0179d-132">IID</span><span class="sxs-lookup"><span data-stu-id="0179d-132">IID</span></span><br/>                      | <span data-ttu-id="0179d-133">IID_IDeliveryOptimizationJob 定義為 EE2584CF-A69C-4848-B633-2649962B3EF7</span><span class="sxs-lookup"><span data-stu-id="0179d-133">IID_IDeliveryOptimizationJob is defined as EE2584CF-A69C-4848-B633-2649962B3EF7</span></span><br/>         |



 

