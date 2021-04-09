---
description: IInstallationJob 介面會定義下列屬性。
ms.assetid: 74087098-bef0-41f8-8d7b-bbca1d000df8
title: IInstallationJob 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81b0083acd90b174349c105525676741c762aa05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690724"
---
# <a name="iinstallationjob-properties"></a>IInstallationJob 屬性

[**IInstallationJob**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationjob)介面會定義下列屬性。



| 屬性                                            | 描述                                                                                                                                                                                                                            |
|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AsyncState**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-get_asyncstate)   | 取得傳遞至 [**IUpdateInstaller. BeginInstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-begininstall) 或 [**IUpdateInstaller. BeginUninstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-beginuninstall) 方法的呼叫端特定狀態物件。               |
| [**IsCompleted**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-get_iscompleted) | 取得值，這個值會指出是否已完整處理 [**IUpdateInstaller. BeginInstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-begininstall) 或 [**IUpdateInstaller. BeginUninstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-beginuninstall) 方法的呼叫。 |
| [**更新**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-get_updates)         | 取得介面，其中包含安裝或卸載中指定之更新的唯讀集合。                                                                                                        |



 

 

 



