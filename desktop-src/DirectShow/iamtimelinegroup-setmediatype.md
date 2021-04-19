---
description: SetMediaType 方法會為群組設定未壓縮的媒體類型。
ms.assetid: 51778563-f119-42e0-826b-966324a85024
title: 'IAMTimelineGroup：： SetMediaType 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetMediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a7c5366525b51367a5348bc47b9acbe0fb799db4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106980171"
---
# <a name="iamtimelinegroupsetmediatype-method"></a>IAMTimelineGroup：： SetMediaType 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`SetMediaType`方法會為群組設定未壓縮的媒體類型。

## <a name="syntax"></a>語法


```C++
HRESULT SetMediaType(
  [in] AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pmt* \[在\]
</dt> <dd>

描述格式的 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type) 結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下列其中一個 **HRESULT** 值：



| 傳回碼                                                                                             | Description                                     |
|---------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                    | 成功。<br/>                             |
| <dl> <dt>**E \_ 指標**</dt> </dl>               | **Null** 指標引數。<br/>           |
| <dl> <dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt> </dl> | 指定的媒體類型無效。<br/> |



 

## <a name="remarks"></a>備註

以下是支援的媒體類型：

-   未壓縮的 RGB 影片
-   每圖元16位，555格式 (MEDIASUBTYPE \_ RGB555) 
-   每個圖元24個位 (MEDIASUBTYPE \_ RGB24) 
-   每圖元32位，Alpha (MEDIASUBTYPE \_ ARGB32，而非 MEDIASUBTYPE \_ RGB32) 
-   16位身歷聲 PCM 音訊 (MEDIASUBTYPE \_ PCM) 

影片類型必須使用格式 \_ VideoInfo 格式區塊的格式類型和 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) 。 不支援 [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) 格式。 此外，不支援 (*biHeight* < 0) 的上而下的影片格式。

若要指定群組的壓縮格式，請呼叫 [**IAMTimelineGroup：： SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md) 方法。

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

 

 




