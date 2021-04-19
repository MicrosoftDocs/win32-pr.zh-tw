---
description: 在系統開機期間，SCM 會啟動所有自動啟動服務及其相依的服務。 例如，如果自動啟動服務相依于需求啟動服務，則也會自動啟動「需求啟動」服務。
ms.assetid: 8aa60e96-a35e-4670-832c-c045d0903618
title: 自動啟動服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40b2e7ef0c65e72ee21145891b6f9598117a7afe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970390"
---
# <a name="automatically-starting-services"></a>自動啟動服務

在系統開機期間，SCM 會啟動所有自動啟動服務及其相依的服務。 例如，如果自動啟動服務相依于需求啟動服務，則也會自動啟動「需求啟動」服務。

載入順序取決於下列各項：

1.  群組在 [載入順序群組] 清單中的順序。 這項資訊會儲存在下列登錄機碼的 **ServiceGroupOrder** 值中：

    **HKEY \_ 本機 \_ 電腦 \\ 系統 \\ CurrentControlSet \\ 控制項**

    若要指定服務的載入順序群組，請使用 [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea)或 [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga)函數的 *lpLoadOrderGroup* 參數。

2.  在標記順序向量中指定之群組內的服務順序。 這項資訊會儲存在下列登錄機碼的 **GroupOrderList** 值中：

    **HKEY \_ 本機 \_ 電腦 \\ 系統 \\ CurrentControlSet \\ 控制項**

3.  針對每項服務列出的相依性。

當開機完成時，系統會執行下列登錄機碼的 **BootVerificationProgram** 值所指定的開機驗證程式： **HKEY \_ 本機 \_ 電腦 \\ 系統 \\ CurrentControlSet \\ 控制項**。

依預設，未設定此值。 系統只會報告第一位使用者登入之後開機是否成功。 您可以提供開機驗證程式來檢查系統是否有問題，並使用 [**NotifyBootConfigStatus**](/windows/desktop/api/Winsvc/nf-winsvc-notifybootconfigstatus) 功能將開機狀態回報給 SCM。

成功開機之後，系統會將資料庫的複本儲存在最後已知良好的 (LKG) 設定中。 如果對使用中資料庫所做的變更導致系統重新開機失敗，系統就可以還原此資料庫複本。 以下是此資料庫的登錄機碼：

**HKEY \_ LOCAL \_ MACHINE \\ SYSTEM \\ ControlSet *XXX* \\ Services**

其中 *XXX* 是儲存在下列登錄值中的值： **HKEY \_ LOCAL \_ MACHINE \\ System \\ Select \\ LastKnownGood**。

如果自動啟動服務的服務 \_ 錯誤 \_ 嚴重錯誤控制層級無法啟動，SCM 會使用 LKG 設定來重新開機電腦。 如果 LKG 設定已在使用中，則開機會失敗。

自動啟動服務可以設定為延遲的自動啟動服務，方法是呼叫 [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) 函式與服務設定 \_ 延遲的 \_ \_ 自動 \_ 啟動 \_ 資訊。 此變更會在下一次系統開機之後生效。 如需詳細資訊，請參閱 [**服務 \_ 延遲的 \_ 自動 \_ 啟動 \_ 資訊**](/windows/desktop/api/Winsvc/ns-winsvc-service_delayed_auto_start_info)。

 

 



