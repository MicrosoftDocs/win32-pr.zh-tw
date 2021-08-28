---
description: 模式 (或自訂) 筆刷是從應用程式定義的點陣圖或與裝置無關的點陣圖 (DIB) 所建立。 下列矩形使用不同的模式筆刷繪製。
ms.assetid: 0de89a6f-d9c7-4f33-8088-c24a48a3ceee
title: 模式筆刷
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d48b7d5f3bc5c4b0fd86eda28a35bb56f02e5ba998353d36d829a71655aa66f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831518"
---
# <a name="pattern-brush"></a>模式筆刷

模式 (或自訂) 筆刷是從應用程式定義的點陣圖或與裝置無關的點陣圖 (DIB) 所建立。 下列矩形使用不同的模式筆刷繪製。

![顯示三個方塊的圖例，每個方塊都以不同的模式填滿](images/csbru-05.png)

若要建立邏輯模式筆刷，應用程式必須先建立點陣圖。 建立點陣圖之後，應用程式可以藉由呼叫 [**CreatePatternBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createpatternbrush) 或 [**CreateDIBPatternBrushPt**](/windows/desktop/api/Wingdi/nf-wingdi-createdibpatternbrushpt) 函式，提供識別點陣圖 (或 DIB) 的控制碼，建立邏輯模式筆刷。 上圖中顯示的筆刷是從單色點陣圖建立。 如需點陣圖、Dib 和建立它們的函式的說明，請參閱 [點陣圖](bitmaps.md)。

 

 



