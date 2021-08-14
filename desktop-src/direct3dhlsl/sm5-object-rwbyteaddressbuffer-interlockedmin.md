---
title: RWByteAddressBuffer：： InterlockedMin 函數
description: 以不可部分完成的方式尋找最小值。
ms.assetid: bf650b2e-9c6c-4458-9565-1e9ec76a1472
keywords:
- InterlockedMin 函式 HLSL
topic_type:
- apiref
api_name:
- InterlockedMin
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 062ae6c5fa37b732411891427770761881429069d030e9266ab20adb3e2d3726
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118509547"
---
# <a name="interlockedmin-function"></a>InterlockedMin 函式

以不可部分完成的方式尋找最小值。

## <a name="syntax"></a>語法

``` syntax
void InterlockedMin(
  in  UINT dest,
  in  UINT value,
  out UINT original_value
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

Nothing

## <a name="remarks"></a>備註

此作業只能在 int 和 uint 具類型的資源和共用記憶體變數上執行。 此函數有三個可能的用途。 第一個是當 R 是共用記憶體變數型別時。 在此情況下，此函式會針對 dest 所參考的共用記憶體暫存器，執行最小值的最小值。 第二個案例是 R 是資源變數類型。 在此案例中，此函式會對 dest 所參考的資源位置執行最小值的最小值。 最後，第三個案例是 R 是本機變數類型。 在此案例中，此函式會減少為儲存在目的地中的 dest 和值的最小值。 多載函式有額外的輸出變數，其會設定為目的地的原始值。 只有在 R 可讀取和可寫入時，才能使用此多載作業。

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

 

 