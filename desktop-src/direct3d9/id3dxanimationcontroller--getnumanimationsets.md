---
description: 傳回目前在動畫控制器中註冊的動畫集合數目。
ms.assetid: 1aacc84d-5025-4601-9a6c-84b3d9b06012
title: 'ID3DXAnimationController：： GetNumAnimationSets 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetNumAnimationSets
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 07a6eee85c515c4b8e923aa9973eddc648ef95cbc152c27951154a7c41fbcf3f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120026818"
---
# <a name="id3dxanimationcontrollergetnumanimationsets-method"></a>ID3DXAnimationController：： GetNumAnimationSets 方法

傳回目前在動畫控制器中註冊的動畫集合數目。

## <a name="syntax"></a>語法


```C++
UINT GetNumAnimationSets();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

類型： **[ **UINT**](../winprog/windows-data-types.md)**

動畫集合數目。

## <a name="remarks"></a>備註

控制器包含任意數目的動畫集合和追蹤。 您可以使用 [**RegisterAnimationOutput**](id3dxanimationcontroller--registeranimationoutput.md)註冊動畫集合。 呼叫 [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) 所建立的動畫控制器會自動註冊已載入的動畫集合。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9anim。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
