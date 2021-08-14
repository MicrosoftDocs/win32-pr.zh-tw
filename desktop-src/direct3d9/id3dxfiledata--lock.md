---
description: 存取. x 檔案資料。
ms.assetid: 0e92914b-47b3-4a88-87ba-ce3c14282dbb
title: 'ID3DXFileData：： Lock 方法 (D3DX9Xof .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.Lock
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: c052f570b3206c5a0661a4cf4ab38b259fb476f4eda1322df80e709608d09bf5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118520705"
---
# <a name="id3dxfiledatalock-method"></a>ID3DXFileData：： Lock 方法

存取. x 檔案資料。

## <a name="syntax"></a>語法


```C++
HRESULT Lock(
  [in]       SIZE_T *pSize,
  [in] const VOID   **ppData
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pSize* \[在\]
</dt> <dd>

類型： **[**大小 \_ T**](../winprog/windows-data-types.md)\***

. X 檔案資料大小的指標。

</dd> <dt>

*ppData* \[在\]
</dt> <dd>

類型： **CONST VOID \* \***

接收 [**ID3DXFileData**](id3dxfiledata.md) 檔案資料物件介面指標的指標位址。 請參閱＜備註＞。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 S \_ OK。 如果方法失敗，則會傳回下列值： D3DXFERR \_ BADVALUE。

## <a name="remarks"></a>備註

*PpData* 指標只在 **ID3DXFileData：： Lock** 期間有效 [**ID3DXFileData：： Unlock**](id3dxfiledata--unlock.md) sequence。 您可以進行多個鎖定呼叫。 不過，您必須確定鎖定呼叫的數目符合解除鎖定呼叫的數目。

由於檔案資料不保證會與位元組界限適當地對齊，因此您應該使用未對齊的指標來存取 *ppData* 。

傳回的參數值因為可能的檔案損毀而無法保證有效;因此，您的程式碼應該會驗證傳回的參數值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Xof。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXFileData](id3dxfiledata.md)
</dt> </dl>

 

 
