---
description: 您可以選擇 Microsoft Update 服務中的電腦，然後使用自動更新註冊該服務。
ms.assetid: d6f3d8ca-3b7e-409c-87b6-db247b7b68e4
title: Opt-In 至 Microsoft Update
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b149eb28024d77f66a08371827187adf05d4b78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112156"
---
# <a name="opt-in-to-microsoft-update"></a>Opt-In 至 Microsoft Update

您可以選擇 Microsoft Update 服務中的電腦，然後使用自動更新註冊該服務。

本主題中的腳本範例說明如何使用 Windows Update Agent (WUA) 向自動更新註冊 Microsoft Update 服務。 或者，若要註冊服務，使用者可以造訪 Microsoft Update。

在您嘗試執行此範例之前，請確認電腦上安裝的 WUA 版本是7.0.6000 版或更新版本。 如需如何判斷已安裝之 WUA 版本的詳細資訊，請參閱 [判斷 wua 的目前版本](determining-the-current-version-of-wua.md)。

## <a name="example"></a>範例

下列腳本範例說明如何使用 Windows Update Agent (WUA) 向自動更新註冊 Microsoft Update 服務。 此範例允許延遲或離線處理（如有需要）。

> [!IMPORTANT]
> 此腳本旨在示範如何使用 Windows Update 代理程式 Api，並提供開發人員如何使用這些 Api 來解決問題的範例。 此腳本並不是用來作為生產程式碼，而且 Microsoft (不支援腳本本身，不過) 支援基礎 Windows Update 代理程式 Api。

 


```VB
Set ServiceManager = CreateObject("Microsoft.Update.ServiceManager")
ServiceManager.ClientApplicationID = "My App"

'add the Microsoft Update Service, GUID
Set NewUpdateService = ServiceManager.AddService2("7971f918-a847-4430-9279-4a52d1efe18d",7,"")

```



在舊版 WUA (7.0.6000) 的最小 WUA 版本，您可以使用登錄設定來簡化加入宣告進程。 設定登錄機碼和值之後，下一次 WUA 執行搜尋時，就會發生 Microsoft Update 加入宣告進程。 加入宣告進程可能會由自動更新或由 API 呼叫者觸發。

例如，要為加入程式設定的登錄機碼和值的完整路徑如下所示：

**HKLM** \\**軟體** \\**Microsoft** \\**Windows** \\**CurrentVersion** \\**Windowsupdate.log** \\**PendingServiceRegistration** \\**7971f918-a847-4430-9279-4a52d1efe18d**

**ClientApplicationID** = 我的應用程式

**RegisterWithAU** = 1

> [!Note]
>
> 只有當 WUA 從7.0.6000 版之前的版本更新為版本7.0.6000 或更新版本時，才會遵守登錄機碼一次。 覆寫現有的登錄值時，我們建議您自行決定，因為覆寫這些值可能會變更先前服務註冊要求的結果。
>
> 建立此登錄機碼需要系統管理認證。 若為 Windows Vista，呼叫端必須在提高許可權的進程中建立登錄機碼。

 

 

 



