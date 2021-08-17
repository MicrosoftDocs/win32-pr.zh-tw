---
title: 授權外掛程式進入點
description: 授權外掛程式進入點
ms.assetid: 6cbfa79a-b57b-44b8-a421-d5e79c1b3757
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d16ca861df6b6546920aaf3f778c61117776ff3861556377b280c990c03711fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118324076"
---
# <a name="authorization-plug-in-entry-points"></a>授權外掛程式進入點

授權外掛程式僅針對 Internet Information Services (IIS) 主機進程進行設定。 每個虛擬目錄只能設定一個授權外掛程式。

所有授權外掛程式都必須支援下列進入點：

-   [**WSManPluginStartup**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_startup)
-   [**WSManPluginShutdown**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_shutdown)
-   [**WSManPluginAuthzUser**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_user)
-   [**WSManPluginAuthzOperation**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_operation)

以下是選擇性的進入點：

-   [**WSManPluginAuthzQueryQuota**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_query_quota)

下表概要說明 Windows 遠端管理 (WinRM) 外掛程式 API 中的授權外掛程式進入點。



| 函式                                                                                      | 描述                                                                                                                                                                                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WSMAN \_ 外掛程式 \_ 授權 \_ 操作**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_operation)              | 呼叫以授權特定的作業。 <br/> 此方法的 DLL 進入點名稱必須是 [**WSManPluginAuthzOperation**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_operation)。<br/>                                                                                                                                                                                                       |
| [**WSMAN \_ 外掛程式 \_ 授權 \_ 查詢 \_ 配額**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_operation)           | 在授權連接取得使用者的配額資訊之後呼叫。 <br/> 此方法的 DLL 進入點名稱必須是 [**WSManPluginAuthzQueryQuota**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_query_quota)。<br/>                                                                                                                                                    |
| [**WSMAN \_ 外掛程式 \_ 授權 \_ 發行 \_ 內容**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_release_context) | 呼叫以釋放外掛程式在 [**WSManPluginAuthzUserComplete**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginauthzusercomplete) 或 [**WSManPluginAuthzOperationComplete**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginauthzoperationcomplete) 方法中報告的內容。 <br/> 此方法的 DLL 進入點名稱必須是 [**WSManPluginAuthzReleaseCoNtext**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_release_context)。<br/> |
| [**WSMAN \_ 外掛程式 \_ 授權 \_ 使用者**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_user)                         | 呼叫以判斷是否允許使用者執行要求。 <br/> 此方法的動態連結程式庫 (DLL) 進入點名稱必須是 [**WSManPluginAuthzUser**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_user)。<br/>                                                                                                                                                            |



 

 

