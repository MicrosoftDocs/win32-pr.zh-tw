---
title: 在物件的 ACL 中設定 Control 存取權限 ACE
description: 您可以使用 ADSI 來設定 control access right ACE，就像是屬性特定的 ACE 一樣，不同的是，IADsAccessControlEntry 屬性是控制項存取權的 rightsGUID。
ms.assetid: 454dc372-47b0-457d-8660-644fcfa59be8
ms.tgt_platform: multiple
keywords:
- 在物件的 ACL 中設定 Control 存取權限 ACE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09f4a4406bfa3d16a3e3be228bf4a0f131d77ad68cb99a6b9b2a8d328f15215e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024806"
---
# <a name="setting-a-control-access-right-ace-in-an-objects-acl"></a>在物件的 ACL 中設定 Control 存取權限 ACE

您可以使用 ADSI 來設定 control access right ACE，就像是屬性特定的 ACE 一樣，不同的是， [**IADsAccessControlEntry**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) 屬性是控制項存取權的 **rightsGUID** 。 請注意，您也可以使用 Win32 安全性 Api 來設定目錄物件的 Acl。

下表列出可用來設定 ACE 屬性之控制項存取權限的 [**IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) 屬性。



| 屬性                                                       | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AccessMask**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) | 若要控制對特殊作業進行擴充許可權存取的控制存取權限，AccessMask 必須包含 **ADS \_ RIGHT \_ DS \_ control \_ 存取** 旗標。 針對定義屬性集的控制存取權限，AccessMask 包含 **ADS \_ 正確的 \_ ds \_ 讀取 \_** 屬性和/或 **ads 的 \_ 正確 \_ ds \_ 寫入 \_** 屬性。<br/> 若為控制已驗證之寫入的控制存取權限， [**AccessMask**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) 會包含 **正確的 \_ \_ DS \_ 本身的廣告**。<br/> |
| [**標誌**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods)      | 此值必須包含 **ADS \_ 旗標 \_ 物件 \_ 類型 \_ 目前** 的旗標。                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) | 這個值必須是 control 存取權限之 **rightsGUID** 屬性的 [**StringFromGUID2**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2)格式。 請注意，在 ACE 中，GUID 字串必須包含開始和終止大括弧，即使 **controlAccessRight** 物件的 **rightsGUID** 屬性不包含大括弧也一樣。                                                                                                                                     |
| [**AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods)    | 這兩個 **ADS 都 \_ ACETYPE \_ 存取 \_ 允許的 \_ 物件** ，授與信任者存取控制許可權或 **ADS ACETYPE 拒絕 \_ \_ 存取 \_ \_ 物件** ，以拒絕受信任者控制存取權限。                                                                                                                                                                                                                                                                                                     |
| [**受託 人**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods)    | 套用 ACE 的安全性主體，例如使用者、群組、電腦等等。                                                                                                                                                                                                                                                                                                                                                                                              |



 

如需建立 ACE 的詳細資訊，請參閱 [設定物件的存取權限](setting-access-rights-on-an-object.md)。

如需設定 ACE 的詳細資訊和程式碼範例，請參閱 [在目錄物件上設定 ace 的範例程式碼](example-code-for-setting-an-ace-on-a-directory-object.md)。

 

