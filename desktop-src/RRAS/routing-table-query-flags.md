---
title: 路由表查詢旗標
description: 將這些常數用於路由器資料表查詢。
ms.assetid: 345a8edc-c2aa-483e-8685-15a692bbfd56
keywords:
- 路由表查詢旗標
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 307dd91e9b3d248e5b2b69869ee1e7d14ae17834f7fe57d9e136da16ba3f6b0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117787446"
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



 

 

 




