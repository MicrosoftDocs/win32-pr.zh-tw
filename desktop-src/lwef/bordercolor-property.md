---
title: 邊框出屬性
description: 邊框出屬性
ms.assetid: 7592db02-c157-45f4-bbcf-e6d5bd99e8e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6981d3ac280669f64219961b74d05c6ba73f1008
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462189"
---
# <a name="bordercolor-property"></a><span data-ttu-id="50645-103">邊框出屬性</span><span class="sxs-lookup"><span data-stu-id="50645-103">BorderColor Property</span></span>

<span data-ttu-id="50645-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="50645-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="50645-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="50645-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="50645-106">傳回目前針對指定字元之文字氣球視窗顯示的框線色彩。</span><span class="sxs-lookup"><span data-stu-id="50645-106">Returns the border color currently displayed for the word balloon window for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="50645-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="50645-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="50645-108">\* 代理程式 ***。 ( "*** CharacterID \***" 的字元 ) 。** 球形邊框</span><span class="sxs-lookup"><span data-stu-id="50645-108">*agent ***.Characters ("*** CharacterID\*\*\*").*\* Balloon.BorderColor</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="50645-109">備註</span><span class="sxs-lookup"><span data-stu-id="50645-109">Remarks</span></span>

<span data-ttu-id="50645-110">標準 RGB 色彩的有效範圍為0到 16777215 (&HFFFFFF) 。</span><span class="sxs-lookup"><span data-stu-id="50645-110">The valid range for a normal RGB color is 0 to 16,777,215 (&HFFFFFF).</span></span> <span data-ttu-id="50645-111">此範圍中數位的最大位元組等於 0;較低的3個位元組（從最高到最大的位元組）分別決定紅色、綠色和藍色的數量。</span><span class="sxs-lookup"><span data-stu-id="50645-111">The high byte of a number in this range equals 0; the lower 3 bytes, from least to most significant byte, determine the amount of red, green, and blue, respectively.</span></span> <span data-ttu-id="50645-112">紅、綠和藍三種元素分別由 0 到 255 (&HFF) 之間的數字表示。</span><span class="sxs-lookup"><span data-stu-id="50645-112">The red, green, and blue components are each represented by a number between 0 and 255 (&HFF).</span></span>

 

 




