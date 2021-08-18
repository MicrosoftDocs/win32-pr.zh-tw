---
title: 'union 關鍵字 (RPC) '
description: 等位需要特殊的 MIDL 關鍵字，以支援其與遠端程序呼叫 (RPC) 的使用。
ms.assetid: e7c8296c-893d-4df7-913a-f969733e1917
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fde18cca09f4db81af8eada2ae102a1bea373ed7859b3a7fc2bb9637f28d584
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011006"
---
# <a name="union-keyword-rpc"></a>union 關鍵字 (RPC) 

C 語言的某些功能（例如等位）需要特殊的 MIDL 關鍵字，才能支援在遠端程序呼叫中使用。 C 語言中的等位是一個變數，可保存不同類型和大小的物件。 開發人員通常會建立一個變數，以追蹤儲存在等位中的類型。 若要在分散式環境中正確運作，表示聯集類型或 *判別* 的變數也必須可供遠端電腦使用。 MIDL 提供 \[ [**switch \_ 型**](/windows/desktop/Midl/switch-type)別 \] ，而 \[ [**參數 \_ 則是**](/windows/desktop/Midl/switch-is)用 \] 來識別判別型別和名稱的關鍵字。

MIDL 需要以兩種方式之一，以聯集傳輸判別：

-   Union 和判別必須提供為參數。
-   Union 和判別必須封裝在結構中。

MIDL： [**nonencapsulated \_ union**](/windows/desktop/Midl/nonencapsulated-unions) 和 [**封裝聯 \_ 集**](/windows/desktop/Midl/encapsulated-unions)提供兩種基本類型的區分等位。 如果聯集是參數，nonencapsulated 聯集的判別就是另一個參數。 如果等位是結構的欄位，則它是另一個欄位。 封裝聯集的定義會轉換成結構定義，其第一個欄位為判別，而第二個和最後一個欄位為聯集。 下列範例示範如何提供 union 和判別作為參數：

``` syntax
typedef [switch_type(short)] union 
{
    [case(0)]    short     sVal;
    [case(1)]    float     fVal;
    [case(2)]    char      chVal;
    [default]    ;
} DISCRIM_UNION_PARAM_TYPE;
 
short UnionParamProc(
    [in, switch_is(sUtype)] DISCRIM_UNION_PARAM_TYPE Union,
    [in] short sUtype);
```

上述範例中的聯集可以包含單一值： **short**、 **float** 或 **char**。 Union 的型別定義包含 MIDL **switch \_ type** 屬性（attribute），此屬性（attribute）會指定判別的型別。 在這裡， \[ switch \_ 類型 (short) \] 指定判別的類型為 **short**。 參數必須是整數類型。

如果聯集是結構的成員，則判別必須是相同結構的成員。 如果 union 是參數，則判別必須是另一個參數。 在上述範例中， **UnionParamProc** 函式的原型會將判別 *sUtype* 顯示為呼叫的最後一個參數。  (判別可以出現在呼叫中的任何位置。 ) 參數中指定的參數類型 **\[ \_ ，就 \]** 必須符合 **\[ switch \_ type \]** 屬性中指定的型別。

下列範例示範如何使用封裝判別與聯集的單一結構：

``` syntax
typedef struct 
{
    short utype;  /* discriminant can precede or follow union */
    [switch_is(utype)] union 
    {
       [case(0)]   short     sVal;
       [case(1)]   float     fVal;
       [case(2)]   char      chVal;
       [default]   ;
    } u;
} DISCRIM_UNION_STRUCT_TYPE;
 
short UnionStructProc(
    [in] DISCRIM_UNION_STRUCT_TYPE u1);
```

Microsoft RPC MIDL 編譯器允許在 [**typedef**](/windows/desktop/Midl/typedef) 結構之外進行聯集宣告。 這項功能是 DCE IDL 的延伸模組。 如需詳細資訊，請參閱聯 [**集**](/windows/desktop/Midl/union)。

 

 