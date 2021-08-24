---
description: 將資料物件新增為 ID3DXFileSaveData 檔資料節點的子系。
ms.assetid: 47faad99-3ee8-4ca8-b8d7-413d4cd5b090
title: 'ID3DXFileSaveData：： AddDataObject 方法 (D3DX9Xof .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData.AddDataObject
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: ed4b0abd35f9f53fb2111f40903e4b2b81a75c9d402a53fbb2fdb1cdc9a75750
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847838"
---
# <a name="id3dxfilesavedataadddataobject-method"></a>ID3DXFileSaveData：： AddDataObject 方法

將資料物件新增為 [**ID3DXFileSaveData**](id3dxfilesavedata.md) 檔資料節點的子系。

## <a name="syntax"></a>語法


```C++
HRESULT AddDataObject(
  [in]               REFGUID           rguidTemplate,
  [in]               LPCSTR            szName,
  [in]         const GUID              *pId,
  [in]               SIZE_T            cbSize,
  [in]               LPCVOID           pvData,
  [in, retval]       ID3DXFileSaveData **ppObj
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*rguidTemplate* \[在\]
</dt> <dd>

類型： **[REFGUID](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**

代表資料物件之範本的 GUID。

</dd> <dt>

*>szname* \[在\]
</dt> <dd>

類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**

要加入之資料物件名稱的指標。 如果物件沒有名稱，請指定 **Null** 。

</dd> <dt>

*pId* \[在\]
</dt> <dd>

類型： **Const [**GUID**](guid.md) \***

代表資料物件之 GUID 的指標。 資料物件必須已向 [**ID3DXFile：： RegisterTemplates**](id3dxfile--registertemplates.md) 或 [**ID3DXFile：： RegisterEnumTemplates**](id3dxfile--registerenumtemplates.md)註冊。 如果物件沒有 GUID，請指定 **Null** 。

</dd> <dt>

*cbSize* \[在\]
</dt> <dd>

類型： **[**大小 \_ T**](../winprog/windows-data-types.md)**

資料物件的大小（以位元組為單位）。

</dd> <dt>

*pvData* \[在\]
</dt> <dd>

類型： **[ **LPCVOID**](../winprog/windows-data-types.md)**

包含資料物件中所有必要資料之緩衝區的指標。

</dd> <dt>

*ppObj* \[在中，retval\]
</dt> <dd>

類型： **[ **ID3DXFileSaveData**](id3dxfilesavedata.md)\*\***

[**ID3DXFileSaveData**](id3dxfilesavedata.md)介面指標的位址，代表將加入資料物件的檔案資料節點。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 S \_ OK。 如果方法失敗，則傳回值可以是下列其中一項： D3DXFERR \_ BADOBJECT、D3DXFERR \_ BADVALUE、E \_ OUTOFMEMORY。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Xof。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXFileSaveData](id3dxfilesavedata.md)
</dt> </dl>

 

 
