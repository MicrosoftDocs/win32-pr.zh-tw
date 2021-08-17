---
description: 將資料參考加入為這個 ID3DXFileSaveData 檔資料節點的子系。 資料參考會指向檔案資料物件。
ms.assetid: 75bfe91e-15ea-41f3-b1f7-071fb7f0093f
title: 'ID3DXFileSaveData：： AddDataReference 方法 (D3DX9Xof .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData.AddDataReference
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 862df88701cffd1059ca67e086cd49d05174bc66e9fa13807df2d2aeb0c9ff1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119121347"
---
# <a name="id3dxfilesavedataadddatareference-method"></a>ID3DXFileSaveData：： AddDataReference 方法

將資料參考加入為這個 [**ID3DXFileSaveData**](id3dxfilesavedata.md) 檔資料節點的子系。 資料參考會指向檔案資料物件。

## <a name="syntax"></a>語法


```C++
HRESULT AddDataReference(
  [in]       LPCSTR szName,
  [in] const GUID   *pId
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*>szname* \[在\]
</dt> <dd>

類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**

要以傳址方式加入之資料物件名稱的指標。 如果資料物件沒有名稱，請指定 **Null** 。

</dd> <dt>

*pId* \[在\]
</dt> <dd>

類型： **Const [**GUID**](guid.md) \***

GUID 的指標，代表要以傳址方式加入的資料物件。 如果是 **Null**，將會加入參考，指向資料物件，並以 >szname 指定的名稱。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 S \_ OK。 如果方法失敗，則傳回值可以是下列其中一項： D3DXFERR \_ BADOBJECT、D3DXFERR \_ BADVALUE、E \_ OUTOFMEMORY。

## <a name="remarks"></a>備註

所參考的檔案資料物件必須有名稱或 GUID。 File 資料物件也必須衍生自不同的父 [**ID3DXFileSaveData**](id3dxfilesavedata.md) 物件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Xof。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXFileSaveData](id3dxfilesavedata.md)
</dt> </dl>

 

 
