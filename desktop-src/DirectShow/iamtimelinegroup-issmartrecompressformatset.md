---
description: IsSmartRecompressFormatSet 方法會判斷是否已針對群組設定智慧 recompression 格式。
ms.assetid: d2b7ecc7-2348-402d-8d96-e0922e06a685
title: 'IAMTimelineGroup：： IsSmartRecompressFormatSet 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.IsSmartRecompressFormatSet
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 078649fd42cd44596ff27558b29d14b6f8cbeddc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977541"
---
# <a name="iamtimelinegroupissmartrecompressformatset-method"></a>IAMTimelineGroup：： IsSmartRecompressFormatSet 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`IsSmartRecompressFormatSet`方法會判斷是否已針對群組設定智慧 recompression 格式。

## <a name="syntax"></a>語法


```C++
HRESULT IsSmartRecompressFormatSet(
   BOOL *pVal
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pVal* 
</dt> <dd>

接收布林值，指出是否已設定壓縮格式。 若 **為 TRUE**，則已設定壓縮格式。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

> [!Note]  
> 標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。

 

> [!Note]  
> 若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。 在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Qedit。h</dt> </dl>      |
| 程式庫<br/> | <dl> <dt>Strmiids .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IAMTimelineGroup 介面**](iamtimelinegroup.md)
</dt> <dt>

[錯誤和成功碼](error-and-success-codes.md)
</dt> </dl>

 

 




