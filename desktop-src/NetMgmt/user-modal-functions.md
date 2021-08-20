---
title: 使用者模式函數
description: 網路管理使用者強制回應功能會取得並設定與安全性系統行為相關的全系統參數。
ms.assetid: e655b9f6-2808-4bd4-998c-c8a2e980920b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: addea3c76d79cbcdb0e359424be154893d2c436c1f6d45157ecf50e748fc9417
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117796794"
---
# <a name="user-modal-functions"></a>使用者模式函數

網路管理使用者強制回應功能會取得並設定與安全性系統行為相關的全系統參數。

使用者模式函數如下所示。



| 函式                                     | 描述                                                                                                                                                                                             |
|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetUserModalsGet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsget) | 傳回安全性資料庫中所有使用者和全域群組的全域資訊，也就是安全性帳戶管理員 (SAM) 資料庫，或在網域控制站的情況下 Active Directory。 |
| [**NetUserModalsSet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsset) | 針對安全性資料庫中的所有使用者和全域群組設定全域資訊。                                                                                                                       |



 

**NetUserModalsGet** 和 **NetUserModalsSet** 函式會檢查和修改強制回應設定，這些設定是影響安全性資料庫中每個帳戶的全域參數 (例如，允許的最小密碼長度) 。 您可以藉由呼叫 **NetUserModalsSet** 來改變所有強制回應設定。 您也可以使用 **net accounts** 命令來改變大部分的 modals。 網路管理使用者強制回應功能不需要伺服器擁有使用者層級安全性。

使用者模式資訊可在下列層級取得：

-   [**使用者 \_ MODALS \_ 資訊 \_ 0**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_0)
-   [**使用者 \_ MODALS \_ 資訊 \_ 1**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1)
-   [**使用者 \_ MODALS \_ 資訊 \_ 2**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_2)
-   [**使用者 \_ MODALS \_ 資訊 \_ 3**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_3)

下列資訊層級僅適用于 [**NetUserModalsSet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsset) ，並取代較舊的方法來傳遞 *Parmnum* 來設定特定欄位：

-   [**使用者 \_ MODALS \_ 資訊 \_ 1001**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1001)
-   [**使用者 \_ MODALS \_ 資訊 \_ 1002**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1002)
-   [**使用者 \_ MODALS \_ 資訊 \_ 1003**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1003)
-   [**使用者 \_ MODALS \_ 資訊 \_ 1004**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1004)
-   [**使用者 \_ MODALS \_ 資訊 \_ 1005**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1005)
-   [**使用者 \_ MODALS \_ 資訊 \_ 1006**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1006)
-   [**使用者 \_ MODALS \_ 資訊 \_ 1007**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1007)

如果您正在針對 Active Directory 進行程式設計，您可以呼叫特定 Active Directory 服務介面 (ADSI) 方法，以達到您可以藉由呼叫網路管理使用者模式函式達成的相同功能。 如需詳細資訊，請參閱 [**IADsDomain**](/windows/desktop/api/iads/nn-iads-iadsdomain)。

 

 