---
description: 存取控制編輯器可以包含 [擁有者] 屬性頁，讓使用者變更物件擁有者。 如需物件擁有者的詳細資訊，請參閱新物件的擁有者，以及在 c + + 中取得物件擁有權。
ms.assetid: b0c421db-450e-4030-98e9-e062202e482c
title: '[擁有者] 屬性頁'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cee9d5c276071674ec274c9955a2e8c5cd5a856a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115813"
---
# <a name="owner-property-page"></a>[擁有者] 屬性頁

存取控制編輯器可以包含 [擁有者] 屬性頁，讓使用者變更物件的擁有者。 如需物件擁有者的詳細資訊，請參閱 [新物件的擁有](owner-of-a-new-object.md) 者，以及 [在 c + + 中取得物件擁有權](taking-object-ownership-in-c--.md)。

當使用者按一下 [[基本安全性] 屬性頁](basic-security-property-page.md)上的 [ **advanced** ] 按鈕時，[**擁有** 者] 屬性頁會顯示在 [ [advanced security] 屬性工作表](advanced-security-property-sheet.md)中。 若要包含 [**擁有** 者] 屬性頁，請 \_ \_ \_ 在 [**ISecurityInformation：： GetObjectInformation**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getobjectinformation)執行所傳回的 [**si \_ 物件 \_ 資訊**](/windows/desktop/api/Aclui/ns-aclui-si_object_info)結構中，設定 si ADVANCED 和 si 編輯擁有者旗標。

 

 
