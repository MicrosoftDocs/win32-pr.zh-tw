---
title: 伺服器 Stub 記憶體管理
description: 伺服器 Stub 記憶體管理
ms.assetid: 99e3ee56-5adb-4b25-bcf2-316d1bbdbdba
keywords:
- 伺服器 Stub 記憶體管理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6e052df6da999e5371ac498a1d39852b4be2b5e
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/08/2020
ms.locfileid: "103842827"
---
# <a name="server-stub-memory-management"></a>伺服器 Stub 記憶體管理

## <a name="an-introduction-to-server-stub-memory-management"></a>Server-Stub 記憶體管理簡介

MIDL 產生的存根可作為用戶端進程與伺服器進程之間的介面。 用戶端 stub 會封送處理傳遞給以 [**\[ in \]**](../midl/in.md)屬性標記之參數的所有資料，並將它傳送至伺服器 stub。 伺服器 stub （接收此資料時）會重建呼叫堆疊，然後執行對應的使用者執行伺服器函數。 伺服器 stub 也會封送處理以 [**\[ out \]**](../midl/out-idl.md)屬性標記的參數資料，並將其傳回給用戶端應用程式。

MSRPC 使用的32位的封送處理資料格式，是 (NDR) 傳輸語法的網路資料表示的相容版本。 如需此格式的詳細資訊，請參閱 [Open Group 網站](https://www.opengroup.org/)。 針對64位平臺，可使用 Microsoft 64 位延伸模組（稱為 NDR64 的 NDR 傳輸語法）來提升效能。

## <a name="unmarshaling-inbound-data"></a>封送輸入資料

在 MSRPC 中，用戶端 stub 會將標記為 [**\[ 的 \]**](../midl/in.md)所有參數資料封送處理成一個連續緩衝區，以傳輸到伺服器 stub。 同樣地，伺服器存根會將以 [**\[ out \]**](../midl/out-idl.md)屬性標記的所有資料封送處理為傳回用戶端存根的連續緩衝區。 雖然 RPC 底下的網路通訊協定層可以分割和 packetize 緩衝區以進行傳輸，但對 RPC 存根而言，片段是透明的。

建立伺服器呼叫框架的記憶體配置可能是昂貴的作業。 伺服器 stub 會盡可能將不必要的記憶體使用量降到最低，並假設伺服器常式不會釋放或重新配置標示為 [**\[ in \]**](../midl/in.md)或 **\[ in、out \]** 屬性的資料。 伺服器 stub 會嘗試盡可能重複使用緩衝區中的資料，以避免不必要的重複。 一般規則是，如果封送處理的資料格式與記憶體格式相同，RPC 將會使用封送處理資料的指標，而不是針對相同的格式化資料配置額外的記憶體。

例如，下列 RPC 呼叫的定義結構，其封送處理格式與記憶體內部格式相同。

``` syntax
typedef struct RpcStructure
{
    long val;
    long val2;
}

void ProcessRpcStructure
(
    [in]  RpcStructure *plInStructure;
    [out] RpcStructure *plOutStructure;
);
```

在此情況下，RPC 不會為 *plInStructure* 所參考的資料配置額外的記憶體;相反地，它只會將已封送處理的資料指標傳遞至伺服器端函式的執行。 如果使用「-穩固」旗標來編譯存根，則 RPC 伺服器 stub 會在封送處理期間驗證緩衝區 (這是 MIDL 編譯器) 的 nmost 最新版本中的預設設定。 RPC 保證傳遞至伺服器端函式的資料是有效的。

請注意，記憶體會配置給 *plOutStructure*，因為它不會將任何資料傳遞給伺服器。

## <a name="memory-allocation-for-inbound-data"></a>輸入資料的記憶體配置

當伺服器 stub 針對標記為 [**\[ in \]**](../midl/in.md)或 **\[ in、out \]** 屬性的參數資料配置記憶體時，可能會發生案例。 當封送處理的資料格式與記憶體格式不同，或組成封送處理資料的結構相當複雜且必須由 RPC 伺服器 stub 以原子方式讀取時，就會發生這種情況。 以下是幾個常見的情況：必須配置記憶體給伺服器 stub 所收到的資料。

-   資料是不同的陣列或一致的不同陣列。 這些是陣列 (或陣列指標) [**\[ 長度 \_ () \]**](../midl/length-is.md)或優先于其上設定 [**\[ \_ \] ()**](../midl/first-is.md)屬性的陣列。 在 NDR 中，只會封送處理和傳輸這些陣列的第一個元素。 例如，在下列程式碼片段中，傳遞至參數的資料 *pv* 會配置給它的記憶體。

    ``` syntax
    void RpcFunction
    (
        [in] long size,
        [in, out] long *pLength,
        [in, out, size_is(size), length_is(*pLength)] long *pv
    );
    ```

-   資料是大小字串或不符合標準的字串。 這些字串通常是標記為的字元資料指標，其 [**\[ 大小 \_ 為 \] ()**](../midl/size-is.md)屬性。 在下列範例中，傳遞至 **SizedString** 伺服器端函式的字串會配置記憶體，而傳遞至 **NormalString** 函式的字串則會重複使用。

    ``` syntax
    void SizedString
    (
        [in] long size,
        [in, size_is(size), string] char *str
    );

    void NormalString
    (
        [in, string] char str
    );
    ```

-   資料是一種簡單的類型，其記憶體大小與其經過封送處理的大小不同，例如 **enum16** 和 **\_ \_ int3264**。
-   資料是由其記憶體對齊小於自然對齊的結構所定義、包含上述任何一種資料類型，或具有尾端的位元組填補。 例如，下列複雜資料結構具有強制的2位元組對齊，並在結尾處有填補。

    ``` syntax
#pragma pack(2)
    typedef struct ComplexPackedStructure
    {
        char c;  
        long l;   // alignment is forced at the second byte
        char c2;  // there will be a trailing one-byte pad to keep 2-byte alignment
    }
    ```

-   資料包含必須依欄位封送處理欄位的結構。 這些欄位包含在 DCOM 介面中定義的介面指標;忽略的指標;使用 [**\[ 範圍 \]**](../midl/range.md)屬性設定的整數值; 陣列的元素，以連接 [**\[ \_ 封送 \]**](../midl/wire-marshal.md)處理、 [**\[ 使用者 \_ 封送 \]**](../midl/user-marshal.md)處理、 [**\[ 傳輸 \_ 為 \]**](../midl/transmit-as.md)和 [**\[ 表示 \_ 為 \]**](../midl/represent-as.md)屬性，以及內嵌複雜資料結構。
-   資料包含聯集、包含聯集的結構，或等位陣列。 只會在網路上封送處理聯集的特定分支。
-   資料包含具有多維度一致性陣列且至少有一個非固定維度的結構。
-   資料包含複雜結構的陣列。
-   資料包含單一資料型別（例如 **enum16** 和 **\_ \_ int3264**）的陣列。
-   資料包含 ref 和介面指標的陣列。
-   資料有套用至指標的 [**\[ 強制 \_ 配置 \]**](../midl/force-allocate.md)屬性。
-   資料有一個 [**\[ 配置 (所有 \_ 節點 \]**](../midl/allocate.md)套用至指標的) 屬性。
-   資料會將 [**\[ byte \_ count \]**](../midl/byte-count.md)屬性套用至指標。

## <a name="64-bit-data-and-ndr64-transfer-syntax"></a>64位資料和 NDR64 傳輸語法

如先前所述，64位的資料會使用稱為 NDR64 的特定64位傳輸語法進行封送處理。 此傳輸語法的開發目的是要解決在32位的 NDR 下將指標封送處理，並傳輸至64位平臺上的伺服器 stub 時所發生的特定問題。 在此情況下，封送處理的32位資料指標不符合64位，而且一定會發生記憶體配置。 為了在64位平臺上建立更一致的行為，Microsoft 開發了稱為 NDR64 的新傳輸語法。

說明此問題的範例如下所示：


```C++
typedef struct PtrStruct
{
  long l;
  long *pl;
}
```



當封送處理時，這個結構會由32位系統上的伺服器存根重複使用。 但是，如果伺服器 stub 位於64位系統上，則以 NDR 封送處理的資料長度為4個位元組，但所需的記憶體大小將會是8。 如此一來，就會強制執行記憶體配置，而且很少會發生緩衝區重複使用。 NDR64 藉由將指標的封送處理大小設為64位，來解決這個問題。

相較于32位的 NDR，簡單的資料 tyes （例如 **enum16** 和 **\_ \_ int3264** ）不會在 NDR64 下使結構或陣列變得複雜。 同樣地，尾端的填充值也不會讓結構變得複雜。 介面指標會被視為最上層的唯一指標;因此，包含介面指標的結構和陣列不會被視為複雜，也不需要特定的記憶體配置以供其使用。

## <a name="initializing-outbound-data"></a>正在初始化輸出資料

Unmarshalled 所有的輸入資料之後，伺服器 stub 需要初始化以 [**\[ out \]**](../midl/out-idl.md)屬性標記的輸出指標。


```C++
typedef struct RpcStructure
{
    long val;
    long val2;
}

void ProcessRpcStructure
(
    [in]  RpcStructure *plInStructure;
    [out] RpcStructure *plOutStructure;
);
```



在上述呼叫中，伺服器 stub 必須將 *plOutStructure* 初始化，因為封送處理的資料中沒有它，而且它是必須提供給伺服器函數執行的隱含 [**\[ ref \]**](../midl/ref.md)指標。 RPC 伺服器 stub 會初始化和零出具有 [**\[ out \]**](../midl/out-idl.md)屬性的最上層參考指標。 它底下的任何 **\[ out \]** 參考指標也會以遞迴方式初始化。 遞迴會在其上設定 [**\[ unique \]**](../midl/unique.md)或 [**\[ ptr \]**](../midl/ptr.md)屬性的任何指標上停止。

伺服器函式的執行不能直接改變最上層的指標值，因此無法重新配置它們。 例如，在上述 **ProcessRpcStructure** 的執行中，下列程式碼無效：


```C++
void ProcessRpcStructure(RpcStructure *plInStructure, rpcStructure *plOutStructure)
{
    plOutStructure = MIDL_user_allocate(sizeof(RpcStructure));
    Process(plOutStructure);
}
```



*plOutStructure* 是堆疊值，且其變更不會傳播回 RPC。 伺服器函式的執行可以嘗試釋放 *plOutStructure* 來避免配置，這可能會導致記憶體損毀。 然後，伺服器 stub 會在指標對指標的大小寫) 中，為最上層 (指標配置空間，而在堆疊上的大小為最上層的簡單結構，其大小會小於預期。

在特定情況下，用戶端可以指定伺服器端的記憶體配置大小。 在下列範例中，用戶端會在輸入 *大小* 參數中指定輸出資料的大小。

``` syntax
void VariableSizeData
(
    [in] long size,
    [out, size_is(size)] char *pv
);
```

在 unmarshalling 輸入資料（包括 *大小*）後，伺服器 stub 會配置大小為 "sizeof (char) size" 的 *pv* 的緩衝區 \* 。 配置空間之後，伺服器存根會將緩衝區零出。 請注意，在這個特殊情況下，存根會使用 **MIDL \_ 使用者 \_ 配置 () 配置** 記憶體，因為緩衝區的大小是在執行時間決定。

請注意，在 DCOM 介面的情況下，如果用戶端和伺服器共用相同的 COM 單元，或 **ICallFrame** 執行時，MIDL 產生的存根可能完全不會參與。 在此情況下，伺服器無法相依于配置行為，而且需要獨立確認用戶端大小的記憶體。

## <a name="server-side-function-implementations-and-outbound-data-marshaling"></a>伺服器端函數執行和輸出資料封送處理

在輸入資料的 unmarshalling 和配置給包含輸出資料的記憶體初始化之後，RPC 伺服器 stub 會立即執行用戶端所呼叫之函式的伺服器端實作為。 此時，伺服器可以修改特別標示 **\[ in、out \]** 屬性的資料，而且可以填入配置給輸出資料的記憶體 (標記為 [**\[ out \]**](../midl/out-idl.md)) 的資料。

處理已封送處理之參數資料的一般規則很簡單：伺服器只能配置新的記憶體，或修改由伺服器存根特別配置的記憶體。 重新配置或釋放現有記憶體的資料可能會對函式呼叫的結果和效能造成負面影響，而且可能很難進行調試。

邏輯上來說，RPC 伺服器與用戶端位於不同的位址空間，而且通常會假設它們不共用記憶體。 如此一來，伺服器函式的執行就可以安全地使用以 [**\[ in \]**](../midl/in.md)屬性標示的資料做為「暫存」記憶體，而不會影響用戶端記憶體位址。 話雖如此，伺服器應該不會嘗試重新配置或 **\[ 釋放 \] 資料**，而是將這些空間的控制權留給 RPC 伺服器 stub 本身。

一般來說，伺服器函式的執行不需要重新配置或釋放 **\[ 以 in、out \]** 屬性標記的資料。 針對固定大小的資料，函式執行邏輯可以直接修改資料。 同樣地，對於可變大小的資料，函式的執行不能修改提供給大小的域值 [**\[ \_ 是 \] ()**](../midl/size-is.md)屬性。 變更用來將資料大小調整為較小或較大的緩衝區傳回給用戶端的域值，可能無法處理異常長度。

如果發生的情況是伺服器常式必須重新配置標示為 **\[ in、out \]** 屬性的資料所使用的記憶體，則伺服器端函式的執行方式可能不知道存根提供的指標是否為使用 **MIDL \_ 使用者 \_ 配置 ()** 或封送處理的網路緩衝區所配置的記憶體。 若要解決這個問題，MS RPC 可以確保在資料上設定 [**\[ force \_ allocate \]**](../midl/force-allocate.md)屬性時，不會發生記憶體遺漏或損毀。 設定 **\[ 強制 \_ 配置 \]** 時，伺服器 stub 一律會配置指標的記憶體，但要注意的是，每次使用時，效能會降低。

當呼叫從伺服器端函式執行傳回時，伺服器存根會將標記為 [**\[ out \]**](../midl/out-idl.md)屬性的資料封送處理，並傳送至用戶端。 請注意，如果伺服器端函數的執行擲回例外狀況，則存根不會封送處理資料。

## <a name="releasing-allocated-memory"></a>釋放配置的記憶體

從伺服器端函式傳回呼叫之後，RPC 伺服器 stub 會釋放堆疊記憶體，不論是否發生例外狀況。 伺服器 stub 會釋放存根所配置的所有記憶體，以及任何使用 **MIDL \_ 使用者 \_ 配置 () 配置** 的記憶體。 伺服器端函式的執行必須一律讓 RPC 成為一致的狀態，方法是擲回例外狀況或傳回錯誤碼。 如果函式在擴展複雜的資料結構期間失敗，則必須確保所有指標都指向有效的資料，或設定為 **Null**。

在這個階段中，伺服器 stub 會釋出不屬於封送處理之緩衝區（包含 [**\[ in \]**](../midl/in.md)資料）的所有記憶體。 這種行為的唯一例外狀況是具有 [**\[ 配置 (不 \_ \]**](../midl/allocate.md)會在其上設定) 屬性的資料-伺服器 stub 不會釋放與這些指標相關聯的任何記憶體。

在伺服器 stub 釋出 stub 和函式執行所配置的記憶體之後，如果特定資料指定了 [**\[ 通知 \_ 旗 \]**](../midl/notify-flag.md)標屬性，存根就會呼叫特定的通知函數。

## <a name="marshalling-a-linked-list-over-rpc----an-example"></a>透過 RPC 封送處理連結清單--範例


```C++
typedef struct _LINKEDLIST
{
    long lSize;
    [size_is(lSize)] char *pData;
    struct _LINKEDLIST *pNext;
} LINKEDLIST, *PLINKEDLIST;

void Test
(
    [in] LINKEDLIST *pIn,
    [in, out] PLINKEDLIST *pInOut,
    [out] LINKEDLIST *pOut
);
```



在上述範例中， **LINKEDLIST** 的記憶體格式將與封送的電傳格式相同。 如此一來，伺服器存根就不會為 *pIn* 下的整個資料指標鏈配置記憶體。 相反地，RPC 會針對整個連結清單重複使用網路緩衝區。 同樣地，存根不會配置 *針腳* 的記憶體，而是會重複使用用戶端所封送的網路緩衝區。

因為函式簽章包含輸出參數 *不悅*，所以伺服器 stub 會配置記憶體以包含傳回的資料。 配置的記憶體一開始會是零，且 **pNext** 設定為 **Null**。 應用程式可以為新的連結清單配置記憶體，並將 *不悅* -> **pNext** 至該連結清單。 *釘* 選和其包含的連結清單可以用來做為臨時區域，但應用程式不應該變更任何 pNext 指標。

應用程式可以自由變更接腳所指向之連結清單的內容，但它不能變更任何 **pNext** *指標，而* 只讓最上層連結本身。 如果應用程式決定縮短連結清單，它就無法得知是否有任何指定的 **pNext** 指標連結為了 RPC 內部緩衝區，或是特別以 **MIDL \_ 使用者 \_ 配置 () 配置** 的緩衝區。 若要解決這個問題，您可以針對會強制使用者配置的連結清單指標新增特定類型宣告，如下列程式碼所示。

``` syntax
typedef [force_allocate] PLINKEDLIST;
```

這個屬性會強制服務器 stub 個別配置連結清單的每個節點，而且應用程式可以呼叫 **MIDL \_ 使用者 \_ free ()**，釋放連結清單的縮寫部分。 然後，應用程式可以安全地將新縮短連結清單結尾的 **pNext** 指標設定為 **Null**。

 

 