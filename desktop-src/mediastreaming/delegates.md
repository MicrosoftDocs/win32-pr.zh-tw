---
title: 委派
description: 媒體串流 API 提供下列事件處理常式函數。
ms.assetid: CDE7B829-D0D1-479D-9B35-4445E711AF58
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdb7dc8f0896c23e7b7cacc42070b454e4dbffc7e016ff978382bd48e837ac11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118236402"
---
# <a name="delegates"></a>委派

[媒體串流 API](media-streaming-api-portal.md)提供下列事件處理常式函數。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                   | 描述                                                                                                                                                                                                            |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ConnectionStatusHandler**](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85))<br/>                   | 代表將處理 [**ConnectionStatusChanged**](connectionstatuschanged.md) 事件的函式，該事件會通知用戶端裝置網路線上狀態中的變更。<br/>               |
| [**DeviceControllerFinderHandler**](/previous-versions/windows/desktop/legacy/hh828843(v=vs.85))<br/>       | 代表將處理 [**DeviceArrival**](devicearrival.md) 和 [**DeviceDeparture**](devicedeparture.md) 事件的函式，這些事件會通知用戶端快取裝置清單中的變更。<br/> |
| [**RenderingParametersUpdateHandler**](/previous-versions/windows/desktop/legacy/hh828994(v=vs.85))<br/> | 表示將處理 [**RenderingParametersUpdate**](renderingparametersupdate.md) 事件的函式，該事件會通知用戶端任何 DMR 轉譯控制項參數的更新。<br/>  |
| [**TransportParametersUpdateHandler**](/previous-versions/windows/desktop/legacy/hh829007(v=vs.85))<br/> | 表示將處理 [**TransportParametersUpdate**](transportparametersupdate.md) 事件的函式，該事件會通知用戶端對任何 DMR 的傳輸參數進行更新。<br/>          |



 

 

