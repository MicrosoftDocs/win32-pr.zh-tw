---
description: 圖形裝置介面所維護的七個預先定義的邏輯股票筆刷 (GDI) 。 另外還有21個由視窗管理介面維護的預先定義的邏輯股票筆刷， (使用者) 。
ms.assetid: ddbc6d54-47f6-4810-9d3a-feede80f2bed
title: 股票筆刷
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b50bcd3b6bbd09e1e547d118161f8054fa6df3c6897a57f7928e053e82108d25
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117698167"
---
# <a name="stock-brush"></a>股票筆刷

圖形裝置介面所維護的七個預先定義的邏輯股票筆刷 (GDI) 。 另外還有21個由視窗管理介面維護的預先定義的邏輯股票筆刷， (使用者) 。

下圖顯示使用七項預先定義的股票筆刷繪製的矩形。

![顯示七個方塊的圖例：一個黑色、三個灰色陰影，而三個方塊出現空白](images/csbru-03.png)

應用程式可以藉由呼叫 [**GetStockObject**](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) 函式，並指定筆刷型別，來取得可識別七個股票筆刷之一的控制碼。

視窗管理介面所維護的21個股票筆刷，會對應至視窗專案的色彩，例如功能表、捲軸和按鈕。 應用程式可以藉由呼叫 [**GetSysColorBrush**](/windows/desktop/api/Winuser/nf-winuser-getsyscolorbrush) 函式並指定系統色彩值，取得識別其中一個筆刷的控制碼。 應用程式可以藉由呼叫 [**GetSysColor**](/windows/win32/api/winuser/nf-winuser-getsyscolor) 函式，來取得對應至特定視窗元素的色彩。 應用程式可以藉由呼叫 [**SetSysColors**](/windows/win32/api/winuser/nf-winuser-setsyscolors) 函式來設定對應至視窗元素的色彩。

 

 
