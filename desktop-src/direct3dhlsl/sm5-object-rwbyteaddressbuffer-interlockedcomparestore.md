---
title: RWByteAddressBuffer：： InterlockedCompareStore 函數
description: 以不可部分完成的方式 Ccompares 比較值的輸入。
ms.assetid: d82a73b6-24a5-4eb3-9f20-15ba263c93d0
keywords:
- InterlockedCompareStore 函式 HLSL
topic_type:
- apiref
api_name:
- InterlockedCompareStore
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dcb19358f98c1280ddb180b7381fb7714d28cc7db145ca36577f5f97f70c9f1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118509687"
---
# <a name="interlockedcomparestore-function"></a>InterlockedCompareStore 函式

以不可部分完成的方式 Ccompares 比較值的輸入。

## <a name="syntax"></a>語法

``` syntax
void InterlockedCompareStore(
  in UINT dest,
  in UINT compare_value,
  in UINT value
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

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

此作業只能在 int 或 uint 型別資源和共用記憶體變數上執行。 此函數有三個可能的用途。 第一個是當 R 是共用記憶體變數型別時。 在此情況下，此函式會在 dest 所參考的共用記憶體暫存器上執行作業。 第二個案例是 R 是資源變數類型。 在此案例中，此函式會在 dest 所參考的資源位置上執行作業。 最後，第三個案例是 R 是本機變數類型。 在此案例中，此函式會縮減為使用本機作業所執行的作業。

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

 

 