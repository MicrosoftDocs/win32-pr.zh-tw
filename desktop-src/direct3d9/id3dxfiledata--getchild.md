---
description: 抓取這個檔案資料物件中的子物件。
ms.assetid: 0c4f1efa-f096-443d-a482-a3c5a9138c3d
title: 'ID3DXFileData：： System.windows.media.visualtreehelper.getchild 方法 (D3DX9Xof .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.GetChild
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 37982ca1e4801b7d70bec503ff9510fc66772651
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946158"
---
# <a name="id3dxfiledatagetchild-method"></a>ID3DXFileData：： System.windows.media.visualtreehelper.getchild 方法

抓取這個檔案資料物件中的子物件。

## <a name="syntax"></a>語法


```C++
HRESULT GetChild(
  [in] SIZE_T        uiChild,
  [in] ID3DXFileData **ppChild
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*uiChild* \[在\]
</dt> <dd>

類型： **[**大小 \_ T**](../winprog/windows-data-types.md)**

要取出之子物件的識別碼。

</dd> <dt>

*ppChild* \[在\]
</dt> <dd>

類型： **[ **ID3DXFileData**](id3dxfiledata.md)\*\***

用來接收子物件介面指標之指標的位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 S \_ OK。 如果方法失敗，則傳回值可以是下列其中一個值： D3DXFERR \_ BADVALUE，D3DXFERR \_ NOMOREOBJECTS。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Xof。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXFileData](id3dxfiledata.md)
</dt> </dl>

 

 
