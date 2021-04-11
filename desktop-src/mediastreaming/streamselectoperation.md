---
title: StreamSelectOperation 類別
description: 註冊當 GetMuteAsync 啟動的非同步作業完成時叫用的事件處理常式，並提供方法來傳回作業的結果。 |StreamSelectOperation 類別
ms.assetid: 681142B4-AECD-42D0-A2D4-494E69A29025
keywords:
- StreamSelectOperation 類別媒體串流 API
- StreamSelectOperation 類別媒體串流 API，說明
topic_type:
- apiref
api_name:
- StreamSelectOperation
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a4a19ff2826f0f2ea3e5ef01841ce482d2f293a3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104196031"
---
# <a name="streamselectoperation-class"></a>StreamSelectOperation 類別

註冊當 [**GetMuteAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getmuteasync) 啟動的非同步作業完成時叫用的事件處理常式，並提供方法來傳回作業的結果。

**StreamSelectOperation** 具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**StreamSelectOperation** 類別有這些方法。



| 方法                                                 | 描述                                                                                                                                       |
|:-------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetResults**](streamselectoperation-getresults.md) | 傳回 [**SelectBestStreamAsync**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85))啟動的非同步作業結果。<br/> |



 

### <a name="properties"></a>屬性

**StreamSelectOperation** 類別具有這些屬性。



| 屬性                                                        | 存取類型           | Description                                                                                                                                                                             |
|:----------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Completed**](streamselectoperation-completed.md)<br/> | 讀取/寫入<br/> | 取得或設定當 [**SelectBestStreamAsync**](/previous-versions/windows/desktop/legacy/hh829002(v=vs.85)) 啟動的非同步作業完成時叫用的事件處理常式。<br/> |



 

 

