---
title: '自訂繪製值 (CommCtrl .h) '
description: 此區段會列出用來識別資料列控制群組件的值。
ms.assetid: 154321c7-99f8-4ed5-a5ff-fb96126b43c7
topic_type:
- apiref
api_name:
- TBCD_CHANNEL
- TBCD_THUMB
- TBCD_TICS
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccf05ab951fdc83ec5be414688be56d710ba0d98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979421"
---
# <a name="custom-draw-values"></a><span data-ttu-id="a4a26-103">自訂繪製值</span><span class="sxs-lookup"><span data-stu-id="a4a26-103">Custom Draw Values</span></span>

<span data-ttu-id="a4a26-104">此區段會列出用來識別資料列控制群組件的值。</span><span class="sxs-lookup"><span data-stu-id="a4a26-104">This section lists the values used to identify a Trackbar control's parts.</span></span>



| <span data-ttu-id="a4a26-105">常數</span><span class="sxs-lookup"><span data-stu-id="a4a26-105">Constant</span></span>                                                                                                                                                   | <span data-ttu-id="a4a26-106">描述</span><span class="sxs-lookup"><span data-stu-id="a4a26-106">Description</span></span>                                                                                                     |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------|
| <span id="TBCD_CHANNEL"></span><span id="tbcd_channel"></span><dl> <span data-ttu-id="a4a26-107"><dt>**TBCD \_ 通道**</dt></span><span class="sxs-lookup"><span data-stu-id="a4a26-107"><dt>**TBCD\_CHANNEL**</dt></span></span> </dl> | <span data-ttu-id="a4a26-108">識別 [對齊程式] 控制項的 thumb 標記所投影的通道。</span><span class="sxs-lookup"><span data-stu-id="a4a26-108">Identifies the channel that the trackbar control's thumb marker slides along.</span></span><br/>                        |
| <span id="TBCD_THUMB"></span><span id="tbcd_thumb"></span><dl> <span data-ttu-id="a4a26-109"><dt>**TBCD \_ THUMB**</dt></span><span class="sxs-lookup"><span data-stu-id="a4a26-109"><dt>**TBCD\_THUMB**</dt></span></span> </dl>       | <span data-ttu-id="a4a26-110">識別 [資料指標] 控制項的 [thumb] 標記。</span><span class="sxs-lookup"><span data-stu-id="a4a26-110">Identifies the trackbar control's thumb marker.</span></span> <span data-ttu-id="a4a26-111">這是使用者移動之控制項的一部分。</span><span class="sxs-lookup"><span data-stu-id="a4a26-111">This is the part of the control that the user moves.</span></span><br/> |
| <span id="TBCD_TICS"></span><span id="tbcd_tics"></span><dl> <span data-ttu-id="a4a26-112"><dt>**TBCD \_ TICS**</dt></span><span class="sxs-lookup"><span data-stu-id="a4a26-112"><dt>**TBCD\_TICS**</dt></span></span> </dl>          | <span data-ttu-id="a4a26-113">識別顯示在 [側邊] 控制項邊緣的刻度。</span><span class="sxs-lookup"><span data-stu-id="a4a26-113">Identifies the tick marks that are displayed along the trackbar control's edge.</span></span><br/>                      |



## <a name="remarks"></a><span data-ttu-id="a4a26-114">備註</span><span class="sxs-lookup"><span data-stu-id="a4a26-114">Remarks</span></span>

<span data-ttu-id="a4a26-115">例如，自訂繪製值是在 [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw)結構的 **dwItemSpec** 成員中指定。</span><span class="sxs-lookup"><span data-stu-id="a4a26-115">Custom Draw values, for example, are specified in the **dwItemSpec** member of the [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4a26-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="a4a26-116">Requirements</span></span>



| <span data-ttu-id="a4a26-117">需求</span><span class="sxs-lookup"><span data-stu-id="a4a26-117">Requirement</span></span> | <span data-ttu-id="a4a26-118">值</span><span class="sxs-lookup"><span data-stu-id="a4a26-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a4a26-119">標頭</span><span class="sxs-lookup"><span data-stu-id="a4a26-119">Header</span></span><br/> | <dl> <span data-ttu-id="a4a26-120"><dt>CommCtrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="a4a26-120"><dt>CommCtrl.h</dt></span></span> </dl> |



 

 





