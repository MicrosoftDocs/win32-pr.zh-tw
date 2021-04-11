---
title: MIDL 與 Mktyplib.exe 之間的差異
description: MIDL 與 Mktyplib.exe 之間的差異
ms.assetid: 86abd70b-7238-49a6-a996-2c8906a14449
keywords:
- Midl 和 ODL MIDL，MIDL 與 Mktyplib.exe 之間的差異
- Mktyplib.exe MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a54b6103cc230e1c5e6700b0ddc93312c767f9b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104022089"
---
# <a name="differences-between-midl-and-mktyplib"></a>MIDL 與 Mktyplib.exe 之間的差異

> [!Note]  
> Mktyplib.exe 工具已淘汰。 請改用 MIDL 編譯器。

 

MIDL 編譯器與 Mktyplib.exe 有幾個重要區域。 因為 MIDL 的方向比 Mktyplib.exe 更接近 C 語法，所以會發生這些差異。

一般而言，您會想要在 IDL 檔案中使用 MIDL 語法。 但是，如果您需要編譯現有的 ODL 檔案，或維持與 Mktyplib.exe 的相容性，請使用 [**/Mktyplib203**](-mktyplib203.md) midl 編譯器選項強制 MIDL 的行為，就像 Mkktyplib.exe，version 2.03 一樣。  (這是 Mktyplib.exe 工具的最後一個版本。 ) 具體而言， **/mktyplib203** 選項會解決這些差異：

-   複雜資料類型的 typedef 語法

    在 Mktyplib.exe 中，下列兩個定義都會產生 \_ \_ 類型程式庫中 "this struct" 的 TKIND 記錄。 標記「結構標籤」 \_ 是選擇性的，如果已使用，將不會顯示在類型程式庫中。

    ``` syntax
    typedef struct struct_tag { ... } this_struct;
    typedef struct { ... } that_struct;
    ```

    如果省略了選擇性標記，MIDL 將會產生它，有效地將標籤新增至使用者提供的定義。 由於第一個定義具有標記，因此 MIDL 會產生 \_ "this struct" 的 TKIND \_ 記錄和 \_ "this STRUCT" 的 TKIND 別名 \_ (將 "this \_ struct" 定義為 "struct \_ tag" ) 的別名。 因為第二個定義中遺漏了標記，所以 MIDL 會產生對 \_ 使用者而言不具意義之名稱的 TKIND 記錄，以及「該結構」的 TKIND \_ 別名 \_ 。

    這對於在其使用者介面中顯示記錄名稱的類型程式庫瀏覽器有潛在的影響。 如果您預期 TKIND \_ 記錄有實際名稱，則使用者介面可能會出現無法辨識的名稱。 此行為也適用于 [**union**](union.md) 和 [**enum**](enum.md) 定義，而 MIDL 編譯器會分別產生 TKIND 聯集 \_ 和 TKIND 列舉 \_ 。

    MIDL 也允許 C 樣式的 [**結構**](struct.md)、 [**等**](union.md)位和 [**列舉**](enum.md) 定義。 例如，下列定義在 MIDL 中是合法的：

    ``` syntax
    struct my_struct { ... };
    typedef struct my_struct your_struct;
    ```

-   Boolean 資料類型

    在 Mktyplib.exe 中， [**布林值**](boolean.md) 基底類型和 mktyplib.exe 資料類型 BOOL 等於 VT \_ bool，它會對應至 VARIANT \_ bool，且定義為 [**簡短**](short.md)。 在 MIDL 中， **布林值** 基底類型相當於 VT \_ UI1 （定義為不 [**帶正負**](unsigned.md)號的字元），而 BOOL 資料類型定義為 [**long**](long.md)。 如果您在同一個檔案中混搭了 IDL 語法和 ODL 語法，同時仍在嘗試維持與 Mktyplib.exe 的相容性，這會導致問題。 由於資料類型的大小不同，因此封送處理常式代碼不會符合類型資訊中所描述的內容。 如果您想要 \_ 在類型程式庫中使用 VT bool，則應該使用 VARIANT \_ bool 資料類型。

-   標頭檔中的 GUID 定義

    在 Mktyplib.exe 中，Guid 會定義在標頭檔中，並具有可有條件地編譯的宏，以產生 GUID predefinition 或具現化的 GUID。 MIDL 通常會將 GUID predefinitions 放在其產生的標頭檔中，而 GUID 只會在 [**/iid**](-iid.md) 參數所產生的檔案中使用 guid 具現化。

使用 [**/mktyplib203**](-mktyplib203.md) 參數無法解決下列行為差異：

-   區分大小寫

    MIDL 會區分大小寫，而 OLE Automation 則否。

-   列舉宣告中的符號範圍

    在 Mktyplib.exe 中，列舉的符號範圍是本機的。 在 MIDL 中，列舉中的符號範圍是全域的，因為它是在 C 中。例如，下列程式碼會在 Mktyplib.exe 中編譯，但會在 MIDL 中產生重複的名稱錯誤：

    ``` syntax
    typedef struct { ... } a;
    enum {a=1, b=2, c=3};
    ```

-   公用屬性的範圍

    如果您將 [**公用**](public.md) 屬性套用至介面區塊，mktyplib.exe 會將該介面區塊內的每個 typedef 視為公用。 MIDL 要求您明確地將 **公用** 屬性套用至您想要公開的 typedef。

-   Importlib 搜尋順序

    如果您匯入多個類型程式庫，而且這些程式庫包含重複的參考，則 Mktyplib.exe 會使用它所找到的第一個參考來解析此項。 MIDL 會使用它所找到的最後一個參考。 例如，假設有下列 ODL 語法，當您使用 Mktyplib.exe 編譯時，程式庫 C 將會從程式庫 A 使用 MOO typedef，如果您使用 MIDL 進行編譯，則會從程式庫 B 使用 MOO typedef：

    ``` syntax
    [...]library A
    {
        typedef struct tagMOO
        {...}MOO
    }

    [...]library B
    {
        typedef struct tagMOO
        {...} MOO
    }

    [...]library C
    {
        importlib (A.TLB)
        importlib (B.TLB)
        typedef struct tagBAA
        {MOO y;}BAA
    }
    ```

    適當的解決方法是使用正確的匯入程式庫名稱來限定每個這類參考，如下所示：

    ``` syntax
    typedef struct tagBAA
        {A.MOO y;}BAA
    ```

-   無法辨識 VOID 資料類型

    MIDL 可識別 C 語言 [**void**](void.md) 資料類型，而且無法辨識 OLE Automation void 資料類型。 如果您有使用 VOID 的 ODL 檔案，請將此定義放在檔案的頂端：

    ``` syntax
#define VOID void
    ```

-   指數標記法

    MIDL 要求以指數標記法表示的值必須包含在引號中。 例如，"-2.5 E + 3"

-   LCID 值和常數

    在剖析檔案時，MIDL 通常不會考慮 LCID。 若要強制執行此行為的值，或如果您在定義常數時需要使用地區設定特有的標記法，請用引號括住值或常數。

如需詳細資訊，請參閱 [**/mktyplib203**](-mktyplib203.md)、 [**/Iid**](-iid.md)和 [封送處理 OLE 資料類型](marshaling-ole-data-types.md)。

 

 




