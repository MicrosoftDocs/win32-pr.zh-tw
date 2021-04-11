---
description: WMI 會檢查應用程式和腳本的存取權限。
ms.assetid: f6808f50-a1fd-434f-8a42-efa3afbe7871
ms.tgt_platform: multiple
title: WMI 安全性常數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d360aa57c12c958db95c4b94f2b06327a3f70dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194909"
---
# <a name="wmi-security-constants"></a>WMI 安全性常數

WMI 會檢查應用程式和腳本對於 WMI 命名空間、印表機、服務、DCOM 應用程式、檔案、共用和其他安全物件等物件的存取權限。 這些安全物件的存取權是由 (ACE) 的存取控制專案所控制。 每個 ACE 都包含指定哪些群組或使用者具有存取權的清單。 如需有關安全性和存取控制清單 (Acl、Dacl 或 Sacl) 的詳細資訊，請參閱 [ (acl 的存取控制清單) ](/windows/desktop/SecAuthZ/access-control-lists) 和 [安全描述項](/windows/desktop/SecAuthZ/security-descriptors)。

WMI 中許多會影響安全物件的提供者方法，都需要系統管理員啟用某些特殊許可權。 您使用的許可權版本取決於程式設計語言，如 [**許可權常數**](privilege-constants.md)中所示。

安全性常數定義于下列主題中：

-   [**事件安全性常數**](event-security-constants.md)
-   [**檔案和目錄存取權限常數**](file-and-directory-access-rights-constants.md)
-   [**命名空間存取權限常數**](namespace-access-rights-constants.md)
-   [**命名空間 ACE 旗標常數**](namespace-ace-flag-constants.md)
-   [**命名空間 ACE 類型常數**](namespace-ace-type-constants.md)
-   [**許可權常數**](privilege-constants.md)

 

 
