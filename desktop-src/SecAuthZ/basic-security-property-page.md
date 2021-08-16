---
description: EditSecurity 函數所顯示之屬性工作表的起始頁。 您也可以使用 CreateSecurityPage 函式來建立基本安全性屬性頁，以插入您自己的屬性工作表中。
ms.assetid: 6623fe7e-e91d-49c7-9ad0-7791c178d12b
title: 基本安全性屬性頁面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a8628b0b096e24a3a7baef94f5ab9913c2cd89825bb15bf6b19d18cd81d1033
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783705"
---
# <a name="basic-security-property-page"></a>基本安全性屬性頁面

[基本安全性] 屬性頁是 [**EditSecurity**](/windows/desktop/api/Aclui/nf-aclui-editsecurity) 函數所顯示之屬性工作表的起始頁。 您也可以使用 [**CreateSecurityPage**](/windows/desktop/api/Aclui/nf-aclui-createsecuritypage) 函式來建立基本安全性屬性頁，以插入您自己的屬性工作表中。

屬性頁會在物件的 [*任意存取控制清單*](/windows/desktop/SecGloss/d-gly) (DACL)  (ace) 的 [[*存取控制] 專案*](/windows/desktop/SecGloss/a-gly)中，[顯示名為的受](trustees.md)信任物件清單。 此頁面也包含物件所支援的存取權限清單。 當使用者從受信任清單中選取名稱時，每個存取權限旁的核取方塊會指出該信任者允許或拒絕的許可權。 然後，使用者可以選取或清除核取方塊，以修改信任者的存取權限。 使用者也可以新增或移除清單中的信任者。

[基本安全性] 屬性頁無法顯示覆雜的 Ace，例如 [特定物件的 ace](object-specific-aces.md)或 ACE 繼承資訊。 若要讓使用者能夠查看或編輯這類資訊，您可以在 [基本安全性] 頁面中包含 [ **Advanced** ] 按鈕。 使用者可以按一下 [ **advanced （advanced** ）] 按鈕，顯示 [advanced security] （ [安全性）屬性工作表](advanced-security-property-sheet.md)。 此屬性工作表具有屬性頁，可讓使用者編輯物件的 [*系統存取控制清單*](/windows/desktop/SecGloss/s-gly) (SACL) 、變更物件的擁有者，或執行物件 DACL 的 advanced 編輯。 若要顯示 [ **Advanced** ] 按鈕，請 \_ 在 [**ISecurityInformation：： GetObjectInformation**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getobjectinformation)執行所傳回的 [**si \_ 物件 \_ 資訊**](/windows/desktop/api/Aclui/ns-aclui-si_object_info)結構中，設定 si Advanced 旗標。

您可以使用 [**SI \_ 物件 \_ 資訊**](/windows/desktop/api/Aclui/ns-aclui-si_object_info)結構的 **pszPageTitle** 成員來指定 [基本安全性] 屬性頁的標題。 預設標題為 [ **安全性**]。

 

 
