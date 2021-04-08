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
# <a name="dwrite_rendering_mode-enumerations"></a>DWRITE \_ 轉譯 \_ 模式列舉

從 Windows 8 開始， **DWRITE 轉譯 \_ \_ 模式** 列舉新增了新的列舉值，並已取代其他列舉值。

從 Windows 8 開始， [**DWRITE \_ 文字 \_ 消除鋸齒 \_ 模式**](/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_text_antialias_mode) 列舉會決定是否要使用 ClearType 來呈現文字。 因此， **DWRITE 轉譯 \_ \_ 模式** 列舉中的所有 ClearType 轉譯模式都已被取代。 這些列舉值現在對應至新的轉譯模式。

此處的表格顯示舊的列舉值，以及它們所對應的新值。 如需新值的描述，請參閱 [**DWRITE 轉譯 \_ \_ 模式**](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)。



| 舊模式                                                                                | 新模式                                                                                |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**DWRITE \_ 轉譯 \_ 模式 \_ CLEARTYPE \_ GDI \_ 傳統**](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)       | [**DWRITE \_ 轉譯 \_ 模式 \_ GDI \_ 傳統**](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)                  |
| [**DWRITE \_ 轉譯 \_ 模式 \_ CLEARTYPE \_ GDI \_ 自然**](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)       | [**DWRITE \_ 轉譯 \_ 模式 \_ GDI \_ 自然**](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)                  |
| [**DWRITE \_ 轉譯 \_ 模式 \_ CLEARTYPE \_ 自然**](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)            | [**DWRITE \_ 轉譯 \_ 模式 \_ CLEARTYPE \_ 自然**](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)            |
| [**DWRITE \_ 轉譯 \_ 模式 \_ CLEARTYPE \_ 自然 \_ 對稱**](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode) | [**DWRITE \_ 轉譯 \_ 模式 \_ CLEARTYPE \_ 自然 \_ 對稱**](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode) |



 

## <a name="in-this-section"></a>本節內容



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>主題</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode"><strong>DWRITE_RENDERING_MODE (Windows 8 和更新版本) </strong></a><br/></td>
<td>表示轉譯字型的方法。 <br/>
<blockquote>
[!Note]<br />
本主題是關於 Windows 8 和更新版本中 <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode"><strong>DWRITE_RENDERING_MODE</strong></a> 。 如需先前版本的詳細資訊，請參閱 <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode"><strong>本主題</strong></a>。
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode"><strong>DWRITE_RENDERING_MODE</strong></a><br/></td>
<td>表示轉譯字型的方法。 <br/>
<blockquote>
[!Note]<br />
本主題是關於 Windows 8 和更新版本之前 <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode"><strong>DWRITE_RENDERING_MODE</strong></a> 的相關資訊。 如需較新版本的詳細資訊，請參閱 <strong>本主題</strong>。
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

 

 





