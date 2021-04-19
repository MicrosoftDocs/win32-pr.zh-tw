---
title: 'Tab 控制項專案狀態 (CommCtrl .h) '
description: 索引標籤控制項現在支援支援 TCM DESELECTALL 訊息的專案狀態 \_ 。 此外，TCITEM 結構支援專案狀態值。
ms.assetid: c4181fe6-0055-45c9-a3d0-8cda051383f2
topic_type:
- apiref
api_name:
- TCIS_BUTTONPRESSED
- TCIS_HIGHLIGHTED
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5214f1a2eee757bfdf5b2a81a8916292b9d7f98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989572"
---
# <a name="tab-control-item-states"></a><span data-ttu-id="a8e6c-104">Tab 控制項專案狀態</span><span class="sxs-lookup"><span data-stu-id="a8e6c-104">Tab Control Item States</span></span>

<span data-ttu-id="a8e6c-105">索引標籤控制項現在支援支援 [**TCM \_ DESELECTALL**](tcm-deselectall.md) 訊息的專案狀態。</span><span class="sxs-lookup"><span data-stu-id="a8e6c-105">Tab control items now support an item state to support the [**TCM\_DESELECTALL**](tcm-deselectall.md) message.</span></span> <span data-ttu-id="a8e6c-106">此外， [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) 結構支援專案狀態值。</span><span class="sxs-lookup"><span data-stu-id="a8e6c-106">Additionally, the [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) structure supports item state values.</span></span>



| <span data-ttu-id="a8e6c-107">常數</span><span class="sxs-lookup"><span data-stu-id="a8e6c-107">Constant</span></span>                                                                                                                                                                     | <span data-ttu-id="a8e6c-108">描述</span><span class="sxs-lookup"><span data-stu-id="a8e6c-108">Description</span></span>                                                                                                                                                                                                                                    |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TCIS_BUTTONPRESSED"></span><span id="tcis_buttonpressed"></span><dl> <span data-ttu-id="a8e6c-109"><dt>**TCIS \_ BUTTONPRESSED**</dt></span><span class="sxs-lookup"><span data-stu-id="a8e6c-109"><dt>**TCIS\_BUTTONPRESSED**</dt></span></span> </dl> | <span data-ttu-id="a8e6c-110">[版本 4.70](common-control-versions.md)。</span><span class="sxs-lookup"><span data-stu-id="a8e6c-110">[Version 4.70](common-control-versions.md).</span></span> <span data-ttu-id="a8e6c-111">已選取 [索引標籤控制項] 專案。</span><span class="sxs-lookup"><span data-stu-id="a8e6c-111">The tab control item is selected.</span></span> <span data-ttu-id="a8e6c-112">只有在已設定 [**TCS \_ 按鈕**](tab-control-styles.md) 樣式旗標的情況下，此狀態才有意義。</span><span class="sxs-lookup"><span data-stu-id="a8e6c-112">This state is only meaningful if the [**TCS\_BUTTONS**](tab-control-styles.md) style flag has been set.</span></span><br/>                                 |
| <span id="TCIS_HIGHLIGHTED"></span><span id="tcis_highlighted"></span><dl> <span data-ttu-id="a8e6c-113"><dt>**TCIS 反 \_ 白顯示**</dt></span><span class="sxs-lookup"><span data-stu-id="a8e6c-113"><dt>**TCIS\_HIGHLIGHTED**</dt></span></span> </dl>       | <span data-ttu-id="a8e6c-114">[版本 4.71](common-control-versions.md)。</span><span class="sxs-lookup"><span data-stu-id="a8e6c-114">[Version 4.71](common-control-versions.md).</span></span> <span data-ttu-id="a8e6c-115">索引標籤控制項專案會反白顯示，並使用目前的反白顯示色彩來繪製索引標籤和文字。</span><span class="sxs-lookup"><span data-stu-id="a8e6c-115">The tab control item is highlighted, and the tab and text are drawn using the current highlight color.</span></span> <span data-ttu-id="a8e6c-116">使用高色彩時，這會是真正的插補，而非遞色色彩。</span><span class="sxs-lookup"><span data-stu-id="a8e6c-116">When using high-color, this will be a true interpolation, not a dithered color.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="a8e6c-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="a8e6c-117">Requirements</span></span>



| <span data-ttu-id="a8e6c-118">需求</span><span class="sxs-lookup"><span data-stu-id="a8e6c-118">Requirement</span></span> | <span data-ttu-id="a8e6c-119">值</span><span class="sxs-lookup"><span data-stu-id="a8e6c-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a8e6c-120">標頭</span><span class="sxs-lookup"><span data-stu-id="a8e6c-120">Header</span></span><br/> | <dl> <span data-ttu-id="a8e6c-121"><dt>CommCtrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="a8e6c-121"><dt>CommCtrl.h</dt></span></span> </dl> |



 

 





