---
title: 處理
description: 程式位址控制碼的格式字串描述中最多有兩個部分。
ms.assetid: 11c6742c-b2f5-4201-8b1c-7e31ae52e0da
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d1c1ce68b74440fc9339fb9cf9170bfdd1fdfcd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316066"
---
# <a name="handles"></a>處理

程式位址控制碼的格式字串描述中最多有兩個部分。 第一個部分是程式 \_ 描述<1> 欄位的控制碼類型，用來指示隱含控制碼。 這部分永遠存在。 第二個部分是程式中任何明確控制碼的參數描述。 下列各節將說明這兩個部分，並討論系結控制碼問題的存根描述元結構的其他 MIDL 編譯器支援。

## <a name="implicit-handles"></a>隱含控制碼

如果程式使用系結的隱含控制碼，程式 \_ 描述的<1> 欄位的控制碼類型，會包含三個有效非零值其中之一。 在 \_ 存根描述元結構的隱含控制碼資訊欄位中，可以找到隱含控制碼的 MIDL 編譯器支援 \_ ：

``` syntax
typedef  (__RPC_FAR * GENERIC_BINDING_ROUTINE)();

typedef struct 
  {
  GENERIC_BINDING_ROUTINE  pfnBind;
  GENERIC_BINDING_ROUTINE  pfnUnbind;
  } GENERIC_BINDING_ROUTINE_PAIR;
  
typedef struct __GENERIC_BINDING_INFO 
  {
  void __RPC_FAR*          pObj;
  unsigned char            Size;
  GENERIC_BINDING_ROUTINE  pfnBind;
  GENERIC_BINDING_ROUTINE    pfnUnbind;
  } GENERIC_BINDING_INFO,  *PGENERIC_BINDING_INFO;

union 
  {
  handle_t*                pAutoHandle;
  handle_t*                pPrimitiveHandle;
  PGENERIC_BINDING_INFO    pGenericBindingInfo;
  } IMPLICIT_HANDLE_INFO;
```

如果程式使用 auto 控制碼， **pAutoHandle** 成員就會包含已定義的存根（自動控制碼變數）位址。

如果程式使用隱含基本控制碼， **pPrimitiveHandle** 成員就會包含已定義的存根（基本控制碼）變數位址。

最後，如果程式使用隱含的泛型控制碼， **pGenericBindingInfo** 成員會將指標的位址保留在對應的泛型系結 **\_ \_ 資訊** 結構中。 資料結構 **MIDL \_ 存根 \_ DESC** 包含泛型系 **\_ \_ 結** 組結構集合的指標。 此集合之零位置的專案會保留給系結和 **解除** 系結 **常式，對應** 至 **pGenericBindingInfo** 在 **隱含 \_ 控制碼 \_ 資訊** 中參考的泛型系結控制碼。 隱含系結控制碼的型別會以格式字串表示。

## <a name="explicit-handles"></a>明確控制碼

有三個可能的明確控制碼類型：內容、泛型和基本。 如果是明確控制碼 (或 \[  \] 僅限輸出的內容控制碼（以) 的相同方式處理），系結處理資訊就會顯示為程式的其中一個參數。 三個可能的描述如下所示。

Primitive

``` syntax
FC_BIND_PRIMITIVE, flag<1>, offset<2>.
```

旗標<1> 指出控制碼是否以指標傳遞。

Offset<2> 提供從堆疊開頭到基本控制碼的位移。

> [!Note]  
> 類型格式字串中的基本控制碼描述會縮減為單一 FC \_ 略過。

 

泛型

``` syntax
FC_BIND_GENERIC, flag_and_size<1>, offset<2>, binding_routine_pair_index<1>, FC_PAD
```

旗標 \_ 和 \_ 大小<1> 具有上方旗標半值和較低大小的半值。 旗標會指出控制碼是否以指標傳遞。 [大小] 欄位提供使用者定義的大小–一般控制碼類型。 在32位系統上，此大小限制為1、2或4個位元組，而64位系統上的1、2、4或8個位元組則為1、2、4或8個位元組。

Offset<2> 欄位提供從指標堆疊開頭到指定大小資料的位移。

系 \_ 結常式 \_ 組 \_ 索引<1> 欄位會將存根描述項的 aGenericBindingRoutinePairs 欄位中的索引提供給泛型控制碼的系結和 **解除** 系結常式函式指標。

> [!Note]  
> 類型格式的泛型控制碼描述僅為相關資料類型的描述。

 

Context

