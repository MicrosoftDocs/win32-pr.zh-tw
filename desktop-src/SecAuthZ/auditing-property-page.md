---
description: 存取控制編輯器可以包含 [審核] 屬性頁，讓使用者在 [物件系統存取控制清單] 中， (SACL)  (Ace) ，來查看和編輯存取控制專案。 如需 Sacl 的詳細資訊，請參閱 (Acl) 的存取控制清單。
ms.assetid: 2a9152b7-c72d-4f03-bc3f-b75927fb4b6c
title: '[審核] 屬性頁'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecf116a9079c5b7b6dfeb7e6df57b45d6a0a2555c14de88a32fee4fadcdc6373
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117784316"
---
# <a name="auditing-property-page"></a>[審核] 屬性頁

存取控制編輯器可以包含 [**審核**] 屬性頁，讓使用者可以在物件的 [*系統存取控制清單*](/windows/desktop/SecGloss/s-gly)中， (SACL)  (ace) ，來查看和編輯 [*存取控制專案*](/windows/desktop/SecGloss/a-gly)。 如需 Sacl 的詳細資訊，請參閱 (Acl) 的 [存取控制清單](access-control-lists.md) 。

**若要查看 [審核] 屬性頁**

-   在 [ [基本安全性] 屬性頁](basic-security-property-page.md)上，按一下 [ **Advanced**]。 [ **審核** ] 屬性頁位於 [ [advanced security] 屬性工作表](advanced-security-property-sheet.md)中。

若要包含 [**審核**] 屬性頁，請在 [**ISecurityInformation：： GetObjectInformation**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getobjectinformation)執行所傳回 [**的 si \_ 物件 \_ 資訊**](/windows/desktop/api/Aclui/ns-aclui-si_object_info)結構中，設定 **si \_ ADVANCED** 和 **si \_ 編輯 \_ 審核** 旗標。

 

 
