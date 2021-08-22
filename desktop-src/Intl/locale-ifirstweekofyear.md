---
description: 地區設定 \_ IFIRSTWEEKOFYEAR
ms.assetid: 866a28b7-e0b8-4b99-96df-345791a24833
title: LOCALE_IFIRSTWEEKOFYEAR
ms.topic: article
ms.date: 03/04/2020
ms.openlocfilehash: da0d8697e8a02bb6943f4a4154a1ea89c4e01cbaed7576631e3a61d161e80503
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147421"
---
# <a name="locale_ifirstweekofyear"></a>地區設定 \_ IFIRSTWEEKOFYEAR

年度的第一周。



| 值 | 意義                                                                                                                          |
|-------|----------------------------------------------------------------------------------------------------------------------------------|
| 0     | 包含1/1 的周是年度的第一周。 請注意，如果1/1 落在一周的最後一天，這可能是一天。 |
| 1     | 1/1 之後的第一周，是一年的第一周。                                                                     |
| 2     | 第一周至少包含四天，這是年度的第一周。 ISO 8601 相容。                                     |

如果 LOCALE_IFIRSTWEEKOFYEAR 為2，LOCALE_IFIRSTDAYOFWEEK 為 0 (星期一) ，而 LOCALE_ICALENDARTYPE 為西曆，則第一周會遵循 ISO 8601 定義，其中第一周是在第一周的第一個星期四。


 

 

 



