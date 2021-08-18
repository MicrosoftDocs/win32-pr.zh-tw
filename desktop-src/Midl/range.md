---
title: range 屬性
description: '\ Range \ 屬性可讓您指定引數或欄位的允許值範圍，其值會在執行時間設定。 當與管道類型搭配使用時，屬性會針對管道區塊中的元素計數指定允許的範圍。'
ms.assetid: 1609fea5-e82c-4389-b4f4-2cd8d0622cde
keywords:
- 範圍屬性 MIDL
topic_type:
- apiref
api_name:
- range
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8be59ef1b212d0f6953063ce7ac3239d8940a5ea54a623990fc3d7af9f36ad3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764308"
---
# <a name="range-attribute"></a>range 屬性

**\[ 範圍 \]** 屬性可讓您指定引數或欄位的允許值範圍，其值會在執行時間進行設定。 當與管道類型搭配使用時，屬性會針對管道區塊中的元素計數指定允許的範圍。

``` syntax
[range(low-val,high-val)] type-specifier declarator
```

## <a name="parameters"></a>參數

<dl> <dt>

*低-val* 
</dt> <dd>

參數或欄位可以容納的最小允許值。

</dd> <dt>

*高 val* 
</dt> <dd>

參數或欄位可以容納的最大允許值。

</dd> <dt>

*類型規範* 
</dt> <dd>

非 [**超**](hyper.md)整數類型或 [**\_ \_ int64**](--int64.md)以外的整數類資料類型、整數型別的型別識別碼、[**列舉**](enum.md)型別或管道型別名稱。

</dd> <dt>

*符中* 
</dt> <dd>

標準 C 宣告子，例如識別碼。

</dd> </dl>

## <a name="remarks"></a>備註

您可以使用 [ **\[ 範圍 \]** ] 屬性來修改敏感性參數或欄位的意義，例如，用於大小或長度、具有一致或不同陣列的意義; 或每次您想要針對有效值的範圍檢查參數或域值。 屬性適用于最上層參數，以及較低層級的參數和欄位。 將 **\[ range \]** 屬性加入至類型並不會變更其電傳格式，因此不會影響回溯相容性。

**\[ 範圍 \]** 屬性也可以用於符合規範的資料，例如緩衝區或具有一致性屬性的陣列。 其效果是將一致資料的所有一致性大小限制為指定的範圍。 如果一致的資料是多維陣列，則每個陣列維度都會限制為指定的範圍。

在一致的資料上使用 **\[ 範圍 \]** 需要編譯目標為「目標 NT60 或更高版本。

請注意，當您編譯 IDL 檔案時，必須使用 [**/robust**](-robust.md) 編譯器選項，才能產生將執行這些檢查的 stub 程式碼。 在沒有 **/robust** 參數的情況下，MIDL 編譯器會忽略這個屬性。

## <a name="examples"></a>範例

``` syntax
HRESULT Method1(
    [in, range(0,100)] ULONG m,
    [in, range(0,100)] ULONG n,
    [size_is(m,n)] ULONG **pplong);

void InPipe(
    [in, range(0, MAX_CHUNK) LONG_PIPE pipe_date);
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[ (IDL) 檔案的介面定義](interface-definition-idl-file.md)
</dt> <dt>

[陣列](/windows/desktop/Rpc/arrays)
</dt> <dt>

[**第一個 \_ 是**](first-is.md)
</dt> <dt>

[**last \_**](last-is.md)
</dt> <dt>

[**長度 \_ 為**](length-is.md)
</dt> <dt>

[**最大值 \_ 為**](max-is.md)
</dt> <dt>

[**/robust**](-robust.md)
</dt> <dt>

[**大小 \_ 為**](size-is.md)
</dt> <dt>

[**切換 \_ 為**](switch-is.md)
</dt> </dl>

 

 