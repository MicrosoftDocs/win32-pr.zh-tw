---
description: 一組屬性工作表和屬性頁，可讓使用者查看和修改物件安全描述項的元件。
ms.assetid: ca709f27-8463-4f11-92ac-2148796e640a
title: 存取控制編輯器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65117fe086b6a374dbd973f2cb657ec9c19cc3a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106992054"
---
# <a name="access-control-editor"></a>存取控制編輯器

存取控制編輯器是一組屬性工作表和屬性頁，可讓使用者查看及修改物件 [*安全描述項*](/windows/desktop/SecGloss/s-gly)的元件。 編輯器是由兩個主要部分所組成：

-   [基本的安全性屬性頁](basic-security-property-page.md)，提供簡單的介面，可讓您在物件的 [*任意存取控制清單*](/windows/desktop/SecGloss/d-gly)中編輯 [*存取控制專案*](/windows/desktop/SecGloss/a-gly) (ace)  (DACL) 。 此頁面可以包含可顯示 [advanced security] 屬性工作表的選擇性 [ **advanced** ] 按鈕。
-   具有屬性頁的 [advanced security 屬性工作表](advanced-security-property-sheet.md) ，可讓使用者編輯物件的 [*系統存取控制清單*](/windows/desktop/SecGloss/s-gly) (SACL) 、變更物件的擁有者，或執行物件 DACL 的先進編輯。

[**CreateSecurityPage**](/windows/desktop/api/Aclui/nf-aclui-createsecuritypage)函式會建立 [基本安全性] 屬性頁。 然後，您可以使用 [**PropertySheet**](/windows/win32/api/prsht/nf-prsht-propertysheeta) 函式或 [**PSM \_ ADDPAGE**](../controls/psm-addpage.md) 訊息，將此頁面加入至屬性工作表。

或者，您可以使用 [**EditSecurity**](/windows/desktop/api/Aclui/nf-aclui-editsecurity) 函式來顯示包含 [基本安全性] 屬性頁的屬性工作表。

針對 [**CreateSecurityPage**](/windows/desktop/api/Aclui/nf-aclui-createsecuritypage) 和 [**EditSecurity**](/windows/desktop/api/Aclui/nf-aclui-editsecurity)，呼叫端必須將指標傳遞至 [**ISecurityInformation**](/windows/win32/api/aclui/nn-aclui-isecurityinformation) 介面的執行。 存取控制編輯器會呼叫這個介面的方法，以抓取正在編輯之物件的存取控制資訊，以及將使用者的輸入傳遞回您的應用程式。 **ISecurityInformation** 方法具有下列用途：

-   初始化屬性頁。

    您的 [**GetObjectInformation**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getobjectinformation) 方法執行會將 [**SI \_ 物件 \_ 資訊**](/windows/desktop/api/Aclui/ns-aclui-si_object_info) 結構傳遞給編輯器。 此結構會指定您想要編輯器顯示的屬性頁，以及決定使用者可使用之編輯選項的其他資訊。

-   提供有關正在編輯之物件的安全性資訊。

    您的 [**GetSecurity**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getsecurity) 執行會將物件的初始 [*安全描述項*](/windows/desktop/SecGloss/s-gly) 傳遞給編輯器。 [**GetAccessRights**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getaccessrights)和 [**MapGeneric**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-mapgeneric)方法會提供物件存取權限的相關資訊。 [**GetInheritTypes**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getinherittypes)方法會提供子物件如何繼承物件之 ace 的相關資訊。

-   將使用者的輸入傳遞回您的應用程式。

    當 **使用者按一下 [** 確定] **或 [** 套用] 時，編輯器會呼叫您的 [**SetSecurity**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-setsecurity) 方法，以傳回包含使用者變更的安全描述項。

 

 
