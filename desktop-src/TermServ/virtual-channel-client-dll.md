---
title: 虛擬通道用戶端 DLL
description: 虛擬通道應用程式的用戶端是在用戶端電腦上遠端桌面服務初始化期間載入的 DLL。 您必須在用戶端電腦上註冊 DLL。
ms.assetid: fca0505c-c4a9-4230-aeaa-ff3dfa62f581
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f8f9ba01db57de6dc030e6c47b09c4173156ef8f85e3969716ae6e10dfc069f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119423578"
---
# <a name="virtual-channel-client-dll"></a>虛擬通道用戶端 DLL

虛擬通道應用程式的用戶端是在用戶端電腦上遠端桌面服務初始化期間載入的 DLL。 您必須在用戶端電腦上註冊 DLL。 如需詳細資訊，請參閱 [虛擬通道用戶端註冊](virtual-channel-client-registration.md)。

用戶端 DLL 必須匯出 [**VirtualChannelEntry**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelentry) 函式，此函式會在初始化期間遠端桌面服務呼叫。 **VirtualChannelEntry** 進入點會接收 [**通道 \_ 進入 \_ 點**](/windows/win32/api/cchannel/ns-cchannel-channel_entry_points)結構的指標。 此結構包含用戶端 DLL 呼叫以存取虛擬通道之函式的指標。



| 函式                                                      | 描述                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**VirtualChannelInit**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelinit)<br/>   | 註冊用戶端要使用的虛擬通道名稱，並提供 [**VirtualChannelInitEvent**](/windows/desktop/api/Cchannel/nc-cchannel-channel_init_event_fn) 回呼函式，遠端桌面服務通知用戶端有關影響用戶端連接的事件。<br/> |
| [**VirtualChannelOpen**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelopen)<br/>   | 開啟指定虛擬通道的用戶端，並提供 [**VirtualChannelOpenEvent**](/windows/desktop/api/Cchannel/nc-cchannel-channel_open_event_fn) 回呼函式，遠端桌面服務通知用戶端有關影響虛擬通道的事件。<br/>                    |
| [**VirtualChannelWrite**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelwrite)<br/> | 將資料寫入虛擬通道。 遠端桌面服務將此資料傳送至虛擬通道的伺服器端。 伺服器端會呼叫 [**WTSVirtualChannelRead**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelread) 函數來讀取資料。<br/>                                             |
| [**VirtualChannelClose**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelclose)<br/> | 關閉虛擬通道。<br/>                                                                                                                                                                                                                                                  |



 

您的 DLL [**VirtualChannelEntry**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelentry) 函式必須呼叫 [**VirtualChannelInit**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelinit) 函式，以初始化虛擬通道的存取權。 當您呼叫 **VirtualChannelInit** 時，您必須將指標傳遞至 [**VirtualChannelInitEvent**](/windows/desktop/api/Cchannel/nc-cchannel-channel_init_event_fn) 回呼函數。 當初始化完成時，遠端桌面服務會呼叫這個回呼函式，並在建立與遠端桌面工作階段主機 (RD 工作階段主機) server 的連接時再次呼叫。

建立連接之後，您可以呼叫 [**VirtualChannelOpen**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelopen) 函式來開啟 [**VirtualChannelInit**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelinit) 呼叫所註冊的虛擬通道。 **VirtualChannelOpen** 呼叫會指定 [**VirtualChannelOpenEvent**](/windows/desktop/api/Cchannel/nc-cchannel-channel_open_event_fn)回呼函數的指標。

在 [**VirtualChannelOpen**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelopen) 呼叫傳回之後，您可以呼叫 [**VirtualChannelWrite**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelwrite) 函式來寫入虛擬通道。 寫入作業是非同步，因此除非遠端桌面服務呼叫您的 [**VirtualChannelOpenEvent**](/windows/desktop/api/Cchannel/nc-cchannel-channel_open_event_fn)函式來表示寫入作業已完成，否則您不能釋放或重複使用傳遞至 **VirtualChannelWrite** 的緩衝區。 當您呼叫 **VirtualChannelWrite** 時，您可以傳遞可識別寫入作業的使用者資料片段。 遠端桌面服務在呼叫 **VirtualChannelOpenEvent** 來通知您作業已完成時，會將此使用者資料傳遞回來。 在虛擬通道的伺服器端，伺服器增益集會呼叫 [**WTSVirtualChannelRead**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelread) 函數來讀取資料。

當伺服器模組將資料寫入虛擬通道時，遠端桌面服務也會呼叫您的 [**VirtualChannelOpenEvent**](/windows/desktop/api/Cchannel/nc-cchannel-channel_open_event_fn) 函數。 伺服器模組會呼叫 [**WTSVirtualChannelWrite**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelwrite) 函數，以將資料寫入至虛擬通道的伺服器端。

用戶端和伺服器模組可將任何大小的資料區塊寫入虛擬通道。 不過，在傳送資料之前，遠端桌面服務會將資料分割成通道 \_ 區塊 \_ 長度位元組的區塊。 遠端桌面服務會針對每個資料區塊呼叫 [**VirtualChannelOpenEvent**](/windows/desktop/api/Cchannel/nc-cchannel-channel_open_event_fn) 函數一次，而不會將資料重建成原始大小的區塊。 每次呼叫 **VirtualChannelOpenEvent** 時，都會指出區塊的大小、伺服器所寫入的總大小，以及資料是否構成伺服器所寫入之區塊的開頭、中間或結尾。

您可以呼叫 [**VirtualChannelClose**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelclose) 函數來關閉通道。 不過，您不需要呼叫它，因為當用戶端與伺服器中斷連線時，遠端桌面服務會自動關閉所有通道。

 

 





