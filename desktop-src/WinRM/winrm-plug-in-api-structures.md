---
title: WinRM 外掛程式 API 結構
description: WinRM 外掛程式 API 結構
ms.assetid: 745619bc-c7b3-48fa-8212-cb1b5b9ed4db
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 685bcf87ef8c634db367db62b3ec1472b50e3b6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301519"
---
# <a name="winrm-plug-in-api-structures"></a>WinRM 外掛程式 API 結構

下表概要說明 Windows 遠端管理 (WinRM) 外掛程式應用程式開發介面 (API) 中的結構。



| 結構                                                        | Description                                                                              |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [**WSMAN \_ 授權 \_ 配額**](/windows/desktop/api/Wsman/ns-wsman-wsman_authz_quota)                 | 以每個使用者為基礎來定義配額資訊。                                           |
| [**WSMAN \_ 憑證 \_ 詳細資料**](/windows/desktop/api/Wsman/ns-wsman-wsman_certificate_details) | 代表用戶端憑證中的欄位。                                     |
| [**WSMAN \_ 命令 \_ ARG \_ 設定**](/windows/desktop/api/Wsman/ns-wsman-wsman_command_arg_set)        | 表示傳入命令列的引數集。                  |
| [**WSMAN \_ 篩選**](/windows/desktop/api/Wsman/ns-wsman-wsman_filter)                            | 定義用於操作的篩選。                                             |
| [**WSMAN \_ 片段**](/windows/desktop/api/Wsman/ns-wsman-wsman_fragment)                        | 定義作業的片段資訊。                                       |
| [**WSMAN \_ 操作 \_ 資訊**](/windows/desktop/api/Wsman/ns-wsman-wsman_operation_info)           | 表示外掛程式必須執行要求的特定資源端點。 |
| [**WSMAN \_ 外掛程式 \_ 要求**](/windows/desktop/api/Wsman/ns-wsman-wsman_plugin_request)           | 包含要求的相關資訊，並傳遞至每個外掛程式作業。       |
| [**WSMAN \_ 寄件者 \_ 詳細資料**](/windows/desktop/api/Wsman/ns-wsman-wsman_sender_details)           | 指定每個輸入要求的用戶端詳細資料。                                      |



 

 

 




