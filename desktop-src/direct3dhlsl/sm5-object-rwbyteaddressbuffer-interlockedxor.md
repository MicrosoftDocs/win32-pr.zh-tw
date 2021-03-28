---
title: RWByteAddressBuffer：： InterlockedXor 函數
description: 在值上執行不可部分完成 XOR。
ms.assetid: 692f8b5e-a81e-4700-8a8d-3594aba85671
keywords:
- InterlockedXor 函式 HLSL
topic_type:
- apiref
api_name:
- InterlockedXor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 920ae912c599b66a03a25d7bc8ecc9b199036b26
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933260"
---
# <a name="interlockedxor-function"></a>InterlockedXor 函式

在值上執行不可部分完成 **XOR** 。

## <a name="syntax"></a>語法

``` syntax
void InterlockedXor(
  in  UINT dest,
  in  UINT value,
  out UINT original_value
);
```

## <a name="parameters"></a>參數

<dl> <dt>

*目的地* \[在\]
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

目的地位址。

</dd> <dt>

*值* \[在\]
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

輸入值。

</dd> <dt>

*原始 \_ 值* \[ 輸出\]
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

原始的值。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

此作業只能在 **INT** 或 **UINT** 型別資源和共用記憶體變數上執行。 此函數有三個可能的用途。 第一個是當 R 是共用記憶體變數型別時。 在此情況下，此函式會使用 *dest* 所參考的共用記憶體暫存器值來執行不可部分完成 **XOR** 。 第二個案例是 R 是資源變數類型。 在此案例中，此函式會使用 *dest* 所參考資源位置的值來執行不可部分完成 **XOR** 。 最後，第三個案例是 R 是本機變數類型。 在此案例中，此函式會縮減為 *dest* 值和 *值* 的 **XOR** 。 作業的結果會取代 *dest* 中的值。 多載函式有額外的輸出變數，其會設定為 *目的地* 的原始值。 只有當 R 是可讀取和可寫入時，才能使用此多載作業。

下列著色器類型支援此函數：



| VS  | 房 協  | DS  | GS  | PS  | CS  |
|-----|-----|-----|-----|-----|-----|
| x   |  x  | x   | x   | x   | x   |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[RWByteAddressBuffer](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 