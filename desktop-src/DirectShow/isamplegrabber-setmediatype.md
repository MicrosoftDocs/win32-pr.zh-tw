---
description: SetMediaType 方法會在範例抓取的輸入釘選上指定連接的媒體類型。
ms.assetid: 9568832f-6666-45c9-9421-485c877affb3
title: 'ISampleGrabber：： SetMediaType 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.SetMediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 060ff0cc10fed441fdb2d6f2bf1bd0e66f3e8b9facec3cb52d8f270b350b1f4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117817699"
---
# <a name="isamplegrabbersetmediatype-method"></a>ISampleGrabber：： SetMediaType 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

方法會在範例抓取的 `SetMediaType` 輸入釘選上指定連接的媒體類型。

## <a name="syntax"></a>語法


```C++
HRESULT SetMediaType(
   const AM_MEDIA_TYPE *pType
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pType* 
</dt> <dd>

[**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type)結構的指標會指定所需的媒體類型。 不需要設定所有結構成員;如需詳細資訊，請參閱備註。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 S \_ OK。

## <a name="remarks"></a>備註

根據預設，範例抓取程式沒有慣用的媒體類型。 若要確保範例抓取程式會連接到正確的篩選，請在建立篩選圖形之前呼叫這個方法。

這個方法會限制篩選器將接受的媒體類型範圍。 當篩選器連線時，它會嘗試符合 *pType* 中提供的媒體類型。 若要這樣做，它會比較主要類型、子類型和格式類型 Guid （依該順序）。 針對上述每個 Guid，如果 *pType* 的值為 GUID \_ Null，範例會接受媒體類型，而不需要進行任何進一步的檢查。 如果 *pType* 有任何其他值，範例會將它與連線類型中的 GUID 做比較。 除非兩個 Guid 完全相符，否則範例捕獲會拒絕連接。

針對影片媒體類型，範例捕獲會忽略格式區塊。 因此，它會接受任何影片大小和畫面播放速率。 當您呼叫時 `SetMediaType` ，請將格式區塊 (**pbFormat**) 設定為 **Null** ，並將 (**cbFormat**) 大小設定為零。 針對音訊媒體類型，範例抓取程式將會檢查 [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) 結構，而且會要求其他篩選準則與該格式連接，除非 *pType* 中的格式區塊為 **Null**，或者格式標記為 WAVE \_ 格式 PCM， \_ 而其他結構成員為零。

範例 1：

-   主要類型：媒體類型 \_ 影片
-   子類型： GUID \_ Null
-   格式類型： GUID \_ Null

範例抓取會接受主要類型等於媒體類型的任何影片類型 \_ 。 它不會檢查子類型。

範例 2：

-   主要類型：媒體類型 \_ 影片
-   子類型： MEDIASUBTYPE \_ RGB24
-   格式類型： GUID \_ Null

現在，範例抓取會檢查子類型，並只接受 RGB 24 video。

**限制：** 無論您設定何種類型，範例捕獲篩選器都會拒絕任何具有由上而下方向的影片類型 (負面 *biHeight*) ，或格式類型為 \_ VideoInfo2。 在此情況下，雖然 `SetMediaType` 方法成功，但篩選準則將不會連接。

> [!Note]  
> 標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。

 

> [!Note]  
> 若要取得 Qedit，請下載[Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Qedit。h</dt> </dl>      |
| 程式庫<br/> | <dl> <dt>Strmiids .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[使用範例捕獲](using-the-sample-grabber.md)
</dt> <dt>

[**ISampleGrabber 介面**](isamplegrabber.md)
</dt> </dl>

 

 
