---
description: 結束使用中的技術。
ms.assetid: 7297aa67-5cd4-4557-b5ef-faa6c27eaeb5
title: 'ID3DXEffect：： End 方法 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.End
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 6c93dc98febe2f5e539d3be678322860fe14069c2f8bf6b75cc42864b922e1f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748658"
---
# <a name="id3dxeffectend-method"></a>ID3DXEffect：： End 方法

結束使用中的技術。

## <a name="syntax"></a>語法


```C++
HRESULT End();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

這個方法一律會傳回值 S \_ OK。

## <a name="remarks"></a>備註

效果中的所有轉譯都是在成對的 [**ID3DXEffect：： Begin**](id3dxeffect--begin.md) 和 **ID3DXEffect：： End** 呼叫中完成。 轉譯所有傳遞之後，必須呼叫 **ID3DXEffect：： end** 以結束使用中的技術。 效果系統會使用在呼叫 **ID3DXEffect：： begin** 時建立的狀態欄塊來回應，以在 **ID3DXEffect：： begin** 之前自動還原管線狀態。

根據預設，效果系統會負責儲存技術之前的狀態，並在技術之後還原狀態。 如果您選擇停用此儲存和還原功能，請參閱 [D3DXFX \_ DONOTSAVESAMPLERSTATE](d3dxfx.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Effect。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 




