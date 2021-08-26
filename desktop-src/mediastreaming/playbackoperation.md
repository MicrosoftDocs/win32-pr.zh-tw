---
title: PlaybackOperation 類別
description: 註冊事件處理常式，此處理程式會在其中一個 MediaRenderer 播放方法啟動的非同步作業完成時叫用，並提供方法來傳回作業的結果。
ms.assetid: 4899254A-C393-4D03-970F-CF272F4761B6
keywords:
- PlaybackOperation 類別媒體串流 API
- PlaybackOperation 類別媒體串流 API，說明
topic_type:
- apiref
api_name:
- PlaybackOperation
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cb0c1bad5fa3cef3223b4b2d6ca9a9ac4aac5523a2eff8cbaf7bcb6ebb884949
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092248"
---
# <a name="playbackoperation-class"></a>PlaybackOperation 類別

註冊事件處理常式，此處理程式會在其中一個 [**MediaRenderer**](mediarenderer.md) 播放方法啟動的非同步作業完成時叫用，並提供方法來傳回作業的結果。

**PlaybackOperation** 具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**PlaybackOperation** 類別有這些方法。



| 方法                                             | 描述                                                                                                                                |
|:---------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetResults**](playbackoperation-getresults.md) | 傳回由其中一個 [**MediaRenderer**](mediarenderer.md) 播放方法啟動的非同步作業結果。<br/> |



 

### <a name="properties"></a>屬性

**PlaybackOperation** 類別具有這些屬性。



| 屬性                                                    | 存取類型           | 描述                                                                                                                                                                           |
|:------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Completed**](playbackoperation-completed.md)<br/> | 讀取/寫入<br/> | 取得或設定當其中一個 [**MediaRenderer**](mediarenderer.md) 播放方法啟動的非同步作業完成時叫用的事件處理常式。 <br/> |



 

 

 





