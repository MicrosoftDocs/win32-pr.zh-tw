---
description: 計數器演算法計數器類型可能會計算取樣的速率或平均位元組數，或針對特定作業的時間長度。
ms.assetid: 4423e35e-2a93-4f68-8494-89df05268cc9
ms.tgt_platform: multiple
title: 計數器演算法計數器類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5568d4df0d1b50fd55a4f9d007d6506cf59a8f67a05885c21d64a6be8812536c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131430"
---
# <a name="counter-algorithm-counter-types"></a>計數器演算法計數器類型

計數器演算法計數器類型可能會計算取樣的速率或平均位元組數，或針對特定作業的時間長度。

[**Win32 \_ PerfRawData \_ PerfDisk \_ PhysicalDisk**](/previous-versions//aa394308(v=vs.85))類別中的 **AvgDiskBytesPerTransfer** 屬性會使用效能 \_ 平均 \_ 大量 countertype。 在此情況下，傳輸是作業，而傳送的位元組累積數目是計數器資料。 針對任何兩個範例，將累積的位元組差異除以累積傳輸中的差異，將會產生範例之間每次傳輸的平均位元組數。

提供下列計數器演算法：



| CounterType                                                                                              | 描述                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [效能 \_平均 \_ 大量](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))十進位1073874176<br/>       | 在作業期間，平均處理的專案數。 此計數器類型會顯示已處理之專案的比率 (例如傳送的位元組數) 至已完成的作業數，而且需要具有效能平均基底的基底屬性 \_ \_ 做為計數器類型。 |
| [效能 \_計數器 \_ 計數器](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 272696320<br/>     | 取樣間隔的每秒完成的平均作業數。 .                                                                                                                                                                          |
| [效能 \_範例 \_ 計數器](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 4260864<br/>        | 每秒完成的平均作業數。 此計數器類型需要具有性能 \_ 範例基底計數器類型的基底屬性 \_ 。                                                                                                                   |
| [效能 \_計數器 \_ BULK \_ COUNT](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 272696576<br/> | 取樣間隔的每秒完成的平均作業數。 此計數器類型與性能 \_ 計數器 \_ 計數器類型相同，但是使用較大的欄位來容納較大的值。                                                  |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[WMI 效能計數器類型](wmi-performance-counter-types.md)
</dt> </dl>

 

