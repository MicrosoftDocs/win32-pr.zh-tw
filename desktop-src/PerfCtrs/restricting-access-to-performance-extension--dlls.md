---
description: 從 Windows Server 2003 開始，效能監視器 Users 群組和 Performance Log Users 群組可供效能 Dll 的開發人員和使用者使用，以及效能資料協助程式 (PDH) API 功能。
ms.assetid: 423359be-9d41-4a5f-91cd-f6d7a6a91d9d
title: 限制對效能延伸模組 Dll 的存取
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd433cad68ec3e50f6b17994da98164e2ae9f237
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849278"
---
# <a name="restricting-access-to-performance-extension-dlls"></a>限制對效能延伸模組 Dll 的存取

從 Windows Server 2003 開始，效能監視器 Users 群組和 Performance Log Users 群組可供效能 Dll 的開發人員和使用者使用，以及效能資料協助程式 (PDH) API 功能。 這些效能安全性群組可供系統管理員使用，以限制對特定使用者清單的效能 Dll 所公開的資訊存取。

效能監視器 Users 群組旨在包含可查看計數器資料的使用者，而不使用效能記錄檔及警示服務記錄計數器資料。 Performance Log Users 群組應該包含有權使用效能記錄檔和警示服務的使用者，以便在本機或遠端伺服器上記錄計數器。 此群組的許可權也包括在本機或遠端系統上建立記錄檔、使用警示服務，以及在服務中執行程式。

請注意，這些效能安全性群組本身並不是存取限制機制。 您必須使用這些群組搭配 Windows 物件存取控制模型來執行此動作。

大部分的應用程式會透過 IPC 機制（通常是共用記憶體）與效能 DLL 通訊。 因此，您可以將效能安全性群組的成員新增至共用記憶體物件的安全描述項，以將 DLL 的存取限制為安全性群組的成員。 執行這項操作時，您也必須將群組成員加入至效能 DLL 所存取之系統物件的安全描述項，以便提供計數器資料，例如記錄檔和資料夾。 如需將 Acl 新增至物件安全描述項的詳細資訊，請參閱 [修改物件的 acl](/windows/desktop/SecAuthZ/modifying-the-acls-of-an-object-in-c--)。

您可以用來修改 IPC 系統物件安全描述項之 ACL 資訊的另一種方法，就是指定具有安全描述項定義語言 (SDDL) 的「效能安全性群組」清單成員，然後呼叫 [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) 來建立安全描述項。 接著會將此安全描述項附加至 IPC 系統物件。 以下顯示的 SDDL 字串包含效能監視器 Users 群組、MU 和 Performance Log Users 群組（LU）。

``` syntax
D:(A;OICI;GA;;;SY)(A;OICI;GA;;;BA)(A;OICI;FRFWFXSDRC;;;NS)(A;OICI;FRFWFXSDRC;;;LU)(A;OICI;FRFX;;;MU) 
```

 

 
