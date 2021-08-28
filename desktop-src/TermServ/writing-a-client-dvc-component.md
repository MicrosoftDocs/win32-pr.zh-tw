---
title: 撰寫用戶端 DVC 模組
description: 若要 (DVC) 用戶端模組寫入動態虛擬通道，您必須先執行並註冊遠端桌面連線 (RDC) 用戶端外掛程式。
ms.assetid: b6f475d4-d2ad-41ce-b3b9-d844fbd23cf0
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faa9f365034ff7771baf8eaeca102d7156f592e71d0cedffc97cef6d75b81fae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008260"
---
# <a name="writing-a-client-dvc-module"></a>撰寫用戶端 DVC 模組

若要 (DVC) 用戶端模組寫入動態虛擬通道，您必須先執行並註冊遠端桌面連線 (RDC) 用戶端外掛程式。 DVC 外掛程式是 [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin)的實作為元件物件模型， (COM) 物件來註冊。

> [!Note]  
> 外掛程式必須在自由執行緒模式中執行。 不支援單元模型執行。

 

以下是由外掛程式具現化的物件所執行的介面清單。



| 介面                                                        | 描述                                                                                                                                                                                          |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin)                                 | 允許遠端桌面連線 (RDC) 用戶端載入遠端桌面連線 (RDC) 用戶端外掛程式。<br/>                                                                 |
| [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback)             | 通知遠端桌面連線 (RDC) 用戶端外掛程式有關特定接聽程式上的傳入要求。<br/>                                                                             |
| [**IWTSVirtualChannelCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelcallback) | 接收有關通道狀態變更或所收到資料的通知。 這個介面的每個實例都與一個 [**IWTSVirtualChannel**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel)的實例相關聯。<br/> |



 

以下是由遠端桌面連線 (RDC) 用戶端所具現化的物件所執行的介面清單，而且是架構的一部分。



| 介面                                                      | 描述                                                                                                        |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [**IWTSVirtualChannelManager**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager) | 管理所有遠端桌面連線 (RDC) 用戶端外掛程式、DVC 接聽程式或靜態虛擬通道。<br/> |
| [**IWTSListener**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistener)                           | 管理 DVC 連接之每個接聽程式的設定。<br/>                                |
| [**IWTSVirtualChannel**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel)               | 控制通道狀態，以及在通道上寫入。<br/>                                           |



 

下圖顯示遠端桌面連線 (RDC) 用戶端與遠端桌面連線 (RDC) 用戶端外掛程式之間的關聯性。

![用戶端和外掛程式的關聯性](images/tsclient.png)

 

 





