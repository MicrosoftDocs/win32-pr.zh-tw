---
title: 'IVMFloppyDriveEvents 介面 (VPCCOMInterfaces .h) '
description: 定義 IVMFloppyDrive 介面的外寄事件介面。 用戶端會執行這些方法來接收從 IVMFloppyDrive 傳送的事件。
ms.assetid: fbb66554-f042-4891-94be-1a12b8c179c2
keywords:
- IVMFloppyDriveEvents 介面 Virtual PC
- IVMFloppyDriveEvents 介面 Virtual PC，說明
topic_type:
- apiref
api_name:
- IVMFloppyDriveEvents
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f9b799bd6227882c2991f9b310f39d38b20692d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106061"
---
# <a name="ivmfloppydriveevents-interface"></a><span data-ttu-id="2fbba-106">IVMFloppyDriveEvents 介面</span><span class="sxs-lookup"><span data-stu-id="2fbba-106">IVMFloppyDriveEvents interface</span></span>

<span data-ttu-id="2fbba-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="2fbba-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="2fbba-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="2fbba-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="2fbba-109">定義 [**IVMFloppyDrive**](ivmfloppydrive.md) 介面的外寄事件介面。</span><span class="sxs-lookup"><span data-stu-id="2fbba-109">Defines the outgoing event interface for the [**IVMFloppyDrive**](ivmfloppydrive.md) interface.</span></span> <span data-ttu-id="2fbba-110">用戶端會執行這些方法來接收從 **IVMFloppyDrive** 傳送的事件。</span><span class="sxs-lookup"><span data-stu-id="2fbba-110">The client implements these methods to receive events sent from **IVMFloppyDrive**.</span></span>

## <a name="members"></a><span data-ttu-id="2fbba-111">成員</span><span class="sxs-lookup"><span data-stu-id="2fbba-111">Members</span></span>

<span data-ttu-id="2fbba-112">**IVMFloppyDriveEvents** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。</span><span class="sxs-lookup"><span data-stu-id="2fbba-112">The **IVMFloppyDriveEvents** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="2fbba-113">**IVMFloppyDriveEvents** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="2fbba-113">**IVMFloppyDriveEvents** also has these types of members:</span></span>

-   [<span data-ttu-id="2fbba-114">方法</span><span class="sxs-lookup"><span data-stu-id="2fbba-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="2fbba-115">方法</span><span class="sxs-lookup"><span data-stu-id="2fbba-115">Methods</span></span>

<span data-ttu-id="2fbba-116">**IVMFloppyDriveEvents** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="2fbba-116">The **IVMFloppyDriveEvents** interface has these methods.</span></span>



| <span data-ttu-id="2fbba-117">方法</span><span class="sxs-lookup"><span data-stu-id="2fbba-117">Method</span></span>                                                      | <span data-ttu-id="2fbba-118">描述</span><span class="sxs-lookup"><span data-stu-id="2fbba-118">Description</span></span>                                                                   |
|:------------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="2fbba-119">**OnMediaEject**</span><span class="sxs-lookup"><span data-stu-id="2fbba-119">**OnMediaEject**</span></span>](ivmfloppydriveevents-onmediaeject.md)   | <span data-ttu-id="2fbba-120">接收媒體已從磁片磁碟機中取出的通知。</span><span class="sxs-lookup"><span data-stu-id="2fbba-120">Receives notification that media has been ejected from the drive.</span></span><br/>  |
| [<span data-ttu-id="2fbba-121">**OnMediaInsert**</span><span class="sxs-lookup"><span data-stu-id="2fbba-121">**OnMediaInsert**</span></span>](ivmfloppydriveevents-onmediainsert.md) | <span data-ttu-id="2fbba-122">接收媒體已插入磁片磁碟機的通知。</span><span class="sxs-lookup"><span data-stu-id="2fbba-122">Receives notification that media has been inserted into the drive.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="2fbba-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="2fbba-123">Requirements</span></span>



| <span data-ttu-id="2fbba-124">需求</span><span class="sxs-lookup"><span data-stu-id="2fbba-124">Requirement</span></span> | <span data-ttu-id="2fbba-125">值</span><span class="sxs-lookup"><span data-stu-id="2fbba-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2fbba-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2fbba-126">Minimum supported client</span></span><br/> | <span data-ttu-id="2fbba-127">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2fbba-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2fbba-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2fbba-128">Minimum supported server</span></span><br/> | <span data-ttu-id="2fbba-129">都不支援</span><span class="sxs-lookup"><span data-stu-id="2fbba-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="2fbba-130">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="2fbba-130">End of client support</span></span><br/>    | <span data-ttu-id="2fbba-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2fbba-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="2fbba-132">產品</span><span class="sxs-lookup"><span data-stu-id="2fbba-132">Product</span></span><br/>                  | <span data-ttu-id="2fbba-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="2fbba-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="2fbba-134">標頭</span><span class="sxs-lookup"><span data-stu-id="2fbba-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="2fbba-135"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="2fbba-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="2fbba-136">IID</span><span class="sxs-lookup"><span data-stu-id="2fbba-136">IID</span></span><br/>                      | <span data-ttu-id="2fbba-137">DIID \_ IVMFloppyDriveEvents 定義為 a9ed3401-4e09-4177-86ec-a13bf9fa7d4e</span><span class="sxs-lookup"><span data-stu-id="2fbba-137">DIID\_IVMFloppyDriveEvents is defined as a9ed3401-4e09-4177-86ec-a13bf9fa7d4e</span></span><br/>      |



 

