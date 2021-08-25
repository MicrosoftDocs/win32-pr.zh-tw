---
description: 設定指定動畫播放軌的優先順序混合加權。
ms.assetid: 8d40b0f6-d79a-42c1-99fb-3f76bd46f30c
title: 'ID3DXAnimationController：： SetTrackPriority 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetTrackPriority
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: be294710fcd6ec2d8e72c7d7c9437623d29a2729a52144d4edfdc91e5be7eea1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119848968"
---
# <a name="id3dxanimationcontrollersettrackpriority-method"></a>ID3DXAnimationController：： SetTrackPriority 方法

設定指定動畫播放軌的優先順序混合加權。

## <a name="syntax"></a>語法


```C++
HRESULT SetTrackPriority(
  [in] UINT              Track,
  [in] D3DXPRIORITY_TYPE Priority
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*追蹤* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

追蹤識別碼。

</dd> <dt>

*優先順序* \[在\]
</dt> <dd>

類型： **[ **D3DXPRIORITY \_ 類型**](./d3dxpriority-type.md)**

追蹤優先權。 這個參數應該設定為 [**D3DXPRIORITY \_ 類型**](./d3dxpriority-type.md)的其中一個常數。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 S \_ OK。 如果方法失敗，則會傳回下列值： D3DERR \_ INVALIDCALL。

## <a name="remarks"></a>備註

## <a name="requirements"></a>需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9anim。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
