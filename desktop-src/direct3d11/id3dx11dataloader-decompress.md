---
title: 'ID3DX11DataLoader 解壓縮方法 (D3DX11core .h) '
description: 請注意，D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 解壓縮編碼的資料。
ms.assetid: 68579c86-9f77-444b-86b3-746cff745be8
keywords:
- 解壓縮方法 Direct3D 11
- 解壓縮方法 Direct3D 11，ID3DX11DataLoader 介面
- ID3DX11DataLoader 介面 Direct3D 11，解壓縮方法
topic_type:
- apiref
api_name:
- ID3DX11DataLoader.Decompress
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a4f2424d46748b33918c8b6870c07dbaf4486217f8f3ba7a0a64f881792b81c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633028"
---
# <a name="id3dx11dataloaderdecompress-method"></a>ID3DX11DataLoader：:D ecompress 方法

> [!Note]  
> D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，不支援 Windows Store 應用程式。

 

解壓縮編碼的資料。

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

類型： **[**大小 \_ T**](/windows/desktop/WinProg/windows-data-types)\***

PpData 所指向之資料的大小。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

傳回值是 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)中列出的其中一個值。

## <a name="remarks"></a>備註

使用這個方法可從檔案系統（例如 ZIP 檔案）載入資源。 從未壓縮的資源載入時，解壓縮階段不需要執行任何工作。

您可以繼承 [**ID3DX11DataLoader 介面**](id3dx11dataloader.md)，並重新定義其成員以支援自訂檔案格式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX11core。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3DX11 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DX11DataLoader](id3dx11dataloader.md)
</dt> <dt>

[D3DX 介面](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

