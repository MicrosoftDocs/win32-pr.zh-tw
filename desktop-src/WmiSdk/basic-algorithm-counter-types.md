---
description: 表示一段時間內樣本之間的差異，而且通常會使用基底值進行計算。
ms.assetid: 613268ab-386b-421d-a5b5-aab6a065999c
ms.tgt_platform: multiple
title: 基本演算法計數器類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70514c10b2695aa940d48341752ef647dcca9719
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979979"
---
# <a name="basic-algorithm-counter-types"></a>基本演算法計數器類型

基本演算法計數器類型通常代表一段時間內樣本之間的差異，而且通常會使用基底值進行計算。 例如， [**Win32 \_ PerfFormattedData \_ PerfDisk \_ PhysicalDisk**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data)類別的 **PercentFreeSpace** 屬性代表實體磁片單元上可用空間的比率，以及所選實體磁片磁碟機所提供的總可用空間。 這個類別也包含基底值 **PercentFreeSpace \_ base**。 將 **PercentFreeSpace** 除以 **PercentFreeSpace \_ Base** 並乘以100%，可取得可用磁碟空間的百分比。

提供下表中的基本演算法。



| CounterType 常數                                                                                    | Description                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [效能 \_原始 \_ 分數](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))小數537003008<br/>       | 子集與其集合的比率（以百分比表示）。 此計數器類型只會顯示目前的百分比，而不會顯示一段時間的平均值。                                    |
| [效能 \_樣本 \_ 分數](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))小數549585920<br/>    | 最後兩個取樣間隔期間，對所有作業的平均點擊率。 此計數器類型需要具有效能 \_ 範例 \_ 基底計數器類型的基底屬性。 |
| [效能 \_計數器 \_ DELTA](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 4195328<br/>        | 此計數器型別顯示最近兩次取樣間隔間之測量屬性 (Attribute) 的變更                                                          |
| [效能 \_計數器 \_ 大型 \_ DELTA](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 4195584<br/> | 與性能 \_ 計數器 DELTA 相同， \_ 但針對較大的值是64位表示。                                                                                        |
| [效能 \_經過 \_ 時間](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))十進位807666944<br/>       | 進程開始的時間與計算此值的時間之間的總時間。                                                                            |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[WMI 效能計數器類型](wmi-performance-counter-types.md)
</dt> </dl>

 

