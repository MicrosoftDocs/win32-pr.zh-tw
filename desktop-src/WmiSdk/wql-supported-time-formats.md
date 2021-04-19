---
description: 描述在 WQL WHERE 子句中支援使用的時間格式。
ms.assetid: d86bd2e3-f5cb-488f-9cd6-5105d82a1842
ms.tgt_platform: multiple
title: WQL-Supported 時間格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58b84d9e37de3529060dc3da6277b2cfb40f7cc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106975030"
---
# <a name="wql-supported-time-formats"></a>WQL-Supported 時間格式

除了 WMI DATETIME 格式之外，還支援下列日期格式以用於 WQL WHERE 子句。



| 格式                                    | 描述                                                                                                                                                                                            |
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| hh \[ \] {AP} M<br/>                   | 以12小時制顯示的小時，以及 AM 或 PM 指定。<br/> 4 PM<br/>                                                                                                             |
| hh:mm<br/>                          | 以冒號分隔的小時和分鐘數。 未指定 AM 或 PM。<br/> 3:23<br/>                                                                                                                  |
| hh： mm \[ \] {AP} M<br/>                | 以冒號分隔的小時和分鐘、選擇性的空格，以及 AM 或 PM 指定。<br/> 上午3:23<br/>                                                                                              |
| hh:mm:ss<br/>                       | 以冒號分隔的小時、分鐘和秒數。 沒有 AM/PM 指定。<br/> 3:23:00<br/>                                                                                                         |
| hh： mm： ss \[ \] {AP} M<br/>             | 以冒號分隔的小時、分鐘和秒、選擇性的空間和 AM/PM 指定。<br/> 3：23：00<br/>                                                                                      |
| hh： mm： ss： uuu<br/>                   | 以冒號分隔的小時、分鐘和秒，以及三位數的位移，表示原始時區偏離 UTC 的分鐘數。<br/>                                    |
| hh： mm： ss： \[ \[ u \] u \] u<br/>           | 以冒號分隔的小時、分鐘和秒數;以及一個、兩個或三位數的位移，表示原始時區偏離 UTC 的分鐘數。<br/>                       |
| hh： mm： ss： uuu \[ \] {AP} M<br/>         | 以冒號分隔的小時、分和秒、三位數的位移，表示原始時區偏離 UTC 和 AM 或 PM 指定的分鐘數。<br/>              |
| hh： mm： ss： \[ \[ u \] u \] u \[ \] {AP} M<br/> | 以冒號分隔的小時、分鐘和秒數;一個、兩個或三位數的位移，表示原始時區偏離 UTC 的分鐘數;和 AM 或 PM 指定。<br/> |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[WHERE 子句](where-clause.md)
</dt> </dl>

 

 




