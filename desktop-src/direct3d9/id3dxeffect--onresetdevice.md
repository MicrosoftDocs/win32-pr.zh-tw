---
description: 您可以使用這個方法來重新取得資源，並儲存初始狀態。
ms.assetid: 782f3537-f61c-4faa-a0b8-d60c516ba241
title: 'ID3DXEffect：： OnResetDevice 方法 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.OnResetDevice
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: d419ad456fcefbf0d6e4a201d4949556d6694e46
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106981996"
---
# <a name="id3dxeffectonresetdevice-method"></a>ID3DXEffect：： OnResetDevice 方法

您可以使用這個方法來重新取得資源，並儲存初始狀態。

## <a name="syntax"></a>語法


```C++
HRESULT OnResetDevice();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 S \_ OK。 如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。

## <a name="remarks"></a>備註

在呼叫任何其他方法之前，請使用 [**IDirect3DDevice9：： reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)) 來 (每次重設裝置時，都要呼叫 **ID3DXEffect：： OnResetDevice** 。 這是重新取得影片記憶體資源和捕捉狀態欄塊的絕佳位置。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Effect。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 
