---
description: 用來設定和查詢效果，以及選擇技術。 效果物件可以包含多個技術來呈現相同的效果。
ms.assetid: bffc64ab-12e7-44e9-b296-262b0459a68a
title: 'ID3DXEffect 介面 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c9f5bdcf90b3e0d317290a569984d1b72d248079de5b3b281325e66af6e443c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119494018"
---
# <a name="id3dxeffect-interface"></a>ID3DXEffect 介面

用來設定和查詢效果，以及選擇技術。 效果物件可以包含多個技術來呈現相同的效果。

## <a name="members"></a>成員

**ID3DXEffect** 介面繼承自 [**ID3DXBaseEffect**](id3dxbaseeffect.md)。 **ID3DXEffect** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ID3DXEffect** 介面具有這些方法。



| 方法                                                                | 描述                                                                                                                                                                                      |
|:----------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ApplyParameterBlock**](id3dxeffect--applyparameterblock.md)       | 將狀態欄塊中的值套用至目前的效果系統狀態。<br/>                                                                                                                 |
| [**開始**](id3dxeffect--begin.md)                                   | 啟動使用中的技術。<br/>                                                                                                                                                           |
| [**BeginParameterBlock**](id3dxeffect--beginparameterblock.md)       | 開始在參數區塊中捕捉狀態變更。<br/>                                                                                                                                   |
| [**BeginPass**](id3dxeffect--beginpass.md)                           | 在主動技術內開始進行。<br/>                                                                                                                                           |
| [**CloneEffect**](id3dxeffect--cloneeffect.md)                       | 建立效果的複本。<br/>                                                                                                                                                          |
| [**CommitChanges**](id3dxeffect--commitchanges.md)                   | 在轉譯之前，將作用中傳遞內發生的狀態變更傳播至裝置。<br/>                                                                                           |
| [**DeleteParameterBlock**](id3dxeffect--deleteparameterblock.md)     | 刪除參數區塊。<br/>                                                                                                                                                             |
| [**結束**](id3dxeffect--end.md)                                       | 結束使用中的技術。<br/>                                                                                                                                                             |
| [**EndParameterBlock**](id3dxeffect--endparameterblock.md)           | 停止捕獲效果參數狀態變更。<br/>                                                                                                                                        |
| [**EndPass**](id3dxeffect--endpass.md)                               | 結束主動傳遞。<br/>                                                                                                                                                                   |
| [**FindNextValidTechnique**](id3dxeffect--findnextvalidtechnique.md) | 搜尋下一個有效的技巧，從指定技術之後的技巧開始。<br/>                                                                                       |
| [**GetCurrentTechnique**](id3dxeffect--getcurrenttechnique.md)       | 取得目前的技巧。<br/>                                                                                                                                                           |
| [**GetDevice**](id3dxeffect--getdevice.md)                           | 捕獲與效果相關聯的裝置。<br/>                                                                                                                                      |
| [**>pooloperations.getpool**](id3dxeffect--getpool.md)                               | 取得共用參數集區的指標。<br/>                                                                                                                                      |
| [**GetStateManager**](id3dxeffect--getstatemanager.md)               | 取得效果狀態管理員。<br/>                                                                                                                                                         |
| [**IsParameterUsed**](id3dxeffect--isparameterused.md)               | 判斷技術是否使用參數。<br/>                                                                                                                                   |
| [**OnLostDevice**](id3dxeffect--onlostdevice.md)                     | 您可以使用此方法來釋放視訊記憶體資源的所有參考，並刪除所有 stateblocks。 只要裝置遺失或在重設裝置之前，都應該呼叫這個方法。<br/> |
| [**OnResetDevice**](id3dxeffect--onresetdevice.md)                   | 您可以使用這個方法來重新取得資源，並儲存初始狀態。<br/>                                                                                                                       |
| [**SetRawValue**](id3dxeffect--setrawvalue.md)                       | 使用記憶體複製來設定著色器常數的連續範圍。<br/>                                                                                                                        |
| [**SetStateManager**](id3dxeffect--setstatemanager.md)               | 設定效果狀態管理員。<br/>                                                                                                                                                         |
| [**SetTechnique**](id3dxeffect--settechnique.md)                     | 設定使用中的技術。<br/>                                                                                                                                                            |
| [**ValidateTechnique**](id3dxeffect--validatetechnique.md)           | 驗證技巧。<br/>                                                                                                                                                                 |



 

## <a name="remarks"></a>備註

ID3DXEffect 介面的取得方式是呼叫 [**D3DXCreateEffect**](d3dxcreateeffect.md)、 [**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md)或 [**D3DXCreateEffectFromResource**](d3dxcreateeffectfromresource.md)。

LPD3DXEFFECT 型別定義為這個介面的指標。


```
typedef interface ID3DXEffect ID3DXEffect;
typedef interface ID3DXEffect *LPD3DXEFFECT;
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Effect。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ID3DXBaseEffect**](id3dxbaseeffect.md)
</dt> <dt>

[效果介面](dx9-graphics-reference-effects-interfaces.md)
</dt> <dt>

[**D3DXCreateEffect**](d3dxcreateeffect.md)
</dt> <dt>

[**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md)
</dt> <dt>

[**D3DXCreateEffectFromResource**](d3dxcreateeffectfromresource.md)
</dt> </dl>

 

 




