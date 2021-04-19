---
description: 通知 Windows Installer 使用重新開機管理員來關閉所有具有檔案使用中的應用程式，並在安裝結束時重新開機這些應用程式。
ms.assetid: bfa19cc8-4cf7-42ed-9e94-acaeca8d707a
title: RmShutdownAndRestart ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc91d1de52f516c0728e8d6469fb8cddc2e50cfb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106982317"
---
# <a name="rmshutdownandrestart-controlevent"></a>RmShutdownAndRestart ControlEvent

此事件會通知 Windows Installer 使用 [重新開機管理員](../rstmgr/restart-manager-portal.md) 來關閉所有具有檔案使用中的應用程式，並在安裝結束時重新開機這些應用程式。

如果下列任一條件成立，此 ControlEvent 就沒有任何作用。

-   執行安裝的作業系統不是 Windows Vista 或 Windows Server 2008。
-   [**MSIRESTARTMANAGERCONTROL**](msirestartmanagercontrol.md)屬性或 [DisableAutomaticApplicationShutdown](disableautomaticapplicationshutdown.md)原則已停用與 [重新開機管理員](../rstmgr/restart-manager-portal.md)的互動。
-   目前沒有任何開啟的 [重新開機管理員](../rstmgr/restart-manager-portal.md) 會話。
-   從 Windows Installer 到 [重新開機管理員](../rstmgr/restart-manager-portal.md) 的任何呼叫都會傳回失敗。

## <a name="typical-use"></a>一般用法

RMShutdownAndRestart 控制項事件只會透過 [ [MsiRMFilesInUse] 對話方塊](msirmfilesinuse-dialog.md)上的[按鈕](pushbutton-control.md)控制項來發行。

 

 
