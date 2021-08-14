---
title: 適用于更佳介面和方法設計的 IDL 技術
description: 當您開發的 RPC 介面和方法都能處理一致和變化的資料時，請考慮使用下列 IDL 特定技術來改善安全性和效能。
ms.assetid: 651bdb5c-ad56-4526-9b7d-7165141e7ceb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3608e908742d4de4b6564787c6d8faffc29efcef81549ff50414cc7716c468b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118929424"
---
# <a name="idl-techniques-for-better-interface-and-method-design"></a>適用于更佳介面和方法設計的 IDL 技術

當您開發的 RPC 介面和方法都能處理一致和變化的資料時，請考慮使用下列 IDL 特定技術來改善安全性和效能。 本主題所參考的屬性是在方法參數上設定的 IDL 屬性，這些屬性會處理一致的資料 (例如， \[ **大小 \_ 為**， \] 而 \[ **最大值 \_ 為** \] 屬性) 或 variant 資料 (例如， \[ **長度 \_ 為**， \]) 為 \[ **字串** \] 屬性。

## <a name="using-the-range-attribute-with-conformant-data-parameters"></a>使用 \[ \] 具有一致資料參數的範圍屬性

\[**範圍** \] 屬性會指示 RPC 執行時間在資料封送處理常式期間執行額外的大小驗證。 具體而言，它會驗證所提供的資料大小是否以關聯參數形式傳遞至指定的範圍內。

\[**範圍** \] 屬性不會影響電傳格式。

如果網路上的值超出允許的範圍，RPC 將會擲回 RPC \_ x 無效系結 \_ \_ 或 rpc \_ x \_ 錯誤的 \_ 存根 \_ 資料例外狀況。 這可提供額外層級的資料驗證，並且有助於防止常見的安全性錯誤，例如緩衝區溢位。 同樣地，使用 \[ **範圍** \] 可以改善應用程式效能，因為以其標示的一致資料具有明確定義的條件約束，可供 RPC 服務考慮。

## <a name="rpc-server-stub-memory-management-rules"></a>RPC 伺服器 Stub 記憶體管理規則

針對啟用 RPC 的應用程式建立 IDL 檔案時，請務必瞭解 RPC 伺服器 stub 記憶體管理規則。 應用程式可以使用與上述相符的資料搭配使用的範圍，來改善伺服器資源的使用方式，以及刻意 \[  \] 避免將可變長度的資料 IDL 屬性（例如 \[ **長度 \_** ）應用在 \] 符合標準的資料。

不建議將 \[ **長度 \_** 的應用程式 \] 設為 IDL 檔案中定義的資料結構欄位。

## <a name="best-practices-for-variable-length-data-parameters"></a>可變長度資料參數的最佳作法

以下是針對可變大小的資料結構、方法參數和欄位定義 IDL 屬性時，所要考慮的幾個最佳作法。

-   使用早期關聯性。 通常最好是定義變數大小參數或欄位，使其在控制整數型別之後立即發生。

    例如

    ``` syntax
    earlyCorr
    (
    [in, range(MIN_COUNT, MAX_COUNT)] long size, 
    [in,size_is(size)] char *pv
    );
    ```

    勝過

    ``` syntax
    lateCorr
    (
    [in,size_is(size)] char *pv, 
    [in, range(MIN_COUNT, MAX_COUNT)] long size)
    );
    ```

    其中 **earlyCorr** 會在可變長度資料參數的正後方宣告 size 參數，而 **lateCorr** 會在它之後宣告 size 參數。 使用早期對應可改善整體效能，特別是在經常呼叫方法的情況下。

-   針對標記為 out 的參數 \[ **，大小 \_ 為** \] 屬性元組，而且在用戶端上或用戶端具有合理上限的情況下，方法定義在參數屬性和順序方面應該類似下列內容：

    ``` syntax
    outKnownSize
    (
    [in,range(MIN_COUNT, MAX_COUNT)] long lSize,
    [out,size_is(lSize)] UserDataType * pArr
    );
    ```

    在此情況下，用戶端會針對 *pArr* 提供固定大小的緩衝區，讓伺服器端 RPC 服務能夠以良好的保證配置合理大小的緩衝區。 請注意，在此範例中，資料是從伺服器收到 \[ **(的** \]) 。 在 \[) **中** 傳遞給伺服器 (的資料定義類似 \] 。

-   在 RPC 應用程式的伺服器端元件決定資料長度的情況下，方法定義應該如下所示：

    ``` syntax
    typedef [range(MIN_COUNT,MAX_COUNT)] long RANGED_LONG;

    outUnknownSize
    (
    [out] RANGED_LONG *pSize,
    [out,size_is(,*pSize)] UserDataType **ppArr
    );
    ```

    **範圍 \_LONG** 是定義給用戶端和伺服器存根的型別，以及指定的大小，用戶端可以正確預測。 在此範例中，用戶端會將 *ppArr* 傳遞為 **Null**，而且 RPC 伺服器應用程式元件會配置正確的記憶體量。 傳回時，用戶端上的 RPC 服務會為傳回的資料配置記憶體。

-   如果用戶端想要將大型符合標準的陣列子集傳送至伺服器，應用程式可以指定子集的大小，如下列範例所示：

    ``` syntax
    inConformantVaryingArray
    (
    [in,range(MIN_COUNT,MAX_COUNT)] long lSize,
    [in] long lLength, 
    [in,size_is(lSize), length_is(lLength)] UserDataType *pArr
    );
    ```

    如此一來，RPC 就只會在網路上傳輸陣列的 *lLength* 元素。 不過，此定義會強制 RPC 服務在伺服器端配置 *lSize* 大小的記憶體。

-   如果用戶端應用程式元件判斷伺服器可以傳回的陣列大小上限，但允許伺服器傳送該陣列的子集，則應用程式可以藉由定義 IDL 來指定這類行為，如下例所示：

    ``` syntax
    inMaxSizeOutLength
    (
    [in, range(MIN_COUNT, MAX_COUNT)] long lSize,
    [out] long *pLength,
    [out,size_is(lSize), length_is(*pLength)] UserDataType *pArr
    );
    ```

    用戶端應用程式元件會指定陣列的大小上限，而伺服器會指定傳回用戶端的元素數目。

-   如果伺服器應用程式元件需要將字串傳回給用戶端應用程式元件，而且如果用戶端知道要從伺服器傳回的大小上限，則應用程式可以使用符合標準的字串類型，如下列範例所示：

    ``` syntax
    outStringKnownSize
    (
    [in,range(MIN_COUNT, MAX_STRING)] long lSize,
    [out,size_is(lSize),string] wchar_t *pString
    );
    ```

-   如果用戶端應用程式元件不應控制字元串的大小，則 RPC 服務可以特別配置記憶體，如下列範例所示：

    ``` syntax
    outStringUnknownSize
    (
    [out] LPWSTR *ppStr
    );
    ```

    呼叫 RPC 方法時，用戶端應用程式元件必須將 *ppStr* 設定為 **Null** 。

 

 




