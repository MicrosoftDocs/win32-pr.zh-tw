---
description: SetRecompFormatFromSource 方法會使用原始檔中的壓縮格式來設定影片 recompression 格式。
ms.assetid: 2d42876a-524b-454d-b4f1-353afe3a4d28
title: 'IAMTimelineGroup：： SetRecompFormatFromSource 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetRecompFormatFromSource
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: adf4bfcf9d76ed40092eba7c612f4213c7aacb0d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106980170"
---
# <a name="iamtimelinegroupsetrecompformatfromsource-method"></a>IAMTimelineGroup：： SetRecompFormatFromSource 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`SetRecompFormatFromSource`方法會使用原始檔中的壓縮格式來設定影片 recompression 格式。

## <a name="syntax"></a>語法


```C++
HRESULT SetRecompFormatFromSource(
   IAMTimelineSrc *pSource
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pSource* 
</dt> <dd>

來源物件之 [**IAMTimelineSrc**](iamtimelinesrc.md) 介面的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值如下。



| 傳回碼                                                                                             | Description                                                                                            |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                    | 成功。<br/>                                                                                    |
| <dl> <dt>**E \_ NO \_ 時間軸**</dt> </dl>          | 群組不在時間軸內。<br/>                                                         |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>           | 記憶體不足。<br/>                                                                        |
| <dl> <dt>**E \_ 指標**</dt> </dl>               | **Null** 指標引數。<br/>                                                                  |
| <dl> <dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt> </dl> | 媒體類型無效。 群組不是影片群組，或原始程式檔沒有影片串流。<br/> |



 

## <a name="remarks"></a>備註

這個方法會尋找與 *pSource* 相關聯的原始程式檔、捕獲檔案中第一個影片資料流程的媒體類型，並使用該類型設定群組壓縮格式。 如需壓縮格式的詳細資訊，請參閱 [**IAMTimelineGroup：： SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md)。

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

 

 




