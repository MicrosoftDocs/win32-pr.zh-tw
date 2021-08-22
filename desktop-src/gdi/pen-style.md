---
description: Style 屬性會指定使用特定表面或幾何畫筆時所顯示的線條模式。 預先定義的畫筆樣式有八個。 下圖顯示由系統定義的七個樣式。
ms.assetid: a9aaa999-529c-46e1-9a3f-b6fdcbeb5b51
title: 畫筆樣式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42cc82510c58d36cec76039488ecc13c826609a0870b929f18d82282a87ba8cc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119666508"
---
# <a name="pen-style"></a>畫筆樣式

Style 屬性會指定使用特定表面或幾何畫筆時所顯示的線條模式。 預先定義的畫筆樣式有八個。 下圖顯示由系統定義的七個樣式。

![圖例顯示七行，每個線條使用不同的預先定義樣式繪製](images/cspen-01.png)

內框架樣式與表面畫筆的純色樣式相同。 不過，與幾何畫筆搭配使用時，它的運作方式不同。 如果幾何畫筆的寬度超過單一圖元，而繪圖函式使用畫筆在填滿的物件周圍繪製框線，系統就會在物件的框架內繪製框線。 藉由使用內建的樣式，應用程式可以確保物件完全出現在指定的維度內，無論幾何畫筆的寬度為何。

除了系統所定義的七種樣式之外，還有第八種樣式，也就是使用者 (或應用程式) 定義。 使用者定義樣式會產生具有自訂一連串虛線和點的行。

您可以使用 [**CreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-createpen)、 [**CreatePenIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createpenindirect)或 [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) 函數來建立具有系統定義樣式的畫筆。 您可以使用 **ExtCreatePen** 函式來建立具有使用者定義樣式的畫筆。

 

 



