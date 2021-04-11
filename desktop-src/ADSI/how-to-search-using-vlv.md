---
title: 如何使用 VLV 搜尋
description: Active Directory 支援 (VLV) 搜尋的虛擬清單視圖。 這種搜尋樣式專門針對大型結果集而設計，可讓應用程式顯示上千個專案的子集，而不需要取得每個專案。
ms.assetid: fea04190-0846-4b62-99f4-7d8fb35fd510
ms.tgt_platform: multiple
keywords:
- 如何使用 VLV 搜尋
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f4a24250c8e54ccb7917f86b193152c62810b93
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103933617"
---
# <a name="how-to-search-using-vlv"></a>如何使用 VLV 搜尋

Active Directory 支援 (VLV) 搜尋的虛擬清單視圖。 這種搜尋樣式專門針對大型結果集而設計，可讓應用程式顯示上千個專案的子集，而不需要取得每個專案。

您可以使用兩種不同的方式來使用 VLV 搜尋。 第一個是根據數值位移來取得特定專案的屬性。 當您抓取搜尋結果以回應滾動操作時，此方法很有用。

使用 VLV 搜尋的第二種方式是搜尋部分或全部的文字屬性，並只顯示搜尋的結果。 這是通訊錄的使用範例。 如果使用者輸入 "s"，則應用程式可以使用 VLV 搜尋來搜尋一般名稱開頭為 "s" 的專案。 如果使用者接著將 "m" 新增至 "s"，則應用程式可以使用另一個 VLV 搜尋來搜尋一般名稱開頭為 "sm" 的專案。

若要執行 VLV 搜尋，請指示 ADSI 使用 VLV 控制項。 若要這樣做，請使用 **ADS \_ SEARCHPREF \_ VLV** 搜尋選項（具有 **ADSTYPE \_ >prov 的 \_ 特定** 值）來呼叫 [**>idirectorysearch：： SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference)方法。 **ADSTYPE \_ >prov 的 \_ 特定** 值是 [**ADS \_ VLV**](/windows/desktop/api/Iads/ns-iads-ads_vlv)結構的指標，其中包含搜尋的相關資料。 [**GetVLVItemCount**](example-code-for-using-a-vlv-search.md)範例函式顯示如何設定這兩個搜尋喜好設定。

所有 VLV 搜尋都必須使用伺服器端結果排序，這是透過在搜尋喜好設定 **上設定 ADS \_ SEARCHPREF \_ 排序 \_** 所執行。 如需 **ADS \_ SEARCHPREF \_ 排序 \_** 搜尋喜好設定的詳細資訊，請參閱 [使用 >idirectorysearch 排序搜尋結果](sorting-the-search-results-with-idirectorysearch.md)。

執行 VLV 搜尋時，會透過呼叫 [**>idirectorysearch：： GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) 與 **ADS \_ VLV \_ 回應** 識別碼，在抓取的資料行中傳回特定數量的搜尋中繼資料。 這項資料會包含在 [**ADS \_ VLV**](/windows/desktop/api/Iads/ns-iads-ads_vlv) 結構中。 特別重要的是 **dwContentCount** 與 **lpCoNtextID** 成員。 **DwContentCount** 成員將包含符合 VLV 搜尋準則的結果數目。 這個值可以用來做為搜尋該類型時，所要傳回之專案總數的估計值。 **LpCoNtextID** 成員包含伺服器定義的值，可傳遞給下一個搜尋來識別搜尋。 使用 **lpCoNtextID** 可以增強搜尋效能。 請注意， **lpCoNtextID** 是伺服器定義的值，且其長度會包含在 **dwCoNtextIDLength** 成員中。 呼叫 [**>idirectorysearch：： FreeColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-freecolumn) 方法時，就會釋放這個緩衝區，因此呼叫端必須配置適當大小的緩衝區，然後複製並儲存搜尋之間的緩衝區內容。

如需 LDAP VLV 控制項的詳細資訊，請參閱 [使用 LDAP VLV 控制項來搜尋](/previous-versions/windows/desktop/ldap/searching-with-the-ldap-vlv-control)。

如需詳細資訊，請參閱

-   取得專案數目
-   依位移搜尋
-   依字串搜尋
-   [使用 VLV 搜尋的範例程式碼](example-code-for-using-a-vlv-search.md)

## <a name="obtaining-the-number-of-items"></a>取得專案數目

**若要取得特定搜尋將傳回的專案數估計值，請執行下列步驟。**

