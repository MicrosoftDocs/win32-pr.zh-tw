---
title: 'VMFloppyDiskImageType 列舉 (VPCCOMInterfaces) '
description: 指定磁片格式。
ms.assetid: 7eb504c0-dfb7-45eb-a943-b453b5f8ca63
keywords:
- VMFloppyDiskImageType 列舉虛擬電腦
topic_type:
- apiref
api_name:
- VMFloppyDiskImageType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f20732e46617288602e841a1047db5db30eba5ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384629"
---
# <a name="vmfloppydiskimagetype-enumeration"></a><span data-ttu-id="32dc7-104">VMFloppyDiskImageType 列舉</span><span class="sxs-lookup"><span data-stu-id="32dc7-104">VMFloppyDiskImageType enumeration</span></span>

<span data-ttu-id="32dc7-105">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="32dc7-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="32dc7-106">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="32dc7-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="32dc7-107">指定磁片格式。</span><span class="sxs-lookup"><span data-stu-id="32dc7-107">Specifies the floppy disk formats.</span></span>

## <a name="syntax"></a><span data-ttu-id="32dc7-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="32dc7-108">Syntax</span></span>


```C++
typedef enum  { 
  vmFloppyDiskImage_Unknown                = 0,
  vmFloppyDiskImage_LowDensity             = 1,
  vmFloppyDiskImage_HighDensity            = 2,
  vmFloppyDiskImage_DMF                    = 3,
  vmFloppyDiskImage_LowDensitySingleSided  = 4,
  vmFloppyDiskImage_MediumDensity          = 5,
  vmFloppyDiskImage_HighDensityMSS         = 6
} VMFloppyDiskImageType;
```



## <a name="constants"></a><span data-ttu-id="32dc7-109">常數</span><span class="sxs-lookup"><span data-stu-id="32dc7-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="32dc7-110"><span id="vmFloppyDiskImage_Unknown"></span><span id="vmfloppydiskimage_unknown"></span><span id="VMFLOPPYDISKIMAGE_UNKNOWN"></span>**vmFloppyDiskImage \_ 不明**</span><span class="sxs-lookup"><span data-stu-id="32dc7-110"><span id="vmFloppyDiskImage_Unknown"></span><span id="vmfloppydiskimage_unknown"></span><span id="VMFLOPPYDISKIMAGE_UNKNOWN"></span>**vmFloppyDiskImage\_Unknown**</span></span>
</dt> <dd>

<span data-ttu-id="32dc7-111">未知的格式。</span><span class="sxs-lookup"><span data-stu-id="32dc7-111">Unknown format.</span></span>

</dd> <dt>

<span data-ttu-id="32dc7-112"><span id="vmFloppyDiskImage_LowDensity"></span><span id="vmfloppydiskimage_lowdensity"></span><span id="VMFLOPPYDISKIMAGE_LOWDENSITY"></span>**vmFloppyDiskImage \_ LowDensity**</span><span class="sxs-lookup"><span data-stu-id="32dc7-112"><span id="vmFloppyDiskImage_LowDensity"></span><span id="vmfloppydiskimage_lowdensity"></span><span id="VMFLOPPYDISKIMAGE_LOWDENSITY"></span>**vmFloppyDiskImage\_LowDensity**</span></span>
</dt> <dd>

<span data-ttu-id="32dc7-113">低密度格式 (720K) 。</span><span class="sxs-lookup"><span data-stu-id="32dc7-113">A low density format (720K).</span></span>

</dd> <dt>

<span data-ttu-id="32dc7-114"><span id="vmFloppyDiskImage_HighDensity"></span><span id="vmfloppydiskimage_highdensity"></span><span id="VMFLOPPYDISKIMAGE_HIGHDENSITY"></span>**vmFloppyDiskImage \_ HighDensity**</span><span class="sxs-lookup"><span data-stu-id="32dc7-114"><span id="vmFloppyDiskImage_HighDensity"></span><span id="vmfloppydiskimage_highdensity"></span><span id="VMFLOPPYDISKIMAGE_HIGHDENSITY"></span>**vmFloppyDiskImage\_HighDensity**</span></span>
</dt> <dd>

<span data-ttu-id="32dc7-115">高密度格式 (1.44 MB) 。</span><span class="sxs-lookup"><span data-stu-id="32dc7-115">A high density format (1.44MB).</span></span>

</dd> <dt>

<span data-ttu-id="32dc7-116"><span id="vmFloppyDiskImage_DMF"></span><span id="vmfloppydiskimage_dmf"></span><span id="VMFLOPPYDISKIMAGE_DMF"></span>**vmFloppyDiskImage \_ DMF**</span><span class="sxs-lookup"><span data-stu-id="32dc7-116"><span id="vmFloppyDiskImage_DMF"></span><span id="vmfloppydiskimage_dmf"></span><span id="VMFLOPPYDISKIMAGE_DMF"></span>**vmFloppyDiskImage\_DMF**</span></span>
</dt> <dd>

