---
title: " (網路管理) 的目錄服務功能"
description: 網路管理目錄服務功能可讓開發人員使用目錄服務中的網域控制站和網域成員資格。
ms.assetid: 9eeb8f40-85c0-49db-a307-193703e4f463
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e3f650ab3101cb26c90ae4d6f3854ed2b84ef4ab8c83ed37172eaf7f0c51fa6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912288"
---
# <a name="directory-service-functions"></a>目錄服務功能

網路管理目錄服務功能可讓開發人員使用目錄服務中的網域控制站和網域成員資格。

網路管理目錄服務功能如下所示。



| 函式                                                                 | 描述                                                                                                                                                                                 |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetAddAlternateComputerName**](/windows/desktop/api/Lmjoin/nf-lmjoin-netaddalternatecomputername)       | 為指定的電腦新增替代名稱。                                                                                                                                          |
| [**NetEnumerateComputerNames**](/windows/desktop/api/Lmjoin/nf-lmjoin-netenumeratecomputernames)           | 列舉指定電腦的名稱。                                                                                                                                                |
| [**NetGetJoinableOUs**](/windows/desktop/api/Lmjoin/nf-lmjoin-netgetjoinableous)                           | 抓取組織單位清單， (Ou) 可在其中建立電腦帳戶。                                                                                                  |
| [**NetGetJoinInformation**](/windows/desktop/api/Lmjoin/nf-lmjoin-netgetjoininformation)                   | 抓取指定電腦的聯結狀態資訊。                                                                                                                               |
| [**NetJoinDomain**](/windows/desktop/api/Lmjoin/nf-lmjoin-netjoindomain)                                   | 將電腦加入工作組或網域。                                                                                                                                                  |
| [**NetProvisionComputerAccount**](/windows/desktop/api/Lmjoin/nf-lmjoin-netprovisioncomputeraccount)       | 布建電腦帳戶，以供稍後用於離線網域加入作業。                                                                                                           |
| [**NetRemoveAlternateComputerName**](/windows/desktop/api/Lmjoin/nf-lmjoin-netremovealternatecomputername) | 移除指定電腦的替代名稱。                                                                                                                                       |
| [**NetRenameMachineInDomain**](/windows/desktop/api/Lmjoin/nf-lmjoin-netrenamemachineindomain)             | 變更網域中的電腦名稱稱。                                                                                                                                                 |
| [**NetSetPrimaryComputerName**](/windows/desktop/api/Lmjoin/nf-lmjoin-netsetprimarycomputername)           | 設定指定電腦的主要電腦名稱稱。                                                                                                                                  |
| [**NetUnjoinDomain**](/windows/desktop/api/Lmjoin/nf-lmjoin-netunjoindomain)                               | Unjoins 工作組或網域中的電腦。                                                                                                                                            |
| [**NetValidateName**](/windows/desktop/api/Lmjoin/nf-lmjoin-netvalidatename)                               | 確認電腦名稱稱、工作組名稱或功能變數名稱的有效性。                                                                                                                   |



 

如需 Active Directory 程式設計的詳細資訊，請參閱 [Active Directory 參考](/windows/desktop/AD/active-directory-domain-services-reference)。 如需組織單位的詳細資訊，請參閱 Active Directory 檔中的 [管理使用者](/windows/desktop/AD/managing-users) 。

 

 