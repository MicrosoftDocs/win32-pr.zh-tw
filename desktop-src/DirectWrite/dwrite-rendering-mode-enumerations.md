---
title: DWRITE_RENDERING_MODE 列舉
description: 從 Windows 8 開始，DWRITE 轉譯 \_ \_ 模式列舉新增了新的列舉值，並已取代其他列舉值。
ms.assetid: 3EA568B4-310D-4F70-9530-5916419282E5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7fe2e7961ae4437e84e2327ecd3ea45840c8a0f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468195"
---
# <a name="dwrite_rendering_mode-enumerations"></a>DWRITE \_ 轉譯 \_ 模式列舉

從 Windows 8 開始， **DWRITE 轉譯 \_ \_ 模式** 列舉新增了新的列舉值，並已取代其他列舉值。

從 Windows 8 開始， [**DWRITE \_ 文字 \_ 消除鋸齒 \_ 模式**](/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_text_antialias_mode)列舉會決定是否要使用 ClearType 來呈現文字。 因此， **DWRITE 轉譯 \_ \_ 模式** 列舉中的所有 ClearType 轉譯模式都已被取代。 這些列舉值現在對應至新的轉譯模式。

此處的表格顯示舊的列舉值，以及它們所對應的新值。 如需新值的描述，請參閱 [**DWRITE 轉譯 \_ \_ 模式**](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)。



| 舊模式                                                                                | 新模式                                                                                |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**DWRITE \_ 轉譯 \_ 模式 \_ CLEARTYPE \_ GDI \_ 傳統**](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)       | [**DWRITE \_ 轉譯 \_ 模式 \_ GDI \_ 傳統**](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)                  |
| [**DWRITE \_ 轉譯 \_ 模式 \_ CLEARTYPE \_ GDI \_ 自然**](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)       | [**DWRITE \_ 轉譯 \_ 模式 \_ GDI \_ 自然**](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)                  |
| [**DWRITE \_ 轉譯 \_ 模式 \_ CLEARTYPE \_ 自然**](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)            | [**DWRITE \_ 轉譯 \_ 模式 \_ CLEARTYPE \_ 自然**](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)            |
| [**DWRITE \_ 轉譯 \_ 模式 \_ CLEARTYPE \_ 自然 \_ 對稱**](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode) | [**DWRITE \_ 轉譯 \_ 模式 \_ CLEARTYPE \_ 自然 \_ 對稱**](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode) |



 

## <a name="in-this-section"></a>本節內容




| 主題 | 描述 | 
|-------|-------------|
| <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode"><strong>DWRITE_RENDERING_MODE (Windows 8 和更新版本) </strong></a><br /> | 表示轉譯字型的方法。 <br /><blockquote>[!Note]<br />本主題是關於 Windows 8 和更新版本中<a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode"><strong>DWRITE_RENDERING_MODE</strong></a> 。 如需先前版本的詳細資訊，請參閱 <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode"><strong>本主題</strong></a>。</blockquote><br /> | 
| <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode"><strong>DWRITE_RENDERING_MODE</strong></a><br /> | 表示轉譯字型的方法。 <br /><blockquote>[!Note]<br />本主題是關於 Windows 8 和更新版本之前<a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode"><strong>DWRITE_RENDERING_MODE</strong></a>的相關資訊。 如需較新版本的詳細資訊，請參閱 <strong>本主題</strong>。</blockquote><br /> | 




 

 

 





