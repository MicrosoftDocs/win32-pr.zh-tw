---
description: 中斷隨機鎖定是指將某個用戶端對檔案的鎖定降級的程式，讓另一個用戶端可以開啟檔案，不論是否有無機會鎖定。
ms.assetid: 0356c167-2973-4820-85a9-bc14abcbf163
title: 中斷隨機鎖定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a29b6bd36d8c000b5288ea2408897415547c802
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984712"
---
# <a name="breaking-opportunistic-locks"></a>中斷隨機鎖定

中斷隨機鎖定是指將某個用戶端對檔案的鎖定降級的程式，讓另一個用戶端可以開啟檔案，不論是否有無機會鎖定。 當其他用戶端要求開啟的作業時，伺服器會延遲開啟的作業，並通知用戶端保存隨機鎖定。

持有鎖定的用戶端接著會採取適用于鎖定類型的動作，例如，放棄讀取緩衝區、關閉檔案等等。 只有當擁有隨機鎖定的用戶端通知伺服器完成時，伺服器才會開啟要求開啟作業的用戶端檔案。 不過，當層級2鎖定中斷時，伺服器會向用戶端回報已中斷，但是未等候任何通知，因為沒有快取的資料會排清至伺服器。

在確認任何獨佔鎖定 (篩選、層級1或批次) 的中斷時，中斷鎖定的持有者無法要求另一個獨佔鎖定。 它可能會降低層級2鎖定或完全無鎖定的獨佔鎖定。 當它即將關閉檔案時，預留位置通常會釋放鎖定並關閉檔案。

應用程式會使用與鎖定中斷的檔案相關聯之重 [**迭結構的**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) **hEvent** 成員，來通知應用程式發生中斷。 應用程式也可以使用 [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) 和 [**HasOverlappedIoCompleted**](/windows/desktop/api/winbase/nf-winbase-hasoverlappediocompleted)等函數。

 

 
