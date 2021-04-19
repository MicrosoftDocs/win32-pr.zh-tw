---
title: 'VMHardDiskType 列舉 (VPCCOMInterfaces) '
description: 指定硬碟映射類型。
ms.assetid: 14480bad-523a-40d8-a6ba-9ec31fe4b217
keywords:
- VMHardDiskType 列舉虛擬電腦
topic_type:
- apiref
api_name:
- VMHardDiskType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b59fed6577aa957bae960f7af65be766a03c727e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969990"
---
# <a name="vmharddisktype-enumeration"></a><span data-ttu-id="6bb2a-104">VMHardDiskType 列舉</span><span class="sxs-lookup"><span data-stu-id="6bb2a-104">VMHardDiskType enumeration</span></span>

<span data-ttu-id="6bb2a-105">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="6bb2a-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="6bb2a-106">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="6bb2a-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="6bb2a-107">指定硬碟映射類型。</span><span class="sxs-lookup"><span data-stu-id="6bb2a-107">Specifies the hard disk image type.</span></span>

## <a name="syntax"></a><span data-ttu-id="6bb2a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="6bb2a-108">Syntax</span></span>


```C++
typedef enum  { 
  vmDiskType_Dynamic       = 0,
  vmDiskType_FixedSize     = 1,
  vmDiskType_Differencing  = 2
} VMHardDiskType;
```



## <a name="constants"></a><span data-ttu-id="6bb2a-109">常數</span><span class="sxs-lookup"><span data-stu-id="6bb2a-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="6bb2a-110"><span id="vmDiskType_Dynamic"></span><span id="vmdisktype_dynamic"></span><span id="VMDISKTYPE_DYNAMIC"></span>**vmDiskType \_ 動態**</span><span class="sxs-lookup"><span data-stu-id="6bb2a-110"><span id="vmDiskType_Dynamic"></span><span id="vmdisktype_dynamic"></span><span id="VMDISKTYPE_DYNAMIC"></span>**vmDiskType\_Dynamic**</span></span>
</dt> <dd>

<span data-ttu-id="6bb2a-111">動態擴充的硬碟映射。</span><span class="sxs-lookup"><span data-stu-id="6bb2a-111">A dynamically expanding hard disk image.</span></span>

</dd> <dt>

<span data-ttu-id="6bb2a-112"><span id="vmDiskType_FixedSize"></span><span id="vmdisktype_fixedsize"></span><span id="VMDISKTYPE_FIXEDSIZE"></span>**vmDiskType \_ FixedSize**</span><span class="sxs-lookup"><span data-stu-id="6bb2a-112"><span id="vmDiskType_FixedSize"></span><span id="vmdisktype_fixedsize"></span><span id="VMDISKTYPE_FIXEDSIZE"></span>**vmDiskType\_FixedSize**</span></span>
</dt> <dd>

<span data-ttu-id="6bb2a-113">固定大小的硬碟映射。</span><span class="sxs-lookup"><span data-stu-id="6bb2a-113">A fixed-size hard disk image.</span></span>

</dd> <dt>

<span data-ttu-id="6bb2a-114"><span id="vmDiskType_Differencing"></span><span id="vmdisktype_differencing"></span><span id="VMDISKTYPE_DIFFERENCING"></span>**vmDiskType \_ 差異**</span><span class="sxs-lookup"><span data-stu-id="6bb2a-114"><span id="vmDiskType_Differencing"></span><span id="vmdisktype_differencing"></span><span id="VMDISKTYPE_DIFFERENCING"></span>**vmDiskType\_Differencing**</span></span>
</dt> <dd>

<span data-ttu-id="6bb2a-115">差異硬碟映射。</span><span class="sxs-lookup"><span data-stu-id="6bb2a-115">A differencing hard disk image.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6bb2a-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="6bb2a-116">Requirements</span></span>



| <span data-ttu-id="6bb2a-117">需求</span><span class="sxs-lookup"><span data-stu-id="6bb2a-117">Requirement</span></span> | <span data-ttu-id="6bb2a-118">值</span><span class="sxs-lookup"><span data-stu-id="6bb2a-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6bb2a-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6bb2a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6bb2a-120">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6bb2a-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6bb2a-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6bb2a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6bb2a-122">都不支援</span><span class="sxs-lookup"><span data-stu-id="6bb2a-122">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="6bb2a-123">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="6bb2a-123">End of client support</span></span><br/>    | <span data-ttu-id="6bb2a-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6bb2a-124">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="6bb2a-125">產品</span><span class="sxs-lookup"><span data-stu-id="6bb2a-125">Product</span></span><br/>                  | <span data-ttu-id="6bb2a-126">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="6bb2a-126">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="6bb2a-127">標頭</span><span class="sxs-lookup"><span data-stu-id="6bb2a-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="6bb2a-128"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="6bb2a-128"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6bb2a-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6bb2a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bb2a-130">**IVMHardDisk**</span><span class="sxs-lookup"><span data-stu-id="6bb2a-130">**IVMHardDisk**</span></span>](ivmharddisk.md)
</dt> </dl>

 

