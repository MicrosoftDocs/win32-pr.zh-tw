---
description: IESP 介面提供將 NPP 連接到網路的方法、捕捉至 capture 檔案的網路流量、取出統計資料，以及將 NPP 從網路中斷連線。
ms.assetid: e483f501-4928-4bfd-b212-e100f2b8f64f
title: 'IESP 介面 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: e7420e21a9f2c6ac92712326fa4a51159c6303d3972756e7a47c0797f22a1d83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037428"
---
# <a name="iesp-interface"></a>IESP 介面

**IESP** 介面提供將 NPP 連接到網路的方法、捕捉至 capture 檔案的網路流量、取出統計資料，以及將 NPP 從網路中斷連線。 當您需要收集專屬 ESP 檔案格式的網路 [*對話統計資料*](c.md) 時，主要會使用此介面。

## <a name="members"></a>成員

**IESP** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IESP** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IESP** 介面具有這些方法。



| 方法                                          | 描述                                                                                                                        |
|:------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [**設定**](iesp-configure.md)             | 提交 capture 的設定資訊<br/>                                                                         |
| [**連線**](iesp-connect.md)                 | 將 NPP 連接到網路。<br/>                                                                                        |
| [**中斷連線**](iesp-disconnect.md)           | 中斷 NPP 與網路的連線。<br/>                                                                                   |
| [**GetControlState**](iesp-getcontrolstate.md) | [*抓取 capture*](c.md)的狀態，指出 capture 正在執行或已暫停。<br/> |
| [**暫停**](iesp-pause.md)                     | 暫時停止目前的捕獲。<br/>                                                                                  |
| [**QueryStations**](iesp-querystations.md)     | 抓取使用網路監視器在子網上捕獲資料的所有電腦清單。<br/>                           |
| [**QueryStatus**](iesp-querystatus.md)         | 抓取 NPP 的狀態。<br/>                                                                                        |
| [**繼續**](iesp-resume.md)                   | 繼續暫停的捕獲。<br/>                                                                                               |
| [**開始**](iesp-start.md)                     | 啟動 capture 並建立檔案。<br/>                                                                        |
| [**停止**](iesp-stop.md)                       | 停止目前的捕獲。<br/>                                                                                              |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                                                                     |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll;</dt><dt>Rmtnpp.dll</dt> </dl> |



 

