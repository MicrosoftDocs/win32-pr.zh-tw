---
description: Graphics 物件提供 DrawLine、DrawImage 和 DrawString 之類的方法來顯示向量影像、點陣影像和文字。
ms.assetid: 721d0c1c-d105-4d9f-b5e9-6ca407b28c4e
title: 使用圖形容器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80570f3a45c8d67b36f677fc404dcd63581e7938
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972825"
---
# <a name="using-graphics-containers"></a>使用圖形容器

[**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)物件提供 [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint))、 [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint))和 [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush))之類的方法來顯示向量影像、點陣影像和文字。 **圖形** 物件也有數個屬性，會影響所繪製專案的品質和方向。 例如，[平滑模式] 屬性會決定是否要將消除鋸齒套用至線條和曲線，而 [世界轉換] 屬性則會影響繪製之專案的位置和旋轉。

[**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)物件通常會與特定顯示裝置相關聯。 當您在視窗中使用 **圖形** 物件來繪圖時， **圖形** 物件也會與該特定視窗相關聯。

[**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)物件可視為容器，因為它包含一組會影響繪圖的屬性，而且會連結到裝置特定的資訊。 您可以藉由呼叫該 **圖形** 物件的 [BeginContainer](/previous-versions//ms535731(v=vs.85))方法，在現有的 **圖形** 物件內建立次要容器。

下列主題會更詳細地討論 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件和嵌套容器：

-   [圖形物件的狀態](-gdiplus-the-state-of-a-graphics-object-use.md)
-   [巢狀圖形容器](-gdiplus-nested-graphics-containers-use.md)

 

 
