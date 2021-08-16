---
title: 使用 >idirectorysearch 進行分頁
description: 分頁會指定伺服器傳回給用戶端的資料列數目。
ms.assetid: cf4aa56a-c6f7-47c8-956d-512a5cffbf22
ms.tgt_platform: multiple
keywords:
- 使用 >idirectorysearch ADSI 進行分頁
- ADSI、搜尋、>idirectorysearch、其他搜尋選項、分頁
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48494c01831e6b69931fc6b6f779ed9b042b7fecaaf17fa62286c094a926ba73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117838938"
---
# <a name="paging-with-idirectorysearch"></a>使用 >idirectorysearch 進行分頁

分頁會指定伺服器傳回給用戶端的資料列數目。 您可以使用資料列數或時間限制來定義頁面。 ADSI COM 物件會根據下表所列的值，抓取每個結果頁面。 當呼叫端到達頁面結尾時，呼叫端會呼叫 [**>idirectorysearch：： GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) ，且 ADSI COM 物件會抓取下一頁。



| 值                                   | 描述                                                                                                                                                                                                                                          |
|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ADS \_ SEARCHPREF \_ PAGESIZE**           | 指定要在頁面中傳回的最大資料列數目。                                                                                                                                                                                            |
| **ADS \_ SEARCHPREF \_ 分頁 \_ 時間 \_ 限制** | 指定伺服器在將頁面傳回至用戶端之前，應該花在收集結果頁面的最長時間（以秒為單位）。 如果達到限制，伺服器會停止搜尋，並傳回已針對頁面取得的資料列。 |



 

如果未設定這些搜尋喜好設定，則預設為不分頁。 在不使用分頁的情況下搜尋 Active Directory，只會傳回前1000筆記錄的最大值，因此，如果結果集有可能包含1000個以上的專案，您就必須使用分頁式搜尋。

搜尋作業可能會導致傳回大量的物件。 如果伺服器在一個集合中傳回結果，它可能會降低用戶端和伺服器的效能，並影響網路負載。 分頁搜尋可用來防止這種情況。 在分頁搜尋中，用戶端可以接受較小封包中的結果。 封包的大小稱為搜尋頁面大小。

分頁搜尋提供用戶端和伺服器的優點。 用戶端可能會在向使用者呈現結果時更具回應性。 這與圖形化使用者介面工具特別相關，這些工具可以在其他執行緒同時接收資料時，開始視窗顯示進程。

在伺服器端，分頁搜尋可讓作業變成可調整的。 例如，如果100用戶端同時發出搜尋要求，且平均每個用戶端都會收到200物件。 如果未指定頁面大小，則在最糟的情況下，伺服器必須有足夠的記憶體來保存20000物件。 相反地，如果每個用戶端指定要做為10個物件的頁面大小，伺服器上的記憶體需求就會降低20倍。

此外，使用分頁搜尋時，用戶端可能會放棄進行中的作業。 相反地，在非分頁的搜尋中，用戶端會接收一個封包中的結果集。 這可能會降低網路效能。

ADSI 會處理用戶端的頁面大小。 用戶端不需要計算正在進行中的物件數目。 ADSI 會封裝用戶端的伺服器互動。 從用戶端的觀點來看，搜尋會傳回完整的結果集。

建議使用分頁。

若要指定最大頁面大小，請將 [ads **\_ SEARCHPREF \_ PAGESIZE** ] 搜尋 **選項 \_ 設定為 [** [**ads \_ SEARCHPREF \_ INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) ] 陣列中的每個頁面最大資料列數，並傳遞至 [**>idirectorysearch：： SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) 方法。

下列程式碼範例顯示如何設定頁面大小上限。


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_PAGESIZE;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = 1000;
```



若要指定頁面時間，請設定 **ads \_ SEARCHPREF \_ 分頁 \_ 時間 \_ 限制** 搜尋選項，並將 **ADSTYPE \_ 整數** 值設定為伺服器在傳遞給 [**>idirectorysearch：： SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference)方法的 [**ADS \_ SEARCHPREF \_ INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info)陣列中，應花費的最大秒數。

下列程式碼範例顯示如何指定頁面時間。


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_PAGED_TIME_LIMIT;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = 60;
```



 

 




