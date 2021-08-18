---
description: 下列列舉支援分散式路由表 (DRT) API。
ms.assetid: 38ce95a0-1603-42c2-8a5e-4370f52c8fc9
title: 分散式路由表列舉
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5ff0a955aed8d6ed6cdf14f3d0e7f6ac2605960123f8008c831dbef5be2da98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011596"
---
# <a name="distributed-routing-table-enumerations"></a>分散式路由表列舉

下列列舉支援分散式路由表 (DRT) API。



| 列舉型別                                                            | 描述                                                                                                                                                           |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DRT \_ 範圍**](/windows/desktop/api/drt/ne-drt-drt_scope)                                        | 定義在使用 [**DrtCreateIpv6UdpTransport**](/windows/desktop/api/drt/nf-drt-drtcreateipv6udptransport)所建立的 ipv6 UDP 傳輸時，將在其中執行的一組 ipv6 範圍。 |
| [**DRT \_ 位址 \_ 旗標**](/windows/desktop/api/drt/ne-drt-drt_address_flags)                       | 定義在執行索引鍵搜尋時，中繼節點可能會傳回的回應集合。                                                         |
| [**DRT \_ 狀態**](/windows/desktop/api/drt/ne-drt-drt_status)                                      | 定義本機節點的可能連接和錯誤狀態。                                                                                                   |
| [**DRT \_ 相符 \_ 類型**](/windows/desktop/api/drt/ne-drt-drt_match_type)                             | 定義執行搜尋時傳回的結果 exactness。                                                                                                 |
| [**DRT \_ LEAFSET \_ 金鑰 \_ 變更 \_ 類型**](/windows/desktop/api/drt/ne-drt-drt_leafset_key_change_type) | 定義可以在本機 DRT 快取的本機分葉集節點上執行的一組變更類型。                                                                |
| [**DRT \_ 事件 \_ 類型**](/windows/desktop/api/drt/ne-drt-drt_event_type)                             | 定義可由 DRT 引發的事件集。                                                                                                              |
| [**DRT \_ 安全性 \_ 模式**](/windows/desktop/api/drt/ne-drt-drt_security_mode)                       | 定義 DRT 可能的安全性模式。 此列舉型別是一種 [**DRT \_ 設定**](/windows/desktop/api/drt/ns-drt-drt_settings) 結構的欄位。                                   |
| [**DRT \_ 註冊 \_ 狀態**](/windows/desktop/api/drt/ne-drt-drt_registration_state)             | 定義已註冊金鑰的狀態。                                                                                                                                |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[分散式路由表結構](distributed-routing-table-structures.md)
</dt> <dt>

[分散式路由表函數](distributed-routing-table-functions.md)
</dt> <dt>

[分散式路由資料表 API 參考](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 



