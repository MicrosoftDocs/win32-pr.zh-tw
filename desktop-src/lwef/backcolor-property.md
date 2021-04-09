---
title: '背景屬性 (舊版 Windows 環境功能) '
description: 背景屬性
ms.assetid: a82c23bc-b280-4a52-9272-68879557cac7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3332fcc6a9081b52300dbee4c69c77602e84a62e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "103685446"
---
# <a name="backcolor-property-legacy-windows-environment-features"></a><span data-ttu-id="365d2-103">背景屬性 (舊版 Windows 環境功能) </span><span class="sxs-lookup"><span data-stu-id="365d2-103">BackColor Property (Legacy Windows Environment Features)</span></span>

<span data-ttu-id="365d2-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="365d2-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="365d2-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="365d2-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="365d2-106">傳回目前顯示在指定字元之文字氣球視窗中的背景色彩。</span><span class="sxs-lookup"><span data-stu-id="365d2-106">Returns the background color currently displayed in the word balloon window for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="365d2-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="365d2-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="365d2-108">\*代理程式 \***。 ( "**_CharacterID_*_" ) 的字元。球形色_*</span><span class="sxs-lookup"><span data-stu-id="365d2-108">*agent\***.Characters ("**_CharacterID_*_").Balloon.BackColor_\*</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="365d2-109">備註</span><span class="sxs-lookup"><span data-stu-id="365d2-109">Remarks</span></span>

<span data-ttu-id="365d2-110">標準 RGB 色彩的有效範圍為0到 16777215 (&HFFFFFF) 。</span><span class="sxs-lookup"><span data-stu-id="365d2-110">The valid range for a normal RGB color is 0 to 16,777,215 (&HFFFFFF).</span></span> <span data-ttu-id="365d2-111">此範圍中數位的最大位元組等於 0;較低的3個位元組（從最高到最大的位元組）分別決定紅色、綠色和藍色的數量。</span><span class="sxs-lookup"><span data-stu-id="365d2-111">The high byte of a number in this range equals 0; the lower 3 bytes, from least to most significant byte, determine the amount of red, green, and blue, respectively.</span></span> <span data-ttu-id="365d2-112">紅、綠和藍三種元素分別由 0 到 255 (&HFF) 之間的數字表示。</span><span class="sxs-lookup"><span data-stu-id="365d2-112">The red, green, and blue components are each represented by a number between 0 and 255 (&HFF).</span></span>

 

 




