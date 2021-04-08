---
title: DWRITE_RENDERING_MODE 列舉
description: 從 Windows 8 開始，DWRITE 轉譯 \_ \_ 模式列舉新增了新的列舉值，並已取代其他列舉值。
ms.assetid: 3EA568B4-310D-4F70-9530-5916419282E5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41fa79cf34a03960ddb42a8a80221e99d47be847
ms.sourcegitcommit: d1b8f5ed3d6e35e93cb254efc49428a072d7ef9a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/12/2019
ms.locfileid: "103931782"
---
# <a name="dwrite_rendering_mode-enumerations"></a><span data-ttu-id="da561-103">DWRITE \_ 轉譯 \_ 模式列舉</span><span class="sxs-lookup"><span data-stu-id="da561-103">DWRITE\_RENDERING\_MODE enumerations</span></span>

<span data-ttu-id="da561-104">從 Windows 8 開始， **DWRITE 轉譯 \_ \_ 模式** 列舉新增了新的列舉值，並已取代其他列舉值。</span><span class="sxs-lookup"><span data-stu-id="da561-104">Starting in Windows 8, the **DWRITE\_RENDERING\_MODE** enumeration added new enumeration values and deprecated others.</span></span>

<span data-ttu-id="da561-105">從 Windows 8 開始， [**DWRITE \_ 文字 \_ 消除鋸齒 \_ 模式**](/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_text_antialias_mode) 列舉會決定是否要使用 ClearType 來呈現文字。</span><span class="sxs-lookup"><span data-stu-id="da561-105">Starting in Windows 8, the [**DWRITE\_TEXT\_ANTIALIAS\_MODE**](/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_text_antialias_mode) enumeration determines whether text is rendered using ClearType.</span></span> <span data-ttu-id="da561-106">因此， **DWRITE 轉譯 \_ \_ 模式** 列舉中的所有 ClearType 轉譯模式都已被取代。</span><span class="sxs-lookup"><span data-stu-id="da561-106">As a result, all the ClearType rendering modes in the **DWRITE\_RENDERING\_MODE** enumeration are deprecated.</span></span> <span data-ttu-id="da561-107">這些列舉值現在對應至新的轉譯模式。</span><span class="sxs-lookup"><span data-stu-id="da561-107">These enumeration values now map to new rendering modes.</span></span>

<span data-ttu-id="da561-108">此處的表格顯示舊的列舉值，以及它們所對應的新值。</span><span class="sxs-lookup"><span data-stu-id="da561-108">The table here shows the old enumeration values and the new values they are mapped to.</span></span> <span data-ttu-id="da561-109">如需新值的描述，請參閱 [**DWRITE 轉譯 \_ \_ 模式**](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)。</span><span class="sxs-lookup"><span data-stu-id="da561-109">For descriptions of the new values, see [**DWRITE\_RENDERING\_MODE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode).</span></span>



