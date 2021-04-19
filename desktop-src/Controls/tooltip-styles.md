---
title: '工具提示樣式 (CommCtrl .h) '
description: 此區段會列出與工具提示控制項搭配使用的控制項樣式。
ms.assetid: a6aeac71-6a69-4903-af78-0bfe1f83e632
topic_type:
- apiref
api_name:
- TTS_ALWAYSTIP
- TTS_BALLOON
- TTS_CLOSE
- TTS_NOANIMATE
- TTS_NOFADE
- TTS_NOPREFIX
- TTS_USEVISUALSTYLE
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff8b89aed88caddceae815414b9f2b4d93a550c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989763"
---
# <a name="tooltip-styles"></a><span data-ttu-id="b9ff8-103">工具提示樣式</span><span class="sxs-lookup"><span data-stu-id="b9ff8-103">Tooltip Styles</span></span>

<span data-ttu-id="b9ff8-104">此區段會列出與工具提示控制項搭配使用的控制項樣式。</span><span class="sxs-lookup"><span data-stu-id="b9ff8-104">This section lists the control styles used with tooltip controls.</span></span>



| <span data-ttu-id="b9ff8-105">常數</span><span class="sxs-lookup"><span data-stu-id="b9ff8-105">Constant</span></span>                                                                                                                                                                     | <span data-ttu-id="b9ff8-106">描述</span><span class="sxs-lookup"><span data-stu-id="b9ff8-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                       |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TTS_ALWAYSTIP"></span><span id="tts_alwaystip"></span><dl> <span data-ttu-id="b9ff8-107"><dt>**TTS \_ ALWAYSTIP**</dt></span><span class="sxs-lookup"><span data-stu-id="b9ff8-107"><dt>**TTS\_ALWAYSTIP**</dt></span></span> </dl>                | <span data-ttu-id="b9ff8-108">指出工具提示控制項出現時，即使工具提示控制項的主控視窗處於非使用中狀態，也會出現工具提示控制項。</span><span class="sxs-lookup"><span data-stu-id="b9ff8-108">Indicates that the tooltip control appears when the cursor is on a tool, even if the tooltip control's owner window is inactive.</span></span> <span data-ttu-id="b9ff8-109">若未使用此樣式，則只有當工具的擁有者視窗為使用中時，工具提示才會出現。</span><span class="sxs-lookup"><span data-stu-id="b9ff8-109">Without this style, the tooltip appears only when the tool's owner window is active.</span></span><br/>                                                                                                                                  |
| <span id="TTS_BALLOON"></span><span id="tts_balloon"></span><dl> <span data-ttu-id="b9ff8-110"><dt>**TTS \_ 氣球**</dt></span><span class="sxs-lookup"><span data-stu-id="b9ff8-110"><dt>**TTS\_BALLOON**</dt></span></span> </dl>                      | <span data-ttu-id="b9ff8-111">[版本 5.80](common-control-versions.md)。</span><span class="sxs-lookup"><span data-stu-id="b9ff8-111">[Version 5.80](common-control-versions.md).</span></span> <span data-ttu-id="b9ff8-112">指出工具提示控制項具有具有圓角的卡通「球標」的外觀，以及指向該專案的詞幹。</span><span class="sxs-lookup"><span data-stu-id="b9ff8-112">Indicates that the tooltip control has the appearance of a cartoon "balloon," with rounded corners and a stem pointing to the item.</span></span> <br/>                                                                                                                                                                      |
| <span id="TTS_CLOSE"></span><span id="tts_close"></span><dl> <span data-ttu-id="b9ff8-113"><dt>**TTS \_ 關閉**</dt></span><span class="sxs-lookup"><span data-stu-id="b9ff8-113"><dt>**TTS\_CLOSE**</dt></span></span> </dl>                            | <span data-ttu-id="b9ff8-114">在工具提示上顯示 [ **關閉** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="b9ff8-114">Displays a **Close** button on the tooltip.</span></span> <span data-ttu-id="b9ff8-115">只有當工具提示具有 TTS \_ 氣球樣式和標題時有效，請參閱 [**TTM \_ SETTITLE**](ttm-settitle.md)。</span><span class="sxs-lookup"><span data-stu-id="b9ff8-115">Valid only when the tooltip has the TTS\_BALLOON style and a title; see [**TTM\_SETTITLE**](ttm-settitle.md).</span></span><br/>                                                                                                                                                                                             |
| <span id="TTS_NOANIMATE"></span><span id="tts_noanimate"></span><dl> <span data-ttu-id="b9ff8-116"><dt>**TTS \_ NOANIMATE**</dt></span><span class="sxs-lookup"><span data-stu-id="b9ff8-116"><dt>**TTS\_NOANIMATE**</dt></span></span> </dl>                | <span data-ttu-id="b9ff8-117">[版本 5.80](common-control-versions.md)。</span><span class="sxs-lookup"><span data-stu-id="b9ff8-117">[Version 5.80](common-control-versions.md).</span></span> <span data-ttu-id="b9ff8-118">在 Windows 98 和 Windows 2000 系統上停用滑動工具提示動畫。</span><span class="sxs-lookup"><span data-stu-id="b9ff8-118">Disables sliding tooltip animation on Windows 98 and Windows 2000 systems.</span></span> <span data-ttu-id="b9ff8-119">舊版系統會忽略這個樣式。</span><span class="sxs-lookup"><span data-stu-id="b9ff8-119">This style is ignored on earlier systems.</span></span><br/>                                                                                                                                                                                      |
| <span id="TTS_NOFADE"></span><span id="tts_nofade"></span><dl> <span data-ttu-id="b9ff8-120"><dt>**TTS \_ NOFADE**</dt></span><span class="sxs-lookup"><span data-stu-id="b9ff8-120"><dt>**TTS\_NOFADE**</dt></span></span> </dl>                         | <span data-ttu-id="b9ff8-121">[版本 5.80](common-control-versions.md)。</span><span class="sxs-lookup"><span data-stu-id="b9ff8-121">[Version 5.80](common-control-versions.md).</span></span> <span data-ttu-id="b9ff8-122">停用淡化工具提示動畫。</span><span class="sxs-lookup"><span data-stu-id="b9ff8-122">Disables fading tooltip animation.</span></span> <br/>                                                                                                                                                                                                                                                                       |
| <span id="TTS_NOPREFIX"></span><span id="tts_noprefix"></span><dl> <span data-ttu-id="b9ff8-123"><dt>**TTS \_ NOPREFIX**</dt></span><span class="sxs-lookup"><span data-stu-id="b9ff8-123"><dt>**TTS\_NOPREFIX**</dt></span></span> </dl>                   | <span data-ttu-id="b9ff8-124">防止系統從字串中移除連字號字元，或在定位字元處終止字串。</span><span class="sxs-lookup"><span data-stu-id="b9ff8-124">Prevents the system from stripping ampersand characters from a string or terminating a string at a tab character.</span></span> <span data-ttu-id="b9ff8-125">若未使用此樣式，系統會自動去除連字號字元，並在第一個定位字元結束字串。</span><span class="sxs-lookup"><span data-stu-id="b9ff8-125">Without this style, the system automatically strips ampersand characters and terminates a string at the first tab character.</span></span> <span data-ttu-id="b9ff8-126">這可讓應用程式使用與功能表項目相同的字串，以及工具提示控制項中的文字。</span><span class="sxs-lookup"><span data-stu-id="b9ff8-126">This allows an application to use the same string as both a menu item and as text in a tooltip control.</span></span><br/> |
| <span id="TTS_USEVISUALSTYLE"></span><span id="tts_usevisualstyle"></span><dl> <span data-ttu-id="b9ff8-127"><dt>**TTS \_ USEVISUALSTYLE**</dt></span><span class="sxs-lookup"><span data-stu-id="b9ff8-127"><dt>**TTS\_USEVISUALSTYLE**</dt></span></span> </dl> | <span data-ttu-id="b9ff8-128">使用主題超連結。</span><span class="sxs-lookup"><span data-stu-id="b9ff8-128">Uses themed hyperlinks.</span></span> <span data-ttu-id="b9ff8-129">主題將會定義工具提示中任何連結的樣式。</span><span class="sxs-lookup"><span data-stu-id="b9ff8-129">The theme will define the styles for any links in the tooltip.</span></span> <span data-ttu-id="b9ff8-130">此樣式一律需要 \_ 設定 TTF PARSELINKS。</span><span class="sxs-lookup"><span data-stu-id="b9ff8-130">This style always requires TTF\_PARSELINKS to be set.</span></span> <br/>                                                                                                                                                                                                          |



## <a name="remarks"></a><span data-ttu-id="b9ff8-131">備註</span><span class="sxs-lookup"><span data-stu-id="b9ff8-131">Remarks</span></span>

<span data-ttu-id="b9ff8-132">\_ \_ 無論您是在建立控制項時指定它們，工具提示控制項一律會有 ws POPUP 和 ws EX \_ 工具視窗視窗樣式。</span><span class="sxs-lookup"><span data-stu-id="b9ff8-132">A tooltip control always has the WS\_POPUP and WS\_EX\_TOOLWINDOW window styles, regardless of whether you specify them when creating the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9ff8-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="b9ff8-133">Requirements</span></span>



| <span data-ttu-id="b9ff8-134">需求</span><span class="sxs-lookup"><span data-stu-id="b9ff8-134">Requirement</span></span> | <span data-ttu-id="b9ff8-135">值</span><span class="sxs-lookup"><span data-stu-id="b9ff8-135">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b9ff8-136">標頭</span><span class="sxs-lookup"><span data-stu-id="b9ff8-136">Header</span></span><br/> | <dl> <span data-ttu-id="b9ff8-137"><dt>CommCtrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="b9ff8-137"><dt>CommCtrl.h</dt></span></span> </dl> |



 

 





