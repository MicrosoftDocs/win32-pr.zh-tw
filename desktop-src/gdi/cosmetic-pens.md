---
description: 表面畫筆的維度會以裝置單位來指定。
ms.assetid: d4386681-3523-4872-b048-2a5cfbf7d039
title: 裝飾筆
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbb312ed0b3825397ff79ebc32d363956ad04519
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691911"
---
# <a name="cosmetic-pens"></a>裝飾筆

表面畫筆的維度會以裝置單位來指定。 因此，使用表面畫筆繪製的線條一律具有固定寬度。 使用表面畫筆繪製的線條，通常會比使用幾何畫筆繪製的線條更快繪製3至10倍。 裝飾筆有三個屬性：寬度、樣式和色彩。 如需這些屬性的詳細資訊，請參閱 [畫筆屬性](pen-attributes.md)。

若要建立表面畫筆，請使用 [**CreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-createpen)、 [**CreatePenIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createpenindirect)或 [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) 函數。 若要取出系統所管理的三個內建裝飾筆之一，請使用 [**GetStockObject**](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) 函數。

建立畫筆 (或取得其中一個股票畫筆) 的控制碼之後，請使用 [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) 函式，在應用程式的裝置內容中選取畫筆 (DC) 。 從此時開始，應用程式會在其工作區中使用此畫筆進行任何線條繪圖作業。

 

 



