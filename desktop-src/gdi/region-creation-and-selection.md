---
description: 應用程式會藉由呼叫與特定圖形相關聯的函式來建立區域。 下表顯示與每個標準圖形相關聯的函式 () 。
ms.assetid: e94ae371-8365-4e42-ac8c-04c3928fcffb
title: 區域建立和選取
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d27a7887e41a04a62015fa3fc9d82f5beeb01d6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972548"
---
# <a name="region-creation-and-selection"></a>區域建立和選取

應用程式會藉由呼叫與特定圖形相關聯的函式來建立區域。 下表顯示與每個標準圖形相關聯的函式 () 。



| 形狀                                   | 函式                                                                                                                         |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| 矩形區域                      | [**CreateRectRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createrectrgn)、 [**CreateRectRgnIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createrectrgnindirect)、 [**SetRectRgn**](/windows/desktop/api/Wingdi/nf-wingdi-setrectrgn) |
| 具有圓角的矩形區域 | [**CreateRoundRectRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createroundrectrgn)                                                                                 |
| 橢圓形區域                       | [**CreateEllipticRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createellipticrgn)、 [ **CreateEllipticRgnIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createellipticrgnindirect)                   |
| 多邊形區域                        | [**CreatePolygonRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createpolygonrgn)、 [ **CreatePolyPolygonRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createpolypolygonrgn)                               |



 

每個區域建立函數都會傳回識別新區域的控制碼。 應用程式可以使用此控制碼，藉由呼叫 [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) 函式並提供此控制碼作為第二個引數，來選取區域進入裝置內容。 將區域選取至裝置內容之後，應用程式就可以對其執行各種作業。

 

 



