---
title: ShowDefaultCharacterProperties 方法
description: ShowDefaultCharacterProperties 方法
ms.assetid: a3b109c0-5701-4a72-baae-bcbb97b025a3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f055b2ca0f00e0a13c24ec95dc82509ae9c45b7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672808"
---
# <a name="showdefaultcharacterproperties-method"></a><span data-ttu-id="7a703-103">ShowDefaultCharacterProperties 方法</span><span class="sxs-lookup"><span data-stu-id="7a703-103">ShowDefaultCharacterProperties Method</span></span>

<span data-ttu-id="7a703-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="7a703-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="7a703-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="7a703-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="7a703-106">顯示預設字元的屬性。</span><span class="sxs-lookup"><span data-stu-id="7a703-106">Displays the default character's properties.</span></span>

</dd> <dt>

<span data-ttu-id="7a703-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="7a703-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="7a703-108">\*代理程式 \* \* *。ShowDefaultCharacterProperties* \*  \[ *X* 、 *Y*\]</span><span class="sxs-lookup"><span data-stu-id="7a703-108">*agent\*\*\*.ShowDefaultCharacterProperties*\* \[ *X* , *Y* \]</span></span>



| <span data-ttu-id="7a703-109">部分</span><span class="sxs-lookup"><span data-stu-id="7a703-109">Part</span></span> | <span data-ttu-id="7a703-110">描述</span><span class="sxs-lookup"><span data-stu-id="7a703-110">Description</span></span>                                                                                                                                                |
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a703-111">*X*</span><span class="sxs-lookup"><span data-stu-id="7a703-111">*X*</span></span>  | <span data-ttu-id="7a703-112">選擇性。</span><span class="sxs-lookup"><span data-stu-id="7a703-112">Optional.</span></span> <span data-ttu-id="7a703-113">指出水準 (*X* ) 螢幕座標以顯示視窗的短整數值。</span><span class="sxs-lookup"><span data-stu-id="7a703-113">A short integer value that indicates the horizontal (*X* ) screen coordinate to display the window.</span></span> <span data-ttu-id="7a703-114">此座標必須以圖元為單位來指定。</span><span class="sxs-lookup"><span data-stu-id="7a703-114">This coordinate must be specified in pixels.</span></span> |
| <span data-ttu-id="7a703-115">*Y*</span><span class="sxs-lookup"><span data-stu-id="7a703-115">*Y*</span></span>  | <span data-ttu-id="7a703-116">選擇性。</span><span class="sxs-lookup"><span data-stu-id="7a703-116">Optional.</span></span> <span data-ttu-id="7a703-117">表示垂直 (*Y*) 螢幕座標以顯示視窗的短整數值。</span><span class="sxs-lookup"><span data-stu-id="7a703-117">A short integer value that indicates the vertical (*Y*) screen coordinate to display the window.</span></span> <span data-ttu-id="7a703-118">此座標必須以圖元為單位來指定。</span><span class="sxs-lookup"><span data-stu-id="7a703-118">This coordinate must be specified in pixels.</span></span>    |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7a703-119">備註</span><span class="sxs-lookup"><span data-stu-id="7a703-119">Remarks</span></span>

<span data-ttu-id="7a703-120">呼叫這個方法會顯示預設的 [字元屬性] 視窗 (不是 [Microsoft 代理程式] 屬性工作表) 。</span><span class="sxs-lookup"><span data-stu-id="7a703-120">Calling this method displays the default character properties window (not the Microsoft Agent property sheet).</span></span> <span data-ttu-id="7a703-121">如果您未指定 X 和 Y 座標，視窗會出現在最後一個顯示的位置。</span><span class="sxs-lookup"><span data-stu-id="7a703-121">If you do not specify the X and Y coordinates, the window appears at the last location it was displayed.</span></span>

## <a name="see-also"></a><span data-ttu-id="7a703-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7a703-122">See Also</span></span>

[<span data-ttu-id="7a703-123">**DefaultCharacterChange 事件**</span><span class="sxs-lookup"><span data-stu-id="7a703-123">**DefaultCharacterChange event**</span></span>](defaultcharacterchange-event.md)


 

 




