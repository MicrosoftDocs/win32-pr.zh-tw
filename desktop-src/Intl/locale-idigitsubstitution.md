---
description: 地區設定 \_ IDIGITSUBSTITUTION
ms.assetid: f3f7d7ac-8f1e-4bfa-84f0-dfe8cff568c3
title: LOCALE_IDIGITSUBSTITUTION
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c063ed5b937c3e4c4ae06e40631b9795f6a73ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112001"
---
# <a name="locale_idigitsubstitution"></a><span data-ttu-id="57ef7-103">地區設定 \_ IDIGITSUBSTITUTION</span><span class="sxs-lookup"><span data-stu-id="57ef7-103">LOCALE\_IDIGITSUBSTITUTION</span></span>

<span data-ttu-id="57ef7-104">**Windows 2000：** 數位的形狀。</span><span class="sxs-lookup"><span data-stu-id="57ef7-104">**Windows 2000:** The shape of digits.</span></span> <span data-ttu-id="57ef7-105">例如，阿拉伯文、泰文和印度數位具有與歐洲數位不同的傳統圖形。</span><span class="sxs-lookup"><span data-stu-id="57ef7-105">For example, Arabic, Thai, and Indic digits have classical shapes different from European digits.</span></span> <span data-ttu-id="57ef7-106">如果地區設定 [ \_ SNATIVEDIGITS](locale-snative-constants.md) 指定為 ASCII 0-9 以外的值，此值會指定是否應將喜好設定提供給其他數位，以供顯示之用。</span><span class="sxs-lookup"><span data-stu-id="57ef7-106">For locales with [LOCALE\_SNATIVEDIGITS](locale-snative-constants.md) specified as values other than ASCII 0-9, this value specifies whether preference should be given to those other digits for display purposes.</span></span> <span data-ttu-id="57ef7-107">例如，如果選擇的值為2，則一律會使用地區設定 SNATIVEDIGITS 所指定的位數 \_ 。</span><span class="sxs-lookup"><span data-stu-id="57ef7-107">For example, if a value of 2 is chosen, the digits specified by LOCALE\_SNATIVEDIGITS are always used.</span></span> <span data-ttu-id="57ef7-108">如果選擇1，一律會使用 ASCII 0-9 位數。</span><span class="sxs-lookup"><span data-stu-id="57ef7-108">If a 1 is chosen, the ASCII 0-9 digits are always used.</span></span> <span data-ttu-id="57ef7-109">如果選擇0，則會在某些情況下使用 ASCII，並在其他情況下使用地區設定 SNATIVEDIGITS 所指定的位數 \_ （視內容而定）。</span><span class="sxs-lookup"><span data-stu-id="57ef7-109">If a 0 is chosen, ASCII is used in some circumstances and the digits specified by LOCALE\_SNATIVEDIGITS are used in others, depending on the context.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="57ef7-110">值</span><span class="sxs-lookup"><span data-stu-id="57ef7-110">Value</span></span></th>
<th><span data-ttu-id="57ef7-111">意義</span><span class="sxs-lookup"><span data-stu-id="57ef7-111">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="57ef7-112">0</span><span class="sxs-lookup"><span data-stu-id="57ef7-112">0</span></span></td>
<td><span data-ttu-id="57ef7-113">以內容為基礎的替代。</span><span class="sxs-lookup"><span data-stu-id="57ef7-113">Context-based substitution.</span></span> <span data-ttu-id="57ef7-114">會根據相同輸出中先前的文字來顯示數位。</span><span class="sxs-lookup"><span data-stu-id="57ef7-114">Digits are displayed based on the previous text in the same output.</span></span> <span data-ttu-id="57ef7-115">歐洲數位遵循拉丁腳本、Arabic-Indic 位數遵循阿拉伯文文字，而其他國家/地區則遵循其他腳本中所撰寫的文字。</span><span class="sxs-lookup"><span data-stu-id="57ef7-115">European digits follow Latin scripts, Arabic-Indic digits follow Arabic text, and other national digits follow text written in various other scripts.</span></span> <span data-ttu-id="57ef7-116">如果沒有上述文字，地區設定和顯示的讀取順序會決定數位替代，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="57ef7-116">When there is no preceding text, the locale and the displayed reading order determine digit substitution, as shown in the following table.</span></span>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="57ef7-117">Locale</span><span class="sxs-lookup"><span data-stu-id="57ef7-117">Locale</span></span></th>
<th><span data-ttu-id="57ef7-118">讀取順序</span><span class="sxs-lookup"><span data-stu-id="57ef7-118">Reading order</span></span></th>
<th><span data-ttu-id="57ef7-119">使用的數位</span><span class="sxs-lookup"><span data-stu-id="57ef7-119">Digits used</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="57ef7-120">阿拉伯文</span><span class="sxs-lookup"><span data-stu-id="57ef7-120">Arabic</span></span></td>
<td><span data-ttu-id="57ef7-121">由右至左</span><span class="sxs-lookup"><span data-stu-id="57ef7-121">Right-to-left</span></span></td>
<td><span data-ttu-id="57ef7-122">阿拉伯文印度語系</span><span class="sxs-lookup"><span data-stu-id="57ef7-122">Arabic-Indic</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="57ef7-123">泰文</span><span class="sxs-lookup"><span data-stu-id="57ef7-123">Thai</span></span></td>
<td><span data-ttu-id="57ef7-124">從左至右</span><span class="sxs-lookup"><span data-stu-id="57ef7-124">Left-to-right</span></span></td>
<td><span data-ttu-id="57ef7-125">泰文數位</span><span class="sxs-lookup"><span data-stu-id="57ef7-125">Thai digits</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="57ef7-126">All others</span><span class="sxs-lookup"><span data-stu-id="57ef7-126">All others</span></span></td>
<td><span data-ttu-id="57ef7-127">任意</span><span class="sxs-lookup"><span data-stu-id="57ef7-127">Any</span></span></td>
<td><span data-ttu-id="57ef7-128">未使用任何替代</span><span class="sxs-lookup"><span data-stu-id="57ef7-128">No substitution used</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="57ef7-129">1</span><span class="sxs-lookup"><span data-stu-id="57ef7-129">1</span></span></td>
<td><span data-ttu-id="57ef7-130">未使用任何替代。</span><span class="sxs-lookup"><span data-stu-id="57ef7-130">No substitution used.</span></span> <span data-ttu-id="57ef7-131">完整的 Unicode 相容性。</span><span class="sxs-lookup"><span data-stu-id="57ef7-131">Full Unicode compatibility.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="57ef7-132">2</span><span class="sxs-lookup"><span data-stu-id="57ef7-132">2</span></span></td>
<td><span data-ttu-id="57ef7-133">原生位數的替代。</span><span class="sxs-lookup"><span data-stu-id="57ef7-133">Native digit substitution.</span></span> <span data-ttu-id="57ef7-134">國家（地區）圖形會根據 LOCALE_SNATIVEDIGITS 來顯示。</span><span class="sxs-lookup"><span data-stu-id="57ef7-134">National shapes are displayed according to LOCALE_SNATIVEDIGITS.</span></span></td>
</tr>
</tbody>
</table>



 

 

 



