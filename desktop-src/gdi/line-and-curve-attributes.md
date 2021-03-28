---
description: 裝置內容 (DC) 包含會影響線條和曲線輸出的屬性。 線條和曲線屬性包括目前的位置、筆刷樣式、筆刷色彩、畫筆樣式、畫筆色彩、轉換等等。
ms.assetid: 9529b389-85f6-421f-8429-9b61cee56ef1
title: 線條和曲線屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6ec13ea49a72447045c45ea2837ba40e64e6741
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991198"
---
# <a name="line-and-curve-attributes"></a>線條和曲線屬性

裝置內容 (DC) 包含會影響線條和曲線輸出的屬性。 *線條和曲線屬性* 包括目前的位置、筆刷樣式、筆刷色彩、畫筆樣式、畫筆色彩、轉換等等。

任何 DC 的預設目前位置位於邏輯 (或全球) 空間 (0、0) 。 您可以藉由呼叫 [**MoveToEx**](/windows/desktop/api/Wingdi/nf-wingdi-movetoex) 函式並傳遞一組新的座標，將這些座標設定為新的位置。

> [!Note]  
> 有兩組線條和曲線繪圖函數。 第一個集合會保留 DC 中的目前位置，而第二個集合會改變位置。 您可以藉由檢查函數名稱來識別改變目前位置的函式。 如果函式名稱的結尾是介係詞 "To"，則函式會將目前的位置設為最後一行所繪製的結束點， ([**LineTo**](/windows/desktop/api/Wingdi/nf-wingdi-lineto)、 [**ArcTo**](/windows/desktop/api/Wingdi/nf-wingdi-arcto)、 [**PolylineTo**](/windows/desktop/api/Wingdi/nf-wingdi-polylineto)或 [**PolyBezierTo**](/windows/desktop/api/Wingdi/nf-wingdi-polybezierto)) 。 如果函式名稱結尾不是這個 [**介係詞，它**](/windows/desktop/api/Wingdi/nf-wingdi-polyline)會將目前的位置保持不變 ([**Arc**](/windows/desktop/api/Wingdi/nf-wingdi-arc)、聚合或 [**PolyBezier**](/windows/desktop/api/Wingdi/nf-wingdi-polybezier)) 。

 

預設筆刷是純白色筆刷。 應用程式可以藉由呼叫 [**CreateBrushIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createbrushindirect) 函數來建立新筆刷。 建立筆刷之後，應用程式可以藉由呼叫 [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) 函式來選取它的 DC。 Windows 提供一組完整的函式，可建立、選取及變更應用程式 DC 中的筆刷。 如需這些函式和一般筆刷的詳細資訊，請參閱 [筆刷](brushes.md)。

預設畫筆是表面的實心黑色畫筆，寬度為一個圖元。 應用程式可以使用 [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) 函數來建立畫筆。 建立畫筆之後，您的應用程式可以藉由呼叫 [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) 函式來選取它的 DC。 Windows 提供一組完整的函式，可建立、選取及變更應用程式 DC 中的畫筆。 如需這些函式和一般畫筆的詳細資訊，請參閱 [畫筆](pens.md)。

預設轉換是識別矩陣) 所指定的 unity 轉換 (。 應用程式可以藉由呼叫 [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) 函數來指定新的轉換。 Windows 提供一組完整的函式，藉由改變其寬度、位置和一般外觀來轉換線條和曲線。 如需這些函數的詳細資訊，請參閱 [座標空間和轉換](coordinate-spaces-and-transformations.md)。

 

 



