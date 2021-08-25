---
description: IDelaydC 介面會提供用來連線到網路的方法、捕捉至 capture 檔案的網路流量、取出統計資料，以及與網路中斷連線。
ms.assetid: ab275653-2377-4af6-a810-48515962c88c
title: 'IDelaydC 介面 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 1b6b965990435dd7b9a1758cc9bf8ac8001c747ae800225a90123da862032ed1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119890558"
---
# <a name="idelaydc-interface"></a>IDelaydC 介面

**IDelaydC** 介面會提供用來連線到網路的方法、捕捉至 capture 檔案的網路流量、取出統計資料，以及與網路中斷連線。

此介面會從網路資料流程捕獲框架，然後將畫面格複製到 capture 檔案。 網路監視器和 NPP 應用程式會使用此介面。 若要接收網路資料，目標 NIC 必須支援混合模式。

## <a name="members"></a>成員

**IDelaydC** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IDelaydC** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IDelaydC** 介面具有這些方法。



| 方法                                                                  | 描述                                                                                                                                             |
|:------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**設定**](idelaydc-configure.md)                                 | 提交用於捕捉的設定資訊。<br/>                                                                                        |
| [**連線**](idelaydc-connect.md)                                     | 將 NPP 連接到網路。<br/>                                                                                                             |
| [**中斷連線**](idelaydc-disconnect.md)                               | 中斷 NPP 與網路的連線。<br/>                                                                                                        |
| [**GetControlState**](idelaydc-getcontrolstate.md)                     | [*抓取 capture*](c.md)的狀態，指出 capture 正在執行或已暫停。<br/>                      |
| [**GetConversationStatistics**](idelaydc-getconversationstatistics.md) | 抓取目前 capture 的 [*會話*](s.md) 和 [*站資訊*](s.md) 。<br/> |
| [**GetTotalStatistics**](idelaydc-gettotalstatistics.md)               | 從目前執行中的 capture 解壓縮時間、緩衝區、驅動程式和其他網路統計資料。<br/>                                              |
| [**暫停**](idelaydc-pause.md)                                         | 暫時停止目前的捕獲。<br/>                                                                                                       |
| [**QueryStations**](idelaydc-querystations.md)                         | 抓取使用網路監視器在子網上捕獲資料的所有電腦清單。<br/>                                                      |
| [**QueryStatus**](idelaydc-querystatus.md)                             | 抓取 NPP 的狀態。<br/>                                                                                                             |
| [**繼續**](idelaydc-resume.md)                                       | 繼續暫停的捕獲。<br/>                                                                                                                    |
| [**開始**](idelaydc-start.md)                                         | 啟動 [*capture 並建立檔案。*](c.md)<br/>                                                           |
| [**停止**](idelaydc-stop.md)                                           | 停止目前的捕獲並關閉 [*capture*](c.md)檔案。<br/>                                                   |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                                                                     |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll;</dt><dt>Rmtnpp.dll</dt> </dl> |



 

