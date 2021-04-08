---
title: 使用 TB
description: 提交至 TBS 的每個命令都會與特定實體相關聯。 這是藉由建立實體的一或多個內容來完成，然後再與該實體提交的每個後續命令相關聯。
ms.assetid: 609f1e95-9868-4e34-8758-71306ac4e51f
keywords:
- TPM 基礎服務 TB、範例
- TPM 基礎服務 TB，使用
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 189d047e6cf969887e390ac7dad1cfc8cdbfa4f9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932263"
---
# <a name="using-tbs"></a>使用 TB

TPM 基本服務功能分為四個功能區域：

-   [資源虛擬化](resource-virtualization.md)
-   [命令排程](command-scheduling.md)
-   [電源管理](power-management.md)
-   [命令封鎖](command-blocking.md)

為了確保不同的實體無法存取彼此的資源，提交至 TBS 的每個命令都會與特定實體相關聯。 這是藉由建立實體的一或多個內容來完成，然後再與該實體提交的每個後續命令相關聯。 每個命令都包含一個內容物件，可讓您在適當的內容底下執行最 TB 的 TPM 命令。 當內容關閉時，命令所建立的所有物件都會從 TPM 進行清除。

實體會先建立內容，然後才會先存取 TB 並維護內容，直到完成執行 TBS 存取為止。 例如，在 TSS 的案例中，TSS 的 TCG core services (TCS) 功能會在啟動時建立 TB 內容，而且會將該內容保持在作用中狀態，直到它關閉為止。

若為 Windows Server 2008 和 Windows Vista，此 TB 會限制對系統管理員、NT 授權單位 \\ LocalService 和 NT 授權單位 NetworkService 帳戶的存取 TB API \\ 。 根據預設，這些帳戶是唯一可連接到 TBS 和建立內容的帳戶。 藉由使用字串 (**REG \_ SZ**) 登錄值名稱來建立登錄機碼 **存取** 權，即可修改存取限制 **SecurityDescriptor** <dl> <dt>

資料類型
</dt> <dd>REG_SZ</dd> </dl> under it as follows:

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         TPM
            Access
               SecurityDescriptor = SecurityDescriptor
```

範例：

**O:BAG：不正確： (A;; 0x00000001;;;BA)  (A;; 0x00000001;;;NS)  (A;; 0x00000001;;;LS)**

根據預設，最大值支援的內容數目是25。 您可以藉由建立或修改 **HKEY \_ LOCAL \_ MACHINE**   \\ **Software** \\ **Microsoft** \\ **Tpm** 下名為 MaxCoNtexts 的 DWORD 登錄值來改變這個數位。 您可以使用效能監視器工具追蹤 TBS 內容的數目，來觀察即時的 TB 內容使用狀況。

針對 Windows 8、Windows Server 2012 和更新版本，此 TB 允許存取標準使用者和系統管理員。 **SecurityDescriptor** 和 **MaxCoNtexts** 登錄機碼已淘汰。 針對 Windows 8、Windows Server 2012 和更新版本，此 TB 會使用命令封鎖來限制對特定命令的存取。

針對 Windows 10 1607 版，此 TB 允許從 AppContainer 應用程式存取。 針對每個 TPM 版本，分別新增了 **BlockedAppContainerCommands** 和 **AllowedW8AppContainerCommands** 金鑰與已封鎖和允許的 TPM 命令相符的清單。

針對 Windows 10 1803 版，將不再支援 **AllowedW8AppContainerCommands** 下的登錄機碼。

 

 




