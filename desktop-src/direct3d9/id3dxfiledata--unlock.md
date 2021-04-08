---
description: 結束 ID3DXFileData：： Lock 所傳回之 ppData 指標的存留期。
ms.assetid: 6032ea1f-3c73-4157-ba3f-41ce9e73d64c
title: 'ID3DXFileData：： Unlock 方法 (D3DX9Xof .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.Unlock
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 8371b87152a6184f34a225b24d2de1b0fd21248f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103696704"
---
# <a name="id3dxfiledataunlock-method"></a>ID3DXFileData：： Unlock 方法

結束 [**ID3DXFileData：： Lock**](id3dxfiledata--lock.md)所傳回之 *ppData* 指標的存留期。

## <a name="syntax"></a>語法


```C++
BOOL Unlock();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

類型： **[ **BOOL**](../winprog/windows-data-types.md)**

傳回值為 S \_ OK。

## <a name="remarks"></a>備註

您必須確保 [**ID3DXFileData：： Lock**](id3dxfiledata--lock.md) 呼叫的數目符合 **ID3DXFileData：： Unlock** 呼叫的數目。 呼叫 Unlock 之後，不應該再使用 **ID3DXFileData：： Lock** 所傳回的 ppData 指標。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Xof。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXFileData](id3dxfiledata.md)
</dt> </dl>

 

 
