---
title: IMsRdpInputSink 介面
description: 遠端桌面輸入接收器。
ms.assetid: ec30b64a-63bb-4f8f-8979-ab2ef9ece6b0
ms.tgt_platform: multiple
keywords:
- IMsRdpInputSink 介面遠端桌面服務
- IMsRdpInputSink 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- IMsRdpInputSink
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2167106577a005f6e4ba13ee77edcdbc77302efad9de00395fc7360ade4c5720
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058838"
---
# <a name="imsrdpinputsink-interface"></a>IMsRdpInputSink 介面

遠端桌面輸入接收器。

## <a name="members"></a>成員

**IMsRdpInputSink** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IMsRdpInputSink** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IMsRdpInputSink** 介面具有這些方法。



| 方法                                                               | 描述                          |
|:---------------------------------------------------------------------|:-------------------------------------|
| [**AddTouchInput**](/previous-versions/windows/desktop/legacy/mt786987(v=vs.85))               | 新增觸控輸入。<br/>         |
| [**BeginTouchFrame**](/previous-versions/windows/desktop/legacy/mt786988(v=vs.85))           | 開始觸控框架。<br/>        |
| [**EndTouchFrame**](/previous-versions/windows/desktop/legacy/mt786989(v=vs.85))               | 結束觸控框架。<br/>          |
| [**SendKeyboardEvent**](/previous-versions/windows/desktop/legacy/mt786990(v=vs.85))       | 傳送鍵盤事件。<br/>     |
| [**SendMouseButtonEvent**](/previous-versions/windows/desktop/legacy/mt786991(v=vs.85)) | 傳送滑鼠按鍵事件。<br/> |
| [**SendMouseMoveEvent**](/previous-versions/windows/desktop/legacy/mt786992(v=vs.85))     | 傳送滑鼠移動事件。<br/>   |
| [**SendMouseWheelEvent**](/previous-versions/windows/desktop/legacy/mt786993(v=vs.85))   | 傳送滑鼠滾輪事件。<br/>  |
| [**SendSyncEvent**](/previous-versions/windows/desktop/legacy/mt786994(v=vs.85))               | 傳送同步處理事件。<br/>         |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1<br/>                                                                 |
| 最低支援的伺服器<br/> | Windows Server 2012 R2<br/>                                                      |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpInputSink 定義為4606850E-76A7-4E28-A47E-C7174F619351<br/>     |



 

