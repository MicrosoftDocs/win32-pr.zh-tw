---
title: 讀取物件 ACL 中的 Control 存取權限集合
description: IADsAccessControlEntry 介面的屬性是用來授與或拒絕 control 存取權限。
ms.assetid: 2c6fef91-990e-4954-9aff-c9ec72d13972
ms.tgt_platform: multiple
keywords:
- 讀取物件 ACL 中的 Control 存取權限集 Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52a7bb241eabc8a853f30e1ff64d469141d694dc56351786fdf7d486f06ed67e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118184882"
---
# <a name="reading-a-control-access-right-set-in-an-objects-acl"></a>讀取物件 ACL 中的 Control 存取權限集合

您可以使用 ADSI 來讀取 control access right ACE，就像您在 ACL 中的任何其他 ACE 一樣。 請注意，您也可以使用 Win32 安全性 Api 來讀取目錄物件上的 Acl。 不過，control 存取權限會以授與和拒絕 control 存取權限的特定方式使用 [**IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) 介面的屬性：

-   [**AccessMask**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) 必須包含 **ADS \_ 正確的 \_ DS \_ 控制 \_ 存取權**。
-   [**旗標**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) 值為 **ADS \_ 旗標 \_ 物件 \_ 類型 \_ 存在**。
-   [**ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) 是 control 存取權限的 **rightsGUID** 屬性字串形式。 GUID 的字串格式與 [**StringFromGUID2**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2) COM 程式庫函數具有相同的字串格式。
-   [**AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) 是 **ADS \_ AceType \_ access 允許的 \_ \_ 物件** ，可授與受信任者控制項存取權或 **ADS AceType 拒絕存取的 \_ \_ \_ \_ 物件** ，以拒絕受信任者控制存取權限。
-   [**信任者**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) 為安全性主體;亦即套用 ACE 的使用者、群組、電腦等等。

使用下列程式讀取 ADSI 物件的 ACE。 下列程式適用于 C 和 c + + 應用程式。

**若要讀取 ADSI 物件的 ACE**

1.  取得物件的 [**IADs**](/windows/desktop/api/iads/nn-iads-iads) 介面指標。
2.  您可以使用 [**IADs：： get**](/windows/desktop/api/iads/nf-iads-iads-get) 方法來取得物件的安全描述項。 包含安全描述項的屬性名稱為 "nTSecurityDescriptor"。 屬性將會以包含 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)指標的 **VARIANT** 傳回。 請注意， **vt** 成員是 **vt \_ 分派**。 在該 **IDispatch** 指標上呼叫 **QueryInterface** 來取得 [**IADsSecurityDescriptor**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor)介面，以便使用該介面上的方法來存取安全描述項 ACL。
3.  使用 [**IADsSecurityDescriptor：： get \_ objdescriptor.discretionaryacl**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) 方法來取得 ACL。 方法會傳回 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) 指標。 在該 **IDispatch** 指標上呼叫 **QueryInterface** 來取得 [**IADsAccessControlList**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrollist)介面，以便使用該介面上的方法來存取 ACL 中的個別 ace。
4.  使用 [**IADsAccessControlList：： get \_ \_ NewEnum**](/windows/desktop/api/iads/nf-iads-iadsaccesscontrollist-get__newenum)方法來列舉 ace。 方法會傳回 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) 指標。 呼叫該 **IUnknown** 指標上的 **QueryInterface** 來取得 [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant)介面。
5.  使用 [**IEnumVARIANT：： Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next) 方法來列舉 ACL 中的 ace。 屬性會以包含 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)指標的 **變異** 形式傳回。 請注意， **vt** 成員是 **vt \_ 分派**。 在該 **IDispatch** 指標上呼叫 **QueryInterface** 來取得 [**IADSACCESSCONTROLENTRY**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry)介面，以讀取 ACE。
6.  呼叫 [**IADsAccessControlEntry：： get \_ AccessMask**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods)方法來取得 **AccessMask** ，並確認 **ADS \_ RIGHT \_ DS \_ CONTROL \_ 存取** 旗標的 **AccessMask** 值。 如果有此旗標，ACE 就會包含 control 存取權限。
7.  呼叫 [**IADsAccessControlEntry：： get \_ Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) 方法來取得物件類型的旗標。
8.  檢查 **ADS \_ 旗標 \_ 物件 \_ 類型 \_ 目前** 旗 [**標的旗標**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods)值。 如果 [ **旗標** ] 設定為 [ **ADS \_ 旗標 \_ 物件 \_ 類型 \_**]，請呼叫 **IADSACCESSCONTROLENTRY：： get \_ ObjectType** 方法，取得包含 ACE 套用之控制項存取權 rightsGUID 的字串。
9.  呼叫 [**IADsAccessControlEntry：： get \_ AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) 方法以取得 ACE 類型。 此類型會是 **ADS \_ ACETYPE \_ access 允許的 \_ \_ 物件** 授與受信任者存取權限，或 **ADS \_ ACETYPE 拒絕存取的 \_ \_ \_ 物件** 拒絕控制存取權。
10. 呼叫 [**IADsAccessControlEntry：： get \_ 信任**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) 程式方法以取得安全性主體，也就是套用 ACE 的使用者、群組、電腦等等。
11. 當 [**ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) 和 **信任** 字串完成時，請使用 [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) 釋放這些字串的記憶體。
12. 完成介面之後，呼叫 **release** 以遞減或釋放所有介面參考。

 

 