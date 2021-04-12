---
title: 'VMDisplayVideoMode 列舉 (VPCCOMInterfaces) '
description: 指定顯示影片模式。
ms.assetid: 9ffd1bb5-115d-4554-92c6-5dcf86f904a5
keywords:
- VMDisplayVideoMode 列舉虛擬電腦
topic_type:
- apiref
api_name:
- VMDisplayVideoMode
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b159a8c251c83643ae9897842b313ea9be567e4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465193"
---
# <a name="vmdisplayvideomode-enumeration"></a><span data-ttu-id="df750-104">VMDisplayVideoMode 列舉</span><span class="sxs-lookup"><span data-stu-id="df750-104">VMDisplayVideoMode enumeration</span></span>

<span data-ttu-id="df750-105">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="df750-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="df750-106">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="df750-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="df750-107">指定顯示影片模式。</span><span class="sxs-lookup"><span data-stu-id="df750-107">Specifies the display video mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="df750-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="df750-108">Syntax</span></span>


```C++
typedef enum  { 
  vmVideoMode_TextMode  = 0,
  vmVideoMode_CGAMode   = 1,
  vmVideoMode_VGAMode   = 2,
  vmVideoMode_SVGAMode  = 3
} VMDisplayVideoMode;
```



## <a name="constants"></a><span data-ttu-id="df750-109">常數</span><span class="sxs-lookup"><span data-stu-id="df750-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="df750-110"><span id="vmVideoMode_TextMode"></span><span id="vmvideomode_textmode"></span><span id="VMVIDEOMODE_TEXTMODE"></span>**vmVideoMode \_ TextMode**</span><span class="sxs-lookup"><span data-stu-id="df750-110"><span id="vmVideoMode_TextMode"></span><span id="vmvideomode_textmode"></span><span id="VMVIDEOMODE_TEXTMODE"></span>**vmVideoMode\_TextMode**</span></span>
</dt> <dd>

<span data-ttu-id="df750-111">文字模式。</span><span class="sxs-lookup"><span data-stu-id="df750-111">Text mode.</span></span>

</dd> <dt>

<span data-ttu-id="df750-112"><span id="vmVideoMode_CGAMode"></span><span id="vmvideomode_cgamode"></span><span id="VMVIDEOMODE_CGAMODE"></span>**vmVideoMode \_ CGAMode**</span><span class="sxs-lookup"><span data-stu-id="df750-112"><span id="vmVideoMode_CGAMode"></span><span id="vmvideomode_cgamode"></span><span id="VMVIDEOMODE_CGAMODE"></span>**vmVideoMode\_CGAMode**</span></span>
</dt> <dd>

<span data-ttu-id="df750-113">CGA 模式。</span><span class="sxs-lookup"><span data-stu-id="df750-113">CGA mode.</span></span>

</dd> <dt>

<span data-ttu-id="df750-114"><span id="vmVideoMode_VGAMode"></span><span id="vmvideomode_vgamode"></span><span id="VMVIDEOMODE_VGAMODE"></span>**vmVideoMode \_ VGAMode**</span><span class="sxs-lookup"><span data-stu-id="df750-114"><span id="vmVideoMode_VGAMode"></span><span id="vmvideomode_vgamode"></span><span id="VMVIDEOMODE_VGAMODE"></span>**vmVideoMode\_VGAMode**</span></span>
</dt> <dd>

<span data-ttu-id="df750-115">VGA 模式。</span><span class="sxs-lookup"><span data-stu-id="df750-115">VGA mode.</span></span>

</dd> <dt>

<span data-ttu-id="df750-116"><span id="vmVideoMode_SVGAMode"></span><span id="vmvideomode_svgamode"></span><span id="VMVIDEOMODE_SVGAMODE"></span>**vmVideoMode \_ SVGAMode**</span><span class="sxs-lookup"><span data-stu-id="df750-116"><span id="vmVideoMode_SVGAMode"></span><span id="vmvideomode_svgamode"></span><span id="VMVIDEOMODE_SVGAMODE"></span>**vmVideoMode\_SVGAMode**</span></span>
</dt> <dd>

<span data-ttu-id="df750-117">SVGA 模式。</span><span class="sxs-lookup"><span data-stu-id="df750-117">SVGA mode.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="df750-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="df750-118">Requirements</span></span>



| <span data-ttu-id="df750-119">需求</span><span class="sxs-lookup"><span data-stu-id="df750-119">Requirement</span></span> | <span data-ttu-id="df750-120">值</span><span class="sxs-lookup"><span data-stu-id="df750-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="df750-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="df750-121">Minimum supported client</span></span><br/> | <span data-ttu-id="df750-122">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="df750-122">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="df750-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="df750-123">Minimum supported server</span></span><br/> | <span data-ttu-id="df750-124">都不支援</span><span class="sxs-lookup"><span data-stu-id="df750-124">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="df750-125">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="df750-125">End of client support</span></span><br/>    | <span data-ttu-id="df750-126">Windows 7</span><span class="sxs-lookup"><span data-stu-id="df750-126">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="df750-127">產品</span><span class="sxs-lookup"><span data-stu-id="df750-127">Product</span></span><br/>                  | <span data-ttu-id="df750-128">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="df750-128">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="df750-129">標頭</span><span class="sxs-lookup"><span data-stu-id="df750-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="df750-130"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="df750-130"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df750-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="df750-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df750-132">**IVMDisplay::VideoMode**</span><span class="sxs-lookup"><span data-stu-id="df750-132">**IVMDisplay::VideoMode**</span></span>](ivmdisplay-videomode.md)
</dt> </dl>

 

