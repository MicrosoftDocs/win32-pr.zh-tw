---
description: 將工作專案加入至執行緒抽取。
ms.assetid: f07789dc-a3d5-4bad-9768-527e701271b8
title: 'ID3DX10ThreadPump：： Azuretasks 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10ThreadPump.AddWorkItem
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 43602019018a9751453eb93f4ffb9b1c29eada6caf120a6721522982c3355dfc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119609318"
---
# <a name="id3dx10threadpumpaddworkitem-method"></a>ID3DX10ThreadPump：： Azuretasks 方法

將工作專案加入至執行緒抽取。

## <a name="syntax"></a>語法


```C++
HRESULT AddWorkItem(
  [in]  ID3DX10DataLoader    *pDataLoader,
  [in]  ID3DX10DataProcessor *pDataProcessor,
  [in]  HRESULT              *pHResult,
  [out] void                 **ppDeviceObject
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pDataLoader* \[在\]
</dt> <dd>

類型： **[ **ID3DX10DataLoader**](id3dx10dataloader.md)\***

當工作專案需要載入資料時，執行緒抽取將使用的載入器。

</dd> <dt>

*pDataProcessor* \[在\]
</dt> <dd>

類型： **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\***

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

傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX10。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>D3DX10 .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DX10ThreadPump](id3dx10threadpump.md)
</dt> <dt>

[D3DX 介面](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




