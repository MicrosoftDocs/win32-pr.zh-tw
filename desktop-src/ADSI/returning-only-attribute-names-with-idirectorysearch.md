---
title: 使用 >idirectorysearch 只傳回屬性名稱
description: 您可以執行搜尋來判斷特定物件可使用的資料類型。
ms.assetid: 47e78b79-2063-420b-aa41-f4f0c35f87ea
ms.tgt_platform: multiple
keywords:
- 使用 >idirectorysearch ADSI 只傳回屬性名稱
- ADSI、搜尋、>idirectorysearch、其他搜尋選項、只傳回屬性名稱
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4b9c69a99cad0ece5c660ba45954fe537abe69cfa88947b52b0d69d7833b4e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119444008"
---
# <a name="returning-only-attribute-names-with-idirectorysearch"></a>使用 >idirectorysearch 只傳回屬性名稱

您可以執行搜尋來判斷特定物件可使用的資料類型。 在此情況下，您只會對屬性名稱感興趣，而不是物件的屬性值。 **ADS \_ SEARCHPREF \_ \_ 僅 ATTRIBTYPES** 選項會導致伺服器只傳回屬性名稱，而不會傳回屬性值。 不過，結果集會包含已指派值的屬性。 例如，請考慮具有下列屬性的物件：

``` syntax
name = Jeff
sn = Smith
department = Empty
phone = 206-555-0111
```

當設定 **ADS \_ SEARCHPREF \_ \_ 僅 ATTRIBTYPES** 選項時，結果集會包含：

``` syntax
name
sn
department
phone
```

預設值是要傳回的屬性值和名稱。

若只要抓取屬性名稱，請在傳遞至 [**>idirectorysearch：： SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference)方法的 [**ads \_ SEARCHPREF \_ INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info)陣列中，將 [ **\_ \_ \_ 僅限 SEARCHPREF ATTRIBTYPES** ] 搜尋選項設定為 [ **TRUE** ] **ADSTYPE \_ 布林** 值。

下列程式碼範例示範如何只取得屬性名稱。


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_ATTRIBTYPES_ONLY;
SearchPref.vValue.dwType = ADSTYPE_BOOLEAN;
SearchPref.vValue.Boolean = TRUE;
```



如需詳細資訊和示範如何使用 **ADS \_ SEARCHPREF \_ ATTRIBTYPES \_ ONLY** 搜尋選項的程式碼範例，請參閱 [搜尋屬性的範例程式碼](example-code-for-searching-for-attributes.md)。

 

 




