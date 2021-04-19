---
description: 取得目前字型物件的描述。 GetDescW 和 GetDescA 與這個方法相同，不同之處在于指標會分別傳回至 D3DXFONT \_ DESCW 或 D3DXFONT \_ DESCA 結構。
ms.assetid: 21bcd3e0-3659-4d64-959a-0f2d65850cb1
title: 'ID3DXFont：： GetDesc 方法 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.GetDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3310971e360fb9994a30d62349d3e7e4b764c7d0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106976704"
---
# <a name="id3dxfontgetdesc-method"></a>ID3DXFont：： GetDesc 方法

取得目前字型物件的描述。 GetDescW 和 GetDescA 與這個方法相同，不同之處在于指標會分別傳回至 [**D3DXFONT \_ DESCW**](d3dxfont-desc.md) 或 **D3DXFONT \_ DESCA** 結構。

## <a name="syntax"></a>語法


```C++
HRESULT GetDesc(
  [out] D3DXFONT_DESC *pDesc
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pDesc* \[擴展\]
</dt> <dd>

類型： **[ **D3DXFONT \_ DESC**](d3dxfont-desc.md)\***

描述字型物件之 [**D3DXFONT \_ DESC**](d3dxfont-desc.md) 結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 S \_ OK。 如果方法失敗，則會傳回下列值： D3DERR \_ INVALIDCALL。

## <a name="remarks"></a>備註

如果已定義 UNICODE，則這個方法會描述 Unicode 字型物件。 否則會呼叫 GetDescA，它會傳回 [**D3DXFONT \_ DESCA**](d3dxfont-desc.md) 結構的指標。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9core。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXFont](id3dxfont.md)
</dt> </dl>

 

 




