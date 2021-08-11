---
title: 使用 >idirectorysearch 的大小限制
description: 用戶端可以專注于從伺服器傳回的少數物件，並忽略結果集的其餘部分。
ms.assetid: 55393177-f49b-4163-8e33-2ec24a64b99a
ms.tgt_platform: multiple
keywords:
- '>idirectorysearch ADSI 的大小限制'
- ADSI、搜尋、>idirectorysearch、其他搜尋選項、大小限制
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d6ee4e23cb3014ea92e8510da88767a433b76c0fe73ccbe74bac6ba0bfc1c49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118178743"
---
# <a name="size-limit-with-idirectorysearch"></a>使用 >idirectorysearch 的大小限制

若要減少記憶體需求或其他目的，用戶端可以專注于從伺服器傳回的少量物件，並忽略不感興趣之結果集的其餘部分。 為了達成此目的，用戶端會指定搜尋大小限制和其他適當的搜尋準則。 例如，如果目錄儲存學校學區的測試分數，您可以藉由指定 10 (10) 和遞減排序次序的大小限制，查詢具有最高測試分數的前十名學生。

大小限制的預設值為 [無限制]。 若要設定大小限制，請將 **ads \_ SEARCHPREF \_ 大小 \_ 限制** 搜尋選項設定為 **ADSTYPE \_ 整數** 值，其中包含傳遞給 [**>idirectorysearch：： SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference)方法的 [**ads \_ SEARCHPREF \_ INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info)陣列大小上限。

下列程式碼範例顯示如何設定大小限制。 大小限制值為零，表示沒有大小限制。


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_SIZE_LIMIT;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = 1000;
```



針對 Active Directory，大小限制會指定搜尋所要傳回的物件數目上限。 此外，針對 Active Directory，搜尋所傳回的最大物件數目是1000物件。

 

 




