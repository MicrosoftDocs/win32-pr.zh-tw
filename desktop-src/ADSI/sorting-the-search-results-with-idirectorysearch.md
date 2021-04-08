---
title: 使用 >idirectorysearch 排序搜尋結果
description: 依預設，搜尋結果不會以任何保證的順序傳回。 [ADS \_ SEARCHPREF \_ 排序 \_ 依據喜好設定] 會指示伺服器在指定的屬性值上排序結果集，然後再傳回給用戶端。
ms.assetid: 1e44a572-7927-4fd5-a3eb-6dad0760d6e5
ms.tgt_platform: multiple
keywords:
- 使用 >idirectorysearch 排序搜尋結果
- ADSI、搜尋、>idirectorysearch、其他搜尋選項、排序搜尋結果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8433d24b06ac4d361d6520d8af3376ea12acac1f
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103683092"
---
# <a name="sorting-the-search-results-with-idirectorysearch"></a>使用 >idirectorysearch 排序搜尋結果

依預設，搜尋結果不會以任何保證的順序傳回。 [ **ADS \_ SEARCHPREF \_ 排序 \_ 依據** 喜好設定] 會指示伺服器在指定的屬性值上排序結果集，然後再傳回給用戶端。

建議您將索引屬性用於排序。 否則，伺服器必須先取得完整的結果集，並在將任何結果傳送至用戶端之前進行排序。 這也適用于分頁搜尋。 請注意，如果篩選準則包含已編制索引的屬性，且該屬性指定為排序關鍵字，則會增加排序搜尋的效能。在此情況下，Active Directory 可在處理篩選時滿足排序。 例如，一組使用者的有效率排序查詢可能具有包含 (sn>smith) 的篩選準則，以及 sn 的排序關鍵字。

使用 **ADS \_ SEARCHPREF \_ 排序 \_ 依據** 搜尋選項的伺服器端排序，將會降低伺服器的效能。 如果您將執行許多搜尋，請考慮以手動方式在用戶端上排序結果，以降低伺服器上的工作負載。

依預設，會停用結果排序。 若要啟用結果排序，請針對搜尋選項設定 **ads \_ SEARCHPREF \_ 排序 \_** ，其 **ADSTYPE \_ >prov \_ 特定** 會指向 [**Ads \_ SEARCHPREF \_ INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info)陣列中傳遞給 [**>idirectorysearch：： SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference)方法的 [**ads \_ 分類結構**](/windows/desktop/api/Iads/ns-iads-ads_sortkey)。 **ADS 分類 \_** 結構是用來指定要排序的屬性，以及排序的順序。

下列程式碼範例顯示如何啟用結果排序。


```C++
ADS_SORTKEY SortKey;
SortKey.pszAttrType = L"cn";
SortKey.pszReserved = NULL;
SortKey.fReverseorder = FALSE;

ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_SORT_ON;
SearchPref.vValue.dwType = ADSTYPE_PROV_SPECIFIC;
SearchPref.vValue.ProviderSpecific.dwLength = sizeof(SortKey);
SearchPref.vValue.ProviderSpecific.lpValue = (LPBYTE)&SortKey;
```



Active Directory 不支援針對已建立的屬性進行排序，因此無法指定用於排序的結構化屬性。 [**DistinguishedName**](/windows/desktop/ADSchema/a-distinguishedname)屬性也不能用來排序。 Active Directory 也不允許在一個以上的屬性上進行排序，因此 **ads \_ SEARCHPREF \_ 排序 \_ 依據** 搜尋選項只能包含一個 [**ads 分類 \_**](/windows/desktop/api/Iads/ns-iads-ads_sortkey) 結構。

 

 