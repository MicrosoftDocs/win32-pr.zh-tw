---
title: GetVolumeOperation 類別
description: 註冊當 GetVolumeAsync 啟動的非同步作業完成時叫用的事件處理常式，並提供方法來傳回作業的結果。
ms.assetid: F7BCE2AB-89B5-44CE-8BDF-347F2E3FD6C9
keywords:
- GetVolumeOperation 類別媒體串流 API
- GetVolumeOperation 類別媒體串流 API，說明
topic_type:
- apiref
api_name:
- GetVolumeOperation
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: edecfc68e243066ca8e0cda4df43d6ca9a654e04b538c9352c2d90624d5682ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972367"
---
# <a name="getvolumeoperation-class"></a>GetVolumeOperation 類別

註冊當 [**GetVolumeAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getvolumeasync) 啟動的非同步作業完成時叫用的事件處理常式，並提供方法來傳回作業的結果。

**GetVolumeOperation** 具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**GetVolumeOperation** 類別有這些方法。



| 方法                                              | 描述                                                                                                                      |
|:----------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------|
| [**GetResults**](getvolumeoperation-getresults.md) | 傳回 [**GetVolumeAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getvolumeasync)啟動的非同步作業結果。<br/> |



 

### <a name="properties"></a>屬性

**GetVolumeOperation** 類別具有這些屬性。



| 屬性                                                     | 存取類型           | 描述                                                                                                                                                                |
|:-------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Completed**](getvolumeoperation-completed.md)<br/> | 讀取/寫入<br/> | 取得或設定當 [**GetVolumeAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getvolumeasync) 啟動的非同步作業完成時叫用的事件處理常式。 <br/> |



 

 

