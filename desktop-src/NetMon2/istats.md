---
description: IStats 介面提供您用來將 NPP 連接到網路、捕捉網路流量、取出統計資料，以及將 NPP 從網路中斷連線的方法。 此介面會產生不含框架的統計資料。
ms.assetid: 57cfcdd6-f16c-4a1c-b2ba-ce98f0576862
title: 'IStats 介面 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: b64816589e3d4d0a2e3ace7be5c895e3d2cf22f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970228"
---
# <a name="istats-interface"></a>IStats 介面

**IStats** 介面提供您用來將 NPP 連接到網路、捕捉網路流量、取出統計資料，以及將 NPP 從網路中斷連線的方法。 此介面會產生不含框架的統計資料。

## <a name="members"></a>成員

**IStats** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IStats** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IStats** 介面具有這些方法。



| 方法                                                                | 描述                                                                                                                                               |
|:----------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**設定**](istats-configure.md)                                 | 設定捕獲檔案的觸發程式、模式比對和緩衝區大小。<br/>                                                                    |
| [**連接**](istats-connect.md)                                     | 將 NPP 連接到網路。<br/>                                                                                                               |
| [**中斷連線**](istats-disconnect.md)                               | 中斷 NPP 與網路的連線。<br/>                                                                                                          |
| [**GetControlState**](istats-getcontrolstate.md)                     | [*抓取 capture*](c.md)的狀態，指出 capture 正在執行或已暫停。<br/>                        |
| [**GetConversationStatistics**](istats-getconversationstatistics.md) | 抓取目前 capture 的 [*會話*](s.md) 和 [*工作站資訊*](s.md) 。<br/> |
| [**GetTotalStatistics**](istats-gettotalstatistics.md)               | 從目前執行中的 capture 解壓縮時間、緩衝區、驅動程式和其他網路統計資料。<br/>                                                |
| [**暫停**](istats-pause.md)                                         | 暫時停止目前的捕獲。<br/>                                                                                                         |
| [**QueryStations**](istats-querystations.md)                         | 抓取使用網路監視器在子網上捕獲資料的所有電腦清單。<br/>                                                  |
| [**QueryStatus**](istats-querystatus.md)                             | 抓取 NPP 的狀態。<br/>                                                                                                               |
| [**繼續**](istats-resume.md)                                       | 重新開機已暫停的捕獲。<br/>                                                                                                                     |
| [**開始**](istats-start.md)                                         | 開始捕獲。<br/>                                                                                                                            |
| [**停止**](istats-stop.md)                                           | 停止目前的捕獲。<br/>                                                                                                                     |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                                                                     |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll;</dt><dt>Rmtnpp.dll</dt> </dl> |



 

