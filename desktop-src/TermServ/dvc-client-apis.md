---
title: DVC 用戶端 Api
description: 動態虛擬通道 (DVC) 用戶端 Api 專門針對連接的遠端桌面連線 (RDC) 用戶端。
ms.assetid: 976a6cc2-7bbe-4ecc-91b4-b7c659eca5ba
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 557f51adbf10562465f93a101e502632a791d5c272b278c5a8b7ea6124637913
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118130814"
---
# <a name="dvc-client-apis"></a>DVC 用戶端 Api

動態虛擬通道 (DVC) 用戶端 Api 專門針對連接的遠端桌面連線 (RDC) 用戶端。 某些 Api 是由 DVC 架構所執行，而有些則是由外掛程式開發人員所執行。 某些 Api 是用來支援遠端桌面連線 (RDC) 用戶端外掛程式，且不會與資料傳輸直接相關。

## <a name="in-this-section"></a>本節內容

<dl> <dt>

[**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin)
</dt> <dd>

允許遠端桌面連線 (RDC) 用戶端載入遠端桌面連線 (RDC) 用戶端外掛程式。

</dd> <dt>

[**IWTSListener**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistener)
</dt> <dd>

管理動態虛擬通道的每個接聽程式的設定 (DVC) 連接。

</dd> <dt>

[**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback)
</dt> <dd>

用來通知遠端桌面連線 (RDC) 用戶端外掛程式有關特定接聽程式上的傳入要求。

</dd> <dt>

[**IWTSVirtualChannelManager**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager)
</dt> <dd>

管理所有遠端桌面連線 (RDC) 用戶端外掛程式和動態虛擬通道 (DVC) 接聽項。

</dd> <dt>

[**IWTSVirtualChannel**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel)
</dt> <dd>

用來控制通道狀態，以及在通道上寫入。

</dd> <dt>

[**IWTSVirtualChannelCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelcallback)
</dt> <dd>

接收有關通道狀態變更或所收到資料的通知。

</dd> <dt>

[**IWTSVirtualChannelCallback2**](iwtsvirtualchannelcallback2.md)
</dt> <dd>

不支援此介面。

</dd> <dt>

[**VirtualChannelGetInstance**](virtualchannelgetinstance.md)
</dt> <dd>

呼叫以讓外掛程式為 DLL 所執行的所有外掛程式建立 [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) 介面的實例。

</dd> </dl>

 

 




