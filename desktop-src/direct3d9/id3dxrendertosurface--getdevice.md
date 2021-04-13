---
description: 抓取與呈現介面相關聯的 Direct3D 裝置。
ms.assetid: 579cf7da-b8e0-4d9f-93b8-b1f47c3d5654
title: 'ID3DXRenderToSurface：： GetDevice 方法 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToSurface.GetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ac01744887412349c71daa34194fc3a0b03b19a9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323311"
---
# <a name="id3dxrendertosurfacegetdevice-method"></a>ID3DXRenderToSurface：： GetDevice 方法

抓取與呈現介面相關聯的 Direct3D 裝置。

## <a name="syntax"></a>語法


```C++
HRESULT GetDevice(
  [out, retval] LPDIRECT3DDEVICE9 *ppDevice
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppDevice* \[退出，retval\]
</dt> <dd>

類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***

[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面指標的位址，表示與轉譯介面相關聯的 Direct3D 裝置物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為「D3D \_ 正常」。 如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。 呼叫這個方法將會增加 [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) 介面上的內部參考計數。 當您使用這個 **IDirect3DDevice9** 介面完成時，請務必呼叫 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) ，否則會發生記憶體流失。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9core。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXRenderToSurface](id3dxrendertosurface.md)
</dt> </dl>

 

 
