---
description: 路徑是使用邏輯單元和目前的轉換來定義的。
ms.assetid: a5a426ec-25e8-4fe1-985c-d078227e8aba
title: 路徑的轉換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7561cc1544a49555eaad4d58cf06d29a4763b6cd40528452c68cea551c99af34
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119888998"
---
# <a name="transformations-of-paths"></a>路徑的轉換

路徑是使用邏輯單元和目前的轉換來定義的。  (如果已呼叫 [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) 函式，則邏輯單元為全球單位;否則，邏輯單元為頁面單位。 ) 應用程式可使用世界轉換來調整、旋轉、切變、轉譯和反映定義路徑的線條和貝茲曲線。

> [!Note]  
> 在路徑括弧內的世界轉換，只會影響設定轉換之後繪製的線條和曲線。 它不會影響在設定之前繪製的線條和曲線。 如需世界轉換的說明，請參閱 [座標空間和轉換](coordinate-spaces-and-transformations.md)。

 

如果畫筆是幾何畫筆，應用程式也可以使用 [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) 來概述用來勾勒出路徑的畫筆形狀。 如需幾何畫筆的描述，請參閱 [畫筆](pens.md)。

 

 



