---
description: '[Advanced security] 屬性頁可讓使用者執行 [存取控制編輯器] 的 [基本安全性] 屬性頁上無法使用的編輯作業。'
ms.assetid: 99911751-d4ac-4325-89f5-23d237bfd428
title: Advanced Security 屬性工作表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c8fe19b9336434c789d5e61a295cf7784afbf3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106982095"
---
# <a name="advanced-security-property-sheet"></a>Advanced Security 屬性工作表

[Advanced security] 屬性頁可讓使用者執行 [存取控制編輯器] 的 [ [基本安全性] 屬性頁](basic-security-property-page.md) 上無法使用的編輯作業。 屬性工作表可以包含下列屬性頁：

-   [ [許可權](permissions-property-page.md) ] 屬性頁可讓您編輯物件的 [*任意存取控制清單*](/windows/desktop/SecGloss/d-gly) (DACL) ，例如編輯 [特定物件的 ace](object-specific-aces.md) 或控制 [ACE 繼承](ace-inheritance.md)。
-   用來查看和編輯物件之 [*系統存取控制清單*](/windows/desktop/SecGloss/s-gly) (SACL) 的 [[審核](auditing-property-page.md)] 屬性頁。
-   用來變更物件擁有者的 [ [擁有](owner-property-page.md) 者] 屬性頁。

使用者可以按一下 [基本安全性] 屬性頁上的 [ **advanced （advanced** ）] 按鈕，顯示 [advanced security] 屬性工作表。 若要顯示 [ **Advanced** ] 按鈕，請 \_ 在 [**ISecurityInformation：： GetObjectInformation**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getobjectinformation)執行所傳回的 [**si \_ 物件 \_ 資訊**](/windows/desktop/api/Aclui/ns-aclui-si_object_info)結構中，設定 si Advanced 旗標。

 

 
