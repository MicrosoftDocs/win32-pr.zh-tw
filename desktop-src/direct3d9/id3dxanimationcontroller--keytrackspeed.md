---
description: 設定可變更動畫播放軌播放速率的事件索引鍵。
ms.assetid: 217d3a2d-0fb7-4995-86ec-7a4e8420e338
title: 'ID3DXAnimationController：： KeyTrackSpeed 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.KeyTrackSpeed
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 09705dd03e7767e94b1508cf4951186a509a3c5b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106993918"
---
# <a name="id3dxanimationcontrollerkeytrackspeed-method"></a>ID3DXAnimationController：： KeyTrackSpeed 方法

設定可變更動畫播放軌播放速率的事件索引鍵。

## <a name="syntax"></a>語法


```C++
D3DXEVENTHANDLE KeyTrackSpeed(
  [in] UINT                Track,
  [in] FLOAT               NewSpeed,
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

*NewSpeed* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

動畫播放軌的新速度。

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

指定用於轉換速度的轉換類型。 請參閱 [**D3DXTRANSITION \_ 類型**](./d3dxtransition-type.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

優先權 blend 事件的事件控制碼。 如果有一或多個輸入參數無效，或沒有可用的事件，則會傳回 **Null** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9anim。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
