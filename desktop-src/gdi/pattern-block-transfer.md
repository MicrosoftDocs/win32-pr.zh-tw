---
description: PatBlt 函式的名稱 (模式區區塊轉送的縮寫) 表示此函式只會在填滿指定的矩形之前，複寫筆刷 (或模式) 。
ms.assetid: 601e1e79-a328-4e63-958a-ca26129e03f8
title: 模式區塊傳輸
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54424348c28b83d1d0d1075072e80b18049546ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991190"
---
# <a name="pattern-block-transfer"></a>模式區塊傳輸

[**PatBlt**](/windows/desktop/api/Wingdi/nf-wingdi-patblt)函式的名稱 (模式區區塊轉送的縮寫) 表示此函式只會在填滿指定的矩形之前，複寫筆刷 (或模式) 。 不過，函式的功能其實更強大。 在複寫筆刷之前，它會使用點陣作業 (ROP) ，將模式的色彩資料與影片顯示器上現有圖元的色彩資料合併。 ROP 是位運算，適用于複寫筆刷的色彩資料位，以及顯示裝置上目標矩形的色彩資料位。 有 256 ROPs;不過， **PatBlt** 函式只會辨識出需要模式和目的地 (不是需要來源) 的函式。 下表指出最常見的 ROPs。



| 人事 登記       | Description                                                                         |
|-----------|-------------------------------------------------------------------------------------|
| PATCOPY   | 將模式複製到目的點陣圖。                                       |
| PATINVERT | 使用布林 XOR 運算子，將目的地點陣圖與模式合併。 |
| DSTINVERT | 反轉目的地點陣圖。                                                     |
| 黑暗 | 將所有輸出變成二進位零。                                                   |
| 白 | 將所有輸出變成二進位檔。                                                    |



 

如需詳細資訊，請參閱 [點陣操作程式碼](raster-operation-codes.md)。

 

 



