---
title: 本機群組函數
description: 本機群組可以包含來自一或多個網域的使用者帳戶或通用群組帳戶。  (的全域群組只能包含來自一個網域的使用者。 ) 本機群組只會在其專屬網域內共用一般許可權和許可權。
ms.assetid: ed4c59d6-6532-4190-9807-95678053fc72
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dd13a23b322a860d6896a213b27fb6263586412
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682486"
---
# <a name="local-group-functions"></a>本機群組函數

*本機群組* 可以包含來自一或多個網域的使用者帳戶或通用群組帳戶。  (的全域群組只能包含來自一個網域的使用者。 ) 本機群組只會在其專屬網域內共用一般許可權和許可權。

網路管理本機群組功能可控制本機群組的成員，方法是只能在定義本機群組的系統本機上呼叫函數。 在工作站上，或在不是網域控制站的伺服器上，您只能使用該系統上定義的本機群組。

在 Active Directory 中，在原生模式下的網域（本機群組）稱為「 *網域本機群組*」。 所有網域控制站、成員伺服器和已加入網域的工作站都可使用網域本機群組。 Active Directory 混合模式網域是在主域控制站上定義，並複寫到網域中的所有其他網域控制站。 因此，本機群組可在其建立所在網域內的所有網域控制站上使用。

本機群組函數會建立或刪除本機群組，以及檢查或調整本機群組的成員資格。 這些函數如下所示。



| 函式                                                   | 描述                                                             |
|------------------------------------------------------------|-------------------------------------------------------------------------|
| [**NetLocalGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupadd)               | 建立本機群組。                                                  |
| [**NetLocalGroupAddMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupaddmembers) | 將一或多個使用者或全域群組新增至現有的本機群組。     |
| [**NetLocalGroupDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupdel)               | 刪除本機群組，從群組中移除所有現有的成員。    |
| [**NetLocalGroupDelMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupdelmembers) | 從現有的本機群組移除一或多個成員。               |
| [**NetLocalGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupenum)             | 傳回伺服器上每個本機群組帳戶的相關資訊。         |
| [**NetLocalGroupGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetinfo)       | 傳回伺服器上特定本機群組帳戶的相關資訊。 |
| [**NetLocalGroupGetMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetmembers) | 列出指定之本機群組的所有成員。                           |
| [**NetLocalGroupSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupsetinfo)       | 設定有關本機群組的一般資訊。                           |
| [**NetLocalGroupSetMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupsetmembers) | 指派成員到本機群組。                                       |



 

您可以藉由指定成員 (SID) 的安全識別碼，將成員新增至本機群組。 若要將成員帳戶名稱轉譯為 SID，請呼叫 [**LookupAccountName**](/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea) 函數。

當您藉由呼叫 [**NetLocalGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupadd) 函數來建立本機群組時，必須提供本機群組名稱。 一開始，本機群組沒有成員。

本機群組帳戶資訊可在下列層級取得：

-   [**LOCALGROUP \_ 資訊 \_ 0**](/windows/desktop/api/Lmaccess/ns-lmaccess-localgroup_info_0)
-   [**LOCALGROUP \_ 資訊 \_ 1**](/windows/desktop/api/Lmaccess/ns-lmaccess-localgroup_info_1)
-   [**LOCALGROUP \_ 資訊 \_ 1002**](/windows/desktop/api/Lmaccess/ns-lmaccess-localgroup_info_1002)

本機群組成員資格資訊可在下列資訊層級取得：

-   [**LOCALGROUP \_ 成員 \_ 資訊 \_ 0**](/windows/desktop/api/Lmaccess/ns-lmaccess-localgroup_members_info_0)
-   [**LOCALGROUP \_ 成員 \_ 資訊 \_ 1**](/windows/desktop/api/Lmaccess/ns-lmaccess-localgroup_members_info_1)
-   [**LOCALGROUP \_ 成員 \_ 資訊 \_ 2**](/windows/desktop/api/Lmaccess/ns-lmaccess-localgroup_members_info_2)
-   [**LOCALGROUP \_ 成員 \_ 資訊 \_ 3**](/windows/desktop/api/Lmaccess/ns-lmaccess-localgroup_members_info_3)

您可以藉由呼叫 [**NetUserGetLocalGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetlocalgroups) 函式來取得使用者所屬的本機群組名稱，並指定下列資訊層級：

[**LOCALGROUP \_ 使用者 \_ 資訊 \_ 0**](/windows/desktop/api/Lmaccess/ns-lmaccess-localgroup_users_info_0)

如需詳細資訊，請參閱網路管理 [群組功能](group-functions.md)。

如果您正在針對 Active Directory 進行程式設計，您可以呼叫特定 Active Directory 服務介面 (ADSI) 方法，以取得您可以藉由呼叫網路管理本機群組功能達成的相同功能。 如需詳細資訊，請參閱 [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup)。

 

 