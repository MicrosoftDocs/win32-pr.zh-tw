---
description: 必須先建立搜尋查詢，應用程式才能在分散式路由表 (的 DRT) 中搜尋。
ms.assetid: b3403a64-128c-461e-9384-8e62c03322e1
title: 搜尋分散式路由表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9016c351412d80b7adb97bc4325dae546e24db68e5737badc311e7c068f1a22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034238"
---
# <a name="searching-a-distributed-routing-table"></a>搜尋分散式路由表

必須先建立搜尋查詢，應用程式才能在分散式路由表 (的 DRT) 中搜尋。 呼叫 [**DrtStartSearch**](/windows/desktop/api/drt/nf-drt-drtstartsearch) 函數時，應用程式會指定所需的索引鍵值。 搜尋的行為是由應用程式在 [**DRT \_ 搜尋 \_ 資訊**](/windows/desktop/api/drt/ns-drt-drt_search_info) 結構中指定的資訊來決定。

一般來說，當搜尋結果和搜尋結束時，會通知應用程式事件。 但是，如果 **fIterative** 是設定在 [ [**DRT \_ 搜尋 \_ 資訊**](/windows/desktop/api/drt/ns-drt-drt_search_info)] 中，當您在每個節點上進行 contact 時，就可以發出應用程式事件的信號。

當事件收到信號之後，應用程式就會針對結果呼叫 [**DrtGetSearchResult**](/windows/desktop/api/drt/nf-drt-drtgetsearchresult) 函式。 如果傳回的程式碼 **為 \_ [確定]**，則會在 API 傳回的 [**DRT \_ 搜尋 \_ 結果**](/windows/desktop/api/drt/ns-drt-drt_search_result) 結構中指向結果。 傳回的結果會落在 [**DRT \_ 搜尋 \_ 資訊**](/windows/desktop/api/drt/ns-drt-drt_search_info)中指定的值範圍內。 如果搜尋找不到任何相符專案，則在結果傳回的結果中，只會傳回「 **DRT \_ E \_ 沒有 \_ 其他** 值」。

下列資訊會詳細說明在 [**drt \_ 搜尋 \_ 資訊**](/windows/desktop/api/drt/ns-drt-drt_search_info) 中包含的成員如何允許應用程式明確地規定 drt 基礎結構的搜尋行為：

## <a name="fallowcurrentinstancematch"></a>fAllowCurrentInstanceMatch

根據預設，DRT 搜尋結果只會包含在本機節點之外找到的相符專案。 設定 **fAllowCurrentInstanceMatch** 會指定搜尋結果也會包含在本機 DRT 實例中找到的相符專案。

## <a name="cmaxendpoints"></a>cMaxEndpoints

搜尋所傳回的結果數量和範圍是由具有 **cMaxEndpoints** (quantity) 和 **pMinimumKey** 和 **pMaximumKey** (範圍) 值的應用程式所指定，並由 [**DRT \_ 搜尋 \_ 資訊**](/windows/desktop/api/drt/ns-drt-drt_search_info)參考。

當 **cMaxEndpoints = 1** 時，drt 基礎結構會搜尋索引鍵，然後在 [ [**DRT \_ 搜尋 \_ 資訊**](/windows/desktop/api/drt/ns-drt-drt_search_info)] 中的 **pMinimumKey** 和 **pMaximumKey** 值所指定的範圍內傳回一個相符項。 此比對可能是完全相符或範圍內最接近的相符項。 如果找不到相符項，則不會再傳回「 **DRT \_ E \_ \_** 」。

如果 **cMaxEndpoints > 1**，則 DRT 基礎結構會傳回範圍內的相符專案，直到 **cMaxEndpoints** 的值為止。 傳回的相符專案可以包含完全相符或範圍內最接近的相符結果。 此外，如果 **pMinimumKey** 和 **pMaximumKey** 設定為相同的值，則只會針對該值執行搜尋，如果找不到，則會傳回不 **\_ \_ 含 \_ 其他的 DRT E** 。

## <a name="fanymatchinrange"></a>fAnyMatchInRange

**FAnyMatchInRange** 成員會指出搜尋是否會在第一個相符範圍位於指定的範圍內時停止，或是如果搜尋將繼續進行最符合 [**DrtStartSearch**](/windows/desktop/api/drt/nf-drt-drtstartsearch) API 中所指定之索引鍵的相符項。 設定 **fAnyMatchInRange** 時，無論在 [**DRT \_ 搜尋 \_ 資訊**](/windows/desktop/api/drt/ns-drt-drt_search_info)中指定的 **cMaxEndpoints** 值為何，都會使用 **cMaxEndpoints = 1** 執行搜尋。

## <a name="fiterative"></a>fIterative

**FIterative** 成員會指定在搜尋期間，由 DRT 基礎結構聯繫的每個節點是否都有與其相關聯的金鑰/端點資料，可透過 [**DRT \_ 搜尋 \_ 結果**](/windows/desktop/api/drt/ns-drt-drt_search_result)提供給應用程式使用。 將 **fIterative** 設為 **TRUE**，就會強制 **cMaxEndpoints = 1** 的值。 當 **fIterative** 在 DRT 的搜尋查詢中設定為 **TRUE** 時，會在與每個節點或「躍點」聯繫之後，將應用程式呼叫回來。 每個躍點結果都包含一個索引鍵，指出 DRT 將在下一個節點搜尋的節點。 躍點結果會透過 [**DrtGetSearchResult**](/windows/desktop/api/drt/nf-drt-drtgetsearchresult) 傳回，以作為 **DRT \_ 相符 \_ 中繼** 結果。

## <a name="pminimumkey-and-pmaximumkey"></a>pMinimumKey 和 pMaximumKey

**PMinimumKey** 和 **pMaximumKey** 成員可以用來搜尋範圍內的索引鍵。 如果 **fAnyMatchInRange** 成員設為 **FALSE**，則會將最接近的 (s) 的金鑰傳回給搜尋目標 (使用 [**DrtStartSearch**](/windows/desktop/api/drt/nf-drt-drtstartsearch) 函數中傳遞的 pKey 引數) 落在範圍內。 請注意，傳遞至 **DrtStartSearch** 的 *pKey* 引數必須落在 **pMinimumKey** 和 **pMaximumKey** 所定義的範圍內。 若要搜尋精確的索引鍵，請將 **pMinimumKey**、 **pMaximumKey** 和 *pKey* 設定為相同的值。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[註冊和取消註冊金鑰](registering-and-deregistering-keys.md)
</dt> <dt>

[關於分散式路由表](about-distributed-routing-tables.md)
</dt> <dt>

[分散式路由資料表 API 參考](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 



