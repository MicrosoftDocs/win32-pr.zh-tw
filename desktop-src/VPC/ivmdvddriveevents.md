---
title: 'IVMDVDDriveEvents 介面 (VPCCOMInterfaces .h) '
description: 定義 IVMDVDDrive 介面的外寄事件介面。
ms.assetid: aa68fb6f-032d-4322-8553-b1e840ae63b8
keywords:
- IVMDVDDriveEvents 介面 Virtual PC
- IVMDVDDriveEvents 介面 Virtual PC，說明
topic_type:
- apiref
api_name:
- IVMDVDDriveEvents
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b301a423f5272288c12a900d0fbd19c0a5d5170
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466837"
---
# <a name="ivmdvddriveevents-interface"></a><span data-ttu-id="4955b-105">IVMDVDDriveEvents 介面</span><span class="sxs-lookup"><span data-stu-id="4955b-105">IVMDVDDriveEvents interface</span></span>

<span data-ttu-id="4955b-106">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="4955b-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="4955b-107">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="4955b-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="4955b-108">定義 [**IVMDVDDrive**](ivmdvddrive.md) 介面的外寄事件介面。</span><span class="sxs-lookup"><span data-stu-id="4955b-108">Defines the outgoing event interface for the [**IVMDVDDrive**](ivmdvddrive.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="4955b-109">成員</span><span class="sxs-lookup"><span data-stu-id="4955b-109">Members</span></span>

<span data-ttu-id="4955b-110">**IVMDVDDriveEvents** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。</span><span class="sxs-lookup"><span data-stu-id="4955b-110">The **IVMDVDDriveEvents** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="4955b-111">**IVMDVDDriveEvents** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="4955b-111">**IVMDVDDriveEvents** also has these types of members:</span></span>

-   [<span data-ttu-id="4955b-112">方法</span><span class="sxs-lookup"><span data-stu-id="4955b-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="4955b-113">方法</span><span class="sxs-lookup"><span data-stu-id="4955b-113">Methods</span></span>

<span data-ttu-id="4955b-114">**IVMDVDDriveEvents** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="4955b-114">The **IVMDVDDriveEvents** interface has these methods.</span></span>



| <span data-ttu-id="4955b-115">方法</span><span class="sxs-lookup"><span data-stu-id="4955b-115">Method</span></span>                                                   | <span data-ttu-id="4955b-116">描述</span><span class="sxs-lookup"><span data-stu-id="4955b-116">Description</span></span>                                                                   |
|:---------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="4955b-117">**OnMediaEject**</span><span class="sxs-lookup"><span data-stu-id="4955b-117">**OnMediaEject**</span></span>](ivmdvddriveevents-onmediaeject.md)   | <span data-ttu-id="4955b-118">接收媒體已從磁片磁碟機中取出的通知。</span><span class="sxs-lookup"><span data-stu-id="4955b-118">Receives notification that media has been ejected from the drive.</span></span><br/>  |
| [<span data-ttu-id="4955b-119">**OnMediaInsert**</span><span class="sxs-lookup"><span data-stu-id="4955b-119">**OnMediaInsert**</span></span>](ivmdvddriveevents-onmediainsert.md) | <span data-ttu-id="4955b-120">接收媒體已插入磁片磁碟機的通知。</span><span class="sxs-lookup"><span data-stu-id="4955b-120">Receives notification that media has been inserted into the drive.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="4955b-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="4955b-121">Requirements</span></span>



| <span data-ttu-id="4955b-122">需求</span><span class="sxs-lookup"><span data-stu-id="4955b-122">Requirement</span></span> | <span data-ttu-id="4955b-123">值</span><span class="sxs-lookup"><span data-stu-id="4955b-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4955b-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4955b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="4955b-125">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4955b-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4955b-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4955b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="4955b-127">都不支援</span><span class="sxs-lookup"><span data-stu-id="4955b-127">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="4955b-128">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="4955b-128">End of client support</span></span><br/>    | <span data-ttu-id="4955b-129">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4955b-129">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="4955b-130">產品</span><span class="sxs-lookup"><span data-stu-id="4955b-130">Product</span></span><br/>                  | <span data-ttu-id="4955b-131">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="4955b-131">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="4955b-132">標頭</span><span class="sxs-lookup"><span data-stu-id="4955b-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="4955b-133"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="4955b-133"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="4955b-134">IID</span><span class="sxs-lookup"><span data-stu-id="4955b-134">IID</span></span><br/>                      | <span data-ttu-id="4955b-135">DIID \_ IVMDVDDriveEvents 定義為 c2a7d8e9-e76c-4eb8-94f7-71a5122d249b</span><span class="sxs-lookup"><span data-stu-id="4955b-135">DIID\_IVMDVDDriveEvents is defined as c2a7d8e9-e76c-4eb8-94f7-71a5122d249b</span></span><br/>         |



 

