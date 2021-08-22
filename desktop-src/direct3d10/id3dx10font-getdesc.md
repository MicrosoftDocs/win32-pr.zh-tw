---
description: 取得目前字型物件的描述。
ms.assetid: f08beb35-351f-4087-a2db-097843463291
title: 'ID3DX10Font：： GetDesc 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.GetDesc
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d684a0bf485db441a0a6bf23cd36496cc13fdfe766eaa890682259b76b3800c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990438"
---
# <a name="id3dx10fontgetdesc-method"></a>ID3DX10Font：： GetDesc 方法

取得目前字型物件的描述。

## <a name="syntax"></a>語法


```C++
HRESULT GetDesc(
  [in] D3DX10_FONT_DESC *pDesc
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pDesc* \[在\]
</dt> <dd>

類型： **[ **D3DX10 \_ 字型 \_ DESC**](d3dx10-font-desc.md)\***

描述字型物件之 [**D3DX10 \_ 字型 \_ DESC**](d3dx10-font-desc.md) 結構的指標。 如果已定義 UNICODE，則會傳回 D3DX10FONT DESCW 的指標， \_ 否則會傳回 D3DX10FONT DESCA 的指標 \_ 。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 S \_ OK。 如果方法失敗，則會傳回下列值： D3DERR \_ INVALIDCALL。

## <a name="remarks"></a>備註

如果已定義 UNICODE，則這個方法會描述 Unicode 字型物件。 否則會呼叫 GetDescA，它會傳回 D3DX10FONT \_ DESCA 結構的指標。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX10。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>D3DX10 .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DX10Font](id3dx10font.md)
</dt> <dt>

[D3DX 介面](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




