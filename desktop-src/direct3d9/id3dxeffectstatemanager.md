---
description: 這是使用者執行的介面，可讓使用者從效果設定裝置狀態。
ms.assetid: ccd3e456-e27b-4128-b20b-99ff8dafcbe1
title: 'ID3DXEffectStateManager 介面 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: fad9df739634625800c0a21fd9ba2a2823d70f8e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323068"
---
# <a name="id3dxeffectstatemanager-interface"></a>ID3DXEffectStateManager 介面

這是使用者執行的介面，可讓使用者從效果設定裝置狀態。 這個介面中的每個方法都必須由使用者執行，然後在發生下列任何一種情況時，用來作為應用程式的回呼：

-   效果會呼叫 [**ID3DXEffect：： BeginPass**](id3dxeffect--beginpass.md)。
-   藉由呼叫適當的狀態變更 API 來動態更新效果狀態。 請參閱個別的方法頁面以取得詳細資料。

當應用程式使用狀態管理員來執行自訂回呼時，在呼叫 [**ID3DXEffect：： BeginPass**](id3dxeffect--beginpass.md) 和 [**ID3DXEffect：： EndPass**](id3dxeffect--endpass.md)時，效果不會再自動儲存和還原狀態。 因為應用程式已在回呼中執行自訂的儲存和還原行為，所以會略過這項自動行為。

## <a name="members"></a>成員

**ID3DXEffectStateManager** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **ID3DXEffectStateManager** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ID3DXEffectStateManager** 介面具有這些方法。



| 方法                                                                                | 描述                                                                                                                  |
|:--------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------|
| [**LightEnable**](id3dxeffectstatemanager--lightenable.md)                           | 必須由使用者執行以啟用/停用燈光的回呼函數。<br/>                                 |
| [**SetFVF**](id3dxeffectstatemanager--setfvf.md)                                     | 必須由使用者執行來設定 FVF 程式碼的回呼函式。<br/>                                         |
| [**SetLight**](id3dxeffectstatemanager--setlight.md)                                 | 必須由使用者執行以設定燈光的回呼函式。<br/>                                            |
| [**SetMaterial**](id3dxeffectstatemanager--setmaterial.md)                           | 必須由使用者執行以設定材質狀態的回呼函式。<br/>                                     |
| [**SetNPatchMode**](id3dxeffectstatemanager--setnpatchmode.md)                       | 必須由使用者執行的回呼函式，以設定 N 個修補程式的細分區段數目。<br/>   |
| [**SetPixelShader**](id3dxeffectstatemanager--setpixelshader.md)                     | 必須由使用者執行以設定圖元著色器的回呼函數。<br/>                                     |
| [**SetPixelShaderConstantB**](id3dxeffectstatemanager--setpixelshaderconstantb.md)   | 必須由使用者所執行的回呼函式，以設定頂點著色器布林值常數的陣列。<br/>        |
| [**SetPixelShaderConstantF**](id3dxeffectstatemanager--setpixelshaderconstantf.md)   | 必須由使用者所執行的回呼函式，以設定頂點著色器浮點數常數的陣列。<br/> |
| [**SetPixelShaderConstantI**](id3dxeffectstatemanager--setpixelshaderconstanti.md)   | 必須由使用者所執行的回呼函式，以設定頂點著色器整數常數的陣列。<br/>        |
| [**Graphicsdevice**](id3dxeffectstatemanager--setrenderstate.md)                     | 必須由使用者執行來設定轉譯狀態的回呼函式。<br/>                                       |
| [**SetSamplerState**](id3dxeffectstatemanager--setsamplerstate.md)                   | 必須由使用者所執行的回呼函式，以設定取樣器。<br/>                                          |
| [**SetTexture**](id3dxeffectstatemanager--settexture.md)                             | 必須由使用者執行以設定材質的回呼函式。<br/>                                          |
| [**SetTextureStageState**](id3dxeffectstatemanager--settexturestagestate.md)         | 必須由使用者執行以設定材質階段狀態的回呼函式。<br/>                            |
| [**SetTransform**](id3dxeffectstatemanager--settransform.md)                         | 必須由使用者執行以設定轉換的回呼函數。<br/>                                        |
| [**SetVertexShader**](id3dxeffectstatemanager--setvertexshader.md)                   | 必須由使用者執行以設定頂點著色器的回呼函數。<br/>                                    |
| [**SetVertexShaderConstantB**](id3dxeffectstatemanager--setvertexshaderconstantb.md) | 必須由使用者所執行的回呼函式，以設定頂點著色器布林值常數的陣列。<br/>        |
| [**SetVertexShaderConstantF**](id3dxeffectstatemanager--setvertexshaderconstantf.md) | 必須由使用者所執行的回呼函式，以設定頂點著色器浮點數常數的陣列。<br/> |
| [**SetVertexShaderConstantI**](id3dxeffectstatemanager--setvertexshaderconstanti.md) | 必須由使用者所執行的回呼函式，以設定頂點著色器整數常數的陣列。<br/>        |



 

## <a name="remarks"></a>備註

使用者藉由實作為衍生自這個介面的類別，以及執行所有介面方法，來建立 ID3DXEffectStateManager 介面。 建立介面之後，您可以使用 [**ID3DXEffect：： GetStateManager**](id3dxeffect--getstatemanager.md) 和 [**ID3DXEffect：： SetStateManager**](id3dxeffect--setstatemanager.md)，取得或設定效果內的狀態管理員。

LPD3DXEFFECTSTATEMANAGER 型別定義為這個介面的指標。


```
typedef interface ID3DXEffectStateManager ID3DXEffectStateManager;
typedef interface ID3DXEffectStateManager *LPD3DXEFFECTSTATEMANAGER;
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Effect。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[效果介面](dx9-graphics-reference-effects-interfaces.md)
</dt> </dl>

 

 
