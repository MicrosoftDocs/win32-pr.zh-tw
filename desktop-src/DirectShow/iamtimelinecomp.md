---
description: IAMTimelineComp 介面會將虛擬追蹤插入或抓取 (DES) 的 DirectShow 編輯服務組合。組合是圖層的集合，可作為單一的複合播放軌。
ms.assetid: b0a47303-9e3c-4b78-ac90-c5d8fce2b727
title: 'IAMTimelineComp 介面 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 645abbb9c5f61fcfd04e433c3cfc61b926ed403d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997752"
---
# <a name="iamtimelinecomp-interface"></a>IAMTimelineComp 介面

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

**IAMTimelineComp** 介面會將虛擬追蹤插入或抓取 (DES) 的 [DirectShow 編輯服務](directshow-editing-services.md)組合。

組合是圖層的集合，可作為單一的複合播放 *軌*。例如，包含兩個追蹤的組合，其之間的轉換可作為轉換 precomposited 的單一追蹤。 組合應只包含一種類型的媒體 (例如音訊或影片) ，但不會強制執行這項限制。 *虛擬追蹤* 是可位於組合中的任何物件，包括追蹤和其他組合。

時間軸中的最上層節點是 *群組*。 群組會同時執行 `IAMTimelineComp` 介面和 [**IAMTimelineGroup**](iamtimelinegroup.md) 介面。

若要建立組合物件，請呼叫 [**IAMTimeline：： CreateEmptyNode**](iamtimeline-createemptynode.md) ，其值時間軸 \_ 主要 \_ 類型為 \_ 複合。 您可以查詢傳回的介面 [**IAMTimelineObj**](iamtimelineobj.md) 指標 `IAMTimelineComp` 。 如需詳細資訊，請參閱 [時間軸模型](the-timeline-model.md) 和 [建立時間軸](constructing-a-timeline.md)。

## <a name="members"></a>成員

**IAMTimelineComp** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **IAMTimelineComp** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IAMTimelineComp** 介面具有這些方法。



| 方法                                                                       | 描述                                                                                                                                               |
|:-----------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetCountOfType**](iamtimelinecomp-getcountoftype.md)                     | 以遞迴方式抓取此組合中所包含之指定型別的物件數目及其所有虛擬追蹤。<br/>                      |
| [**GetNextVTrack**](iamtimelinecomp-getnextvtrack.md)                       | 抓取指定虛擬追蹤之後的下一個虛擬追蹤。<br/>                                                                              |
| [**GetRecursiveLayerOfType**](iamtimelinecomp-getrecursivelayeroftype.md)   | 執行此組合中所包含之虛擬追蹤的深度優先順序，並從該順序抓取 *n* 個虛擬追蹤。<br/> |
| [**GetRecursiveLayerOfTypeI**](iamtimelinecomp-getrecursivelayeroftypei.md) | 不支援。<br/>                                                                                                                                 |
| [**GetVTrack**](iamtimelinecomp-getvtrack.md)                               | 依指定的優先順序抓取虛擬追蹤。<br/>                                                                                         |
| [**VTrackGetCount**](iamtimelinecomp-vtrackgetcount.md)                     | 抓取組合中包含的虛擬追蹤數目。<br/>                                                                           |
| [**VTrackInsBefore**](iamtimelinecomp-vtrackinsbefore.md)                   | 依指定的優先順序將虛擬追蹤插入組合中。<br/>                                                                        |
| [**VTrackSwapPriorities**](iamtimelinecomp-vtrackswappriorities.md)         | 切換兩個追蹤的優先權層級。<br/>                                                                                                    |



 

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



 

 
