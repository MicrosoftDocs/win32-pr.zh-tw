---
title: 存取控制在 Active Directory Domain Services 中的運作方式
description: Active Directory Domain Services 中物件的存取控制是以 Windows NT 和 Windows 2000 存取控制模型為基礎。
ms.assetid: 70eed84b-ada0-48e7-b448-704586e9afaa
ms.tgt_platform: multiple
keywords:
- Active Directory Domain Services、安全性、描述
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2893c068e5a841ed609808964f203211309eaf4f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103933063"
---
# <a name="how-access-control-works-in-active-directory-domain-services"></a>存取控制在 Active Directory Domain Services 中的運作方式

Active Directory Domain Services 中物件的存取控制是以 Windows NT 和 Windows 2000 存取控制模型為基礎。 如需此模型及其元件（如安全描述項、存取權杖、Sid、Acl 和 Ace）的詳細資訊和詳細說明，請參閱 [存取控制模型](/windows/desktop/SecAuthZ/access-control-model)。

Active Directory Domain Services 中資源的存取權限通常會透過使用 (ACE) 的存取控制專案來授與。 ACE 會定義特定使用者或群組之物件的存取權或審核許可權。  (ACL) 的存取控制清單，是針對物件所定義之存取控制專案的已排序集合。 安全描述項支援可建立和管理 Acl 的屬性和方法。 如需安全性模型的詳細資訊，請參閱 [安全性](/windows/desktop/SecAuthZ/access-control) 或 *Windows 2000 伺服器資源套件*。  (此資源可能無法在某些語言及國家或地區使用。 ) 

安全性模型的基本大綱是：

-   安全描述項。 每個目錄物件都有自己的安全描述項，其中包含保護物件的安全性資料。 安全描述項可包含 (DACL) 的任意存取控制清單。 DACL 包含 Ace 的清單。 每個 ACE 都授與或拒絕使用者或群組的一組存取權限。 存取權限會對應到可以在物件上執行的作業，例如讀取和寫入屬性。
-   安全性內容。 存取目錄物件時，應用程式會指定進行存取嘗試的安全性主體認證。 經過驗證後，這些認證會決定應用程式的安全性內容，包括與安全性主體相關聯的群組成員資格和許可權。 如需安全性環境的詳細資訊，請參閱 [安全性內容和 Active Directory Domain Services](security-contexts-and-active-directory-domain-services.md)。
-   存取檢查。 只有當物件的安全描述項將必要的存取權限授與嘗試操作 (的安全性主體，或安全性主體所屬的群組) 時，系統才會授與物件的存取權。

下表列出用來操作 Active Directory Domain Services 之存取控制功能的 ADSI 介面。



| 介面                                                 | 描述                                                               |
|-----------------------------------------------------------|---------------------------------------------------------------------------|
| [**IADsSecurityDescriptor**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) | 用來讀取和寫入目錄服務物件的安全性屬性。 |
| [**IADsAccessControlList**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrollist)   | 用來管理和列舉目錄服務物件的所有 Ace。     |
| [**IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) | 用來讀取和寫入 ACE 屬性。                                    |



 

 

 