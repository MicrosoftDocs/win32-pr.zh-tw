---
title: 路由表查詢旗標
description: 將這些常數用於路由器資料表查詢。
ms.assetid: 345a8edc-c2aa-483e-8685-15a692bbfd56
keywords:
- 路由表查詢旗標
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b37ab647efb192e29aae421e02bef1dec065e3b2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840911"
---
# <a name="routing-table-query-flags"></a>路由表查詢旗標

將這些常數用於路由器資料表查詢。



| 常數              | 值      | 描述                                                                |
|-----------------------|------------|----------------------------------------------------------------------------|
| RTM \_ 相符項 \_ 無      | 0x00000000 | 不符合任何準則;系統會傳回目的地的所有路由。 |
| RTM \_ 相符的 \_ 擁有者     | 0x00000001 | 與相同擁有者的路由相符。                                            |
| RTM \_ 相符 \_ NEIGHBOUR | 0x00000002 | 符合相同鄰近的路由。                                     |
| RTM \_ 相符 \_ PREF      | 0x00000004 | 符合具有相同喜好設定的路由。                              |
| RTM \_ 符合 \_ NEXTHOP   | 0x00000008 | 符合具有相同下一個躍點的路由。                                |
| RTM \_ 相符 \_ 介面 | 0x00000010 | 符合相同介面上的路由。                             |
| RTM \_ \_ 完全相符      | 0x0000FFFF | 符合所有準則的路由。                                          |
| RTM \_ 最佳 \_ 通訊協定   | 0          | 傳回路由，不論哪一個通訊協定擁有它。                      |
| RTM \_ 此 \_ 通訊協定   | ~0         | 傳回呼叫通訊協定的最佳路由。                           |



 

 

 




