---
description: 分散式路由表 (DRT) API 會利用下列功能。
ms.assetid: 1ceff217-d410-47fa-99a2-8588f001859e
title: 分散式路由表函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cd48c3a60f458285ce5f607f9ab6bcf7a557cd9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977918"
---
# <a name="distributed-routing-table-functions"></a>分散式路由表函數

分散式路由表 (DRT) API 會利用下列功能。

## <a name="lifetime-management-functions"></a>存留期管理函數



| 函式                                           | 描述                                                                                                    |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**DrtOpen**](/windows/desktop/api/drt/nf-drt-drtopen)                         | 使用 [**DRT \_ 設定**](/windows/desktop/api/drt/ns-drt-drt_settings) 結構所指定的準則建立本機的 DRT 實例。  |
| [**DrtClose**](/windows/desktop/api/drt/nf-drt-drtclose)                       | 關閉並移除 DRT 的本機實例。                                                              |
| [**DrtGetEventData**](/windows/desktop/api/drt/nf-drt-drtgeteventdata)         | 抓取與訊號事件相關聯的事件資料。                                                         |
| [**DrtGetEventDataSize**](/windows/desktop/api/drt/nf-drt-drtgeteventdatasize) | 傳回與訊號事件相關聯之 [**DRT \_ 事件 \_ 資料**](/windows/desktop/api/drt/ns-drt-drt_event_data) 結構的大小。 |



 

## <a name="module-management-functions"></a>模組管理函式



| 函式                                                                           | 描述                                                                                                                           |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**DrtCreatePnrpBootstrapResolver**](/windows/desktop/api/drt/nf-drt-drtcreatepnrpbootstrapresolver)           | 根據 PNRP 通訊協定建立啟動程式解析程式。                                                                              |
| [**DrtDeletePnrpBootstrapResolver**](/windows/desktop/api/drt/nf-drt-drtdeletepnrpbootstrapresolver)           | 根據 PNRP 通訊協定刪除啟動程式解析程式。                                                                              |
| [**DrtCreateDnsBootstrapResolver**](/windows/desktop/api/drt/nf-drt-drtcreatednsbootstrapresolver)             | 建立啟動載入器提供者，此提供者會依名稱連接已知的主機。                                                             |
| [**DrtDeleteDnsBootstrapResolver**](/windows/desktop/api/drt/nf-drt-drtdeletednsbootstrapresolver)             | 刪除啟動載入器提供者，此提供者會依名稱連接已知的主機。                                                             |
| [**DrtCreateIpv6UdpTransport**](/windows/desktop/api/drt/nf-drt-drtcreateipv6udptransport)                     | 建立以 IPv6 UDP 通訊協定為基礎的傳輸。                                                                                   |
| [**DrtDeleteIpv6UdpTransport**](/windows/desktop/api/drt/nf-drt-drtdeleteipv6udptransport)                     | 刪除以 IPv6 UDP 通訊協定為基礎的傳輸。                                                                                   |
| [**DrtCreateDerivedKeySecurityProvider**](/windows/desktop/api/drt/nf-drt-drtcreatederivedkeysecurityprovider) | 建立適用于 DRT 的衍生金鑰安全性提供者。                                                                                  |
| [**DrtCreateDerivedKey**](/windows/desktop/api/drt/nf-drt-drtcreatederivedkey)                                 | 建立當 DRT 使用衍生金鑰安全性提供者時，可供 [**DrtRegisterKey**](/windows/desktop/api/drt/nf-drt-drtregisterkey) 使用的金鑰。 |
| [**DrtDeleteDerivedKeySecurityProvider**](/windows/desktop/api/drt/nf-drt-drtdeletederivedkeysecurityprovider) | 刪除適用于 DRT 的衍生金鑰安全性提供者。                                                                                  |
| [**DrtCreateNullSecurityProvider**](/windows/desktop/api/drt/nf-drt-drtcreatenullsecurityprovider)             | 建立 null 安全性提供者。 此安全性提供者不需要節點來驗證金鑰。                                 |
| [**DrtDeleteNullSecurityProvider**](/windows/desktop/api/drt/nf-drt-drtdeletenullsecurityprovider)             | 刪除 null 安全性提供者。                                                                                                     |



 

