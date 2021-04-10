---
title: 'vmFloppyDriveEvent 列舉 (VPCCOMInterfaces) '
description: 指定磁片磁碟機事件。
ms.assetid: 31d0c748-609a-4e03-8b5c-0a17a2587242
keywords:
- vmFloppyDriveEvent 列舉虛擬電腦
topic_type:
- apiref
api_name:
- vmFloppyDriveEvent
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a11b1485f91264713cf96a4f95cab8286261eea4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686302"
---
# <a name="vmfloppydriveevent-enumeration"></a><span data-ttu-id="8f8f2-104">vmFloppyDriveEvent 列舉</span><span class="sxs-lookup"><span data-stu-id="8f8f2-104">vmFloppyDriveEvent enumeration</span></span>

<span data-ttu-id="8f8f2-105">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="8f8f2-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="8f8f2-106">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="8f8f2-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="8f8f2-107">指定磁片磁碟機事件。</span><span class="sxs-lookup"><span data-stu-id="8f8f2-107">Specifies the floppy drive events.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f8f2-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="8f8f2-108">Syntax</span></span>


```C++
typedef enum  { 
  vmFloppyDriveEvent_OnInsert  = 1,
  vmFloppyDriveEvent_OnEject   = 2
} vmFloppyDriveEvent;
```



## <a name="constants"></a><span data-ttu-id="8f8f2-109">常數</span><span class="sxs-lookup"><span data-stu-id="8f8f2-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="8f8f2-110"><span id="vmFloppyDriveEvent_OnInsert"></span><span id="vmfloppydriveevent_oninsert"></span><span id="VMFLOPPYDRIVEEVENT_ONINSERT"></span>**vmFloppyDriveEvent \_ OnInsert**</span><span class="sxs-lookup"><span data-stu-id="8f8f2-110"><span id="vmFloppyDriveEvent_OnInsert"></span><span id="vmfloppydriveevent_oninsert"></span><span id="VMFLOPPYDRIVEEVENT_ONINSERT"></span>**vmFloppyDriveEvent\_OnInsert**</span></span>
</dt> <dd>

<span data-ttu-id="8f8f2-111">連接磁片磁碟機，或將實際媒體插入主機磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="8f8f2-111">A floppy disk image is attached or real media is inserted into a host drive.</span></span>

</dd> <dt>

<span data-ttu-id="8f8f2-112"><span id="vmFloppyDriveEvent_OnEject"></span><span id="vmfloppydriveevent_oneject"></span><span id="VMFLOPPYDRIVEEVENT_ONEJECT"></span>**vmFloppyDriveEvent \_ OnEject**</span><span class="sxs-lookup"><span data-stu-id="8f8f2-112"><span id="vmFloppyDriveEvent_OnEject"></span><span id="vmfloppydriveevent_oneject"></span><span id="VMFLOPPYDRIVEEVENT_ONEJECT"></span>**vmFloppyDriveEvent\_OnEject**</span></span>
</dt> <dd>

<span data-ttu-id="8f8f2-113">媒體已被取出。</span><span class="sxs-lookup"><span data-stu-id="8f8f2-113">Media has been ejected.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8f8f2-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="8f8f2-114">Requirements</span></span>



| <span data-ttu-id="8f8f2-115">需求</span><span class="sxs-lookup"><span data-stu-id="8f8f2-115">Requirement</span></span> | <span data-ttu-id="8f8f2-116">值</span><span class="sxs-lookup"><span data-stu-id="8f8f2-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f8f2-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8f8f2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8f8f2-118">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8f8f2-118">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8f8f2-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8f8f2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8f8f2-120">都不支援</span><span class="sxs-lookup"><span data-stu-id="8f8f2-120">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="8f8f2-121">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="8f8f2-121">End of client support</span></span><br/>    | <span data-ttu-id="8f8f2-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8f8f2-122">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="8f8f2-123">產品</span><span class="sxs-lookup"><span data-stu-id="8f8f2-123">Product</span></span><br/>                  | <span data-ttu-id="8f8f2-124">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="8f8f2-124">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="8f8f2-125">標頭</span><span class="sxs-lookup"><span data-stu-id="8f8f2-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f8f2-126"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="8f8f2-126"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f8f2-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8f8f2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f8f2-128">**IVMFloppyDriveEvents**</span><span class="sxs-lookup"><span data-stu-id="8f8f2-128">**IVMFloppyDriveEvents**</span></span>](ivmfloppydriveevents.md)
</dt> </dl>

 

