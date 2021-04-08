---
title: 'VMDVDDriveEvent 列舉 (VPCCOMInterfaces) '
description: 指定 DVD 磁片磁碟機事件。
ms.assetid: 17126138-614f-42d9-937e-1aca9393557c
keywords:
- VMDVDDriveEvent 列舉虛擬電腦
topic_type:
- apiref
api_name:
- VMDVDDriveEvent
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 967fcd545c0ddd24d01c5dc779929ef4639c6736
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685881"
---
# <a name="vmdvddriveevent-enumeration"></a><span data-ttu-id="ca9b8-104">VMDVDDriveEvent 列舉</span><span class="sxs-lookup"><span data-stu-id="ca9b8-104">VMDVDDriveEvent enumeration</span></span>

<span data-ttu-id="ca9b8-105">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="ca9b8-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="ca9b8-106">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="ca9b8-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="ca9b8-107">指定 DVD 磁片磁碟機事件。</span><span class="sxs-lookup"><span data-stu-id="ca9b8-107">Specifies the DVD drive events.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca9b8-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ca9b8-108">Syntax</span></span>


```C++
typedef enum  { 
  vmDVDDriveEvent_OnInsert  = 1,
  vmDVDDriveEvent_OnEject   = 2
} VMDVDDriveEvent;
```



## <a name="constants"></a><span data-ttu-id="ca9b8-109">常數</span><span class="sxs-lookup"><span data-stu-id="ca9b8-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ca9b8-110"><span id="vmDVDDriveEvent_OnInsert"></span><span id="vmdvddriveevent_oninsert"></span><span id="VMDVDDRIVEEVENT_ONINSERT"></span>**vmDVDDriveEvent \_ OnInsert**</span><span class="sxs-lookup"><span data-stu-id="ca9b8-110"><span id="vmDVDDriveEvent_OnInsert"></span><span id="vmdvddriveevent_oninsert"></span><span id="VMDVDDRIVEEVENT_ONINSERT"></span>**vmDVDDriveEvent\_OnInsert**</span></span>
</dt> <dd>

<span data-ttu-id="ca9b8-111">附加 ISO 映像，或將實際媒體插入主機磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="ca9b8-111">An ISO image is attached or real media is inserted into a host drive.</span></span>

</dd> <dt>

<span data-ttu-id="ca9b8-112"><span id="vmDVDDriveEvent_OnEject"></span><span id="vmdvddriveevent_oneject"></span><span id="VMDVDDRIVEEVENT_ONEJECT"></span>**vmDVDDriveEvent \_ OnEject**</span><span class="sxs-lookup"><span data-stu-id="ca9b8-112"><span id="vmDVDDriveEvent_OnEject"></span><span id="vmdvddriveevent_oneject"></span><span id="VMDVDDRIVEEVENT_ONEJECT"></span>**vmDVDDriveEvent\_OnEject**</span></span>
</dt> <dd>

<span data-ttu-id="ca9b8-113">媒體已被退出。</span><span class="sxs-lookup"><span data-stu-id="ca9b8-113">The media has been ejected.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ca9b8-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="ca9b8-114">Requirements</span></span>



| <span data-ttu-id="ca9b8-115">需求</span><span class="sxs-lookup"><span data-stu-id="ca9b8-115">Requirement</span></span> | <span data-ttu-id="ca9b8-116">值</span><span class="sxs-lookup"><span data-stu-id="ca9b8-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca9b8-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ca9b8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ca9b8-118">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ca9b8-118">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ca9b8-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ca9b8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ca9b8-120">都不支援</span><span class="sxs-lookup"><span data-stu-id="ca9b8-120">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="ca9b8-121">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="ca9b8-121">End of client support</span></span><br/>    | <span data-ttu-id="ca9b8-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ca9b8-122">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="ca9b8-123">產品</span><span class="sxs-lookup"><span data-stu-id="ca9b8-123">Product</span></span><br/>                  | <span data-ttu-id="ca9b8-124">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="ca9b8-124">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="ca9b8-125">標頭</span><span class="sxs-lookup"><span data-stu-id="ca9b8-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca9b8-126"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="ca9b8-126"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca9b8-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ca9b8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca9b8-128">**IVMDVDDriveEvents**</span><span class="sxs-lookup"><span data-stu-id="ca9b8-128">**IVMDVDDriveEvents**</span></span>](ivmdvddriveevents.md)
</dt> </dl>

 