1.  以所有零或 **Null** 值填滿 [**ADS \_ VLV**](/windows/desktop/api/Iads/ns-iads-ads_vlv)結構。
2.  使用下列值填滿 [**ADS \_ SEARCHPREF \_ 資訊**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) 。

    -   將 **dwSearchPref** 成員設定為 **ADS \_ SEARCHPREF \_ VLV**。
    -   將 **VValue dwType** 成員設定為 **ADSTYPE \_ >prov \_ 特定** 的成員。
    -   將 **vValue. ProviderSpecific. dwLength** 成員設定為 [**ADS \_ VLV**](/windows/desktop/api/Iads/ns-iads-ads_vlv) 結構的大小。
    -   將 **vValue. ProviderSpecific. lpValue** 成員設為步驟1中 [**ADS \_ VLV**](/windows/desktop/api/Iads/ns-iads-ads_vlv) 結構的位址。

3.  填妥 [**ADS \_**](/windows/desktop/api/Iads/ns-iads-ads_sortkey) 分類結構，如 [使用 >idirectorysearch 排序搜尋結果](sorting-the-search-results-with-idirectorysearch.md) 所示，以針對所需的屬性進行排序。
4.  填寫另一個 [**廣告 \_ SEARCHPREF \_ 資訊**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) ，將 [**ADS \_**](/windows/desktop/api/Iads/ns-iads-ads_sortkey) 分類結構新增至搜尋喜好設定，如 [使用 >idirectorysearch 排序搜尋結果](sorting-the-search-results-with-idirectorysearch.md)所示。
5.  新增任何其他所需的搜尋喜好設定，並呼叫 [**>idirectorysearch：： SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) 來設定搜尋喜好設定。
6.  使用 [**>idirectorysearch：： ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch)執行搜尋。
7.  藉由呼叫 [**>idirectorysearch：： GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow)來取得結果的第一個資料列。
8.  呼叫 [**>idirectorysearch：： GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) 與 **ADS \_ VLV \_ 回應** ，以取得 VLV 搜尋中繼資料。
9.  將 [**ads \_ 搜尋資料 \_ 行**](/windows/desktop/api/Iads/ns-iads-ads_search_column)結構的 **pADsValues->ProviderSpecific** 轉換成 [**ads \_ VLV**](/windows/desktop/api/Iads/ns-iads-ads_vlv)結構指標。 此 **ADS \_ VLV** 結構的 **dwContentCount** 成員會包含搜尋該類型所傳回的大約專案數。
10. 如果將執行相同類型的其他 VLV 搜尋，請複製 **lpCoNtextID** 的資料，並將其保留供下一次 VLV 搜尋之用。

[**GetVLVItemCount**](example-code-for-using-a-vlv-search.md)範例函式示範如何進行此作業。

## <a name="searching-by-offset"></a>依位移搜尋

讓 VLV 搜尋快速搜尋的其中一件事，就是可以依數值位移來搜尋特定的結果。 例如，如果搜尋會導致傳回10000個專案，則 VLV 搜尋可讓您取得大約4072nd 專案的相關資訊，而不需要取得有問題專案的所有專案。

位移會指定為位移和內容計數之間的比率。 比例會很有用，因為伺服器可能無法精確估計清單中的專案數，或清單大小可能會在使用者流覽時變更。 因為您必須指出清單的開頭和結尾，所以您可以在第一個搜尋要求中使用內容計數的估計值，以及位移值。 伺服器會使用這項資料，根據其內容計數的概念，在清單中計算對應的位移，這是透過 [**ADS \_ VLV**](/windows/desktop/api/Iads/ns-iads-ads_vlv)結構的 **dwContentCount** 成員傳送至用戶端的回應。 例如，如果您將清單大小估計為3000，而且您想要讓位移成為清單輸入1500，則會將 **dwContentCount** 設定為3000並 **dwOffset** 為1500。 如果伺服器將實際的清單大小估計為4500，則會將位移重新計算為2250，並在 **dwContentCount** 和 **dwOffset** 中傳回新的估計值。

