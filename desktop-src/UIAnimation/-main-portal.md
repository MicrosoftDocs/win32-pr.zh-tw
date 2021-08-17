---
title: Windows動畫管理員
description: Windows 的動畫管理員 (Windows 動畫) 啟用使用者介面元素的豐富動畫。
ms.assetid: 1d840263-d9da-4cab-9bc3-0c143c9c8741
keywords:
- Windows動畫 Windows 動畫，入口網站
- Windows動畫管理員 Windows 動畫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2e6a8f81fbef55525eff04df52a31f8ee942707c354697658ee0ba01647d082
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117755612"
---
# <a name="windows-animation-manager"></a>Windows動畫管理員

## <a name="purpose"></a>目的

Windows 的動畫管理員 (Windows 動畫) 啟用使用者介面元素的豐富動畫。 它的設計目的是簡化將動畫新增至應用程式使用者介面的程式，並讓開發人員能夠執行流暢、自然和互動式的動畫。

動畫架構會管理動畫的排程和執行。 它提供實用數學函式的程式庫，可用於指定一段時間的 UI 元素行為，也可讓開發人員執行提供其他行為的自訂函式。

Windows動畫不會執行轉譯;它可用於任何圖形平台，包括 Direct2D、Direct3D 或 GDI+。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                   | 描述                                                                                                                                       |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [Windows動畫開發指南](windows-animation-developer-guide.md)<br/> | 開發人員指南提供 Windows 動畫的總覽，並提供涵蓋基本動畫工作的範例程式碼。<br/>          |
| [Windows動畫參考](windows-animation-reference.md)<br/>               | 本節所包含的主題會提供 Windows 動畫管理員的參考規格。<br/>                           |
| [Windows動畫範例](windows-animation-samples.md)<br/>                   | 本節所包含的主題會提供支援 Windows 動畫管理員檔的程式碼範例詳細資料。 <br/> |
| [Windows動畫詞彙](-ui-animation-glossary.md)<br/>                     | 本詞彙包含使用 Windows 動畫管理員之開發人員感興趣的詞彙和縮寫。<br/>                               |



 

## <a name="developer-audience"></a>開發人員對象

Windows動畫的設計目的是要讓熟悉 COM、UI 程式設計概念和一般動畫概念的有經驗的 C/c + + 開發人員使用。

## <a name="run-time-requirements"></a>執行階段需求求

Windows 的動畫管理員是在 Windows 7 中引進。

需要 Windows vista Windows 動畫管理員支援的應用程式，可以利用 Windows Vista 的平臺更新。 需要 Windows Vista 平臺更新的應用程式可以 Windows Update 確認是否已安裝，或是下載並安裝在背景中（否則為）。 如需詳細資訊，請參閱[關於 Windows Vista 的平臺更新](../win7ip/platform-update-for-windows-vista-overview.md)。

## <a name="additional-resources"></a>其他資源

-   [Windows Scenic 動畫總覽](https://channel9.msdn.com/blogs/yochay/windows-scenic-animation-overview) (影片) 
-   [在 Windows 7：動畫管理員深入探討和教學](https://channel9.msdn.com/blogs/yochay/inside-windows-7-animation-manager-deep-dive)課程 (影片) 
-   [Windows 動畫- (影片的 Advanced 主題](https://channel9.msdn.com/posts/yochay/Windows-Animation-Advance-Topics/)) 
-   [Windows動畫管理員範例程式碼](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager)

## <a name="related-topics"></a>相關主題

[動畫總覽 (.NET Framework) ](/dotnet/framework/wpf/graphics-multimedia/animation-overview)