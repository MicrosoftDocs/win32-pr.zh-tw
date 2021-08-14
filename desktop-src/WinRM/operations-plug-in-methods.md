---
title: 操作外掛程式方法
description: 操作外掛程式方法
ms.assetid: 81fe751f-51fd-4da6-b44a-0af9007eea9a
ms.tgt_platform: multiple
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8bcfc2263a9ecd35c050499f0547b5bc5190e5896b430edabe6be8490239b62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118323890"
---
# <a name="operations-plug-in-methods"></a>操作外掛程式方法

所有作業外掛程式進入點都有回呼機制，可報告呼叫成功或失敗。 某些回呼機制會呼叫多次，直到報告所有結果為止。

下表提供操作回呼方法的總覽。



| 方法                                                                         | 描述                                                                                                                                          |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WSManPluginFreeRequestDetails**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginfreerequestdetails)         | 釋放配置給 [**WSMAN \_ 外掛程式 \_ 要求**](/windows/desktop/api/Wsman/ns-wsman-wsman_plugin_request) 結構的記憶體。                                          |
| [**WSManPluginGetOperationParameters**](/windows/desktop/api/Wsman/nf-wsman-wsmanplugingetoperationparameters) | 取得操作資訊，例如與作業相關聯的超時時間和資料限制。                                         |
| [**WSManPluginOperationComplete**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginoperationcomplete)           | 記錄作業的完成。                                                                                                              |
| [**WSManPluginReceiveResult**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginreceiveresult)                   | 將結果報告給 Windows 遠端管理 (WinRM) 外掛程式。                                                                                       |
| [**WSManPluginReportCoNtext**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginreportcontext)                   | 將 shell 和命令內容回報給 WinRM 基礎結構，以便可以針對 shell 和/或命令執行進一步的作業。 |



 

 

 




