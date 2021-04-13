---
title: Dwmapi.dll) 常數的 DWM 模糊 (
description: DWM \_ BLURBEHIND 結構用來指出其中一個成員包含有效資訊的旗標。
ms.assetid: d6dd552c-1f3b-4f16-8705-f5016ed55d9e
topic_type:
- apiref
api_name:
- DWM_BB_ENABLE
- DWM_BB_BLURREGION
- DWM_BB_TRANSITIONONMAXIMIZED
api_location:
- Dwmapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbe08e0315d4c4b906cdb897ac7ad5dd34d50fbf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508811"
---
# <a name="dwm-blur-behind-constants"></a><span data-ttu-id="8d1a5-103">常數模糊背後常數</span><span class="sxs-lookup"><span data-stu-id="8d1a5-103">DWM Blur Behind Constants</span></span>

<span data-ttu-id="8d1a5-104">[**DWM \_ BLURBEHIND**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind)結構用來指出其中一個成員包含有效資訊的旗標。</span><span class="sxs-lookup"><span data-stu-id="8d1a5-104">Flags used by the [**DWM\_BLURBEHIND**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind) structure to indicate which of its members contain valid information.</span></span>

<dl> <dt>

<span data-ttu-id="8d1a5-105"><span id="DWM_BB_ENABLE"></span><span id="dwm_bb_enable"></span>**DWM \_ BB \_ 啟用**</span><span class="sxs-lookup"><span data-stu-id="8d1a5-105"><span id="DWM_BB_ENABLE"></span><span id="dwm_bb_enable"></span>**DWM\_BB\_ENABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d1a5-106">0x00000001</span><span class="sxs-lookup"><span data-stu-id="8d1a5-106">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="8d1a5-107">已指定 **fEnable** 成員的值。</span><span class="sxs-lookup"><span data-stu-id="8d1a5-107">A value for the **fEnable** member has been specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8d1a5-108"><span id="DWM_BB_BLURREGION"></span><span id="dwm_bb_blurregion"></span>**DWM \_ BB \_ BLURREGION**</span><span class="sxs-lookup"><span data-stu-id="8d1a5-108"><span id="DWM_BB_BLURREGION"></span><span id="dwm_bb_blurregion"></span>**DWM\_BB\_BLURREGION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d1a5-109">0x00000002</span><span class="sxs-lookup"><span data-stu-id="8d1a5-109">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="8d1a5-110">已指定 **hRgnBlur** 成員的值。</span><span class="sxs-lookup"><span data-stu-id="8d1a5-110">A value for the **hRgnBlur** member has been specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8d1a5-111"><span id="DWM_BB_TRANSITIONONMAXIMIZED"></span><span id="dwm_bb_transitiononmaximized"></span>**DWM \_ BB \_ TRANSITIONONMAXIMIZED**</span><span class="sxs-lookup"><span data-stu-id="8d1a5-111"><span id="DWM_BB_TRANSITIONONMAXIMIZED"></span><span id="dwm_bb_transitiononmaximized"></span>**DWM\_BB\_TRANSITIONONMAXIMIZED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d1a5-112">0x00000004</span><span class="sxs-lookup"><span data-stu-id="8d1a5-112">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="8d1a5-113">已指定 **fTransitionOnMaximized** 成員的值。</span><span class="sxs-lookup"><span data-stu-id="8d1a5-113">A value for the **fTransitionOnMaximized** member has been specified.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8d1a5-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="8d1a5-114">Requirements</span></span>



| <span data-ttu-id="8d1a5-115">需求</span><span class="sxs-lookup"><span data-stu-id="8d1a5-115">Requirement</span></span> | <span data-ttu-id="8d1a5-116">值</span><span class="sxs-lookup"><span data-stu-id="8d1a5-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8d1a5-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8d1a5-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8d1a5-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8d1a5-118">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="8d1a5-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8d1a5-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8d1a5-120">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8d1a5-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="8d1a5-121">標頭</span><span class="sxs-lookup"><span data-stu-id="8d1a5-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d1a5-122"><dt>Dwmapi.dll。h</dt></span><span class="sxs-lookup"><span data-stu-id="8d1a5-122"><dt>Dwmapi.h</dt></span></span> </dl> |



 

 





