---
description: 用來解壓縮編碼的資料。 這通常是用來從檔案系統（例如 ZIP 檔案）載入資源。 從未壓縮的資源載入時，解壓縮階段不需要執行任何工作。
ms.assetid: 7f7e3ffd-8dac-403f-813b-d6d21d146fa7
title: 'ID3DX10DataLoader：:D ecompress 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10DataLoader.Decompress
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c9e532bae8cb121fc93f3fdf2a5a1ee23e597c66599277b73b3b36b15ebbb963
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119989118"
---
# <a name="id3dx10dataloaderdecompress-method"></a>ID3DX10DataLoader：:D ecompress 方法

用來解壓縮編碼的資料。 這通常是用來從檔案系統（例如 ZIP 檔案）載入資源。 從未壓縮的資源載入時，解壓縮階段不需要執行任何工作。

## <a name="syntax"></a>語法


```C++
HRESULT Decompress(
  [out] void   **ppData,
  [in]  SIZE_T *pcBytes
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppData* \[擴展\]
</dt> <dd>

類型： **void \* \***

要解壓縮之原始資料的指標。

</dd> <dt>

*pcBytes* \[在\]
</dt> <dd>

類型： **[**大小 \_ T**](../winprog/windows-data-types.md)\***

PpData 所指向之資料的大小。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。

## <a name="remarks"></a>備註

您可以繼承 [**ID3DX10DataLoader 介面**](id3dx10dataloader.md)，也可以重新定義其成員。 您可以重新定義解壓縮，以支援您自己的自訂檔案格式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX10。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>D3DX10 .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DX10DataLoader](id3dx10dataloader.md)
</dt> <dt>

[D3DX 介面](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
