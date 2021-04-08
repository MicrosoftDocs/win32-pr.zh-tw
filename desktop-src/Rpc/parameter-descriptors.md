---
title: 參數描述項
description: 如先前所述，\ 8211; Oi 和 \ 8211; Oif 樣式參數描述項存在。
ms.assetid: c2dad284-abe5-4b38-b3a6-3c7373fc5b84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22f6f8b19eb6632c4111547925151865b03b9adc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682885"
---
# <a name="parameter-descriptors"></a>參數描述項

如先前所述， [**-Oi**](/windows/desktop/Midl/-oi) 和 **– Oif** 樣式參數描述項存在。

## <a name="the-oi-parameter-descriptors"></a>– Oi 參數描述項

完全解讀的存根需要 RPC 呼叫中每個參數的其他資訊。 程式的參數描述會在程式的描述之後立即執行。

[**Simple – Oi**](/windows/desktop/Midl/-oi)

**參數描述項**

的描述格式 \[  \] 或傳回簡單類型參數的格式為：

``` syntax
FC_IN_PARAM_BASETYPE 
simple_type<1>
```

–或–

``` syntax
FC_RETURN_PARAM_BASETYPE 
simple_type<1>
```

其中，簡單 \_ 類型<1> 是指出簡單類型的 FC 權杖。 這些代碼如下所示：

``` syntax
4e  FC_IN_PARAM_BASETYPE 
53  FC_RETURN_PARAM_BASETYPE
```

**Other – Oi**

**參數描述項**

所有其他參數類型之描述的格式為：

``` syntax
param_direction<1> 
stack_size<1> 
type_offset<2>
```

其中 \_ 每個描述的參數方向<1> 欄位必須是下表所示的其中一個。



| Hex | 旗標                          | 意義                                                     |
|-----|-------------------------------|-------------------------------------------------------------|
| 4d  | \_PARAM 中的 FC \_                 | In 參數。                                            |
| 50  | FC \_ IN \_ OUT \_ 參數            | In/out 參數。                                        |
| 51  | FC \_ 輸出 \_ 參數                | Out 參數。                                           |
| 52  | FC \_ 傳回 \_ 參數             | 程式傳回值。                                   |
| 4f  | A FC \_ IN \_ PARAM \_ 沒有 \_ 免費 \_ INST | Xmit/rep 中的，表示未進行任何釋放的參數。 |



 

堆疊 \_ 大小<1> 是堆疊上參數的大小，以參數在堆疊上佔據的整數數目表示。

> [!Note]  
> 64位平臺上不支援 [**– Oi**](/windows/desktop/Midl/-oi) 模式。

 

Type \_ offset<2> field 是 type format string 資料表中的位移，表示引數的型別描述項。

## <a name="the-oif-parameter-descriptors"></a>– Oif 參數描述項

參數描述有兩種可能的格式：一個用於基底類型，另一個用於所有其他類型。

基底類型：

``` syntax
PARAM_ATTRIBUTES<2> 
stack_offset<2> 
type_format_char<1> 
unused<1>
```

其他：

``` syntax
PARAM_ATTRIBUTES<2> 
stack_offset<2> 
type_offset<2>
```

在兩個堆疊 \_ 位移<2> 指出虛擬引數堆疊上的位移（以位元組為單位）。 針對基底類型，引數型別是由對應至類型的格式字元直接提供。 針對其他類型，[類型 \_ 位移]<2> 欄位會在類型格式字串資料表中提供引數的型別描述項所在的位移。

[參數屬性] 欄位的定義如下：

``` syntax
typedef struct
  {
  unsigned short  MustSize            : 1;    // 0x0001
  unsigned short  MustFree            : 1;    // 0x0002
  unsigned short  IsPipe              : 1;    // 0x0004
  unsigned short  IsIn                : 1;    // 0x0008
  unsigned short  IsOut               : 1;    // 0x0010
  unsigned short  IsReturn            : 1;    // 0x0020
  unsigned short  IsBasetype          : 1;    // 0x0040
  unsigned short  IsByValue           : 1;    // 0x0080
  unsigned short  IsSimpleRef         : 1;    // 0x0100
  unsigned short  IsDontCallFreeInst  : 1;    // 0x0200
  unsigned short  SaveForAsyncFinish  : 1;    // 0x0400
  unsigned short  Unused              : 2;
  unsigned short  ServerAllocSize     : 3;    // 0xe000
  } PARAM_ATTRIBUTES, *PPARAM_ATTRIBUTES;
```

-   只有在參數必須調整大小時，才會設定 **MustSize** 位。
-   如果伺服器必須呼叫參數的 NdrFree 常式，則會設定 **MustFree** 位 \* 。
-   **IsSimpleRef** 位是針對屬於其他指標以外之任何其他指標的參考指標而設定的，而且沒有配置屬性的參數。 針對這類型別，參數描述的型別 \_ offset<> 欄位，除了基底型別的參考指標之外，還提供對參考型別的位移; 參考指標只會略過。
-   **IsDontCallFreeInst** 位是針對特定的代表設定為 \_ 不應呼叫其免費實例常式的參數。
-   如果參數為 \[ **out** \] 、 \[ **in** \] 或 \[ **in、out** 指標 \] 或 enum16 指標，且將在伺服器解譯器的堆疊上初始化 **\_**，則 ServerAllocSize 位為非零值，而不是使用 I RpcAllocate 的呼叫。 如果是非零值，則這個值會乘以8以取得參數的位元組數目。 請注意，這麼做表示一律會為指標配置至少8個位元組。
-   **IsBasetype** 位是針對由 Main [**– Oif**](/windows/desktop/Midl/-oi)解譯器迴圈封送處理的簡單類型所設定。 尤其是，在其上具有範圍屬性的簡單類型，並不會標示為基底類型，以強制使用 FC 範圍權杖來強制執行範圍常式封送處理 \_ 。
-   **IsByValue** 位是針對以傳值方式傳送的複合類型而設定，但不會針對簡單類型設定，不論引數是否為指標。 其所設定的複合類型為結構、等位、 [**傳輸 \_ 為**](/windows/desktop/Midl/transmit-as)， [**表示 \_ 為**](/windows/desktop/Midl/represent-as)、 [**連網 \_ 封送**](/windows/desktop/Midl/wire-marshal) 處理和 SAFEARRAY。 一般來說，在 [**– Oicf**](/windows/desktop/Midl/-oi) 解譯器中，主要解譯器迴圈的優點引進了位，以確保簡單引數 (稱為複合類型引數，) 可正確取值。 先前的解譯器版本中從未使用過此位。

 

 