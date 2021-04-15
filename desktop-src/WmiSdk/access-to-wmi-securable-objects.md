---
description: WMI 依賴標準的 Windows 安全描述項來控制及保護對安全物件的存取，例如 WMI 命名空間、印表機、服務和 DCOM 應用程式。
ms.assetid: 5893457d-3fc2-4d64-a6c2-0f410052ce52
ms.tgt_platform: multiple
title: 存取 WMI 安全物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ad4ea78cd45d57856b0909283e7c2624fb26bd5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194716"
---
# <a name="access-to-wmi-securable-objects"></a>存取 WMI 安全物件

WMI 依賴標準的 Windows [*安全描述項*](/windows/desktop/SecGloss/s-gly) 來控制及保護對安全物件的存取，例如 WMI 命名空間、印表機、服務和 DCOM 應用程式。 如需詳細資訊，請參閱 [WMI 命名空間的存取](access-to-wmi-namespaces.md)。

本節將討論下列主題：

-   [安全描述項和 Sid](#security-descriptors-and-sids)
-   [存取控制](#access-control)
-   [變更存取安全性](#changing-access-security)
-   [相關主題](#related-topics)

## <a name="security-descriptors-and-sids"></a>安全描述項和 Sid

WMI 會使用物件的安全描述項來比較嘗試存取安全物件的使用者 [*存取權杖*](/windows/desktop/SecGloss/a-gly) ，以維護存取安全性。

在系統上建立使用者或群組時，系統會將 [*(sid 的安全識別碼*](/windows/desktop/SecGloss/s-gly) 提供給帳戶，) sid 可確保使用與先前刪除之帳戶同名的帳戶，不會繼承先前的安全性設定。 存取權杖的建立方式是結合 SID、使用者所屬群組的清單，以及啟用或停用的許可權清單。 這些權杖會指派給使用者所擁有的所有進程和執行緒。

## <a name="access-control"></a>存取控制

當使用者想要使用受保護的物件時，存取權杖會與物件之安全描述項中 [*(DACL) 的任意存取控制清單*](/windows/desktop/SecGloss/d-gly) 進行比較。 DACL 包含稱為 [*存取控制專案 (ACE)*](/windows/desktop/SecGloss/a-gly)的許可權。 [*系統存取控制清單 (SACL)*](/windows/desktop/SecGloss/s-gly) 進行與 dacl 相同的動作，但可以產生安全性審核事件。 從 Windows Vista 開始，WMI 可以在 Windows 安全性記錄檔中建立審核專案。 如需有關在 WMI 中進行審核的詳細資訊，請參閱 [Wmi 命名空間的存取](access-to-wmi-namespaces.md)。

DACL 和 SACL 都包含一份 Ace 清單，說明哪些使用者具有特定存取權限，包括寫入 WMI 存放庫、遠端存取和執行，以及登入許可權。 WMI 會將這些 Acl 儲存在 WMI 存放庫中。

Ace 具有三種類型的存取層級或授與/拒絕許可權：允許、拒絕 DACL，以及) Sacl 的系統審核 (。 拒絕 Ace 在 DACL 或 SACL 中允許 Ace 之前。 檢查使用者存取權限時，WMI 會透過存取控制清單連續執行，直到找到適用于要求存取權杖的允許 ACE 為止。 在此時間點之後不會檢查剩餘的 Ace。 如果找不到適當的 allow ACE，則會拒絕存取。 如需詳細資訊，請參閱 [DACL 中的 Ace 順序](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl) 和 [建立 DACL](/windows/desktop/SecBP/creating-a-dacl)。

## <a name="changing-access-security"></a>變更存取安全性

使用適當的許可權，您可以使用腳本或應用程式來變更安全物件的安全性。 您也可以使用 [*Wmi 控制項*](gloss-w.md)來變更 wmi 命名空間上的安全性設定，或在定義命名空間類別的 [*受控物件格式 (MOF)*](gloss-m.md)檔中加入 [安全描述項定義語言 (SDDL)](/windows/desktop/SecAuthZ/security-descriptor-definition-language)字串。 如需詳細資訊，請參閱 [存取 Wmi 命名空間](access-to-wmi-namespaces.md)、 [保護 wmi 命名空間](securing-wmi-namespaces.md)，以及 [變更安全物件的存取安全性](changing-access-security-on-securable-objects.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[WMI 安全描述項物件](wmi-security-descriptor-objects.md)
</dt> <dt>

[WMI 安全性常數](wmi-security-constants.md)
</dt> <dt>

[使用者帳戶控制和 WMI](user-account-control-and-wmi.md)
</dt> <dt>

[WMI 安全描述項物件](wmi-security-descriptor-objects.md)
</dt> <dt>

[存取 WMI 命名空間](access-to-wmi-namespaces.md)
</dt> </dl>

 

 
