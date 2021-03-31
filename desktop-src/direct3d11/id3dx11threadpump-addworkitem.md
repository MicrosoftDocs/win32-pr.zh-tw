---
title: 'ID3DX11ThreadPump Azuretasks 方法 (D3DX11core .h) '
description: 請注意，D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 將工作專案加入至執行緒抽取。
ms.assetid: 2578506c-6175-457a-bf10-94929bb3c0c4
keywords:
- Azuretasks 方法 Direct3D 11
- Azuretasks 方法 Direct3D 11，ID3DX11ThreadPump 介面
- ID3DX11ThreadPump 介面 Direct3D 11，Azuretasks 方法
topic_type:
- apiref
api_name:
- ID3DX11ThreadPump.AddWorkItem
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebf249405bd71287f93444ae8d23dab694027360
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322687"
---
# <a name="id3dx11threadpumpaddworkitem-method"></a>ID3DX11ThreadPump：： Azuretasks 方法

> [!Note]  
> D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。

 

將工作專案加入至執行緒抽取。

## <a name="syntax"></a>語法


```C++
HRESULT AddWorkItem(
  [in]  ID3DX11DataLoader    *pDataLoader,
  [in]  ID3DX11DataProcessor *pDataProcessor,
  [in]  HRESULT              *pHResult,
  [out] void                 **ppDeviceObject
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pDataLoader* \[在\]
</dt> <dd>

類型： **[ **ID3DX11DataLoader**](id3dx11dataloader.md)\***

當工作專案需要載入資料時，執行緒抽取將使用的載入器。

</dd> <dt>

*pDataProcessor* \[在\]
</dt> <dd>

類型： **[ **ID3DX11DataProcessor**](id3dx11dataprocessor.md)\***

當工作專案需要處理資料時，執行緒抽取將使用的處理器。

</dd> <dt>

*pHResult* \[在\]
</dt> <dd>

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***

傳回值的指標。 可能是 **Null**。

</dd> <dt>

*ppDeviceObject* \[擴展\]
</dt> <dd>

類型： **void \* \***

使用物件的裝置。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

傳回值是 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)中列出的其中一個值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX11core。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3DX11 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DX11ThreadPump](id3dx11threadpump.md)
</dt> <dt>

[D3DX 介面](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





