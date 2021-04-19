---
description: 設定可變更動畫播放軌權數的事件索引鍵。將多個追蹤結合在一起時，權數會用來做為乘數。
ms.assetid: fb2859de-9e77-49dd-be48-a50e22e2fc3a
title: 'ID3DXAnimationController：： KeyTrackWeight 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.KeyTrackWeight
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 74f5e38392f6b4ac192f02b9d85421c8357a16ee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106997416"
---
# <a name="id3dxanimationcontrollerkeytrackweight-method"></a>ID3DXAnimationController：： KeyTrackWeight 方法

設定可變更動畫播放軌權數的事件索引鍵。將多個追蹤結合在一起時，權數會用來做為乘數。

## <a name="syntax"></a>語法


```C++
D3DXEVENTHANDLE KeyTrackWeight(
  [in] UINT                Track,
  [in] FLOAT               NewWeight,
  [in] DOUBLE              StartTime,
  [in] DOUBLE              Duration,
  [in] D3DXTRANSITION_TYPE Transition
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*追蹤* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

要修改之追蹤的識別碼。

</dd> <dt>

*NewWeight* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

曲目的新加權。

</dd> <dt>

*StartTime* \[在\]
</dt> <dd>

類型： **[ **DOUBLE**](../winprog/windows-data-types.md)**

全域時間索引鍵。 指定將進行變更的全域時間。

</dd> <dt>

*持續時間* \[在\]
</dt> <dd>

類型： **[ **DOUBLE**](../winprog/windows-data-types.md)**

轉換時間，指定順利完成轉換所需要的時間。

</dd> <dt>

*轉換* \[在\]
</dt> <dd>

類型： **[ **D3DXTRANSITION \_ 類型**](./d3dxtransition-type.md)**

指定用於在加權之間轉換的轉換類型。 請參閱 [**D3DXTRANSITION \_ 類型**](./d3dxtransition-type.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

優先權 blend 事件的事件控制碼。 如果有一或多個輸入參數無效，或沒有可用的事件，則會傳回 **Null** 。

## <a name="remarks"></a>備註

權數的使用方式就像乘數，用來決定要將這份追蹤與其他曲目結合在一起的程度。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9anim。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
