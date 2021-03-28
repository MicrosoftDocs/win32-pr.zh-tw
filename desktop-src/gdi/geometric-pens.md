---
description: 幾何畫筆的維度是以邏輯單元來指定。
ms.assetid: e7030490-d10c-4d1c-87ae-5b4cc4858ee1
title: 幾何畫筆
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9725f6440f62458d4c87232400f16e27f9b978ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991222"
---
# <a name="geometric-pens"></a>幾何畫筆

幾何畫筆的維度是以邏輯單元來指定。 因此，以幾何畫筆繪製的線條可以調整，也就是它們可能會變得較寬或較窄，視目前的世界轉換而定。 如需有關「世界」轉換的詳細資訊，請參閱 [座標空間和轉換](coordinate-spaces-and-transformations.md)。

除了與裝飾畫筆共用的三個屬性 (寬度、樣式和色彩) 之外，幾何畫筆還具有下列四個屬性：模式、選擇性的影線、結束樣式和聯結樣式。 如需這些屬性的詳細資訊，請參閱 [畫筆屬性](pen-attributes.md)。

若要建立幾何畫筆，應用程式會使用 [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) 函數。 如同裝飾筆， [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) 函式會在應用程式的 DC 中選取幾何畫筆。

 

 



