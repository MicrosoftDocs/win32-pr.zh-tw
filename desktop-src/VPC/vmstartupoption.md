---
title: 'VMStartupOption 列舉 (VPCCOMInterfaces) '
description: 指定啟動選項。
ms.assetid: ac4de9a7-7fc7-4361-89dd-e7da8f5dbb92
keywords:
- VMStartupOption 列舉虛擬電腦
topic_type:
- apiref
api_name:
- VMStartupOption
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dc4a3bbcc1c82c57dfe144f818c29b403fd83a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465189"
---
# <a name="vmstartupoption-enumeration"></a><span data-ttu-id="af64e-104">VMStartupOption 列舉</span><span class="sxs-lookup"><span data-stu-id="af64e-104">VMStartupOption enumeration</span></span>

<span data-ttu-id="af64e-105">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="af64e-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="af64e-106">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="af64e-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="af64e-107">指定啟動選項。</span><span class="sxs-lookup"><span data-stu-id="af64e-107">Specifies the start-up option.</span></span>

## <a name="syntax"></a><span data-ttu-id="af64e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="af64e-108">Syntax</span></span>


```C++
typedef enum  { 
  vmStartupOption_Normal                      = 0,
  vmStartupOption_FixParentTimestampMismatch  = 1
} VMStartupOption;
```



## <a name="constants"></a><span data-ttu-id="af64e-109">常數</span><span class="sxs-lookup"><span data-stu-id="af64e-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="af64e-110"><span id="vmStartupOption_Normal"></span><span id="vmstartupoption_normal"></span><span id="VMSTARTUPOPTION_NORMAL"></span>**vmStartupOption \_ 正常**</span><span class="sxs-lookup"><span data-stu-id="af64e-110"><span id="vmStartupOption_Normal"></span><span id="vmstartupoption_normal"></span><span id="VMSTARTUPOPTION_NORMAL"></span>**vmStartupOption\_Normal**</span></span>
</dt> <dd>

<span data-ttu-id="af64e-111">正常啟動。</span><span class="sxs-lookup"><span data-stu-id="af64e-111">Start normally.</span></span>

</dd> <dt>

<span data-ttu-id="af64e-112"><span id="vmStartupOption_FixParentTimestampMismatch"></span><span id="vmstartupoption_fixparenttimestampmismatch"></span><span id="VMSTARTUPOPTION_FIXPARENTTIMESTAMPMISMATCH"></span>**vmStartupOption \_ FixParentTimestampMismatch**</span><span class="sxs-lookup"><span data-stu-id="af64e-112"><span id="vmStartupOption_FixParentTimestampMismatch"></span><span id="vmstartupoption_fixparenttimestampmismatch"></span><span id="VMSTARTUPOPTION_FIXPARENTTIMESTAMPMISMATCH"></span>**vmStartupOption\_FixParentTimestampMismatch**</span></span>
</dt> <dd>

<span data-ttu-id="af64e-113">修正父時間戳記不符的問題。</span><span class="sxs-lookup"><span data-stu-id="af64e-113">Fix the parent timestamp mismatch.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="af64e-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="af64e-114">Requirements</span></span>



| <span data-ttu-id="af64e-115">需求</span><span class="sxs-lookup"><span data-stu-id="af64e-115">Requirement</span></span> | <span data-ttu-id="af64e-116">值</span><span class="sxs-lookup"><span data-stu-id="af64e-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="af64e-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="af64e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="af64e-118">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="af64e-118">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="af64e-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="af64e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="af64e-120">都不支援</span><span class="sxs-lookup"><span data-stu-id="af64e-120">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="af64e-121">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="af64e-121">End of client support</span></span><br/>    | <span data-ttu-id="af64e-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="af64e-122">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="af64e-123">產品</span><span class="sxs-lookup"><span data-stu-id="af64e-123">Product</span></span><br/>                  | <span data-ttu-id="af64e-124">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="af64e-124">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="af64e-125">標頭</span><span class="sxs-lookup"><span data-stu-id="af64e-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="af64e-126"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="af64e-126"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af64e-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="af64e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af64e-128">**IVMVirtualMachine::Startup2**</span><span class="sxs-lookup"><span data-stu-id="af64e-128">**IVMVirtualMachine::Startup2**</span></span>](ivmvirtualmachine-startup2.md)
</dt> </dl>

 

