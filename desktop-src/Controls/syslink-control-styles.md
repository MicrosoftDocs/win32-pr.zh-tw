---
title: 'SysLink 控制項樣式 (CommCtrl) '
description: 建立 SysLink 控制項時，會使用下列樣式常數。
ms.assetid: e9a8c99b-86c4-4385-ae20-b2b78a07b491
topic_type:
- apiref
api_name:
- LWS_TRANSPARENT
- LWS_IGNORERETURN
- LWS_NOPREFIX
- LWS_USEVISUALSTYLE
- LWS_USECUSTOMTEXT
- LWS_RIGHT
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 490a64a21ec81c1c91cc34ec8bebd2995476db4f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977698"
---
# <a name="syslink-control-styles"></a><span data-ttu-id="aefbd-103">SysLink 控制項樣式</span><span class="sxs-lookup"><span data-stu-id="aefbd-103">SysLink Control Styles</span></span>

<span data-ttu-id="aefbd-104">建立 SysLink 控制項時，會使用下列樣式常數。</span><span class="sxs-lookup"><span data-stu-id="aefbd-104">The following style constants are used when creating SysLink controls.</span></span>



| <span data-ttu-id="aefbd-105">常數</span><span class="sxs-lookup"><span data-stu-id="aefbd-105">Constant</span></span>                                                                                                                                                                        | <span data-ttu-id="aefbd-106">描述</span><span class="sxs-lookup"><span data-stu-id="aefbd-106">Description</span></span>                                                                                                                                                               |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LWS_TRANSPARENT"></span><span id="lws_transparent"></span><dl> <span data-ttu-id="aefbd-107"><dt>**LWS \_ 透明**</dt></span><span class="sxs-lookup"><span data-stu-id="aefbd-107"><dt>**LWS\_TRANSPARENT**</dt></span></span> </dl>             | <span data-ttu-id="aefbd-108">背景混合模式是透明的。</span><span class="sxs-lookup"><span data-stu-id="aefbd-108">The background mix mode is transparent.</span></span> <br/>                                                                                                                       |
| <span id="LWS_IGNORERETURN_"></span><span id="lws_ignorereturn_"></span><dl> <span data-ttu-id="aefbd-109"><dt>**LWS \_IGNORERETURN**</dt></span><span class="sxs-lookup"><span data-stu-id="aefbd-109"><dt>**LWS\_IGNORERETURN** </dt></span></span> </dl>       | <span data-ttu-id="aefbd-110">當連結具有鍵盤焦點，且使用者按下 Enter 鍵時，控制項會忽略按鍵，並將其傳遞至主控制項對話方塊。</span><span class="sxs-lookup"><span data-stu-id="aefbd-110">When the link has keyboard focus and the user presses Enter, the keystroke is ignored by the control and passed to the host dialog box.</span></span><br/>                        |
| <span id="LWS_NOPREFIX"></span><span id="lws_noprefix"></span><dl> <span data-ttu-id="aefbd-111"><dt>**LWS \_ NOPREFIX**</dt></span><span class="sxs-lookup"><span data-stu-id="aefbd-111"><dt>**LWS\_NOPREFIX**</dt></span></span> </dl>                      | <span data-ttu-id="aefbd-112">**Windows Vista**。</span><span class="sxs-lookup"><span data-stu-id="aefbd-112">**Windows Vista**.</span></span> <span data-ttu-id="aefbd-113">如果文字包含連字號，則會被視為常值字元，而不是快速鍵的前置詞。</span><span class="sxs-lookup"><span data-stu-id="aefbd-113">If the text contains an ampersand, it is treated as a literal character rather than the prefix to a shortcut key.</span></span><br/>                           |
| <span id="LWS_USEVISUALSTYLE_"></span><span id="lws_usevisualstyle_"></span><dl> <span data-ttu-id="aefbd-114"><dt>**LWS \_USEVISUALSTYLE**</dt></span><span class="sxs-lookup"><span data-stu-id="aefbd-114"><dt>**LWS\_USEVISUALSTYLE** </dt></span></span> </dl> | <span data-ttu-id="aefbd-115">**Windows Vista**。</span><span class="sxs-lookup"><span data-stu-id="aefbd-115">**Windows Vista**.</span></span> <span data-ttu-id="aefbd-116">連結會以目前的視覺效果樣式顯示。</span><span class="sxs-lookup"><span data-stu-id="aefbd-116">The link is displayed in the current visual style.</span></span><br/>                                                                                          |
| <span id="LWS_USECUSTOMTEXT"></span><span id="lws_usecustomtext"></span><dl> <span data-ttu-id="aefbd-117"><dt>**LWS \_ USECUSTOMTEXT**</dt></span><span class="sxs-lookup"><span data-stu-id="aefbd-117"><dt>**LWS\_USECUSTOMTEXT**</dt></span></span> </dl>       | <span data-ttu-id="aefbd-118">**Windows Vista**。</span><span class="sxs-lookup"><span data-stu-id="aefbd-118">**Windows Vista**.</span></span> <span data-ttu-id="aefbd-119">當繪製控制項時，會傳送 [NM \_ CUSTOMTEXT](nm-customtext.md) 通知，讓應用程式可以動態提供文字。</span><span class="sxs-lookup"><span data-stu-id="aefbd-119">An [NM\_CUSTOMTEXT](nm-customtext.md) notification is sent when the control is drawn, so that the application can supply text dynamically.</span></span><br/> |
| <span id="LWS_RIGHT"></span><span id="lws_right"></span><dl> <span data-ttu-id="aefbd-120"><dt>**LWS \_ RIGHT**</dt></span><span class="sxs-lookup"><span data-stu-id="aefbd-120"><dt>**LWS\_RIGHT**</dt></span></span> </dl>                               | <span data-ttu-id="aefbd-121">**Windows Vista**。</span><span class="sxs-lookup"><span data-stu-id="aefbd-121">**Windows Vista**.</span></span> <span data-ttu-id="aefbd-122">文字是靠右對齊。</span><span class="sxs-lookup"><span data-stu-id="aefbd-122">The text is right-justified.</span></span><br/>                                                                                                                |



## <a name="requirements"></a><span data-ttu-id="aefbd-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="aefbd-123">Requirements</span></span>



| <span data-ttu-id="aefbd-124">需求</span><span class="sxs-lookup"><span data-stu-id="aefbd-124">Requirement</span></span> | <span data-ttu-id="aefbd-125">值</span><span class="sxs-lookup"><span data-stu-id="aefbd-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="aefbd-126">標頭</span><span class="sxs-lookup"><span data-stu-id="aefbd-126">Header</span></span><br/> | <dl> <span data-ttu-id="aefbd-127"><dt>CommCtrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="aefbd-127"><dt>CommCtrl.h</dt></span></span> </dl> |



 

 





