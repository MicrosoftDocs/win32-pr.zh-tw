---
title: Transmit_as 屬性
description: '\ 傳輸 \_ as \ 屬性提供一種方式來控制資料封送處理，而不需要擔心在低層級 \ 郵件上封送處理資料，也就是不需要擔心資料大小或在異類環境中交換的位元組。'
ms.assetid: 04e670c9-b091-457d-aeca-058cf5b664e8
keywords:
- 遠端程序呼叫 RPC、屬性、transmit_as
- transmit_as
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 617422c50bae46de72bac1e548b6f248b19d0cb2436ac0c08b265bbba4f5a6cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120016638"
---
# <a name="the-transmit_as-attribute"></a>傳輸 \_ 為屬性

[ **\[** [**傳輸 \_ 為**](/windows/desktop/Midl/transmit-as)] **\]** 屬性可讓您控制資料封送處理，而不需要擔心較低層級的封送處理資料，也就是不需要擔心資料大小或在異類環境中交換的位元組。 藉由讓您減少透過網路傳輸的資料量，[ **\[ 傳輸 \_ 為 \]** ] 屬性可以讓您的應用程式更有效率。

您可以使用 [ **\[ 傳輸 \_ 為 \]** ] 屬性來指定 RPC 存根將透過網路傳輸的資料類型，而不是使用應用程式所提供的資料類型。 您提供的常式會將資料類型轉換為用於傳輸的型別和型別。 您也必須提供常式來釋出用於資料類型和傳輸類型的記憶體。 例如，下列會將 **xmit \_ 型** 別定義為針對指定為屬於類型 **type \_ 規格** 的所有應用程式資料所傳送的資料類型：

``` syntax
typedef [transmit_as (xmit_type)] type_spec type;
```

下表描述四個程式設計人員提供的常式名稱。 **Type** 是應用程式已知的資料類型，而 **xmit \_ 類型** 是用於傳輸的資料類型。



| 常式傳回的值                                                 | 描述                                                                                                                                     |
|---------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**輸入 \_ 至 \_ xmit**](the-type-to-xmit-function.md)     | 配置傳送型別的物件，並從應用程式類型轉換成透過網路傳送的型別， (呼叫端和稱為) 的物件。 |
| [**\_從 \_ xmit 輸入**](the-type-from-xmit-function.md) | 從傳輸型別轉換為應用程式類型 (呼叫端和稱為) 的物件。                                                                  |
| [**輸入 \_ 免費 \_ inst**](the-type-free-inst-function.md) | 釋出應用程式類型所使用的資源 (只呼叫) 的物件。                                                                              |
| [**輸入 \_ 免費 \_ xmit**](the-type-free-xmit-function.md) | 釋出 **型** 別傳回的儲存空間， _\__ *_以 \_ xmit_* 常式 (呼叫端和稱為) 的物件。                                                      |



 

除了這四個程式設計人員提供的函式以外，應用程式不會操作傳輸的型別。 傳送的類型只定義為透過網路移動資料。 將資料轉換為應用程式所使用的型別之後，會釋出傳輸類型所使用的記憶體。

這些程式設計人員提供的常式是由用戶端或伺服器應用程式根據方向屬性提供。 如果參數為 **\[** [](/windows/desktop/Midl/in) **\]** ，則用戶端會傳送至伺服器。 用戶端必須 **要有型別 \_ 才能 \_ xmit** 和 **輸入 \_ free \_ xmit** 函數。 伺服器需要 **\_ 來自 \_ xmit 的類型** ，並 **輸入 \_ free \_ inst** 函數。 針對 **\[** [**out**](/windows/desktop/Midl/out-idl) **\]** 參數，伺服器會傳送至用戶端。 當用戶端程式必須 **\_ 從 \_ xmit** 函式提供型別時，伺服器應用程式必須將型別實 **\_ \_ xmit** 和 **輸入 \_ free \_ xmit** 函數。 針對暫存 **xmit \_ 型** 別物件，存根會呼叫 **類型** _\__ *_free \_ xmit_* ，以釋出對 **\_ \_ xmit** 的呼叫所配置的任何記憶體。

