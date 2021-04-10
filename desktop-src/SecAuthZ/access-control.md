---
description: 存取控制是指可控制哪些人可以存取作業系統中資源的安全性功能。 應用程式會呼叫存取控制功能，以設定可以存取特定資源的人員，或控制應用程式所提供資源的存取權。
ms.assetid: d9ce4ec5-5c09-4b33-93a1-39638a925986
title: " (授權) 的存取控制"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31c0198f0ce0de77750e0587d9b54c1e20cee756
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026626"
---
# <a name="access-control-authorization"></a> (授權) 的存取控制

存取控制是指可控制哪些人可以存取作業系統中資源的安全性功能。 應用程式會呼叫存取控制功能，以設定可以存取特定資源的人員，或控制應用程式所提供資源的存取權。

本總覽說明用來控制對 Windows 物件（例如檔案）的存取，以及控制系統管理功能存取權的安全性模型，例如設定系統時間或審核使用者動作。 [存取控制模型](access-control-model.md)主題提供存取控制元件的概要說明，以及它們彼此互動的方式。

下列主題說明存取控制：

-   [C2 層級安全性](c2-level-security.md)
-   [存取控制模型](access-control-model.md)
-   [安全描述項定義語言](security-descriptor-definition-language.md)
-   [特權](privileges.md)
-   [稽核產生](audit-generation.md)
-   [安全物件](securable-objects.md)
-   [低層級存取控制](low-level-access-control.md)

以下是常見的存取控制工作：

-   [Dacl 如何控制物件的存取](how-dacls-control-access-to-an-object.md)
-   [控制在 c + + 中建立子物件](controlling-child-object-creation-in-c--.md)
-   [用來控制物件屬性存取權的 Ace](aces-to-control-access-to-an-object-s-properties.md)
-   [要求存取物件的存取權限](requesting-access-rights-to-an-object.md)

下列主題提供存取控制工作的範例程式碼：

-   [使用 c + + 修改物件的 Acl](modifying-the-acls-of-an-object-in-c--.md)
-   [在 c + + 中建立新物件的安全描述項](creating-a-security-descriptor-for-a-new-object-in-c--.md)
-   [控制在 c + + 中建立子物件](controlling-child-object-creation-in-c--.md)
-   [在 c + + 中啟用和停用許可權](enabling-and-disabling-privileges-in-c--.md)
-   [在 c + + 中以存取權杖搜尋 SID](searching-for-a-sid-in-an-access-token-in-c--.md)
-   [在 c + + 中尋找檔案物件的擁有者](finding-the-owner-of-a-file-object-in-c--.md)
-   [以 c + + 取得物件擁有權](taking-object-ownership-in-c--.md)
-   [建立 DACL](/windows/desktop/SecBP/creating-a-dacl)

 

 
