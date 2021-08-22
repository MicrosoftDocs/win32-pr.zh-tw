---
title: 用戶端 Shell API 結構和定義
description: 下表概要說明 Windows 遠端管理 (WinRM) 用戶端 Shell API 的結構和其他定義。
ms.assetid: b7a3c92e-6796-482f-9d70-18a48cce4ad8
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c9c3d1f6f9f9d476e9b49ef309e5236e4421e0b5afa77fa1072b92f2060cfcd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119643258"
---
# <a name="client-shell-api-structures-and-definitions"></a>用戶端 Shell API 結構和定義

下表概要說明 Windows 遠端管理 (WinRM) 用戶端 Shell API 的結構和其他定義。



| 函式                                                                      | 描述                                                                                  |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**WSMAN \_ SHELL \_ 完成函式 \_**](/windows/win32/api/wsman/nc-wsman-wsman_shell_completion_function) | 針對 shell 作業呼叫的回呼函式，這會導致遠端要求。 |



 



| 結構                                                                      | 描述                                                                                                                                 |
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**WSMAN \_ 驗證認證 \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_authentication_credentials) | 定義驗證方法，以及用於伺服器或 proxy 驗證的認證。                                              |
| [**WSMAN \_ 資料**](/windows/desktop/api/Wsman/ns-wsman-wsman_data)                                              | 儲存用於 WinRM API 的輸入和輸出資料。                                                                                     |
| [**WSMAN \_ 資料 \_ 二進位檔**](/windows/desktop/api/Wsman/ns-wsman-wsman_data_binary)                               | 儲存用於各種 WinRM API 函式的二進位資料。                                                                                |
| [**WSMAN \_ 資料 \_ 文字**](/windows/desktop/api/Wsman/ns-wsman-wsman_data_text)                                   | 儲存以文字為基礎的資料，以搭配各種 WinRM API 函式使用。                                                                            |
| [**WSMAN \_ 環境 \_ 變數**](/windows/desktop/api/Wsman/ns-wsman-wsman_environment_variable)             | 使用名稱和值組來定義個別的環境變數。                                                                  |
| [**WSMAN \_ 環境 \_ 變數 \_ 集**](/windows/desktop/api/Wsman/ns-wsman-wsman_environment_variable_set)    | 定義環境變數的陣列。                                                                                                  |
| [**WSMAN \_ 錯誤**](/windows/desktop/api/Wsman/ns-wsman-wsman_error)                                     | 包含錯誤資訊。                                                                                                                 |
| [**WSMAN \_ 金鑰**](/windows/desktop/api/Wsman/ns-wsman-wsman_key)                                                | 代表選取器集合內的索引鍵和值組，用來識別特定的資源。                                       |
| [**WSMAN \_ 選項**](/windows/desktop/api/Wsman/ns-wsman-wsman_option)                                          | 表示特定的選項名稱和值組。                                                                                           |
| [**WSMAN \_ 選項 \_ 組**](/windows/desktop/api/Wsman/ns-wsman-wsman_option_set)                                 | 表示一組選項。                                                                                                                |
| [**WSMAN \_ PROXY \_ 資訊**](/windows/desktop/api/Wsman/ns-wsman-wsman_proxy_info)                                 | 設定每個會話的 proxy 資訊。                                                                                                |
| [**WSMAN \_ 接收 \_ 資料 \_ 結果**](/windows/desktop/api/Wsman/ns-wsman-wsman_receive_data_result)              | 代表從 [**WSManReceiveShellOutput**](/windows/desktop/api/Wsman/nf-wsman-wsmanreceiveshelloutput) API 接收的輸出資料。                                |
| [**WSMAN \_ 回應 \_ 資料**](/windows/desktop/api/Wsman/ns-wsman-wsman_response_data)                           | 表示從 [**WSMan**](wsman.md) 操作接收的輸出資料。                                                                |
| [**WSMAN \_ 選取器 \_ 集合**](/windows/desktop/api/Wsman/ns-wsman-wsman_selector_set)                             | 定義一組代表資源身分識別的索引鍵。                                                                            |
| [**WSMAN \_ SHELL \_ 非同步**](/windows/desktop/api/Wsman/ns-wsman-wsman_shell_async)                               | 定義傳遞至所有 shell 作業的非同步結構。                                                                   |
| [**WSMAN \_ SHELL \_ 中斷連接 \_ 資訊**](/windows/desktop/api/Wsman/ns-wsman-wsman_shell_disconnect_info)          | TBD                                                                                                                                         |
| [**WSMAN \_ SHELL \_ 啟動 \_ 資訊**](/windows/desktop/api/Wsman/ns-wsman-wsman_shell_startup_info_v10)                | 儲存使用 [**WSManCreateShell**](/windows/desktop/api/Wsman/nf-wsman-wsmancreateshell) 外掛程式呼叫建立 shell 所需的所有 shell 特定資料。 |
| [**已 \_ 設定 WSMAN 串流 \_ 識別碼 \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_stream_id_set)                          | 列出用於 shell 和命令的輸入或輸出的所有資料流程。                                                  |
| [**WSMAN 使用者 \_ 名稱 \_ 密碼認證 \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_username_password_creds)      | 定義用於驗證的認證。                                                                                            |



 

 

 