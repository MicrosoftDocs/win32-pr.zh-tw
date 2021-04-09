---
title: '動畫控制項 (MSAA UI 元素參考) '
description: 動畫控制項以無訊息模式顯示交錯 (AVI) 剪輯的音訊影片。 動畫控制項通常會在複製檔案時，或在執行其他一些耗時的工作時顯示。
ms.assetid: 2a31d4ba-a1bd-478b-86a9-726fa93ab714
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43ca7cf7e4b8a2174dae81b1770b2d877f749502
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673328"
---
# <a name="animation-control-msaa-ui-element-reference"></a><span data-ttu-id="a0594-104">動畫控制項 (MSAA UI 元素參考) </span><span class="sxs-lookup"><span data-stu-id="a0594-104">Animation Control (MSAA UI Element Reference)</span></span>

<span data-ttu-id="a0594-105">動畫控制項以無訊息模式顯示交錯 (AVI) 剪輯的音訊影片。</span><span class="sxs-lookup"><span data-stu-id="a0594-105">Animation controls silently display an audio video interleaved (AVI) clip.</span></span> <span data-ttu-id="a0594-106">動畫控制項通常會在複製檔案時，或在執行其他一些耗時的工作時顯示。</span><span class="sxs-lookup"><span data-stu-id="a0594-106">Animation controls are usually displayed when files are being copied or when some other time-consuming task is being performed.</span></span>

<span data-ttu-id="a0594-107">動畫控制項的視窗類別名稱是在 \_ Commctrl 中定義為 "SysAnimate32" 的動畫類別。</span><span class="sxs-lookup"><span data-stu-id="a0594-107">The window class name for an animation control is ANIMATE\_CLASS, which is defined as "SysAnimate32" in Commctrl.h.</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="a0594-108">IAccessible 方法</span><span class="sxs-lookup"><span data-stu-id="a0594-108">IAccessible Methods</span></span>

<span data-ttu-id="a0594-109">動畫控制項支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 方法：</span><span class="sxs-lookup"><span data-stu-id="a0594-109">Animation controls support the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="a0594-110">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="a0594-110">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="a0594-111">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="a0594-111">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="a0594-112">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="a0594-112">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [<span data-ttu-id="a0594-113">**accSelect**</span><span class="sxs-lookup"><span data-stu-id="a0594-113">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a><span data-ttu-id="a0594-114">IAccessible 屬性</span><span class="sxs-lookup"><span data-stu-id="a0594-114">IAccessible Properties</span></span>

<span data-ttu-id="a0594-115">動畫控制項支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性：</span><span class="sxs-lookup"><span data-stu-id="a0594-115">Animation controls support the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



| <span data-ttu-id="a0594-116">屬性</span><span class="sxs-lookup"><span data-stu-id="a0594-116">Property</span></span>                                                                             | <span data-ttu-id="a0594-117">註解</span><span class="sxs-lookup"><span data-stu-id="a0594-117">Comments</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a0594-118">**取得 \_ accChildCount**</span><span class="sxs-lookup"><span data-stu-id="a0594-118">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | <span data-ttu-id="a0594-119">**ChildCount** 屬性為零。</span><span class="sxs-lookup"><span data-stu-id="a0594-119">The **ChildCount** property is zero.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="a0594-120">**取得 \_ accKeyboardShortcut**</span><span class="sxs-lookup"><span data-stu-id="a0594-120">**get\_accKeyboardShortcut**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | <span data-ttu-id="a0594-121">動畫控制項沒有鍵盤快速鍵。</span><span class="sxs-lookup"><span data-stu-id="a0594-121">Animation controls do not have keyboard shortcuts.</span></span> <span data-ttu-id="a0594-122">但是，如果控制項的標籤包含存取金鑰 (控制項標籤的文字中有加底線的字元) ， [**get \_ accKeyboardShortcut 就**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) 會傳回非 Null 字串。</span><span class="sxs-lookup"><span data-stu-id="a0594-122">However, if the label for the control contains an access key (an underlined character in the text of the control's label), [**get\_accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) returns a non-NULL string.</span></span> <span data-ttu-id="a0594-123">此字串包含附加至字串 "Alt +" 的存取金鑰字元。</span><span class="sxs-lookup"><span data-stu-id="a0594-123">This string contains the access key character appended to the string "Alt+".</span></span> <span data-ttu-id="a0594-124">例如，如果標籤為「正在下載檔案」， **KeyboardShortcut** 會是 "Alt + d"。</span><span class="sxs-lookup"><span data-stu-id="a0594-124">For example, if the label is "Downloading Files", **KeyboardShortcut** is "Alt+d".</span></span>                                                                                        |
| [<span data-ttu-id="a0594-125">**取得 \_ accName**</span><span class="sxs-lookup"><span data-stu-id="a0594-125">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | <span data-ttu-id="a0594-126">**Name** 屬性是從標記動畫控制項的靜態文字控制項取得。</span><span class="sxs-lookup"><span data-stu-id="a0594-126">The **Name** property is obtained from the static text control that labels the animation control.</span></span> <span data-ttu-id="a0594-127">當您建立控制項時，伺服器開發人員必須確保靜態文字控制項會緊接在定位順序中所標記的控制項之前。</span><span class="sxs-lookup"><span data-stu-id="a0594-127">When creating controls, server developers must ensure that a static text control immediately precedes the control that it labels within the tab order.</span></span>                                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="a0594-128">**取得 \_ accParent**</span><span class="sxs-lookup"><span data-stu-id="a0594-128">**get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | <span data-ttu-id="a0594-129">**父** 屬性是在控制項周圍 ([**角色 \_ 系統 \_ 視窗**](object-roles.md)) 的視窗，而且具有與控制項相同的 **名稱** 屬性和視窗類別名稱。</span><span class="sxs-lookup"><span data-stu-id="a0594-129">The **Parent** property is a window ( [**ROLE\_SYSTEM\_WINDOW**](object-roles.md) ) that surrounds the control and has the same **Name** property and window class name as the control.</span></span>                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="a0594-130">**取得 \_ accRole**</span><span class="sxs-lookup"><span data-stu-id="a0594-130">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | <span data-ttu-id="a0594-131">**Role** 屬性是 [**角色 \_ 系統 \_ 動畫**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="a0594-131">The **Role** property is [**ROLE\_SYSTEM\_ANIMATION**](object-roles.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="a0594-132">**取得 \_ accState**</span><span class="sxs-lookup"><span data-stu-id="a0594-132">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | <span data-ttu-id="a0594-133">**State** 屬性是一或多個下列物件狀態常數的組合：[**狀態 \_ 系統 \_ 不可見**](object-state-constants.md) \| [**狀態 \_ 系統 \_ 無法使用**](object-state-constants.md)的 \| [**狀態 \_ 系統 \_ 聚焦**](object-state-constants.md)的 \| [**狀態 \_ 系統 \_ 動畫**](object-state-constants.md)</span><span class="sxs-lookup"><span data-stu-id="a0594-133">The **State** property is a combination of one or more of the following object state constants: [**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_UNAVAILABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSED**](object-state-constants.md) \| [**STATE\_SYSTEM\_ANIMATED**](object-state-constants.md)</span></span><br/> <span data-ttu-id="a0594-134">如需詳細資訊，請參閱 [物件狀態常數](object-state-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="a0594-134">For more information, see [Object State Constants](object-state-constants.md).</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="a0594-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="a0594-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0594-136">IAccessible 介面</span><span class="sxs-lookup"><span data-stu-id="a0594-136">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





