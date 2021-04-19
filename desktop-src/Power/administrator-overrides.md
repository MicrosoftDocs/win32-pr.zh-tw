---
description: 系統管理員覆寫
ms.assetid: 25b6ce86-52c8-4f7f-97af-86b2eaf3e9af
title: 系統管理員覆寫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c43e16c9aa3eb3ab9fd5ee7c8d17b9bb4536315
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107001368"
---
# <a name="administrator-overrides"></a>系統管理員覆寫

Windows 在所有的電源原則物件上都有 (ACL) 的單一預設存取控制清單。 ACL 會授與「讀取」、「寫入」和「變更」許可權給已驗證的使用者群組的成員。 所有其他使用者都會被授與唯讀許可權。 呼叫電源原則函式的應用程式可以使用 [**PowerSettingAccessCheck**](/windows/desktop/api/PowrProf/nf-powrprof-powersettingaccesscheck) 函式，來判斷使用者是否具有指定之電源設定的許可權。

您可以透過群組原則覆寫電源設定。 您可以透過網域群組原則或本機群組原則來設定覆寫。 [**PowerSettingAccessCheck**](/windows/desktop/api/PowrProf/nf-powrprof-powersettingaccesscheck) 將會報告指定的電源設定是否有群組原則覆寫。

當命令無法完成時，命令列工具 **PowerCfg.exe** 會顯示錯誤訊息，因為使用者沒有變更電源設定的許可權，或因為電源設定有群組原則覆寫。

主控台中的電源選項應用程式不支援設定電源原則存取權限。 變更許可權必須透過 **PowerCfg.exe** 完成。

 

 



