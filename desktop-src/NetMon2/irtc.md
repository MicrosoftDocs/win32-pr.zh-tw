---
description: IRTC 介面提供了用來將 NPP 連接到網路、捕捉網路流量、取出統計資料，以及將 NPP 從網路中斷連線的方法。
ms.assetid: 9252a9ba-2c3e-40b9-b8de-84ef5d4831a7
title: 'IRTC 介面 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: f330892da5844305d4d1f3ffa3aee0bf6e9ef50fb2a1cd951c332e2b17eb3b12
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118132927"
---
# <a name="irtc-interface"></a>IRTC 介面

**IRTC** 介面提供了用來將 NPP 連接到網路、捕捉網路流量、取出統計資料，以及將 NPP 從網路中斷連線的方法。 **IRTC** 會取得僅限本機進入點的介面，這是參與即時捕捉的必要專案。 此介面包含可將回呼交給 NPP 的方法。

## <a name="members"></a>成員

**IRTC** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IRTC** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IRTC** 介面具有這些方法。



| 方法                                                              | 描述                                                                                                                                             |
|:--------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**設定**](irtc-configure.md)                                 | 設定捕捉的觸發程式、模式比對和緩衝區大小。<br/>                                                                             |
| [**連線**](irtc-connect.md)                                     | 將 NPP 連接到網路。<br/>                                                                                                             |
| [**中斷連線**](irtc-disconnect.md)                               | 中斷 NPP 與網路的連線。<br/>                                                                                                        |
| [**GetControlState**](irtc-getcontrolstate.md)                     | [*抓取 capture*](c.md)的狀態，指出 capture 正在執行或已暫停。<br/>                      |
| [**GetConversationStatistics**](irtc-getconversationstatistics.md) | 抓取目前 capture 的 [*會話*](s.md) 和 [*站資訊*](s.md) 。<br/> |
| [**GetTotalStatistics**](irtc-gettotalstatistics.md)               | 從目前執行中的 capture 解壓縮時間、緩衝區、驅動程式和其他網路統計資料。<br/>                                              |
| [**暫停**](irtc-pause.md)                                         | 暫時停止目前的捕獲。<br/>                                                                                                       |
| [**QueryStations**](irtc-querystations.md)                         | 抓取子網上使用網路監視器來捕捉網路資料的所有電腦清單。<br/>                                        |
| [**QueryStatus**](irtc-querystatus.md)                             | 抓取 NPP 的狀態。<br/>                                                                                                             |
| [**繼續**](irtc-resume.md)                                       | 重新開機已暫停的捕獲。<br/>                                                                                                                   |
| [**開始**](irtc-start.md)                                         | 開始捕獲。<br/>                                                                                                                            |
| [**停止**](irtc-stop.md)                                           | 停止目前的捕獲。<br/>                                                                                                                   |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                                                                     |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll;</dt><dt>Rmtnpp.dll</dt> </dl> |



 

