---
description: 系統管理員覆寫
ms.assetid: 25b6ce86-52c8-4f7f-97af-86b2eaf3e9af
title: 系統管理員覆寫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af73f6d6fe3fe7d4edb8272c4d39c385a84973e4a3263c448505f5235adec855
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033018"
---
# <a name="administrator-overrides"></a>系統管理員覆寫

Windows 在所有的電源原則物件上都有一個預設的存取控制清單 (ACL) 。 ACL 會授與「讀取」、「寫入」和「變更」許可權給已驗證的使用者群組的成員。 所有其他使用者都會被授與唯讀許可權。 呼叫電源原則函式的應用程式可以使用 [**PowerSettingAccessCheck**](/windows/desktop/api/PowrProf/nf-powrprof-powersettingaccesscheck) 函式，來判斷使用者是否具有指定之電源設定的許可權。

您可以透過群組原則覆寫電源設定。 您可以透過網域群組原則或本機群組原則來設定覆寫。 [**PowerSettingAccessCheck**](/windows/desktop/api/PowrProf/nf-powrprof-powersettingaccesscheck) 將會報告指定的電源設定是否有群組原則覆寫。

當命令無法完成時，命令列工具 **PowerCfg.exe** 會顯示錯誤訊息，因為使用者沒有變更電源設定的許可權，或因為電源設定有群組原則覆寫。

主控台中的電源選項應用程式不支援設定電源原則存取權限。 變更許可權必須透過 **PowerCfg.exe** 完成。

 

 



