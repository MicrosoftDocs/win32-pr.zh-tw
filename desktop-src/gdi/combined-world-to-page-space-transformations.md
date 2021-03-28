---
description: 五個世界對頁轉換可以合併成單一的 3 x 3 矩陣。
ms.assetid: d17ba826-8e8d-4121-8afd-0f256121b54c
title: 結合的世界到頁面空間轉換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b770ef614fe1538a528de640cacc5ad54b28c37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972737"
---
# <a name="combined-world-to-page-space-transformations"></a>結合的世界到頁面空間轉換

五個世界對頁轉換可以合併成單一的 3 x 3 矩陣。 [**CombineTransform**](/windows/desktop/api/Wingdi/nf-wingdi-combinetransform)函式可用來將兩個世界空間與頁面空間的轉換結合在一起。 結合的轉換可用來改變與特定裝置內容相關聯的輸出 (DC) ，方法是呼叫 [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) 函式，並提供此矩陣的元素。 當應用程式呼叫 **SetWorldTransform** 時，它會將 3 x 3 矩陣的元素儲存在 [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) 結構中。 此結構的成員對應至 3 x 3 矩陣的前兩個數據行;矩陣的最後一個資料行不是必要的，因為它的值是常數。

您可以藉由呼叫 [**GetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-getworldtransform) 函式並提供指向 [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) 結構的指標，來恢復目前世界轉換矩陣的元素。

 

 



