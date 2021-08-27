---
description: 應用程式會使用 ID3DXEffectPool 介面來識別要在效果間共用的參數。 請參閱複製和共用 (Direct3D 9) 中的參數共用。 此介面沒有任何方法。
ms.assetid: dd5e55eb-9436-422d-9743-38be44d05962
title: 'ID3DXEffectPool 介面 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectPool
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 42b7669d974fffde76c8c8f1e7beb4f8d78bf58fda3810130b255d4bc5a693df
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120118678"
---
# <a name="id3dxeffectpool-interface"></a>ID3DXEffectPool 介面

應用程式會使用 **ID3DXEffectPool** 介面來識別要在效果間共用的參數。 請參閱 [複製和共用 (Direct3D 9) ](cloning-and-sharing.md)中的參數共用。 此介面沒有任何方法。

## <a name="members"></a>成員

**ID3DXEffectPool** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面，但沒有其他成員。

## <a name="remarks"></a>備註

ID3DXEffectPool 介面是藉由呼叫 [**D3DXCreateEffectPool**](d3dxcreateeffectpool.md)來取得。

LPD3DXEFFECTPOOL 型別定義為這個介面的指標。


```
typedef interface ID3DXEffectPool ID3DXEffectPool;
typedef interface ID3DXEffectPool *LPD3DXEFFECTPOOL;
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

 

 
