---
description: Time/Date 資料類型具有個別儲存的時間和日期，並使用不帶正負號的整數做為位欄位，如下所示。
ms.assetid: 02c6076e-7f81-489c-9997-1435dec81852
title: 時間/日期
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c3c5cccc2f1211918b52008f0d81a7e4693dfd14766696b77cd184d75f4309d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810738"
---
# <a name="timedate"></a>時間/日期

Time/Date 資料類型具有個別儲存的時間和日期，並使用不帶正負號的整數做為位欄位，如下所示。

## <a name="time"></a>時間

時間會以不帶正負號的2位元組整數編碼，並具有下列位欄位。



| 目錄           | Bits        | 數值範圍 |
|--------------------|-------------|-------------|
| 小時              | 0 1 2 3 4   | 0–23        |
| minutes            | 5 6 7 8 9 A | 0–59        |
| 2秒間隔 | B C D E F   | 0–29        |



 

## <a name="date"></a>日期

日期會以不帶正負號的2位元組整數編碼，並具有下列位欄位。



| 目錄 | Bits          | 數值範圍              |
|----------|---------------|--------------------------|
| year     | 0 1 2 3 4 5 6 | 0– 119 (相對於 1980)  |
| 月    | 7 8 9 A       | 1–12                     |
| day      | B C D E F     | 1–31                     |



 

 

 



