---
title: RWByteAddressBuffer：： InterlockedExchange 函數
description: 以不可部分完成的方式交換值。
ms.assetid: a50f4cba-a7a2-44b0-9de7-003b4c7a947f
keywords:
- InterlockedExchange 函式 HLSL
topic_type:
- apiref
api_name:
- InterlockedExchange
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 47c51374b7dcd62ac208e0aa8811a8d693ce0ac6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104990899"
---
# <a name="interlockedexchange-function"></a>InterlockedExchange 函式

以不可部分完成的方式交換值。

## <a name="syntax"></a>語法

``` syntax
void InterlockedExchange(
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

這種作業只能對純量類型的資源和共用記憶體變數執行。 此函數有三個可能的用途。 第一個是當 R 是共用記憶體變數型別時。 在此情況下，此函式會在 dest 所參考的共用記憶體暫存器上執行作業。 第二個案例是 R 是資源變數類型。 在此案例中，此函式會在 dest 所參考的資源位置上執行作業。 最後，第三個案例是 R 是本機變數類型。 在此案例中，此函式會縮減為使用本機作業所執行的作業。 只有當 R 可讀取和寫入時，才能使用此作業。

下列著色器類型支援此函數：



| VS  | 房 協  | DS  | GS  | PS  | CS  |
|-----|-----|-----|-----|-----|-----|
|  x  |  x  |  x  |  x  | x   | x   |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[RWByteAddressBuffer](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 