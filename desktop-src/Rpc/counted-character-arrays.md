---
title: 計算的字元陣列
description: '\ Size \_ 為 \ 屬性工作表示陣列的上限，而 \ 的長度 \_ 為 \ 屬性工作表示要傳送的陣列元素數目。'
ms.assetid: bed10259-3034-4be8-91f5-5201c2e19c6b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 360652436a73b445aa2dbb013e0e05145154e20e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463409"
---
# <a name="counted-character-arrays"></a>計算的字元陣列

\[ [Size \_ 為](/windows/desktop/Midl/size-is) \] attribute 指出陣列的上限，而 \[ [length \_ 為](/windows/desktop/Midl/length-is) \] attribute 表示要傳送的陣列元素數目。 除了陣列之外，遠端程式原型還必須包含任何代表長度或大小的變數，這些變數會決定已傳送的陣列元素 (它們可以是不同的參數，或與結構中的字串一起組合) 。 這些屬性可以與寬字元或單一位元組字元陣列搭配使用，就如同使用其他類型的陣列一樣。

本節中的資訊說明字元陣列的遠端過程參數原型。 它分成下列主題：

-   [\[in、out、size \_ 為 \] 原型](-in-out-size-is-prototype.md)
-   [\[在中，大小 \_ 為和輸出，大小 \_ 為 \] 原型](-in-size-is-and-out-size-is-prototype.md)

 

 