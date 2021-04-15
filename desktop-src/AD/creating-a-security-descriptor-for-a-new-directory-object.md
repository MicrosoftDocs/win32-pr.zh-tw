---
title: 建立新目錄物件的安全描述項
description: 您可以使用 ADSI 來建立安全描述項，並將其設定為新物件的 nTSecurityDescriptor 屬性，或使用它來取代現有物件的 nTSecurityDescriptor 屬性。
ms.assetid: b9ff626f-17f1-4fc1-9d6e-4f47e29a5aeb
ms.tgt_platform: multiple
keywords:
- 建立新目錄物件 AD 的安全描述項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78265d27c52023d669e27fc9890fd2d5273e2ffd
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104462900"
---
# <a name="creating-security-descriptors-for-new-directory-objects"></a>建立新目錄物件的安全描述項

您可以使用 ADSI 來建立安全描述項，並將其設定為新物件的 **nTSecurityDescriptor** 屬性，或使用它來取代現有物件的 **nTSecurityDescriptor** 屬性。

若要建立物件的安全描述項：

1.  使用 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 來建立新安全描述項的 ADSI COM 物件，並取得該物件的 [**IADsSecurityDescriptor**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) 介面指標。 請注意，類別識別碼是 **CLSID \_ SecurityDescriptor**。
2.  您可以使用 [**IADsSecurityDescriptor：:p \_**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) 的 [內容] 擁有者方法來設定物件的擁有者。 信任者是使用者、群組或其他安全性主體。 應用程式應該使用來自要套用 ACE 之信任者的使用者或群組物件中的適當屬性值。
3.  您可以使用 [**IADsSecurityDescriptor：:p 的內容 \_ 控制**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) 方法，來控制是否由物件的父容器繼承 dacl 和 sacl。
4.  使用 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 為新的安全描述項建立適用于 DACL 的 ADSI COM 物件，並取得該物件的 [**IADsAccessControlList**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrollist) 介面指標。 請注意，類別識別碼是 **CLSID \_ AccessControlList**。
5.  針對要新增至 DACL 的每個 ACE，請使用 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 來建立新 ACE 的 ADSI COM 物件，並取得該物件的 [**IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) 介面指標。 請注意，類別識別碼是 CLSID \_ AccessControlEntry。
6.  針對要新增至 DACL 的每個 ACE，使用 ACE [**IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) 物件的屬性方法來設定 ace 的屬性。 如需有關在 ACE 上設定之屬性的詳細資訊，請參閱 [設定物件的存取權限](setting-access-rights-on-an-object.md)。
7.  針對要新增至 DACL 的每個 ACE，在 [**IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry)物件上使用 **QueryInterface** 方法來取得 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)指標。 [**IADsAccessControlList：： AddAce**](/windows/desktop/api/iads/nf-iads-iadsaccesscontrollist-addace)方法需要對 ACE 的 **IDispatch** 介面指標。
8.  針對要新增至 DACL 的每個 ACE，請使用 [**IADsAccessControlList：： AddAce**](/windows/desktop/api/iads/nf-iads-iadsaccesscontrollist-addace) 將新的 ace 新增至 dacl。 請注意，在 ACL 中的 Ace 順序可能會影響對物件的存取評估。 對物件的正確存取權可能會要求您建立新的 ACL、從現有 ACL 將 Ace 以正確的順序新增至新的 ACL，然後將安全描述項中的現有 ACL 取代為新的 ACL。 如需詳細資訊，請參閱 [DACL 中的 Ace 順序](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl)。
9.  遵循步驟4-8 來建立新安全描述項的 SACL。
10. 使用 [**IADsSecurityDescriptor：:p 的 \_ objdescriptor.discretionaryacl**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) 方法來設定 DACL。 如需 Dacl 的詳細資訊，請參閱 [Null dacl 和空白的 dacl](null-dacls-and-empty-dacls.md)。
11. 使用 [**IADsSecurityDescriptor：:p 的 \_ SystemAcl**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) 方法來設定 SACL。
12. 使用 **IADsSecurityDescriptor** 物件的 **QueryInterface** 方法來取得 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面，將 [**IADsSecurityDescriptor**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor)物件轉換成 [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) 。 然後將 **變數** 的 **vt** 成員設定為 **Vt \_ 分派**，然後將 **variant** 的 **pdispVal** 成員設定為與 **IDispatch** 指標相等。
13. 取得物件的 [**IADs**](/windows/desktop/api/iads/nn-iads-iads) 介面指標。
14. 使用具有 "nTSecurityDescriptor" 的 [**IADs：:P 內容**](/windows/desktop/api/iads/nf-iads-iads-put) 類型，以及上面建立的 [**變異**](/windows/win32/api/oaidl/ns-oaidl-variant) 數，將新的安全描述項寫入至屬性快取。
15. 您可以使用 [**IADs：： SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) 方法來更新目錄中物件的屬性。

 

 