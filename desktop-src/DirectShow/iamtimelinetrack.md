---
description: IAMTimelineTrack 介面提供在 DirectShow 編輯服務 (DES) 中操作追蹤物件的方法。追蹤包含在最終輸出中所呈現的來源清單。
ms.assetid: 42ac88f2-1361-413a-a9b0-95f5c32a7c3c
title: 'IAMTimelineTrack 介面 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 71003694d33b33980fb262f06f6b2e7aa55a70d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994894"
---
# <a name="iamtimelinetrack-interface"></a>IAMTimelineTrack 介面

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`IAMTimelineTrack`介面提供在 [DirectShow 編輯服務](directshow-editing-services.md) (DES) 中操作 *追蹤* 物件的方法。

追蹤包含在最終輸出中所呈現的來源清單。 相同播放軌內的來源可能不會重迭。 影片播放軌可以有效果和轉換。 轉譯引擎會在套用轉換之前套用效果。 音訊播放軌可以有效果，但不能有轉換。 如需詳細資訊，請參閱 [時間軸模型](the-timeline-model.md)。

若要建立 track 物件，請呼叫 [**IAMTimeline：： CreateEmptyNode**](iamtimeline-createemptynode.md) ，並提供值時間軸的 \_ 主要 \_ 類型 \_ 追蹤。 您可以查詢傳回的介面 **IAMTimelineObj** 指標 `IAMTimelineTrack` 。

## <a name="members"></a>成員

**IAMTimelineTrack** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **IAMTimelineTrack** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IAMTimelineTrack** 介面具有這些方法。



| 方法                                                          | 描述                                                                                                                                          |
|:----------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AreYouBlank**](iamtimelinetrack-areyoublank.md)             | 判斷此曲目是否為空白 (不包含任何來源物件) 。<br/>                                                                       |
| [**GetNextSrc**](iamtimelinetrack-getnextsrc.md)               | 搜尋播放程式在指定時間或之後出現的下一個來源的軌跡。<br/>                                                       |
| [**GetNextSrc2**](iamtimelinetrack-getnextsrc2.md)             | 使用指定的做為 [**REFTIME**](reftime.md) 值，在曲目中搜尋在指定時間或之後出現的下一個來源。<br/> |
| [**GetNextSrcEx**](iamtimelinetrack-getnextsrcex.md)           | 抓取指定來源之後的下一個來源。<br/>                                                                                     |
| [**GetSourcesCount**](iamtimelinetrack-getsourcescount.md)     | 抓取曲目中的來源數目。<br/>                                                                                             |
| [**GetSrcAtTime**](iamtimelinetrack-getsrcattime.md)           | 根據指定的界限條件，抓取最接近指定時間的來源物件。<br/>                                |
| [**GetSrcAtTime2**](iamtimelinetrack-getsrcattime2.md)         | 取得最接近指定時間的來源物件，指定為 [**REFTIME**](reftime.md) 值。<br/>                                   |
| [**InsertSpace**](iamtimelinetrack-insertspace.md)             | 分割存在於指定時間的任何物件，並在兩者之間插入空格。<br/>                                                       |
| [**InsertSpace2**](iamtimelinetrack-insertspace2.md)           | 使用 [**REFTIME**](reftime.md) 值，分割存在於指定時間的任何物件，並在兩者之間插入空格。<br/>              |
| [**MoveEverythingBy**](iamtimelinetrack-moveeverythingby.md)   | 不支援。<br/>                                                                                                                            |
| [**MoveEverythingBy2**](iamtimelinetrack-moveeverythingby2.md) | 不支援。<br/>                                                                                                                            |
| [**SrcAdd**](iamtimelinetrack-srcadd.md)                       | 將來源新增至曲目。<br/>                                                                                                               |
| [**ZeroBetween**](iamtimelinetrack-zerobetween.md)             | 從指定時間之間的曲目中移除所有專案。<br/>                                                                            |
| [**ZeroBetween2**](iamtimelinetrack-zerobetween2.md)           | 從指定時間（指定為 [**REFTIME**](reftime.md) 值）之間的追蹤中移除所有專案。<br/>                                |



 

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



 

 
