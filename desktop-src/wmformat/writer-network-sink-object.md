---
title: 寫入器網路接收物件
description: 寫入器網路接收物件
ms.assetid: f7765b42-693a-4f48-b750-17579e860b6d
keywords:
- Windows媒體格式 SDK，寫入器網路接收物件
- Advanced Systems Format (ASF) 、writer 網路接收物件
- ASF (Advanced 系統格式) 、寫入器網路接收物件
- 物件，寫入器網路接收物件
- 寫入器網路接收物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2011fd161fc4ac5e1cd03d955f06259e6499e343970cc309b1e8c41db051a32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843723"
---
# <a name="writer-network-sink-object"></a>寫入器網路接收物件

寫入器網路接收物件是用來將數位媒體寫入至網路。

寫入器網路接收物件是由函式 [**WMCreateWriterNetworkSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriternetworksink)所建立，它會將指標設定為 **IWMWriterNetworkSink** 介面。 您可以藉由呼叫 **QueryInterface** 方法來取得寫入器網路接收物件的其他介面。



| 介面                                              | 描述                                                                                                                                                                                                     |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMClientConnections**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmclientconnections)   | 收集連線用戶端的資訊。                                                                                                                                                                      |
| [**IWMClientConnections2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmclientconnections2) | 抓取 advanced 用戶端資訊。                                                                                                                                                                          |
| [**IWMRegisterCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback)     | 讓應用程式從物件取得狀態訊息。                                                                                                                                                 |
| [**IWMWriterNetworkSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriternetworksink)   | 開啟和關閉埠、設定和抓取可連接至接收器物件的用戶端數目上限、設定寫入器物件所要使用的網路通訊協定，以及執行其他的 advanced 函數。 |
| [**IWMWriterSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink)                 | 配置記憶體、判斷接收是否即時運作，以及處理數個回呼函數。                                                                                                |



 

下列回呼介面可以由應用程式執行，以追蹤寫入器網路接收物件的進度。



| 介面                                      | 描述                                                                    |
|------------------------------------------------|--------------------------------------------------------------------------------|
| [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | 必須將狀態資訊傳達給主應用程式時，才需要此資訊。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**廣播 ASF 資料**](broadcasting-asf-data.md)
</dt> <dt>

[**物件**](objects.md)
</dt> <dt>

[**使用寫入器接收器**](working-with-writer-sinks.md)
</dt> </dl>

 

 