## <a name="registration-functions"></a>註冊函式



| 函式                                     | 描述                                                    |
|----------------------------------------------|----------------------------------------------------------------|
| [**DrtRegisterKey**](/windows/desktop/api/drt/nf-drt-drtregisterkey)     | 在 DRT 中註冊金鑰。                                    |
| [**DrtUpdateKey**](/windows/desktop/api/drt/nf-drt-drtupdatekey)         | 更新與已註冊金鑰相關聯的應用程式資料。 |
| [**DrtUnregisterKey**](/windows/desktop/api/drt/nf-drt-drtunregisterkey) | 從 DRT 取消註冊金鑰。                                |



 

## <a name="search-functions"></a>搜尋函數



| 函式                                                 | 描述                                                                                                                                                                                                             |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DrtStartSearch**](/windows/desktop/api/drt/nf-drt-drtstartsearch)                 | 使用在 [**drt \_ 搜尋 \_ 資訊**](/windows/desktop/api/drt/ns-drt-drt_search_info) 結構中指定的準則，在 drt 中搜尋金鑰。                                                                                                      |
| [**DrtContinueSearch**](/windows/desktop/api/drt/nf-drt-drtcontinuesearch)           | 繼續在 \_ \_ \_ drt 中搜尋金鑰的 drt 搜尋傳回路徑。 只有在相關聯的 [**DRT \_ 搜尋 \_ 資訊**](/windows/desktop/api/drt/ns-drt-drt_search_info)結構中將 **FIterative** 旗標設為 **TRUE** 時，才會使用此函數。 |
| [**DrtGetSearchResult**](/windows/desktop/api/drt/nf-drt-drtgetsearchresult)         | 抓取 (s) 的搜尋結果。                                                                                                                                                                                         |
| [**DrtGetSearchResultSize**](/windows/desktop/api/drt/nf-drt-drtgetsearchresultsize) | 傳回下一個可用搜尋結果的大小。                                                                                                                                                                   |
| [**DrtGetSearchPath**](/windows/desktop/api/drt/nf-drt-drtgetsearchpath)             | 傳回在搜尋作業期間連接的節點清單。                                                                                                                                                          |
| [**DrtGetSearchPathSize**](/windows/desktop/api/drt/nf-drt-drtgetsearchpathsize)     | 傳回搜尋路徑的大小，這表示搜尋作業中使用的節點數目。                                                                                                             |
| [**DrtEndSearch**](/windows/desktop/api/drt/nf-drt-drtendsearch)                     | 取消搜尋在 DRT 中的金鑰，如此一來，透過 [**DRT \_ 搜尋 \_ 結果**](/windows/desktop/api/drt/ns-drt-drt_search_result) 傳回結果的結果就會停止。 您可以在發出搜尋之後的任何時間點呼叫此 API。              |



 

## <a name="instance-name-functions"></a>實例名稱函數



| 函式                                                 | 描述                                                      |
|----------------------------------------------------------|------------------------------------------------------------------|
| [**DrtGetInstanceName**](/windows/desktop/api/drt/nf-drt-drtgetinstancename)         | 取得與 DRT 實例相關聯的名稱。                    |
| [**DrtGetInstanceNameSize**](/windows/desktop/api/drt/nf-drt-drtgetinstancenamesize) | 傳回分散式路由表實例名稱的大小。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[分散式路由表列舉](distributed-routing-table-enumerations.md)
</dt> <dt>

[分散式路由表結構](distributed-routing-table-structures.md)
</dt> <dt>

[分散式路由資料表 API 參考](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 