某些指導方針適用于應用程式類型實例。 如果應用程式類型是指標或包含指標，則 \_ **\_ xmit** 常式的型別必須配置記憶體給指標指向 (應用程式類型物件本身是由存根) 的一般方式來操作。

針對包含 **\[ 傳輸 \_ 為 \]** 屬性之類型的 **\[ out \]** 和 **\[ in、out \] out \]** 參數或其中一個元件，系統 \_ 會自動為具有屬性的資料物件呼叫 **free \_ inst** 常式類型。 對於 **in** 參數，  \_ 只有在將 **\[ \_ \] as** 屬性套用至參數時，才會呼叫 type **free \_ inst** 常式。 如果屬性已套用至參數的元件，則 \_ 不會呼叫類型 **free \_ inst** 常式。 對於內嵌資料和最多一次的呼叫，不會釋出呼叫 (與最上層屬性) （僅限 **in** 參數）相關。

用戶端和伺服器都必須提供這四個函式，才能有效使用 MIDL 2.0。 例如，連結清單可以傳輸為大小的陣列。 **\_ \_ Xmit** 常式的類型會引導連結清單，並將已排序的資料複製到陣列中。 陣列元素已排序，因此不需要傳送與清單結構相關聯的許多指標。 **\_ \_ Xmit** 常式的型別會讀取陣列，並將它的元素放入連結清單結構中。

雙連結清單 (雙重 \_ 連結 \_ 清單) 包含前一個和下一個清單元素的資料和指標：

``` syntax
typedef struct _DOUBLE_LINK_LIST 
{
    short sNumber;
    struct _DOUBLE_LINK_LIST * pNext;
    struct _DOUBLE_LINK_LIST * pPrevious;
} DOUBLE_LINK_LIST;
```

**\[**[**傳輸 \_ as**](/windows/desktop/Midl/transmit-as) **\]** 屬性可以用來透過網路以陣列形式傳送，而不是傳送複雜結構。 陣列中的專案順序會以較低的成本保留清單中元素的順序：

``` syntax
typedef struct _DOUBLE_XMIT_TYPE 
{
    short sSize;
    [size_is(sSize)] short asNumber[];
} DOUBLE_XMIT_TYPE;
```

[ **\[ 傳輸 \_ 為 \]** ] 屬性會出現在 IDL 檔案中：

``` syntax
typedef [transmit_as(DOUBLE_XMIT_TYPE)]  DOUBLE_LINK_LIST DOUBLE_LINK_TYPE;
```

在下列範例中， **ModifyListProc** 會將類型為 DOUBLE 連結類型的參數定義 \_ \_ 為 **\[ in、 \] out** 參數：

``` syntax
void ModifyListProc([in, out] DOUBLE_LINK_TYPE * pHead)
```

四個程式設計人員定義的函式會在函式名稱中使用類型的名稱，並視需要使用所呈現和傳輸的類型作為參數類型：

``` syntax
void __RPC_USER DOUBLE_LINK_TYPE_to_xmit ( 
    DOUBLE_LINK_TYPE __RPC_FAR * pList, 
    DOUBLE_XMIT_TYPE __RPC_FAR * __RPC_FAR * ppArray);

void __RPC_USER DOUBLE_LINK_TYPE_from_xmit ( 
    DOUBLE_XMIT_TYPE __RPC_FAR * pArray,
    DOUBLE_LINK_TYPE __RPC_FAR * pList);

void __RPC_USER DOUBLE_LINK_TYPE_free_inst ( 
    DOUBLE_LINK_TYPE __RPC_FAR * pList);

void __RPC_USER DOUBLE_LINK_TYPE_free_xmit ( 
    DOUBLE_XMIT_TYPE __RPC_FAR * pArray);
```

 

 