---
title: 使用者的延伸錯誤資訊
description: 如果有可用的延伸錯誤資訊，參與建立延伸錯誤資訊的元件就必須能夠輕鬆地找出問題。
ms.assetid: 10c54f53-f449-4e7d-ba84-7b000beaee22
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4d2c7a67bb678472fbd3abbf90e0885590c795e2ffc46213a7acbb397da149c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021303"
---
# <a name="extended-error-information-for-the-user"></a>使用者的延伸錯誤資訊

如果有可用的延伸錯誤資訊，參與建立延伸錯誤資訊的元件就必須能夠輕鬆地找出問題。 第一個步驟是檢查最後一個延伸的錯誤記錄，並判斷問題的來源。 這通常是 RPC S 錯誤的原因 \_ \_ \* 。 尋找偵測位置，並判斷此偵測位置的參數是什麼意思。 它們通常表示函式呼叫失敗或特定檢查。 從該處，判斷函數或檢查失敗的原因，並採取更正動作。

最後一筆記錄之前的記錄會指出錯誤抵達的路徑，而且通常會做為例行性檢查，而不是疑難排解程式中的且有助於。

 

 




