---
description: 下列結構支援分散式路由表 (DRT) API 函式。
ms.assetid: 3ff85b24-5ec0-4b26-b30e-1bf8030a575d
title: 分散式路由表結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d454d2c28008422da897dc91ca9a3dc29db374b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983646"
---
# <a name="distributed-routing-table-structures"></a>分散式路由表結構

下列結構支援分散式路由表 (DRT) API 函式。



| 結構                                                  | Description                                                                                                                                                                              |
|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DRT \_ 資料**](/windows/desktop/api/drt/ns-drt-drt_data)                              | 包含資料 blob。 此結構是由數個 DRT 函數所使用。                                                                                                                   |
| [**DRT \_ 註冊**](/windows/desktop/api/drt/ns-drt-drt_registration)              | 包含金鑰註冊。 這是「 [**DRT \_ 搜尋」 \_ 結果**](/windows/desktop/api/drt/ns-drt-drt_search_result) 結構的成員，而且是傳遞給 [**DrtRegisterKey**](/windows/desktop/api/drt/nf-drt-drtregisterkey)的引數。 |
| [**DRT \_ 位址**](/windows/desktop/api/drt/ns-drt-drt_address)                        | 包含參與搜尋之 DRT 節點的相關端點資訊。 這項資訊適用于將連線能力問題進行疑難排解。                                   |
| [**DRT \_ 位址 \_ 清單**](/windows/desktop/api/drt/ns-drt-drt_address_list)             | 包含一組代表在搜尋金鑰期間所聯繫之節點的 [**DRT \_ 位址**](/windows/desktop/api/drt/ns-drt-drt_address) 結構。                                                             |
| [**DRT \_ 安全性 \_ 提供者**](/windows/desktop/api/Drt/ns-drt-drt_security_provider)   | 定義必須由安全性提供者所執行的介面。                                                                                                                   |
| [**DRT \_ 啟動 \_ 程式提供者**](/windows/desktop/api/drt/ns-drt-drt_bootstrap_provider) | 定義啟動載入器提供者必須執行的介面。                                                                                                                  |
| [**DRT \_ 設定**](/windows/desktop/api/drt/ns-drt-drt_settings)                      | 在初始化時定義 DRT 設定。 此結構會作為引數傳遞至 [**DrtOpen**](/windows/desktop/api/drt/nf-drt-drtopen)。                                                                           |
| [**DRT \_ 搜尋 \_ 資訊**](/windows/desktop/api/drt/ns-drt-drt_search_info)               | 定義搜尋查詢。 此結構會作為引數傳遞至 [**DrtStartSearch**](/windows/desktop/api/drt/nf-drt-drtstartsearch)。                                                                             |
| [**DRT \_ 搜尋 \_ 結果**](/windows/desktop/api/drt/ns-drt-drt_search_result)           | 包含搜尋結果。 [**DrtGetSearchResult**](/windows/desktop/api/drt/nf-drt-drtgetsearchresult)會傳回這個結構。                                                                                |
| [**DRT \_ 事件 \_ 資料**](/windows/desktop/api/drt/ns-drt-drt_event_data)                 | 包含在應用程式收到事件信號之後呼叫 [**DrtGetEventData**](/windows/desktop/api/drt/nf-drt-drtgeteventdata) 所傳回的事件資料。                                                    |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[分散式路由表列舉](distributed-routing-table-enumerations.md)
</dt> <dt>

[分散式路由表函數](distributed-routing-table-functions.md)
</dt> <dt>

[分散式路由資料表 API 參考](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 