| <span data-ttu-id="da561-110">舊模式</span><span class="sxs-lookup"><span data-stu-id="da561-110">Old mode</span></span>                                                                                | <span data-ttu-id="da561-111">新模式</span><span class="sxs-lookup"><span data-stu-id="da561-111">New mode</span></span>                                                                                |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="da561-112">**DWRITE \_ 轉譯 \_ 模式 \_ CLEARTYPE \_ GDI \_ 傳統**</span><span class="sxs-lookup"><span data-stu-id="da561-112">**DWRITE\_RENDERING\_MODE\_CLEARTYPE\_GDI\_CLASSIC**</span></span>](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)       | [<span data-ttu-id="da561-113">**DWRITE \_ 轉譯 \_ 模式 \_ GDI \_ 傳統**</span><span class="sxs-lookup"><span data-stu-id="da561-113">**DWRITE\_RENDERING\_MODE\_GDI\_CLASSIC**</span></span>](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)                  |
| [<span data-ttu-id="da561-114">**DWRITE \_ 轉譯 \_ 模式 \_ CLEARTYPE \_ GDI \_ 自然**</span><span class="sxs-lookup"><span data-stu-id="da561-114">**DWRITE\_RENDERING\_MODE\_CLEARTYPE\_GDI\_NATURAL**</span></span>](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)       | [<span data-ttu-id="da561-115">**DWRITE \_ 轉譯 \_ 模式 \_ GDI \_ 自然**</span><span class="sxs-lookup"><span data-stu-id="da561-115">**DWRITE\_RENDERING\_MODE\_GDI\_NATURAL**</span></span>](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)                  |
| [<span data-ttu-id="da561-116">**DWRITE \_ 轉譯 \_ 模式 \_ CLEARTYPE \_ 自然**</span><span class="sxs-lookup"><span data-stu-id="da561-116">**DWRITE\_RENDERING\_MODE\_CLEARTYPE\_NATURAL**</span></span>](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)            | [<span data-ttu-id="da561-117">**DWRITE \_ 轉譯 \_ 模式 \_ CLEARTYPE \_ 自然**</span><span class="sxs-lookup"><span data-stu-id="da561-117">**DWRITE\_RENDERING\_MODE\_CLEARTYPE\_NATURAL**</span></span>](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)            |
| [<span data-ttu-id="da561-118">**DWRITE \_ 轉譯 \_ 模式 \_ CLEARTYPE \_ 自然 \_ 對稱**</span><span class="sxs-lookup"><span data-stu-id="da561-118">**DWRITE\_RENDERING\_MODE\_CLEARTYPE\_NATURAL\_SYMMETRIC**</span></span>](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode) | [<span data-ttu-id="da561-119">**DWRITE \_ 轉譯 \_ 模式 \_ CLEARTYPE \_ 自然 \_ 對稱**</span><span class="sxs-lookup"><span data-stu-id="da561-119">**DWRITE\_RENDERING\_MODE\_CLEARTYPE\_NATURAL\_SYMMETRIC**</span></span>](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode) |



 

## <a name="in-this-section"></a><span data-ttu-id="da561-120">本節內容</span><span class="sxs-lookup"><span data-stu-id="da561-120">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="da561-121">主題</span><span class="sxs-lookup"><span data-stu-id="da561-121">Topic</span></span></th>
<th><span data-ttu-id="da561-122">描述</span><span class="sxs-lookup"><span data-stu-id="da561-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="da561-123"><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode"><strong>DWRITE_RENDERING_MODE (Windows 8 和更新版本) </strong></a></span><span class="sxs-lookup"><span data-stu-id="da561-123"><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode"><strong>DWRITE_RENDERING_MODE (Windows 8 and later)</strong></a></span></span><br/></td>
<td><span data-ttu-id="da561-124">表示轉譯字型的方法。</span><span class="sxs-lookup"><span data-stu-id="da561-124">Represents a method of rendering glyphs.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="da561-125">本主題是關於 Windows 8 和更新版本中 <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode"><strong>DWRITE_RENDERING_MODE</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="da561-125">This topic is about <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode"><strong>DWRITE_RENDERING_MODE</strong></a> in Windows 8 and later.</span></span> <span data-ttu-id="da561-126">如需先前版本的詳細資訊，請參閱 <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode"><strong>本主題</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="da561-126">For info on the previous version see <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode"><strong>this topic</strong></a>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="da561-127"><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode"><strong>DWRITE_RENDERING_MODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="da561-127"><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode"><strong>DWRITE_RENDERING_MODE</strong></a></span></span><br/></td>
<td><span data-ttu-id="da561-128">表示轉譯字型的方法。</span><span class="sxs-lookup"><span data-stu-id="da561-128">Represents a method of rendering glyphs.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="da561-129">本主題是關於 Windows 8 和更新版本之前 <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode"><strong>DWRITE_RENDERING_MODE</strong></a> 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="da561-129">This topic is about <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode"><strong>DWRITE_RENDERING_MODE</strong></a> previous to Windows 8 and later.</span></span> <span data-ttu-id="da561-130">如需較新版本的詳細資訊，請參閱 <strong>本主題</strong>。</span><span class="sxs-lookup"><span data-stu-id="da561-130">For info on the newer version see <strong>this topic</strong>.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

 

 