<span data-ttu-id="32dc7-117"> (1.68 Mb) 的散發媒體格式。</span><span class="sxs-lookup"><span data-stu-id="32dc7-117">A distribution media format (1.68Mb).</span></span>

</dd> <dt>

<span data-ttu-id="32dc7-118"><span id="vmFloppyDiskImage_LowDensitySingleSided"></span><span id="vmfloppydiskimage_lowdensitysinglesided"></span><span id="VMFLOPPYDISKIMAGE_LOWDENSITYSINGLESIDED"></span>**vmFloppyDiskImage \_ LowDensitySingleSided**</span><span class="sxs-lookup"><span data-stu-id="32dc7-118"><span id="vmFloppyDiskImage_LowDensitySingleSided"></span><span id="vmfloppydiskimage_lowdensitysinglesided"></span><span id="VMFLOPPYDISKIMAGE_LOWDENSITYSINGLESIDED"></span>**vmFloppyDiskImage\_LowDensitySingleSided**</span></span>
</dt> <dd>

<span data-ttu-id="32dc7-119">單面低密度格式。</span><span class="sxs-lookup"><span data-stu-id="32dc7-119">A single-sided low density format.</span></span>

</dd> <dt>

<span data-ttu-id="32dc7-120"><span id="vmFloppyDiskImage_MediumDensity"></span><span id="vmfloppydiskimage_mediumdensity"></span><span id="VMFLOPPYDISKIMAGE_MEDIUMDENSITY"></span>**vmFloppyDiskImage \_ MediumDensity**</span><span class="sxs-lookup"><span data-stu-id="32dc7-120"><span id="vmFloppyDiskImage_MediumDensity"></span><span id="vmfloppydiskimage_mediumdensity"></span><span id="VMFLOPPYDISKIMAGE_MEDIUMDENSITY"></span>**vmFloppyDiskImage\_MediumDensity**</span></span>
</dt> <dd>

<span data-ttu-id="32dc7-121"> (1.2 MB) 的中等密度格式。</span><span class="sxs-lookup"><span data-stu-id="32dc7-121">A medium density format (1.2MB).</span></span>

</dd> <dt>

<span data-ttu-id="32dc7-122"><span id="vmFloppyDiskImage_HighDensityMSS"></span><span id="vmfloppydiskimage_highdensitymss"></span><span id="VMFLOPPYDISKIMAGE_HIGHDENSITYMSS"></span>**vmFloppyDiskImage \_ HighDensityMSS**</span><span class="sxs-lookup"><span data-stu-id="32dc7-122"><span id="vmFloppyDiskImage_HighDensityMSS"></span><span id="vmfloppydiskimage_highdensitymss"></span><span id="VMFLOPPYDISKIMAGE_HIGHDENSITYMSS"></span>**vmFloppyDiskImage\_HighDensityMSS**</span></span>
</dt> <dd>

<span data-ttu-id="32dc7-123">高密度的多重磁區大小 (MSS) ， (XDF) 的延伸發佈格式使用。</span><span class="sxs-lookup"><span data-stu-id="32dc7-123">A high-density Multiple Sector Size (MSS), used by eXtended Distribution Format (XDF).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="32dc7-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="32dc7-124">Requirements</span></span>



| <span data-ttu-id="32dc7-125">需求</span><span class="sxs-lookup"><span data-stu-id="32dc7-125">Requirement</span></span> | <span data-ttu-id="32dc7-126">值</span><span class="sxs-lookup"><span data-stu-id="32dc7-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="32dc7-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="32dc7-127">Minimum supported client</span></span><br/> | <span data-ttu-id="32dc7-128">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="32dc7-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="32dc7-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="32dc7-129">Minimum supported server</span></span><br/> | <span data-ttu-id="32dc7-130">都不支援</span><span class="sxs-lookup"><span data-stu-id="32dc7-130">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="32dc7-131">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="32dc7-131">End of client support</span></span><br/>    | <span data-ttu-id="32dc7-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="32dc7-132">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="32dc7-133">產品</span><span class="sxs-lookup"><span data-stu-id="32dc7-133">Product</span></span><br/>                  | <span data-ttu-id="32dc7-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="32dc7-134">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="32dc7-135">標頭</span><span class="sxs-lookup"><span data-stu-id="32dc7-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="32dc7-136"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="32dc7-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32dc7-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="32dc7-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32dc7-138">**IVMVirtualPC::CreateFloppyDiskImage**</span><span class="sxs-lookup"><span data-stu-id="32dc7-138">**IVMVirtualPC::CreateFloppyDiskImage**</span></span>](ivmvirtualpc-createfloppydiskimage.md)
</dt> <dt>

[<span data-ttu-id="32dc7-139">**IVMVirtualPC::GetFloppyDiskImageType**</span><span class="sxs-lookup"><span data-stu-id="32dc7-139">**IVMVirtualPC::GetFloppyDiskImageType**</span></span>](ivmvirtualpc-getfloppydiskimagetype.md)
</dt> </dl>

 

