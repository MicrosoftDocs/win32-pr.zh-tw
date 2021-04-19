---
description: 將資料物件新增為 ID3DXFileSaveData 物件的子系。
ms.assetid: 710a1588-d766-4555-97a3-4b5a517ce805
title: 'ID3DXFileSaveObject：： AddDataObject 方法 (D3DX9Xof .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveObject.AddDataObject
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: d1586035a0d8a81c2210009bad903aac5197bcf7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106981826"
---
# <a name="id3dxfilesaveobjectadddataobject-method"></a>ID3DXFileSaveObject：： AddDataObject 方法

將資料物件新增為 [**ID3DXFileSaveData**](id3dxfilesavedata.md) 物件的子系。

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

資料物件名稱的指標。 如果物件沒有名稱，請指定 **Null** 。

</dd> <dt>

*pId* \[在\]
</dt> <dd>

類型： **Const [**GUID**](guid.md) \***

代表資料物件之 GUID 的指標。 如果物件沒有 GUID，請指定 **Null** 。

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

如果方法成功，則傳回值為 S \_ OK。 如果方法失敗，則傳回值可以是下列其中一項： D3DXFERR \_ BADOBJECT、DXFILEERR \_ BADVALUE、E \_ OUTOFMEMORY。

## <a name="remarks"></a>備註

如果資料參考物件將參考資料物件，則 >szname 或 pId 參數都必須為非 **Null**。

使用 [**ID3DXFileSaveObject：： save**](id3dxfilesaveobject--save.md) 方法將建立的資料儲存至磁片。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Xof。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXFileSaveObject](id3dxfilesaveobject.md)
</dt> </dl>

 

 
