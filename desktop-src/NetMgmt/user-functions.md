---
title: 使用者函式
description: 網路管理使用者功能可控制安全性資料庫中的使用者帳戶，也就是安全性帳戶管理員 (SAM) 資料庫，或在網域控制站的情況下 Active Directory。 使用者函數如下所示。
ms.assetid: cf0e5102-3924-46c0-8124-0aa04e95f48d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34c8d7b59ff121c0225f166888b42ef1a731336ed80799cd0593ba38b4fb04ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117796814"
---
# <a name="user-functions"></a>使用者函式

網路管理使用者功能可控制安全性資料庫中的使用者帳戶，也就是安全性帳戶管理員 (SAM) 資料庫，或在網域控制站的情況下 Active Directory。 使用者函數如下所示。



| 函式                                               | 描述                                                         |
|--------------------------------------------------------|---------------------------------------------------------------------|
| [**NetUserAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd)                       | 新增使用者帳戶，並指派密碼和許可權層級。     |
| [**NetUserChangePassword**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserchangepassword) | 變更指定網路伺服器或網域的使用者密碼。 |
| [**NetUserDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserdel)                       | 從伺服器刪除使用者帳戶。                             |
| [**NetUserEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserenum)                     | 列出伺服器上的所有使用者帳戶。                                |
| [**NetUserGetGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetgroups)           | 傳回使用者所屬通用群組名的清單。       |
| [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo)               | 傳回伺服器上特定使用者帳戶的相關資訊。    |
| [**NetUserGetLocalGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetlocalgroups) | 傳回使用者所屬的本機群組名稱清單。        |
| [**NetUserSetGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetgroups)           | 設定指定之使用者帳戶的全域群組成員資格。         |
| [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo)               | 設定使用者帳戶的密碼和其他元素。             |



 

存取網路資源的每個使用者或應用程式都必須具有安全性資料庫中的帳戶。 目錄服務會使用此帳戶來驗證使用者或應用程式是否有權連線到資源。 當使用者或應用程式要求存取資源時，Windows 的安全性系統會檢查是否有適當的使用者帳戶或群組帳戶，以允許存取。

一旦藉由呼叫 [**NetUserDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserdel) 函式來移除使用者帳戶，使用者就無法再存取伺服器，除非使用 guest 帳戶。

因為使用者的密碼是機密的，所以 [**NetUserEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserenum) 函式或 [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo) 函式不會傳回它。 當您呼叫 [**NetUserAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd)時，最初會指派密碼。

使用者帳戶資訊可在下列層級取得：

-   [**使用者 \_ 資訊 \_ 0**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_0)
-   [**使用者 \_ 資訊 \_ 1**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1)
-   [**使用者 \_ 資訊 \_ 2**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_2)
-   [**使用者 \_ 資訊 \_ 3**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_3)
-   [**使用者 \_ 資訊 \_ 4**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_4)
-   [**使用者 \_ 資訊 \_ 10**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_10)
-   [**使用者 \_ 資訊 \_ 11**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_11)
-   [**使用者 \_ 資訊 \_ 20**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_20)
-   [**使用者 \_ 資訊 \_ 21**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_21)
-   [**使用者 \_ 資訊 \_ 22**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_22)
-   [**使用者 \_ 資訊 \_ 23**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_23)

此外，當您呼叫 [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) 函式時，下列資訊層級會是有效的：

-   [**使用者 \_ 資訊 \_ 1003**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1003)
-   [**使用者 \_ 資訊 \_ 1005**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1005)
-   [**使用者 \_ 資訊 \_ 1006**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1006)
-   [**使用者 \_ 資訊 \_ 1007**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1007)
-   [**使用者 \_ 資訊 \_ 1008**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1008)
-   [**使用者 \_ 資訊 \_ 1009**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1009)
-   [**使用者 \_ 資訊 \_ 1010**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1010)
-   [**使用者 \_ 資訊 \_ 1011**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1011)
-   [**使用者 \_ 資訊 \_ 1012**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1012)
-   [**使用者 \_ 資訊 \_ 1014**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1014)
-   [**使用者 \_ 資訊 \_ 1017**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1017)
-   [**使用者 \_ 資訊 \_ 1020**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1020)
-   [**使用者 \_ 資訊 \_ 1024**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1024)
-   [**使用者 \_ 資訊 \_ 1051**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1051)
-   [**使用者 \_ 資訊 \_ 1052**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1052)
-   [**使用者 \_ 資訊 \_ 1053**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1053)

下列功能可讓應用程式檢查密碼合規性。



| 函式                                                               | 描述                                                                                                |
|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**NetValidatePasswordPolicyFree**](/windows/desktop/api/Lmaccess/nf-lmaccess-netvalidatepasswordpolicyfree) | 釋放 [**NetValidatePasswordPolicy**](/windows/desktop/api/Lmaccess/nf-lmaccess-netvalidatepasswordpolicy) 函式所配置的記憶體。 |
| [**NetValidatePasswordPolicy**](/windows/desktop/api/Lmaccess/nf-lmaccess-netvalidatepasswordpolicy)         | 確認密碼符合複雜性、過時、最小長度和歷程記錄重複使用需求。            |



 

如果您正在針對 Active Directory 進行程式設計，您可以呼叫特定 Active Directory 服務介面 (ADSI) 方法，以取得您可以藉由呼叫網路管理使用者功能達成的相同功能。 如需詳細資訊，請參閱 [**IADsUser**](/windows/desktop/api/iads/nn-iads-iadsuser) 和 [**IADsComputer**](/windows/desktop/api/iads/nn-iads-iadscomputer)。

 

 