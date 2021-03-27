---
title: RWByteAddressBuffer：： InterlockedCompareExchange 函數
description: 比較輸入與比較值，並以不可部分完成的方式交換結果。
ms.assetid: 9d6e8d95-5157-49a7-8a79-f3ca6ba87ebb
keywords:
- InterlockedCompareExchange 函式 HLSL
topic_type:
- apiref
api_name:
- InterlockedCompareExchange
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 18c7e5d58fe926d09e7ec48ee12a2336627d5db2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682818"
---
# <a name="interlockedcompareexchange-function"></a>InterlockedCompareExchange 函式

比較輸入與比較值，並以不可部分完成的方式交換結果。

## <a name="syntax"></a>語法

``` syntax
void InterlockedCompareExchange(
  in  UINT dest,
  in  UINT compare_value,
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

*比較 \_ 值* \[\]
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

比較值。

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

以不可部分完成的方式比較 *dest* 中的值與 *\_ 值*，如果值相符，則會將值儲存在 *dest* 中，並以 *原始 \_ 值* 傳回 *dest* 的原始值。 此作業只能在 **int** 或 *uint* 型別資源和共用記憶體變數上執行。 此函數有三個可能的用途。 第一個是當 R 是共用記憶體變數型別時。 在此情況下，此函式會在 *dest* 所參考的共用記憶體暫存器上執行作業。 第二個案例是 R 是資源變數類型。 在此案例中，此函式會在 *dest* 所參考的資源位置上執行作業。 最後，第三個案例是 R 是本機變數類型。 在此案例中，此函式會縮減為使用本機作業所執行的作業。 只有當 R 可讀取和寫入時，才能使用此作業。

> [!Note]  
> 如果您在 [**for**](dx-graphics-hlsl-for.md)或 [**while**](dx-graphics-hlsl-while.md)計算著色器迴圈中呼叫 **InterlockedCompareExchange** ，以便正確編譯，您必須在該迴圈中使用 [ **\[ 允許 \_ uav \_ 條件 \]** ] 屬性。

 

下列著色器類型支援此函數：



| VS  | 房 協  | DS  | GS  | PS  | CS  |
|-----|-----|-----|-----|-----|-----|
| x   | x   | x   | x   | x   | x   |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[RWByteAddressBuffer](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 