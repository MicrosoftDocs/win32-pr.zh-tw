---
description: 設定可啟用或停用動畫播放軌的事件索引鍵。
ms.assetid: de81e646-0b94-40d3-89c2-060d118d17b2
title: 'ID3DXAnimationController：： KeyTrackEnable 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.KeyTrackEnable
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f22c732ff57e948ebcc2e89d790d352e4dc057ba
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322679"
---
# <a name="id3dxanimationcontrollerkeytrackenable-method"></a>ID3DXAnimationController：： KeyTrackEnable 方法

設定可啟用或停用動畫播放軌的事件索引鍵。

## <a name="syntax"></a>語法


```C++
D3DXEVENTHANDLE KeyTrackEnable(
  [in] UINT   Track,
  [in] BOOL   NewEnable,
  [in] DOUBLE StartTime
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*追蹤* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

要修改之動畫播放軌的識別碼。

</dd> <dt>

*NewEnable* \[在\]
</dt> <dd>

類型： **[ **BOOL**](../winprog/windows-data-types.md)**

啟用旗標。 將此設為 **TRUE** 以啟用動畫播放軌，或設定為 **FALSE** 以停用曲目。

</dd> <dt>

*StartTime* \[在\]
</dt> <dd>

類型： **[ **DOUBLE**](../winprog/windows-data-types.md)**

全域時間索引鍵。 指定將進行變更的全域時間。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

優先權 blend 事件的事件控制碼。 如果 Track 無效，則會傳回 **Null** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9anim。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
