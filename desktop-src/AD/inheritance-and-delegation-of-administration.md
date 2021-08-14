---
title: 管理的繼承和委派
description: 描述在物件樹狀結構中繼承許可權的 AD DS 支援，以及物件特定的繼承。
ms.assetid: db9cf8d9-6831-4456-b2a5-9f5b4f3e9100
ms.tgt_platform: multiple
keywords:
- 管理繼承和委派 Active Directory
- Active Directory Active Directory，許可權繼承
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b48ff4d913cbd8bf16f7b2c67adf86d61515298dcac267291641d30504e1e32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118187521"
---
# <a name="inheritance-and-delegation-of-administration"></a>管理的繼承和委派

Active Directory Domain Services 支援在物件樹狀結構中繼承許可權，以允許在樹狀結構中較高的層級執行系統管理工作。 這可讓系統管理員設定根目錄附近物件的可繼承許可權，例如網域和組織單位，並將這些許可權散發給樹狀結構中的各種物件。

您可以根據每個 ACE 來設定繼承。 下表列出可在 **AceFlags** 中指定以控制 ACE 繼承的旗標。



| 旗標                                                     | 描述                                                                                                                                     |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| **ADS \_ ACEFLAG \_ 繼承 \_ ACE**<br/>                | 使 ACE 在樹狀結構中被繼承。<br/>                                                                                     |
| **ADS \_ ACEFLAG \_ 沒有 \_ 傳播 \_ 繼承 \_ ACE**<br/> | 使 ACE 只在樹狀結構中繼承一個層級。<br/>                                                                      |
| **ADS \_ ACEFLAG \_ 只會繼承 \_ \_ ACE**<br/>          | 使 ACE 在指定的物件上被忽略，而且只會被繼承，並且在繼承的地方有效。<br/> |



 

除了設定繼承之外，Active Directory Domain Services 還支持對象特定的繼承。 這允許將可繼承 Ace 繼承到樹狀結構，但只在特定類型的物件上生效。 這非常適合用來委派管理。 例如，這可以用來設定組織單位上的特定物件可繼承 ACE，讓群組能夠完全掌控組織單位中的所有使用者物件，而不是其他任何專案。 因此，該組織單位中的使用者管理會委派給該群組中的使用者。

### <a name="delegating-service-administration-with-security-groups"></a>使用安全性群組委派服務管理

使用安全性群組來定義和委派與您的應用程式伺服器相關聯的系統管理角色。 例如，您的服務可能會與 MyService 系統管理員群組相關聯。 識別為 MyService 系統管理員的使用者將會新增至 MyService Administrators 群組。 MyService 的安裝程式可以在目錄上設定 Acl，讓 MyService 系統管理員有足夠的許可權可讀取/寫入 MyService 相關的屬性，或建立 MyService 特定的物件。

### <a name="roles-in-security-groups-for-computers-running-your-service"></a>執行服務的電腦安全性組中的角色

使用安全性群組來定義在目錄中被授與您服務物件存取權的電腦集合。 例如，您的服務可能會與群組 MyService 伺服器相關聯。 所有執行 MyService 伺服器的電腦都會新增至 MyService Servers 群組，然後此群組就可以存取 MyService 伺服器需要讀取/寫入資料的目錄部分。 MyService 的安裝程式可以在目錄上設定 Acl，讓 MyService 伺服器有足夠的許可權可讀取/寫入 MyService 相關的屬性，或建立 MyService 特定的物件。

 

 





