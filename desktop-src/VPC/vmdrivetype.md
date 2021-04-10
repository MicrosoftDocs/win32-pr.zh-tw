---
title: 'VMDriveType 列舉 (VPCCOMInterfaces) '
description: 指定連接至匯流排位置的磁片磁碟機類型。
ms.assetid: 7d3acff2-e1e3-4622-a448-0996ee7436ae
keywords:
- VMDriveType 列舉虛擬電腦
topic_type:
- apiref
api_name:
- VMDriveType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e6001a4a68db51b64eea9bb44d1d4c75863d315
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685882"
---
# <a name="vmdrivetype-enumeration"></a><span data-ttu-id="321f8-104">VMDriveType 列舉</span><span class="sxs-lookup"><span data-stu-id="321f8-104">VMDriveType enumeration</span></span>

<span data-ttu-id="321f8-105">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="321f8-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="321f8-106">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="321f8-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="321f8-107">指定連接至匯流排位置的磁片磁碟機類型。</span><span class="sxs-lookup"><span data-stu-id="321f8-107">Specifies the type of drive attached to a bus location.</span></span>

## <a name="syntax"></a><span data-ttu-id="321f8-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="321f8-108">Syntax</span></span>


```C++
typedef enum  { 
  vmDriveType_Null      = 0,
  vmDriveType_HardDisk  = 1,
  vmDriveType_DVD       = 2
} VMDriveType;
```



## <a name="constants"></a><span data-ttu-id="321f8-109">常數</span><span class="sxs-lookup"><span data-stu-id="321f8-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="321f8-110"><span id="vmDriveType_Null"></span><span id="vmdrivetype_null"></span><span id="VMDRIVETYPE_NULL"></span>**vmDriveType \_ Null**</span><span class="sxs-lookup"><span data-stu-id="321f8-110"><span id="vmDriveType_Null"></span><span id="vmdrivetype_null"></span><span id="VMDRIVETYPE_NULL"></span>**vmDriveType\_Null**</span></span>
</dt> <dd>

<span data-ttu-id="321f8-111">沒有連接的磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="321f8-111">There is no drive attached.</span></span>

</dd> <dt>

<span data-ttu-id="321f8-112"><span id="vmDriveType_HardDisk"></span><span id="vmdrivetype_harddisk"></span><span id="VMDRIVETYPE_HARDDISK"></span>**vmDriveType \_ 硬碟**</span><span class="sxs-lookup"><span data-stu-id="321f8-112"><span id="vmDriveType_HardDisk"></span><span id="vmdrivetype_harddisk"></span><span id="VMDRIVETYPE_HARDDISK"></span>**vmDriveType\_HardDisk**</span></span>
</dt> <dd>

<span data-ttu-id="321f8-113">磁片磁碟機已連接。</span><span class="sxs-lookup"><span data-stu-id="321f8-113">There is a hard disk attached.</span></span>

</dd> <dt>

<span data-ttu-id="321f8-114"><span id="vmDriveType_DVD"></span><span id="vmdrivetype_dvd"></span><span id="VMDRIVETYPE_DVD"></span>**vmDriveType \_ DVD**</span><span class="sxs-lookup"><span data-stu-id="321f8-114"><span id="vmDriveType_DVD"></span><span id="vmdrivetype_dvd"></span><span id="VMDRIVETYPE_DVD"></span>**vmDriveType\_DVD**</span></span>
</dt> <dd>

<span data-ttu-id="321f8-115">已附加 CD 或 DVD 光碟機。</span><span class="sxs-lookup"><span data-stu-id="321f8-115">There is a CD or DVD drive attached.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="321f8-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="321f8-116">Requirements</span></span>



| <span data-ttu-id="321f8-117">需求</span><span class="sxs-lookup"><span data-stu-id="321f8-117">Requirement</span></span> | <span data-ttu-id="321f8-118">值</span><span class="sxs-lookup"><span data-stu-id="321f8-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="321f8-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="321f8-119">Minimum supported client</span></span><br/> | <span data-ttu-id="321f8-120">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="321f8-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="321f8-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="321f8-121">Minimum supported server</span></span><br/> | <span data-ttu-id="321f8-122">都不支援</span><span class="sxs-lookup"><span data-stu-id="321f8-122">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="321f8-123">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="321f8-123">End of client support</span></span><br/>    | <span data-ttu-id="321f8-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="321f8-124">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="321f8-125">產品</span><span class="sxs-lookup"><span data-stu-id="321f8-125">Product</span></span><br/>                  | <span data-ttu-id="321f8-126">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="321f8-126">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="321f8-127">標頭</span><span class="sxs-lookup"><span data-stu-id="321f8-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="321f8-128"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="321f8-128"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="321f8-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="321f8-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="321f8-130">**IVMVirtualMachine::AttachedDriveTypes**</span><span class="sxs-lookup"><span data-stu-id="321f8-130">**IVMVirtualMachine::AttachedDriveTypes**</span></span>](ivmvirtualmachine-attacheddrivetypes.md)
</dt> </dl>

 

