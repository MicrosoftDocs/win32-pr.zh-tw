---
description: 數位監視會監視數位的呼叫。
ms.assetid: 6ba28fdf-87d5-4d39-9e12-8201585a86ee
title: 數位監視
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2454f6886bba4e859348df929c1a35f10c3d481
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106966693"
---
# <a name="digit-monitoring"></a>數位監視

數位監視會監視數位的呼叫。 TAPI 允許根據兩種方法 (數位模式) 來發出信號：

-   脈衝位數會以脈衝或旋轉順序發出信號。 在偵測的情況下，這些跳動資訊清單本身就只是可聽見的點擊順序。 有效的脈衝數位為 ' 0 ' 到 ' 9 '。
-   DTMF 數位會以 DTMF (雙色調的多重頻率) 色調來發出信號。 有效的 DTMF 數位為 ' 0 ' 到 ' 9 '、' A '。 ' B '、' C '、' d '、' \* ' 和 ' \# '。 可以監視 DTMF 數位的開頭和下邊緣。

應用程式可以使用 [**lineMonitorDigits**](/windows/desktop/api/Tapi/nf-tapi-linemonitordigits)來啟用或停用指定之呼叫的數位監視。 啟用數位監視時，偵測到的數位會導致應用程式收到 [**行 \_ MONITORDIGITS**](line-monitordigits.md) 訊息的通知。 此訊息提供偵測到數位的呼叫控制碼，以及數位值和數位模式。 數位監視的範圍是由呼叫的存留期所限制。 呼叫 *中斷* 連線或 *閒置* 時，呼叫上的數位監視就會結束。

 

 



