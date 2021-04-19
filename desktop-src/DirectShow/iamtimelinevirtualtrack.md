---
description: IAMTimelineVirtualTrack 介面提供在 DirectShow 編輯服務 (DES) 中使用虛擬追蹤的方法。 組合和追蹤支援此介面。
ms.assetid: 69d1d2ea-d33f-406d-a9ca-ddfb890bed34
title: 'IAMTimelineVirtualTrack 介面 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineVirtualTrack
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2295f1c336270818242f0d992a369e6a66f9237a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978687"
---
# <a name="iamtimelinevirtualtrack-interface"></a>IAMTimelineVirtualTrack 介面

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`IAMTimelineVirtualTrack`介面提供在[DirectShow 編輯服務](directshow-editing-services.md) (DES) 中使用虛擬追蹤的方法。 組合和追蹤支援此介面。

## <a name="members"></a>成員

**IAMTimelineVirtualTrack** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **IAMTimelineVirtualTrack** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IAMTimelineVirtualTrack** 介面具有這些方法。



| 方法                                                               | 描述                                       |
|:---------------------------------------------------------------------|:--------------------------------------------------|
| [**SetTrackDirty**](iamtimelinevirtualtrack-settrackdirty.md)       | 不支援。<br/>                         |
| [**TrackGetPriority**](iamtimelinevirtualtrack-trackgetpriority.md) | 抓取物件的優先權層級。<br/> |



 

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



 

 
