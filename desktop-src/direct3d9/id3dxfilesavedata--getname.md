---
description: 抓取這個 ID3DXFileSaveData 檔資料節點的名稱。
ms.assetid: ea697d23-42e7-4661-b605-3654f6a31055
title: 'ID3DXFileSaveData：： GetName 方法 (D3DX9Xof .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData.GetName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 7aa6ef69a5296830b2f3bb992fb24ac23fa58adeeea629fd0e1bdeacf6173344
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119856647"
---
# <a name="id3dxfilesavedatagetname-method"></a>ID3DXFileSaveData：： GetName 方法

抓取這個 [**ID3DXFileSaveData**](id3dxfilesavedata.md) 檔資料節點的名稱。

## <a name="syntax"></a>語法


```C++
HRESULT GetName(
  [in]      LPSTR  szName,
  [in, out] SIZE_T *puiSize
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*>szname* \[在\]
</dt> <dd>

類型： **[ **LPSTR**](../winprog/windows-data-types.md)**

用來接收此檔案資料節點名稱之指標的位址。 如果此參數為 **Null**，則 *puiSize* 會傳回字串的大小。 如果 >szname 指向有效的記憶體，則會將這個檔案資料節點的名稱複製到 >szname 中，直到 *puiSize* 指定的字元數。

</dd> <dt>

*puiSize* \[in、out\]
</dt> <dd>

類型： **[**大小 \_ T**](../winprog/windows-data-types.md)\***

字串大小的指標，代表這個檔案資料節點的名稱。 如果 >szname 提供名稱的參考，則這個參數可以是 **Null** 。 如果 >szname 為 **Null**，此參數將會傳回字串的大小。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 S \_ OK。 如果方法失敗，則會傳回下列值： D3DXFERR \_ BADVALUE。

## <a name="remarks"></a>備註

若要讓這個方法成功， *>szname* 或 *puiSize* 必須為非 **Null**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Xof。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXFileSaveData](id3dxfilesavedata.md)
</dt> </dl>

 

 