> [!Note]
>
> VLV 搜尋中的所有數值都是近似值，不應該用於絕對值。 例如，如果您針對比例100中的第50個專案發出 VLV 搜尋，則不保證會取得確切的中間專案。
>
> **若要依位移搜尋特定專案，請執行下列步驟。**
>
> 1.  以下列值填滿 [**ADS \_ VLV**](/windows/desktop/api/Iads/ns-iads-ads_vlv) 結構。 結構的其他成員應設定為零或 **Null**。
>
>     -   將 **dwContentCount** 成員設定為要抓取之專案比例的最大值。
>     -   將 **dwOffset** 成員設定為要取得之專案或專案的比率（相對於 **dwContentCount**）。
>     -   將 **lpCoNtextID** 成員設定為內容識別碼緩衝區複本的位址，並將 **dwCoNtextIDLength** 設定為內容識別碼緩衝區的長度（以位元組為單位）。 如果未儲存任何內容識別碼，則這兩個成員都應該是零或 **Null**。
>
> 2.  設定搜尋喜好設定，如取得專案數目的步驟2到5中所示。
> 3.  使用 [**>idirectorysearch：： ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch)執行搜尋。
> 4.  藉由呼叫 [**>idirectorysearch：： GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow)來取得結果的第一個資料列。
> 5.  使用要抓取的屬性名稱來呼叫 [**>idirectorysearch：： GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) ，以取得所要求專案的實際資料。
> 6.  呼叫 [**>idirectorysearch：： GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) 與 **ADS \_ VLV \_ 回應** ，以取得 VLV 搜尋中繼資料。
> 7.  將 [**ads \_ 搜尋資料 \_ 行**](/windows/desktop/api/Iads/ns-iads-ads_search_column)結構的 **pADsValues->ProviderSpecific** 轉換成 [**ads \_ VLV**](/windows/desktop/api/Iads/ns-iads-ads_vlv)結構指標。
> 8.  製作 **lpCoNtextID** 資料的複本，並將其保留供下一次 VLV 搜尋之用。

 

[**GetVLVItemText**](example-code-for-using-a-vlv-search.md)範例函式示範如何進行此作業。

您也可以使用單一搜尋呼叫來取出多個資料列。 這是在步驟1中，適當地設定 [**ADS \_ VLV**](/windows/desktop/api/Iads/ns-iads-ads_vlv)結構的 **dwBeforeCount** 和 **dwAfterCount** 成員來完成。 **DwBeforeCount** 成員包含有問題專案之前出現在清單中的專案數，而 **dwAfterCount** 成員包含有問題專案之後出現在清單中的專案數。 這兩個計數都會排除專案本身，因此將 **dwBeforeCount** 設定為10，並將 **dwAfterCount** 設定為10，將會導致總共傳回21個專案。 此選項可讓您快取用戶端上的搜尋結果。

## <a name="searching-by-string"></a>依字串搜尋

您也可以使用 VLV 搜尋來尋找具有字串屬性的專案，其值符合全部或部分字串，而不需要取得所有專案。 字串比對會針對 **ads \_ SEARCHPREF \_ SORT \_ ON** 搜尋喜好設定的 [**ads \_**](/windows/desktop/api/Iads/ns-iads-ads_sortkey)排序結構中所指定的屬性來執行。

**若要依字串搜尋特定專案，請執行下列步驟。**

1.  以下列值填滿 [**ADS \_ VLV**](/windows/desktop/api/Iads/ns-iads-ads_vlv) 結構。 結構的其他成員應設定為零或 **Null**。

    -   將 **pszTarget** 成員設定為以 Null 結束的字串指標，其中包含要搜尋的字串。
    -   將 **lpCoNtextID** 成員設定為內容識別碼緩衝區複本的位址，並將 **dwCoNtextIDLength** 設定為內容識別碼緩衝區的長度（以位元組為單位）。 如果未儲存任何內容識別碼，則這兩個成員都應該是零或 **Null**。

2.  設定搜尋喜好設定，如取得專案數目的步驟2到5中所示。
3.  使用 [**>idirectorysearch：： ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch)執行搜尋。
4.  藉由呼叫 [**>idirectorysearch：： GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow)來取得結果的第一個資料列。
5.  使用要抓取的屬性名稱來呼叫 [**>idirectorysearch：： GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) ，以取得所要求專案的實際資料。
6.  呼叫 [**>idirectorysearch：： GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) 與 **ADS \_ VLV \_ 回應** ，以取得 VLV 搜尋中繼資料。
7.  將 [**ads \_ 搜尋資料 \_ 行**](/windows/desktop/api/Iads/ns-iads-ads_search_column)結構的 **pADsValues->ProviderSpecific** 轉換成 [**ads \_ VLV**](/windows/desktop/api/Iads/ns-iads-ads_vlv)結構指標。
8.  製作 **lpCoNtextID** 資料的複本，並將其保留供下一次 VLV 搜尋之用。 如有需要， **dwOffset** 成員會包含第一個專案的索引，其字串屬性以 **pszTarget** 中指定的值開頭。

[**GetVLVItemsByString**](example-code-for-using-a-vlv-search.md)範例函式示範如何進行此作業。

類似于依索引搜尋，也可以使用單一搜尋呼叫來取出多個資料列。 這項作業的完成方式是以同樣的方式設定 [**ADS \_ VLV**](/windows/desktop/api/Iads/ns-iads-ads_vlv)結構的 **dwBeforeCount** 和 **dwAfterCount** 成員。

 

 