---
title: pipe 屬性
description: 管道類型的函式可讓您在遠端程序呼叫中，傳輸具型別資料的開放式資料流程。
ms.assetid: 85b76a55-8df2-4417-9a39-3e3bf49651fc
keywords:
- pipe 屬性 MIDL
topic_type:
- apiref
api_name:
- pipe
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0aaab8d399c99e02b5393ee9f5258da53aea491
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314761"
---
# <a name="pipe-attribute"></a>pipe 屬性

**管道** 類型的函式可讓您在遠端程序呼叫中，傳輸具型別資料的開放式資料流程。

``` syntax
typedef pipe element-type pipe-declarator;
```

## <a name="parameters"></a>參數

<dl> <dt>

*元素類型* 
</dt> <dd>

定義傳輸緩衝區中單一元素的大小。 *元素類型* 可以是 [基底類型](midl-base-types.md)、預先定義的 \_ 類型、[**結構**](struct.md)、 [**32b 列舉**](v1-enum.md)或類型識別碼。 有幾項限制適用于 *元素 \_ 類型*，如下列備註所述。

</dd> <dt>

*管道-宣告子* 
</dt> <dd>

指定一或多個識別符或識別碼指標。 以逗號分隔多個宣告子。

</dd> </dl>

## <a name="remarks"></a>備註

您可以使用 **管道** 類型的函式，以雙向傳送資料。 **\[** [**In**](in.md) **\]** pipe 參數可讓伺服器在遠端程序呼叫期間，從用戶端提取資料流程。 **\[**[**輸出**](out-idl.md) **\]** 管道參數可讓伺服器將資料流程推送回用戶端。 您可以提供用戶端常式來推送和提取資料流程，以及配置資料的全域緩衝區。 用戶端和伺服器 stub 常式會封送處理和 unmarshal 資料，並將緩衝區的參考傳回到應用程式。

下列限制適用于管道：

-   管道元素不可以是或包含指標、符合標準的陣列、控制碼或內容控制碼。 此外，在 Microsoft 管道的管道中，管道元素不能是或包含聯 [**集**](union.md)、 [**16b 列舉**](enum.md)或 [**\_ \_ int3264**](--int3264.md)。
-   您無法將 **\[** [**傳輸 \_ 視為**](transmit-as.md) **\]** 、 **\[** [**表示 \_ as**](represent-as.md) **\]** 、電傳 **\[** [**\_ 封送**](wire-marshal.md)處理 **\]** 或 **\[** [**使用者 \_ 封送**](user-marshal.md)處理 **\]** 屬性套用至管道類型或 *元素類型*。
-   管道類型不可以是結構或等位的成員、指標的目標或陣列的基底類型。
-   宣告為管道類型的資料類型只能用來做為遠端呼叫的參數。
-   您可以用傳值方式或參考 (**\[** [**ref**](ref.md)指標) 來傳遞管道參數 **\]** 。 但是，您無法將 **\[** [**ptr**](ptr.md) **\]** 屬性套用至以傳址方式傳遞的管道。 不論方向為何，您都不能指定具有 **\[** [**唯一**](unique.md) **\]** 或完整指標的管道參數。
-   您無法在 **\[** [**物件**](object.md)介面中使用管道 **\]** 。
-   您無法將 **\[** [**等冪**](idempotent.md) **\]** 屬性套用至具有管道參數的常式。
-   您無法使用序列化屬性，使用 **\[** 管線 [**進行編碼**](encode.md) **\]** 和解碼 **\[** [](decode.md) **\]** 。
-   您無法使用自動控制碼（預設值）或搭配使用 **\[** [**auto \_ 控制碼**](auto-handle.md) **\]** 屬性和管道。

> [!Note]  
> MIDL 編譯器只支援 [**/Oif**](-oi.md) 模式中的管道。

 

如需使用管道參數來執行常式的詳細資訊，請參閱《 RPC 程式設計人員指南》中的 [管道](/windows/desktop/Rpc/pipes) 和參考。

## <a name="examples"></a>範例

``` syntax
typedef pipe unsigned char UCHAR_PIPE1, UCHAR_PIPE2;
 
//SIMPLE_STRUCT defined elsewhere
typedef pipe SIMPLE_STRUCT SIMPLE_STRUCT_PIPE;
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**自動 \_ 處理**](auto-handle.md)
</dt> <dt>

[MIDL 基底類型](midl-base-types.md)
</dt> <dt>

[**解碼**](decode.md)
</dt> <dt>

[**編碼**](encode.md)
</dt> <dt>

[**枚舉**](enum.md)
</dt> <dt>

[**idempotent**](idempotent.md)
</dt> <dt>

[**在**](in.md)
</dt> <dt>

[**物件**](object.md)
</dt> <dt>

[**擴展**](out-idl.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**表示 \_ 為**](represent-as.md)
</dt> <dt>

[**結構**](struct.md)
</dt> <dt>

[**傳輸 \_ 為**](transmit-as.md)
</dt> <dt>

[**獨特**](unique.md)
</dt> <dt>

[**使用者 \_ 封送處理**](user-marshal.md)
</dt> <dt>

[**網路 \_ 封送處理**](wire-marshal.md)
</dt> </dl>

 

 