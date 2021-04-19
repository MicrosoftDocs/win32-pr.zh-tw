---
title: Windows 事件記錄檔列舉
description: Windows 事件記錄檔會定義下列列舉。
ms.assetid: 2dd0e9ef-057b-4d0a-8b21-e7f14e5ae6e3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c019a090d1a12e30948e5ed1f5672853caed848c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106966204"
---
# <a name="windows-event-log-enumerations"></a>Windows 事件記錄檔列舉

Windows 事件記錄檔會定義下列列舉。



| 列舉型別                                                                          | 描述                                                                                                                        |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**.EVT \_ 通道 \_ 時鐘 \_ 類型**](/windows/desktop/api/WinEvt/ne-winevt-evt_channel_clock_type)                          | 定義值，這些值會指定記錄事件通道時要使用的時間戳記型別。                                         |
| [**.EVT \_ 通道 \_ 設定 \_ 屬性 \_ 識別碼**](/windows/desktop/api/WinEvt/ne-winevt-evt_channel_config_property_id)         | 定義識別通道設定屬性的識別碼。                                                   |
| [**.EVT \_ 通道 \_ 隔離 \_ 類型**](/windows/desktop/api/WinEvt/ne-winevt-evt_channel_isolation_type)                  | 定義要套用至通道的預設存取權限。                                                                    |
| [**.EVT \_ 通道 \_ 參考 \_ 旗標**](/windows/desktop/api/WinEvt/ne-winevt-evt_channel_reference_flags)                | 定義值，這些值會指定參考通道的方式。                                                                       |
| [**.EVT \_ 通道 \_ SID \_ 類型**](/windows/desktop/api/WinEvt/ne-winevt-evt_channel_sid_type)                              | 定義值，這些值會判斷事件是否包含記錄事件之主體 (SID) 的安全識別碼。 |
| [**.EVT \_ 通道 \_ 類型**](/windows/desktop/api/WinEvt/ne-winevt-evt_channel_type)                                       | 定義通道的類型。                                                                                                     |
| [**.EVT \_ 事件 \_ 中繼資料 \_ 屬性 \_ 識別碼**](/windows/desktop/api/WinEvt/ne-winevt-evt_event_metadata_property_id)         | 定義識別事件定義之中繼資料屬性的識別碼。                                              |
| [**.EVT \_ 事件 \_ 屬性 \_ 識別碼**](/windows/desktop/api/WinEvt/ne-winevt-evt_event_property_id)               | 定義值，以決定要取出的查詢資訊。                                                               |
| [**.EVT \_ EXPORTLOG \_ 旗標**](/windows/desktop/api/WinEvt/ne-winevt-evt_exportlog_flags)                                 | 定義指出事件是否來自通道或記錄檔的值。                                                   |
| [**.EVT \_ 格式 \_ 訊息 \_ 旗標**](/windows/desktop/api/WinEvt/ne-winevt-evt_format_message_flags)                      | 定義值，這些值會指定事件中要格式化的訊息字串。                                                       |
| [**.EVT \_ 記錄 \_ 屬性 \_ 識別碼**](/windows/desktop/api/WinEvt/ne-winevt-evt_log_property_id)                                | 定義識別通道或記錄檔之記錄檔中繼資料屬性的識別碼。                                   |
| [**.EVT \_ 登入 \_ 類別**](/windows/desktop/api/WinEvt/ne-winevt-evt_login_class)                                         | 定義您可以用來連接到遠端電腦的連接方法類型。                                             |
| [**.EVT \_ 開啟 \_ 記錄 \_ 旗標**](/windows/desktop/api/WinEvt/ne-winevt-evt_open_log_flags)                                  | 定義值，這個值會指定是否要開啟通道或匯出的記錄檔。                                                    |
| [**.EVT \_ 發行者 \_ 中繼資料 \_ 屬性 \_ 識別碼**](/windows/desktop/api/WinEvt/ne-winevt-evt_publisher_metadata_property_id) | 定義識別提供者之中繼資料屬性的識別碼。                                                       |
| [**.EVT \_ 查詢 \_ 旗標**](/windows/desktop/api/WinEvt/ne-winevt-evt_query_flags)                                         | 定義值，這些值會指定如何傳回查詢結果，以及您是否要針對通道或記錄檔進行查詢。           |
| [**.EVT \_ 查詢 \_ 屬性 \_ 識別碼**](/windows/desktop/api/WinEvt/ne-winevt-evt_query_property_id)                            | 定義識別碼，以識別您可以取得的查詢資訊。                                                 |
| [**.EVT \_ 轉譯 \_ 內容 \_ 旗標**](/windows/desktop/api/WinEvt/ne-winevt-evt_render_context_flags)                      | 定義值，這些值會指定要從事件存取的資訊類型。                                                  |
| [**.EVT \_ 轉譯 \_ 旗標**](/windows/desktop/api/WinEvt/ne-winevt-evt_render_flags)                                       | 定義值，這些值會指定要呈現的內容。                                                                                    |
| [**.EVT \_ RPC \_ 登入 \_ 旗標**](/windows/desktop/api/WinEvt/ne-winevt-evt_rpc_login_flags)                                | 定義連接到遠端電腦時，您可以用來驗證使用者的驗證類型。                |
| [**.EVT \_ 搜尋 \_ 旗標**](/windows/desktop/api/WinEvt/ne-winevt-evt_seek_flags)                                           | 定義要從中搜尋結果集中的相對位置。                                                                |
| [**.EVT \_ 訂閱 \_ 旗標**](/windows/desktop/api/WinEvt/ne-winevt-evt_subscribe_flags)                                 | 定義可指定何時開始訂閱事件的可能值。                                                      |
| [**.EVT \_ 訂閱 \_ 通知 \_ 動作**](/windows/desktop/api/WinEvt/ne-winevt-evt_subscribe_notify_action)                | 定義訂用帳戶服務可以傳遞給您回呼的可能資料類型。                                     |
| [**.EVT \_ 系統 \_ 屬性 \_ 識別碼**](/windows/desktop/api/WinEvt/ne-winevt-evt_system_property_id)                          | 定義識別事件之系統定義屬性的識別碼。                                                   |
| [**.EVT \_ 變異 \_ 類型**](/windows/desktop/api/WinEvt/ne-winevt-evt_variant_type)                                       | 定義變異數資料項目可能的資料類型。                                                                            |



 

 

 




