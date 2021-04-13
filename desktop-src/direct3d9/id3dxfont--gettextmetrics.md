---
description: 捕獲 TEXTMETRIC 結構中所識別的字型特性。 這個方法支援 ANSI 和 Unicode 編譯器設定。
ms.assetid: 37788281-5bb0-45bb-b6d4-bdc4d811e3af
title: 'ID3DXFont：： GetTextMetrics 方法 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.GetTextMetrics
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6ce6064804d2aac2846cbea6971f145fc07759f3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322883"
---
# <a name="id3dxfontgettextmetrics-method"></a>ID3DXFont：： GetTextMetrics 方法

捕獲 [**TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica) 結構中所識別的字型特性。 這個方法支援 ANSI 和 Unicode 編譯器設定。

## <a name="syntax"></a>語法


```C++
BOOL GetTextMetrics(
  [out] TEXTMETRIC *pTextMetrics
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pTextMetrics* \[擴展\]
</dt> <dd>

類型： **[ **TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica)\***

[**TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica)結構的指標，其中包含字型屬性。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **BOOL**](../winprog/windows-data-types.md)**

如果函式成功則為非零，否則為 0。

## <a name="remarks"></a>備註

編譯器設定也會決定結構類型。 如果已定義 Unicode，函數會傳回 TEXTMETRICW 結構。 否則，函式呼叫會傳回 TEXTMETRICA 結構。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9core。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXFont](id3dxfont.md)
</dt> </dl>

 

 
