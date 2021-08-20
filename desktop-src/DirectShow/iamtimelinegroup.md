---
description: IAMTimelineGroup 介面會設定及抓取 DirectShow 編輯服務 (DES) 中群組的屬性。群組包含一或多個追蹤，而且可能有一或多個組合，而這些組合接著會包含統一類型的來源剪輯，例如影片或音訊。 群組是時間軸中最上層的組合，也會公開 IAMTimelineComp 介面。 時間軸可以包含多個群組。每個群組都有下列屬性。相關聯的媒體類型。群組轉譯的畫面播放速率，以每秒畫面格數 (FPS) 。 所有的編輯都會在四捨五入到最接近的框架界限時進行，如群組 FPS 設定所定義。優先權層級，用於以相同媒體類型的多個資料流程寫入檔案 (例如，兩部影片串流 AVI 檔案) 。若要建立群組物件，請呼叫 IAMTimeline：： CreateEmptyNode 與值時間軸的 \_ 主要 \_ 類型 \_ 群組。 您可以查詢所傳回的 IAMTimelineGroup 介面 IAMTimelineObj 指標。
ms.assetid: c24e5e0a-43a5-4ba7-ac28-6e2ebb341a38
title: 'IAMTimelineGroup 介面 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9356e3edef0b61c119ec4cca774e9ec5976ac3732e0f0a508d103bc22bb0fef0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118155504"
---
# <a name="iamtimelinegroup-interface"></a>IAMTimelineGroup 介面

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`IAMTimelineGroup`介面會設定[DirectShow 編輯服務](directshow-editing-services.md) (DES) 中群組的屬性。

群組包含一或多個追蹤，而且可能有一或多個組合，而這些組合接著會包含統一類型的來源剪輯，例如影片或音訊。 群組是時間軸中最上層的組合，也會公開 [**IAMTimelineComp**](iamtimelinecomp.md) 介面。 時間軸可以包含多個群組。

每個群組都有下列屬性。

-   相關聯的媒體類型。
-   群組轉譯的畫面播放速率，以每秒畫面格數 (FPS) 。 所有的編輯都會在四捨五入到最接近的框架界限時進行，如群組 FPS 設定所定義。
-   優先權層級，用於以相同媒體類型的多個資料流程寫入檔案 (例如，兩部影片串流 AVI 檔案) 。

若要建立群組物件，請呼叫 [**IAMTimeline：： CreateEmptyNode**](iamtimeline-createemptynode.md) 與值時間軸的 \_ 主要 \_ 類型 \_ 群組。 您可以查詢所傳回的 **IAMTimelineGroup** 介面 [**IAMTimelineObj**](iamtimelineobj.md)指標。

## <a name="members"></a>成員

**IAMTimelineGroup** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **IAMTimelineGroup** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IAMTimelineGroup** 介面具有這些方法。



| 方法                                                                            | 描述                                                                                     |
|:----------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [**ClearRecompressFormatDirty**](iamtimelinegroup-clearrecompressformatdirty.md) | 不支援。<br/>                                                                       |
| [**GetGroupName**](iamtimelinegroup-getgroupname.md)                             | 抓取群組的應用程式定義名稱。<br/>                                 |
| [**GetMediaType**](iamtimelinegroup-getmediatype.md)                             | 抓取群組的未壓縮媒體類型。<br/>                                 |
| [**GetOutputBuffering**](iamtimelinegroup-getoutputbuffering.md)                 | 抓取預覽期間預先轉譯的畫面格數目。<br/>                   |
| [**GetOutputFPS**](iamtimelinegroup-getoutputfps.md)                             | 捕獲此群組的輸出畫面播放速率。<br/>                                       |
| [**GetPreviewMode**](iamtimelinegroup-getpreviewmode.md)                         | 抓取群組的預覽模式。<br/>                                            |
| [**GetPriority**](iamtimelinegroup-getpriority.md)                               | 抓取群組的優先順序。<br/>                                                      |
| [**GetSmartRecompressFormat**](iamtimelinegroup-getsmartrecompressformat.md)     | 抓取 smart recompression 目前的壓縮格式。<br/>                    |
| [**GetTimeline**](iamtimelinegroup-gettimeline.md)                               | 抓取此群組所屬的時間軸。<br/>                                  |
| [**IsRecompressFormatDirty**](iamtimelinegroup-isrecompressformatdirty.md)       | 不支援。<br/>                                                                       |
| [**IsSmartRecompressFormatSet**](iamtimelinegroup-issmartrecompressformatset.md) | 判斷是否已針對群組設定智慧壓縮格式。<br/>                 |
| [**SetGroupName**](iamtimelinegroup-setgroupname.md)                             | 設定群組的應用程式定義名稱。<br/>                                      |
| [**SetMediaType**](iamtimelinegroup-setmediatype.md)                             | 設定群組的未壓縮媒體類型。<br/>                                      |
| [**SetMediaTypeForVB**](iamtimelinegroup-setmediatypeforvb.md)                   | 指定 Automation 用戶端的群組媒體類型。<br/>                              |
| [**SetOutputBuffering**](iamtimelinegroup-setoutputbuffering.md)                 | 指定預覽期間預先轉譯的畫面格數目。<br/>                   |
| [**SetOutputFPS**](iamtimelinegroup-setoutputfps.md)                             | 設定此群組的未壓縮輸出畫面播放速率。<br/>                              |
| [**SetPreviewMode**](iamtimelinegroup-setpreviewmode.md)                         | 設定群組的預覽模式。<br/>                                                 |
| [**SetRecompFormatFromSource**](iamtimelinegroup-setrecompformatfromsource.md)   | 使用來源檔案中的壓縮格式，設定影片 recompression 格式。<br/> |
| [**SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md)     | 指定用於智慧型 recompression 的壓縮格式。<br/>                       |
| [**SetTimeline**](iamtimelinegroup-settimeline.md)                               | 不支援。<br/>                                                                       |



 

## <a name="remarks"></a>備註

> [!Note]  
> 標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。

 

> [!Note]  
> 若要取得 Qedit，請下載[Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Qedit。h</dt> </dl>      |
| 程式庫<br/> | <dl> <dt>Strmiids .lib</dt> </dl> |



 

 
