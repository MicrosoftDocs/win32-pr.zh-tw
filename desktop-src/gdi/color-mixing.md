---
description: 色彩混合可讓應用程式藉由結合畫筆或筆刷色彩與現有影像中的色彩來建立新的色彩。
ms.assetid: 4a5dff8c-f75f-41d2-8367-33d97d4fd010
title: 色彩混合
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed1adde68360d7050e0cebb6e7d5ac073b36a3c18c3687990c1f2aea6a5719f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105727"
---
# <a name="color-mixing"></a>色彩混合

色彩混合可讓應用程式藉由結合畫筆或筆刷色彩與現有影像中的色彩來建立新的色彩。 應用程式可以選擇繪製畫筆或筆刷色彩， (有效地繪製任何現有的影像) 或混搭色彩與已存在的色彩。

前景混合模式（有時稱為二元點陣運算）會決定如何混合這些色彩。 應用程式可以合併色彩，同時保留兩種色彩的所有元件;遮罩色彩、移除或仲裁不常見的元件;或單獨遮罩色彩，移除或仲裁常見的元件。 這些基本混合作業有幾種變化。

色彩混合會受限於色彩近似值。 如果色彩混合的結果是裝置無法產生的色彩，系統就會使用它可以產生的色彩來接近結果。 如果應用程式混合遞色色彩，則會混合用來建立遞色色彩的個別色彩，且結果會受限於色彩近似值。

應用程式會使用 [**SetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-setrop2) 函數來設定前景混合模式，並使用 [**GetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-getrop2) 函數來抓取目前的模式。

雖然有背景混合模式，但該模式不會控制色彩的混合。 相反地，它會指定繪製樣式線條、影線筆刷和文字時，是否要使用背景色彩。

 

 



