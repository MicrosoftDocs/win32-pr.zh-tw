---
title: 'VMMouseButton 列舉 (VPCCOMInterfaces) '
description: 指定滑鼠按鍵。
ms.assetid: d09e63cb-9dc5-424f-b130-c0b0dd07fe11
keywords:
- VMMouseButton 列舉虛擬電腦
topic_type:
- apiref
api_name:
- VMMouseButton
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18744af5a4f8068b9bb371cb15e06c365561f2cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466369"
---
# <a name="vmmousebutton-enumeration"></a><span data-ttu-id="fa27a-104">VMMouseButton 列舉</span><span class="sxs-lookup"><span data-stu-id="fa27a-104">VMMouseButton enumeration</span></span>

<span data-ttu-id="fa27a-105">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="fa27a-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="fa27a-106">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="fa27a-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="fa27a-107">指定滑鼠按鍵。</span><span class="sxs-lookup"><span data-stu-id="fa27a-107">Specifies the mouse button.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa27a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="fa27a-108">Syntax</span></span>


```C++
typedef enum  { 
  vmMouseButton_Left    = 1,
  vmMouseButton_Right   = 2,
  vmMouseButton_Center  = 3
} VMMouseButton;
```



## <a name="constants"></a><span data-ttu-id="fa27a-109">常數</span><span class="sxs-lookup"><span data-stu-id="fa27a-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="fa27a-110"><span id="vmMouseButton_Left"></span><span id="vmmousebutton_left"></span><span id="VMMOUSEBUTTON_LEFT"></span>**\_左 vmMouseButton**</span><span class="sxs-lookup"><span data-stu-id="fa27a-110"><span id="vmMouseButton_Left"></span><span id="vmmousebutton_left"></span><span id="VMMOUSEBUTTON_LEFT"></span>**vmMouseButton\_Left**</span></span>
</dt> <dd>

<span data-ttu-id="fa27a-111">滑鼠左鍵。</span><span class="sxs-lookup"><span data-stu-id="fa27a-111">The left mouse button.</span></span>

</dd> <dt>

<span data-ttu-id="fa27a-112"><span id="vmMouseButton_Right"></span><span id="vmmousebutton_right"></span><span id="VMMOUSEBUTTON_RIGHT"></span>**vmMouseButton \_ Right**</span><span class="sxs-lookup"><span data-stu-id="fa27a-112"><span id="vmMouseButton_Right"></span><span id="vmmousebutton_right"></span><span id="VMMOUSEBUTTON_RIGHT"></span>**vmMouseButton\_Right**</span></span>
</dt> <dd>

<span data-ttu-id="fa27a-113">滑鼠右鍵。</span><span class="sxs-lookup"><span data-stu-id="fa27a-113">The right mouse button.</span></span>

</dd> <dt>

<span data-ttu-id="fa27a-114"><span id="vmMouseButton_Center"></span><span id="vmmousebutton_center"></span><span id="VMMOUSEBUTTON_CENTER"></span>**vmMouseButton \_ 中心**</span><span class="sxs-lookup"><span data-stu-id="fa27a-114"><span id="vmMouseButton_Center"></span><span id="vmmousebutton_center"></span><span id="VMMOUSEBUTTON_CENTER"></span>**vmMouseButton\_Center**</span></span>
</dt> <dd>

<span data-ttu-id="fa27a-115">中間的滑鼠按鍵。</span><span class="sxs-lookup"><span data-stu-id="fa27a-115">The center mouse button.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fa27a-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="fa27a-116">Requirements</span></span>



| <span data-ttu-id="fa27a-117">需求</span><span class="sxs-lookup"><span data-stu-id="fa27a-117">Requirement</span></span> | <span data-ttu-id="fa27a-118">值</span><span class="sxs-lookup"><span data-stu-id="fa27a-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa27a-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fa27a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="fa27a-120">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fa27a-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fa27a-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fa27a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="fa27a-122">都不支援</span><span class="sxs-lookup"><span data-stu-id="fa27a-122">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="fa27a-123">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="fa27a-123">End of client support</span></span><br/>    | <span data-ttu-id="fa27a-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="fa27a-124">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="fa27a-125">產品</span><span class="sxs-lookup"><span data-stu-id="fa27a-125">Product</span></span><br/>                  | <span data-ttu-id="fa27a-126">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="fa27a-126">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="fa27a-127">標頭</span><span class="sxs-lookup"><span data-stu-id="fa27a-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa27a-128"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="fa27a-128"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa27a-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fa27a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa27a-130">**IVMMouse**</span><span class="sxs-lookup"><span data-stu-id="fa27a-130">**IVMMouse**</span></span>](ivmmouse.md)
</dt> </dl>

 

