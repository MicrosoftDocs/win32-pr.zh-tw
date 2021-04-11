---
title: 工作安全性強化
description: 使用「工作安全性強化」功能，可讓工作擁有者以最少的必要許可權來執行其工作。
ms.assetid: ba03add5-aa05-4bef-baec-684ca17363bd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ab70679d605a9ad56c6d26116245ae17d41a7a1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183524"
---
# <a name="task-security-hardening"></a>工作安全性強化

使用「工作安全性強化」功能，可讓工作擁有者以最少的必要許可權來執行其工作。 請注意，這項功能預設為啟用，而且工作擁有者可以使用 [工作流程權杖安全識別碼類型] 和 [工作所需的許可權] 陣列進行進一步的調整。

## <a name="task-process-token-sid-type-and-task-required-privileges-array"></a>工作進程權杖 SID 類型和工作所需的許可權陣列

在工作定義層級指定 **ProcessTokenSidType** ，可讓工作擁有者要求以「無」 sid 類型或「不受限制」的 sid 類型來執行工作流程。 如果欄位存在於工作定義中，驗證可確保工作 UserId 包含其中一個作業系統內建服務帳戶的名稱或對應的 SID 字串：「網路服務」或「本機服務」。

SID 類型「無」表示工作會在不包含處理常式權杖 SID 的進程中執行， (不會對處理常式權杖群組清單) 進行任何變更。 在該情況下， (LocalService/NetworkService) 的工作主體帳戶 SID 具有處理常式權杖的完整存取權。

「不受限制」的 SID 類型表示工作 SID 將衍生自完整的工作路徑，並新增至「處理權杖群組」清單。 例如，在 \\ \\ \\ \\ 本地服務帳戶中執行的 microsoft Windows RAC RACTask，工作 SID 衍生自名稱 RACTask，其中 "-" 會取代為 ""，因為 "" \\ \\ 是不正確使用者名稱字元。 工作 SID 的已知組名會是 "NT TASK \\ <modified full task path> " (domainname \\ username 格式) 。  (DACL) 的程式權杖預設任意存取控制清單也會進行修改，只允許工作 SID 和本機系統 SID 的完整控制權，以及對工作主體帳戶 SID 的讀取控制。 "schtasks.exe/showsid/tn <full task path> " 將會顯示對應至工作的工作 SID。

當非 COM 的工作動作啟動時，排程引擎會記錄工作主體帳戶、取得處理常式權杖，並查詢權杖所擁有的許可權清單，然後與 RequiredPrivileges 中指定的許可權清單進行比較。 如果未在後者指定許可權，則會將其標示為已移除的「SE」 \_ 許可權 \_ 。 接著會使用 CreateProcessAsUser API，以產生的權杖控制碼啟動可執行檔動作。

COM 工作動作啟動時，必須由 taskhost.exe 進程啟動。 排程引擎會使用與啟動工作相同的帳戶，查詢每個執行中 taskhost.exe 的內容區塊。 如果它發現主機進程是以啟動工作所需的許可權超集合來啟動，則該工作會在該進程中裝載。 如果找不到這種處理常式，它會將工作主體帳戶下 taskhost 中執行之所有工作的強化資訊與指定的 RequiredPrivileges mask 結合，然後啟動 taskhost.exe 的新實例。

如果工作定義中沒有 RequiredPrivileges，則不含 SeImpersonatePrivilege 的工作主體帳戶預設許可權將用於工作進程。 如果 **ProcessTokenSidType** 不存在於工作定義中，則會使用「不受限制」作為預設值。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[工作註冊資訊](task-registration-information.md)
</dt> <dt>

[關於工作排程器](about-the-task-scheduler.md)
</dt> <dt>

[工作的安全性內容](security-contexts-for-running-tasks.md)
</dt> </dl>

 

 




