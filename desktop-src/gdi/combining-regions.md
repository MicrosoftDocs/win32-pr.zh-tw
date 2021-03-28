---
description: 應用程式會藉由呼叫 CombineRgn 函數來合併兩個區域。
ms.assetid: d16f9ca5-33e2-4752-900e-743245838377
title: 結合區域
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f51db22daea448acfb02120844ca2859a5ba11e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104566481"
---
# <a name="combining-regions"></a>結合區域

應用程式會藉由呼叫 [**CombineRgn**](/windows/desktop/api/Wingdi/nf-wingdi-combinergn) 函數來合併兩個區域。 使用這個函式，應用程式可以結合兩個區域的交集部分，除了兩個區域的交集部分、整體的兩個原始區域等等。 以下是定義區域組合的五個值。



| 值     | 意義                                                                               |
|-----------|---------------------------------------------------------------------------------------|
| R G N \_ 和  | 兩個原始區域的交集部分會定義新的區域。                   |
| R G N \_ 複製 | 這兩個原始區域的第一個 (複本) 會定義新的區域。               |
| R G N \_ 差異 | 第一個區域中未與第二個區域相交的部分會定義新的區域。 |
| R G N \_ 或   | 這兩個原始區域會定義新的區域。                                         |
| R G N \_ XOR  | 兩個不重迭的原始區域中的部分會定義新的區域。      |



 

下圖顯示由呼叫 [**CombineRgn**](/windows/desktop/api/Wingdi/nf-wingdi-combinergn)所產生的五個可能的正方形和圓形區域組合。

![示範上表所述之結果的圖例](images/csrgn-02.png)

 

 



