---
description: 在六種預先定義的對應模式中，一個是裝置相依 (MM \_ 文字) ，其餘五個 (MM \_ HIENGLISH、mm \_ LOENGLISH、MM \_ HIMETRIC、mm \_ LOMETRIC 和 MM \_ 緹) 與裝置無關。
ms.assetid: 722df020-edf2-4763-b58c-3e29fa7007db
title: 預先定義的對應模式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f252f587e98a739306a84450a1d9669ed21873cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972564"
---
# <a name="predefined-mapping-modes"></a>預先定義的對應模式

在六種預先定義的對應模式中，一個是裝置相依 (MM \_ 文字) ，其餘五個 (MM \_ HIENGLISH、mm \_ LOENGLISH、MM \_ HIMETRIC、mm \_ LOMETRIC 和 MM \_ 緹) 與裝置無關。

預設對應模式為 MM \_ TEXT。 一個邏輯單元等於一個圖元。 正 x 向右，正 y 為關閉。 此模式會直接對應至裝置的座標系統。 邏輯到實體的對應只會包含 x 和 y 中由應用程式控制的視窗和視口來源所定義的位移。 此區和視窗範圍全都設定為1，建立一對一的對應。

顯示幾何圖形 (圓形、正方形、多邊形等的應用程式) 使用其中一個裝置獨立的對應模式。 例如，如果您要撰寫應用程式來提供試算表程式的圖表功能，並且想要保證每個圓形圖的直徑都是2英寸，請使用 MM \_ LOENGLISH 對應模式並呼叫適當的函式來繪製和填滿圖表。 指定 MM \_ LOENGLISH 可保證圖表的直徑在任何顯示或印表機上都是一致的。 如果 \_ 使用 mm 文字而不是 mm \_ LOENGLISH，則在 VGA 顯示器上顯示為圓形的圖表會在 EGA 顯示器上顯示為橢圓形，並在 300 DPI (每英寸) 雷射印表機的點上顯示為極小。

 

 



