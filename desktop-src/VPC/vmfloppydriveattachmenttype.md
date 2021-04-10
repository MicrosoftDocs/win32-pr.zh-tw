---
title: 'VMFloppyDriveAttachmentType 列舉 (VPCCOMInterfaces) '
description: 指定連接到軟碟磁碟機的內容。
ms.assetid: aba1be92-bd07-4edb-ad62-f8d76dbd19b9
keywords:
- VMFloppyDriveAttachmentType 列舉虛擬電腦
topic_type:
- apiref
api_name:
- VMFloppyDriveAttachmentType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a4a291778b2fea8039bf41fc04799a03421342f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934566"
---
# <a name="vmfloppydriveattachmenttype-enumeration"></a><span data-ttu-id="2d47c-104">VMFloppyDriveAttachmentType 列舉</span><span class="sxs-lookup"><span data-stu-id="2d47c-104">VMFloppyDriveAttachmentType enumeration</span></span>

<span data-ttu-id="2d47c-105">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="2d47c-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="2d47c-106">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="2d47c-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="2d47c-107">指定連接到軟碟磁碟機的內容。</span><span class="sxs-lookup"><span data-stu-id="2d47c-107">Specifies what is attached to a floppy drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d47c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="2d47c-108">Syntax</span></span>


```C++
typedef enum  { 
  vmFloppyDrive_None       = 0,
  vmFloppyDrive_Image      = 1,
  vmFloppyDrive_HostDrive  = 2
} VMFloppyDriveAttachmentType;
```



## <a name="constants"></a><span data-ttu-id="2d47c-109">常數</span><span class="sxs-lookup"><span data-stu-id="2d47c-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="2d47c-110"><span id="vmFloppyDrive_None"></span><span id="vmfloppydrive_none"></span><span id="VMFLOPPYDRIVE_NONE"></span>**vmFloppyDrive \_ 無**</span><span class="sxs-lookup"><span data-stu-id="2d47c-110"><span id="vmFloppyDrive_None"></span><span id="vmfloppydrive_none"></span><span id="VMFLOPPYDRIVE_NONE"></span>**vmFloppyDrive\_None**</span></span>
</dt> <dd>

<span data-ttu-id="2d47c-111">沒有附加任何專案。</span><span class="sxs-lookup"><span data-stu-id="2d47c-111">There is nothing attached.</span></span>

</dd> <dt>

<span data-ttu-id="2d47c-112"><span id="vmFloppyDrive_Image"></span><span id="vmfloppydrive_image"></span><span id="VMFLOPPYDRIVE_IMAGE"></span>**vmFloppyDrive \_ 影像**</span><span class="sxs-lookup"><span data-stu-id="2d47c-112"><span id="vmFloppyDrive_Image"></span><span id="vmfloppydrive_image"></span><span id="VMFLOPPYDRIVE_IMAGE"></span>**vmFloppyDrive\_Image**</span></span>
</dt> <dd>

<span data-ttu-id="2d47c-113">已附加磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="2d47c-113">There is a floppy disk image file attached.</span></span>

</dd> <dt>

<span data-ttu-id="2d47c-114"><span id="vmFloppyDrive_HostDrive"></span><span id="vmfloppydrive_hostdrive"></span><span id="VMFLOPPYDRIVE_HOSTDRIVE"></span>**vmFloppyDrive \_ HostDrive**</span><span class="sxs-lookup"><span data-stu-id="2d47c-114"><span id="vmFloppyDrive_HostDrive"></span><span id="vmfloppydrive_hostdrive"></span><span id="VMFLOPPYDRIVE_HOSTDRIVE"></span>**vmFloppyDrive\_HostDrive**</span></span>
</dt> <dd>

<span data-ttu-id="2d47c-115">有連接的主機軟碟磁碟機。</span><span class="sxs-lookup"><span data-stu-id="2d47c-115">There is a host floppy drive attached.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2d47c-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="2d47c-116">Requirements</span></span>



| <span data-ttu-id="2d47c-117">需求</span><span class="sxs-lookup"><span data-stu-id="2d47c-117">Requirement</span></span> | <span data-ttu-id="2d47c-118">值</span><span class="sxs-lookup"><span data-stu-id="2d47c-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d47c-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2d47c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2d47c-120">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2d47c-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2d47c-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2d47c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2d47c-122">都不支援</span><span class="sxs-lookup"><span data-stu-id="2d47c-122">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="2d47c-123">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="2d47c-123">End of client support</span></span><br/>    | <span data-ttu-id="2d47c-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2d47c-124">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="2d47c-125">產品</span><span class="sxs-lookup"><span data-stu-id="2d47c-125">Product</span></span><br/>                  | <span data-ttu-id="2d47c-126">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="2d47c-126">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="2d47c-127">標頭</span><span class="sxs-lookup"><span data-stu-id="2d47c-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d47c-128"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="2d47c-128"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d47c-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2d47c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d47c-130">**IVMFloppyDrive：：附件**</span><span class="sxs-lookup"><span data-stu-id="2d47c-130">**IVMFloppyDrive::Attachment**</span></span>](ivmfloppydrive-attachment.md)
</dt> </dl>

 

