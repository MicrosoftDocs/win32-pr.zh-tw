---
description: ID3DXAnimationSet：： GetCallback 方法-取得動畫集中特定回呼的相關資訊。
ms.assetid: e8388bfc-5438-4216-a98f-dd0dbca12c87
title: 'ID3DXAnimationSet：： GetCallback 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet.GetCallback
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4ded66bbe90320250667511d1c9468073693ce789cdb7add8574f42a4756136d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120026588"
---
# <a name="id3dxanimationsetgetcallback-method"></a>ID3DXAnimationSet：： GetCallback 方法

取得動畫集中特定回呼的相關資訊。

## <a name="syntax"></a>語法


```C++
HRESULT GetCallback(
  [in]  DOUBLE Position,
  [in]  DWORD  Flags,
  [out] DOUBLE *pCallbackPosition,
  [out] LPVOID *ppCallbackData
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*位置* \[在\]
</dt> <dd>

類型： **[ **DOUBLE**](../winprog/windows-data-types.md)**

要尋找回呼的位置。

</dd> <dt>

*旗標* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

回呼搜尋旗標。 這個參數可以設定為 [**D3DXCALLBACK \_ 搜尋 \_ 旗標**](./d3dxcallback-search-flags.md)中一或多個旗標的組合。

</dd> <dt>

*pCallbackPosition* \[擴展\]
</dt> <dd>

類型： **[ **DOUBLE**](../winprog/windows-data-types.md)\***

回呼位置的指標。

</dd> <dt>

*ppCallbackData* \[擴展\]
</dt> <dd>

類型： **[ **LPVOID**](../winprog/windows-data-types.md)\***

回呼資料指標的位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

這個方法的傳回值是由應用程式設計人員所執行。 一般情況下，如果沒有發生錯誤，請將方法程式設計為傳回「D3D \_ 正常」。 否則，請將方法程式設計成從 [D3DERR](d3derr.md) 或 [**D3DXERR**](./d3dxerr.md)傳回適當的錯誤訊息。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9anim。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXAnimationSet](id3dxanimationset.md)
</dt> </dl>

 

 
