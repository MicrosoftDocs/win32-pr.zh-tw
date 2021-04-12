---
title: 'WTNCA 值 (Uxtheme) '
description: 指定修改視窗視覺化樣式屬性的旗標。 使用其中一個，或下列值的位元組合。
ms.assetid: C71D1957-6572-4242-B715-C54BDFBBD6B7
topic_type:
- apiref
api_name:
- WTNCA_NODRAWCAPTION
- WTNCA_NODRAWICON
- WTNCA_NOSYSMENU
- WTNCA_NOMIRRORHELP
- WTNCA_VALIDBITS
api_location:
- Uxtheme.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebaf543b688d0b403962da43029ac9aa85422bc6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105941"
---
# <a name="wtnca-values"></a><span data-ttu-id="c76cd-104">WTNCA 值</span><span class="sxs-lookup"><span data-stu-id="c76cd-104">WTNCA Values</span></span>

<span data-ttu-id="c76cd-105">指定修改視窗視覺化樣式屬性的旗標。</span><span class="sxs-lookup"><span data-stu-id="c76cd-105">Specifies flags that modify window visual style attributes.</span></span> <span data-ttu-id="c76cd-106">使用其中一個，或下列值的位元組合。</span><span class="sxs-lookup"><span data-stu-id="c76cd-106">Use one, or a bitwise combination of the following values.</span></span>



| <span data-ttu-id="c76cd-107">常數/值</span><span class="sxs-lookup"><span data-stu-id="c76cd-107">Constant/value</span></span>                                                                                                                                                                                                                                  | <span data-ttu-id="c76cd-108">Description</span><span class="sxs-lookup"><span data-stu-id="c76cd-108">Description</span></span>                                                                             |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------|
| <span id="WTNCA_NODRAWCAPTION"></span><span id="wtnca_nodrawcaption"></span><dl> <span data-ttu-id="c76cd-109"><dt>**WTNCA \_NODRAWCAPTION**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="c76cd-109"><dt>**WTNCA\_NODRAWCAPTION**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="c76cd-110">防止繪製視窗標題。</span><span class="sxs-lookup"><span data-stu-id="c76cd-110">Prevents the window caption from being drawn.</span></span><br/>                                |
| <span id="WTNCA_NODRAWICON"></span><span id="wtnca_nodrawicon"></span><dl> <span data-ttu-id="c76cd-111"><dt>**WTNCA \_NODRAWICON**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="c76cd-111"><dt>**WTNCA\_NODRAWICON**</dt> <dt>0x00000002</dt></span></span> </dl>          | <span data-ttu-id="c76cd-112">防止繪製系統圖示。</span><span class="sxs-lookup"><span data-stu-id="c76cd-112">Prevents the system icon from being drawn.</span></span><br/>                                   |
| <span id="WTNCA_NOSYSMENU"></span><span id="wtnca_nosysmenu"></span><dl> <span data-ttu-id="c76cd-113"><dt>**WTNCA \_NOSYSMENU**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="c76cd-113"><dt>**WTNCA\_NOSYSMENU**</dt> <dt>0x00000004</dt></span></span> </dl>             | <span data-ttu-id="c76cd-114">防止出現系統圖示功能表。</span><span class="sxs-lookup"><span data-stu-id="c76cd-114">Prevents the system icon menu from appearing.</span></span><br/>                                |
| <span id="WTNCA_NOMIRRORHELP"></span><span id="wtnca_nomirrorhelp"></span><dl> <span data-ttu-id="c76cd-115"><dt>**WTNCA \_NOMIRRORHELP**</dt> <dt>0x00000008</dt></span><span class="sxs-lookup"><span data-stu-id="c76cd-115"><dt>**WTNCA\_NOMIRRORHELP**</dt> <dt>0x00000008</dt></span></span> </dl>    | <span data-ttu-id="c76cd-116">防止問號的鏡像，即使是由右至左 (RTL) 版面配置。</span><span class="sxs-lookup"><span data-stu-id="c76cd-116">Prevents mirroring of the question mark, even in right-to-left (RTL) layout.</span></span><br/> |
| <span id="WTNCA_VALIDBITS"></span><span id="wtnca_validbits"></span><dl> <span data-ttu-id="c76cd-117"><dt>**WTNCA \_ VALIDBITS**</dt></span><span class="sxs-lookup"><span data-stu-id="c76cd-117"><dt>**WTNCA\_VALIDBITS**</dt></span></span> </dl>                                                                             | <span data-ttu-id="c76cd-118">包含所有有效位的遮罩。</span><span class="sxs-lookup"><span data-stu-id="c76cd-118">A mask that contains all the valid bits.</span></span><br/>                                     |



## <a name="requirements"></a><span data-ttu-id="c76cd-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="c76cd-119">Requirements</span></span>



| <span data-ttu-id="c76cd-120">需求</span><span class="sxs-lookup"><span data-stu-id="c76cd-120">Requirement</span></span> | <span data-ttu-id="c76cd-121">值</span><span class="sxs-lookup"><span data-stu-id="c76cd-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c76cd-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c76cd-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c76cd-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c76cd-123">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="c76cd-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c76cd-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c76cd-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c76cd-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="c76cd-126">標頭</span><span class="sxs-lookup"><span data-stu-id="c76cd-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="c76cd-127"><dt>Uxtheme。h</dt></span><span class="sxs-lookup"><span data-stu-id="c76cd-127"><dt>Uxtheme.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c76cd-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c76cd-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="c76cd-129">**參考**</span><span class="sxs-lookup"><span data-stu-id="c76cd-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c76cd-130">**WTA \_ 選項**</span><span class="sxs-lookup"><span data-stu-id="c76cd-130">**WTA\_OPTIONS**</span></span>](/windows/desktop/api/Uxtheme/ns-uxtheme-wta_options)
</dt> <dt>

[<span data-ttu-id="c76cd-131">**SetWindowThemeNonClientAttributes**</span><span class="sxs-lookup"><span data-stu-id="c76cd-131">**SetWindowThemeNonClientAttributes**</span></span>](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowthemenonclientattributes)
</dt> </dl>

 

 





