---
description: IAMTimelineSrc 介面會提供方法，在 (DES) 的 DirectShow 編輯服務中操作和設定來源物件上的屬性。
ms.assetid: 39a64718-1fac-4d90-8340-b712d3bad2ec
title: 'IAMTimelineSrc 介面 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 25733b1353bc0cbd92c40335a8d342473b03a806
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978611"
---
# <a name="iamtimelinesrc-interface"></a>IAMTimelineSrc 介面

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`IAMTimelineSrc`介面會提供方法，在 (DES) 的[DirectShow 編輯服務](directshow-editing-services.md)中操作和設定來源物件上的屬性。 來源物件代表來自媒體來源的一個資料流程。

您可以設定媒體開始和媒體停止時間，以在原始程式檔中使用部分資料。 這些值會指定來源物件的開頭和結尾，相對於原始媒體來源。 媒體時間可能與物件在時間軸上的開始和停止時間不同，可進行快速或緩慢的播放動作。 使用音訊來源 (時，會發生音調變化。 ) 

若要建立來源物件，請呼叫 [**IAMTimeline：： CreateEmptyNode**](iamtimeline-createemptynode.md) 與值時間軸的 \_ 主要 \_ 類型 \_ 來源。 您可以查詢所傳回的 **IAMTimelineSrc** 介面 [**IAMTimelineObj**](iamtimelineobj.md)指標。 如需詳細資訊，請參閱 [建立時間軸](constructing-a-timeline.md) 和 [使用來源](working-with-sources.md)。

## <a name="members"></a>成員

**IAMTimelineSrc** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **IAMTimelineSrc** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IAMTimelineSrc** 介面具有這些方法。



| 方法                                                    | 描述                                                                                              |
|:----------------------------------------------------------|:---------------------------------------------------------------------------------------------------------|
| [**FixMediaTimes**](iamtimelinesrc-fixmediatimes.md)     | 將指定的時間值四捨五入到最接近的框架界限。<br/>                               |
| [**FixMediaTimes2**](iamtimelinesrc-fixmediatimes2.md)   | 將指定的時間值（指定為 **REFTIME** 值）四捨五入至最接近的框架界限。<br/> |
| [**GetDefaultFPS**](iamtimelinesrc-getdefaultfps.md)     | 抓取來源物件的預設畫面播放速率。<br/>                                             |
| [**GetMediaLength**](iamtimelinesrc-getmedialength.md)   | 抓取此來源物件的媒體長度。<br/>                                             |
| [**GetMediaLength2**](iamtimelinesrc-getmedialength2.md) | 以 **REFTIME** 值形式抓取此來源物件的媒體長度。<br/>                     |
| [**GetMediaName**](iamtimelinesrc-getmedianame.md)       | 抓取此來源物件所表示之原始程式檔的名稱。<br/>                      |
| [**GetMediaTimes**](iamtimelinesrc-getmediatimes.md)     | 抓取媒體的開始和停止時間。<br/>                                                     |
| [**GetMediaTimes2**](iamtimelinesrc-getmediatimes2.md)   | 以 **REFTIME** 值形式抓取媒體開始和停止時間。<br/>                              |
| [**GetStreamNumber**](iamtimelinesrc-getstreamnumber.md) | 抓取來源物件目前的資料流程數目。<br/>                                    |
| [**GetStretchMode**](iamtimelinesrc-getstretchmode.md)   | 捕獲影片來源的延展模式。<br/>                                                 |
| [**IsNormalRate**](iamtimelinesrc-isnormalrate.md)       | 指出是否會以正常播放速率播放剪輯。<br/>                             |
| [**ModifyStopTime**](iamtimelinesrc-modifystoptime.md)   | 設定相對於時程表的停止時間。<br/>                                                 |
| [**ModifyStopTime2**](iamtimelinesrc-modifystoptime2.md) | 將停止時間設定為 **REFTIME** 值。<br/>                                                   |
| [**SetDefaultFPS**](iamtimelinesrc-setdefaultfps.md)     | 設定來源物件的預設畫面播放速率。<br/>                                                  |
| [**SetMediaLength**](iamtimelinesrc-setmedialength.md)   | 指定原始程式檔的持續時間。<br/>                                                    |
| [**SetMediaLength2**](iamtimelinesrc-setmedialength2.md) | 指定原始程式檔的持續時間，做為 **REFTIME** 值。<br/>                            |
| [**SetMediaName**](iamtimelinesrc-setmedianame.md)       | 指定此來源物件所表示之原始程式檔的名稱。<br/>                      |
| [**SetMediaTimes**](iamtimelinesrc-setmediatimes.md)     | 設定媒體停止和開始時間。<br/>                                                          |
| [**SetMediaTimes2**](iamtimelinesrc-setmediatimes2.md)   | 將媒體停止和開始時間設定為 **REFTIME** 值。<br/>                                   |
| [**SetStreamNumber**](iamtimelinesrc-setstreamnumber.md) | 指定要從與此來源物件相關聯之來源檔案讀取的資料流程。<br/>       |
| [**SetStretchMode**](iamtimelinesrc-setstretchmode.md)   | 設定影片來源的延展模式。<br/>                                                      |
| [**SpliceWithNext**](iamtimelinesrc-splicewithnext.md)   | 將此來源物件聯結至另一個來源物件。<br/>                                            |



 

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



 

 
