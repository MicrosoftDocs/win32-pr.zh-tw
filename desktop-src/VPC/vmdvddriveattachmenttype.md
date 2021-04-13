---
title: 'VMDVDDriveAttachmentType 列舉 (VPCCOMInterfaces) '
description: 指定連接至 DVD 光碟機的內容。
ms.assetid: 66f33974-8622-4fa3-b5ac-3fae5a637434
keywords:
- VMDVDDriveAttachmentType 列舉虛擬電腦
topic_type:
- apiref
api_name:
- VMDVDDriveAttachmentType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f63c5918fd414a5a83a114ebddf5752647e8db83
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465760"
---
# <a name="vmdvddriveattachmenttype-enumeration"></a><span data-ttu-id="ab67f-104">VMDVDDriveAttachmentType 列舉</span><span class="sxs-lookup"><span data-stu-id="ab67f-104">VMDVDDriveAttachmentType enumeration</span></span>

<span data-ttu-id="ab67f-105">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="ab67f-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="ab67f-106">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="ab67f-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="ab67f-107">指定連接至 DVD 光碟機的內容。</span><span class="sxs-lookup"><span data-stu-id="ab67f-107">Specifies what is attached to a DVD drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab67f-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ab67f-108">Syntax</span></span>


```C++
typedef enum  { 
  vmDVDDrive_None       = 0,
  vmDVDDrive_Image      = 1,
  vmDVDDrive_HostDrive  = 2
} VMDVDDriveAttachmentType;
```



## <a name="constants"></a><span data-ttu-id="ab67f-109">常數</span><span class="sxs-lookup"><span data-stu-id="ab67f-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ab67f-110"><span id="vmDVDDrive_None"></span><span id="vmdvddrive_none"></span><span id="VMDVDDRIVE_NONE"></span>**Add-vmdvddrive \_ 無**</span><span class="sxs-lookup"><span data-stu-id="ab67f-110"><span id="vmDVDDrive_None"></span><span id="vmdvddrive_none"></span><span id="VMDVDDRIVE_NONE"></span>**vmDVDDrive\_None**</span></span>
</dt> <dd>

<span data-ttu-id="ab67f-111">沒有附加任何專案。</span><span class="sxs-lookup"><span data-stu-id="ab67f-111">There is nothing attached.</span></span>

</dd> <dt>

<span data-ttu-id="ab67f-112"><span id="vmDVDDrive_Image"></span><span id="vmdvddrive_image"></span><span id="VMDVDDRIVE_IMAGE"></span>**Add-vmdvddrive \_ 影像**</span><span class="sxs-lookup"><span data-stu-id="ab67f-112"><span id="vmDVDDrive_Image"></span><span id="vmdvddrive_image"></span><span id="VMDVDDRIVE_IMAGE"></span>**vmDVDDrive\_Image**</span></span>
</dt> <dd>

<span data-ttu-id="ab67f-113">已附加 ISO 影像檔案。</span><span class="sxs-lookup"><span data-stu-id="ab67f-113">There is an ISO image file attached.</span></span>

</dd> <dt>

<span data-ttu-id="ab67f-114"><span id="vmDVDDrive_HostDrive"></span><span id="vmdvddrive_hostdrive"></span><span id="VMDVDDRIVE_HOSTDRIVE"></span>**Add-vmdvddrive \_ HostDrive**</span><span class="sxs-lookup"><span data-stu-id="ab67f-114"><span id="vmDVDDrive_HostDrive"></span><span id="vmdvddrive_hostdrive"></span><span id="VMDVDDRIVE_HOSTDRIVE"></span>**vmDVDDrive\_HostDrive**</span></span>
</dt> <dd>

<span data-ttu-id="ab67f-115">已連接主機 CD 或 DVD 光碟機。</span><span class="sxs-lookup"><span data-stu-id="ab67f-115">There is a host CD or DVD drive attached.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ab67f-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="ab67f-116">Requirements</span></span>



| <span data-ttu-id="ab67f-117">需求</span><span class="sxs-lookup"><span data-stu-id="ab67f-117">Requirement</span></span> | <span data-ttu-id="ab67f-118">值</span><span class="sxs-lookup"><span data-stu-id="ab67f-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab67f-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ab67f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ab67f-120">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ab67f-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ab67f-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ab67f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ab67f-122">都不支援</span><span class="sxs-lookup"><span data-stu-id="ab67f-122">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="ab67f-123">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="ab67f-123">End of client support</span></span><br/>    | <span data-ttu-id="ab67f-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ab67f-124">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="ab67f-125">產品</span><span class="sxs-lookup"><span data-stu-id="ab67f-125">Product</span></span><br/>                  | <span data-ttu-id="ab67f-126">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="ab67f-126">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="ab67f-127">標頭</span><span class="sxs-lookup"><span data-stu-id="ab67f-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab67f-128"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="ab67f-128"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab67f-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ab67f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab67f-130">**IVMDVDDrive：：附件**</span><span class="sxs-lookup"><span data-stu-id="ab67f-130">**IVMDVDDrive::Attachment**</span></span>](ivmdvddrive-attachment.md)
</dt> </dl>

 

