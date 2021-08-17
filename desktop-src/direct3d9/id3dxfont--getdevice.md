---
description: 抓取與字型物件相關聯的 Direct3D 裝置。
ms.assetid: c713cbe2-6e6e-476b-a995-14fa149cb088
title: 'ID3DXFont：： GetDevice 方法 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.GetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e0f89594f77044db20bade062b245ccabe072a0ccae1fb5fa76f23bb18a8db0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119121145"
---
# <a name="id3dxfontgetdevice-method"></a>ID3DXFont：： GetDevice 方法

抓取與字型物件相關聯的 Direct3D 裝置。

## <a name="syntax"></a>語法


```C++
HRESULT GetDevice(
  [out] LPDIRECT3DDEVICE9 *ppDevice
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppDevice* \[擴展\]
</dt> <dd>

類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***

[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面指標的位址，表示與字型物件相關聯的 Direct3D 裝置物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 S \_ OK。 如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，D3DXERR \_ INVALIDDATA。

## <a name="remarks"></a>備註

> [!Note]  
> 呼叫這個方法將會增加 [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) 介面上的內部參考計數。 當您使用這個 **IDirect3DDevice9** 介面完成時，請務必呼叫 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) ，否則會發生記憶體流失。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9core。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXFont](id3dxfont.md)
</dt> </dl>

 

 