``` syntax
FC_BIND_CONTEXT flags<1> offset<2> context_rundown_routine_index<1> param_num<1>
```

旗標<1> 指出控制碼的傳遞方式，以及其型別。 下表顯示有效的旗標。



| Hex | 旗標                                   |
|-----|----------------------------------------|
| 80  | 控制碼 \_ 參數 \_ 為 \_ VIA \_ PTR            |
| 40  | 句 \_ 柄 \_ 參數 \_ 位於                  |
| 20  | 控制碼 \_ 參數 \_ 已 \_ 退出                 |
| 21  | 控制碼 \_ 參數 \_ 為 \_ RETURN              |
| 08  | NDR \_ STRICT \_ 內容 \_ 控制碼           |
| 04  | NDR \_ 內容 \_ 控制碼 \_ 沒有 \_ 序列化    |
| 02  | NDR \_ 內容 \_ 控制碼 \_ 序列化        |
| 01  | NDR \_ 內容 \_ 控制碼 \_ 不 \_ 可以是 \_ Null |



 

前四個旗標一直都存在，最後四個旗標已新增到 Windows 2000 中。

Offset<2> 欄位提供從堆疊開頭到內容控制碼的位移。

內容取消 \_ \_ 常式 \_ 索引<1> 為此內容控制碼所用的取消常式提供存根描述元之 **apfnNdrRundownRoutines** 欄位的索引。 編譯器一律會產生索引。 針對沒有取消常式的常式，這是包含 null 之資料表位置的索引。

針對內建的存根 **-Oi2**，param \_ num<1> 提供序數計數，從零開始，以指定在指定程式中的內容控制碼。

在舊版的解譯器中，param \_ num<1> 在其程式中提供內容控制碼的參數編號，從零開始。

> [!Note]  
> 在 [描述] 中，類型格式字串中的內容控制碼描述不會有<2> 的位移。

 

## <a name="the-new-oif-header"></a>New – Oif 標頭

如先前所述，– [**Oif**](/windows/desktop/Midl/-oi) 標頭會在 **– Oi** 標頭上展開。 為了方便起見，所有欄位如下所示：

 (舊的標頭) 

``` syntax
handle_type<1> 
Oi_flags<1>
[rpc_flags<4>]
proc_num<2>  
stack_size<2>
[explicit_handle_description<>]
```

 ([**– Oif**](/windows/desktop/Midl/-oi) 延伸模組) 

``` syntax
constant_client_buffer_size<2>
constant_server_buffer_size<2>
INTERPRETER_OPT_FLAGS<1>
number_of_params<1>
```

常數 \_ 用戶端 \_ 緩衝區 \_ 大小<2> 提供編譯器預先計算的封送處理緩衝區大小。 這可能只是部分大小，因為 ClientMustSize 旗標會觸發調整大小。

常數 \_ 伺服器 \_ 緩衝區 \_ 大小<2> 提供編譯器所預先計算的封送處理緩衝區大小。 這可能只是部分大小，因為 ServerMustSize 旗標會觸發調整大小。

解譯器 \_ OPT \_ 旗標是在 Ndrtypes 中定義：

``` syntax
typedef struct
  {
  unsigned char   ServerMustSize      : 1;    // 0x01
  unsigned char   ClientMustSize      : 1;    // 0x02
  unsigned char   HasReturn           : 1;    // 0x04
  unsigned char   HasPipes            : 1;    // 0x08
  unsigned char   Unused              : 1;
  unsigned char   HasAsyncUuid        : 1;    // 0x20
  unsigned char   HasExtensions       : 1;    // 0x40
  unsigned char   HasAsyncHandle      : 1;    // 0x80
  } INTERPRETER_OPT_FLAGS, *PINTERPRETER_OPT_FLAGS;
```

-   如果伺服器需要執行緩衝區調整大小傳遞，就會設定 ServerMustSize 位。
-   如果用戶端需要執行緩衝區調整大小傳遞，就會設定 ClientMustSize 位。
-   如果程式有傳回值，則會設定 HasReturn 位。
-   如果管道封裝需要用來支援管道引數，則會設定 HasPipes 位。
-   如果程式是非同步 DCOM 程式，則會設定 HasAsyncUuid 位。
-   HasExtensions 位表示使用 Windows 2000 和更新版本的延伸模組。
-   HasAsyncHandle 位表示非同步 RPC 程式。

HasAsyncHandle 位一開始是用於不同的非同步支援 DCOM 實，因此無法用於 DCOM 中目前的樣式非同步支援。 HasAsyncUuid 位目前表示這一點。

 

 