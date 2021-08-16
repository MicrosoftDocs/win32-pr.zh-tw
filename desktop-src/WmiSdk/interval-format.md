---
description: 使用類似日期和時間語法的格式來定義日期時間間隔，方法是將字串分成數天、小時、分鐘、秒和毫秒的欄位。
ms.assetid: 13a3ca74-e3e9-44d7-9254-e288eb70ae4c
ms.tgt_platform: multiple
title: 間隔格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30db455b6b39349b3da2f8328b22597d8b9c16c47387ba7f6b15d81e62ceb134
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118318534"
---
# <a name="interval-format"></a>間隔格式

WMI 會使用類似日期和時間語法的格式來定義日期時間間隔，方法是將字串分成數天、小時、分鐘、秒和微秒的欄位。

下列範例會顯示日期時間間隔的格式。

``` syntax
ddddddddHHMMSS.mmmmmm:000
```

下表列出日期時間間隔的欄位。



| 欄位    | 描述                                                                                                                                                                                                                                  |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| dddddddd | 代表數天 (00000000 到 99999999) 的八位數。                                                                                                                                                                    |
| HH       | 一天中使用24小時制的兩位數小時 (00 到 23) 。                                                                                                                                                                       |
| MM       | 小時的兩位數分鐘 (00 到 59) 。                                                                                                                                                                                                |
| SS       | 分鐘 (00 到 59) 的兩位數秒數。                                                                                                                                                                                   |
| mmmmmm   | 第二個數字的毫秒數， (000000 到 999999) 。 使用此欄位時不需要您的實作為支援評估，但此欄位必須一律存在，以保留字元串的固定長度性質。 |



 

間隔一律具有尾端的 "： 000" 作為最後四個字元。 此外，與日期和時間不同的是，您無法使用星號來指出未使用的欄位。 此外，代表間隔的 [CIM \_ DATETIME](cim-datetime.md) 類型的所有屬性，都必須以 [子類型](standard-wmi-qualifiers.md) 標準辨識符號標示，並將限定詞設定為「間隔」。

下列字串代表1天、12小時、0分鐘和32秒的間隔。

``` syntax
00000001120032.000000:000
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[日期和時間格式](date-and-time-format.md)
</dt> <dt>

[關於 WMI](about-wmi.md)
</dt> <dt>

[CIM \_ DATETIME](cim-datetime.md)
</dt> </dl>

 

 



