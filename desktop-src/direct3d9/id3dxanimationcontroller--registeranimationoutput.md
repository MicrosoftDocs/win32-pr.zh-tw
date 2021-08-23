---
description: 將動畫輸出新增至動畫控制器，並註冊用於調整、旋轉和轉譯 (SRT) 轉換的指標。
ms.assetid: 8c3197bc-9d03-40ba-869b-151f9c8e96ba
title: 'ID3DXAnimationController：： RegisterAnimationOutput 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.RegisterAnimationOutput
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: dc48eb9f2fd6ee5fee6c04936801997145a5ea21542b9b5ff8ec6d257eee80e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987818"
---
# <a name="id3dxanimationcontrollerregisteranimationoutput-method"></a>ID3DXAnimationController：： RegisterAnimationOutput 方法

將動畫輸出新增至動畫控制器，並註冊用於調整、旋轉和轉譯 (SRT) 轉換的指標。

## <a name="syntax"></a>語法


```C++
HRESULT RegisterAnimationOutput(
  [in] LPCSTR         Name,
  [in] D3DXMATRIX     *pMatrix,
  [in] D3DXVECTOR3    *pScale,
  [in] D3DXQUATERNION *pRotation,
  [in] D3DXVECTOR3    *pTranslation
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*名稱* \[在\]
</dt> <dd>

類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**

動畫輸出的名稱。

</dd> <dt>

*pMatrix* \[在\]
</dt> <dd>

類型： **[ **D3DXMATRIX**](d3dxmatrix.md)\***

[**D3DXMATRIX**](d3dxmatrix.md)結構的指標，其中包含 SRT 轉換資料。 可以是 **Null**。

</dd> <dt>

*pScale* \[在\]
</dt> <dd>

類型： **[ **D3DXVECTOR3**](d3dxvector3.md)\***

[**D3DXVECTOR3**](d3dxvector3.md)向量的指標，可描述動畫集合的尺規。 可以是 **Null**。

</dd> <dt>

*pRotation* \[在\]
</dt> <dd>

類型： **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

[**D3DXQUATERNION**](d3dxquaternion.md)四元數的指標，該四元數描述動畫集合的旋轉。 可以是 **Null**。

</dd> <dt>

*pTranslation* \[在\]
</dt> <dd>

類型： **[ **D3DXVECTOR3**](d3dxvector3.md)\***

描述動畫集合轉譯的 [**D3DXVECTOR3**](d3dxvector3.md) 向量指標。 可以是 **Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 S \_ OK。 如果方法失敗，則傳回值可以是下列其中一個值： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。

## <a name="remarks"></a>備註

如果動畫輸出已經註冊，pMatrix 就會填入輸入轉換資料。

使用 [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) 建立的動畫集合會自動註冊所有載入的動畫集合。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9anim。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
