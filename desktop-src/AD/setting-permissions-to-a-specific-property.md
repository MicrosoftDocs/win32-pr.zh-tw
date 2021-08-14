---
title: 設定特定屬性的許可權
description: 許可權可以設定為套用至物件的特定屬性。
ms.assetid: 7bafba5a-a437-4777-98a0-f478b738a8ca
ms.tgt_platform: multiple
keywords:
- 設定特定屬性 AD 的許可權
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca7f55fba3ae2be54a29ade3dee1dc161fa0c6d2dbe478fb42f39319fbeaf4fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118183312"
---
# <a name="setting-permissions-to-a-specific-property"></a>設定特定屬性的許可權

許可權可以設定為套用至物件的特定屬性。

**若要設定套用至物件之特定屬性的許可權**

1.  將 [**IADsAccessControlEntry. AccessMask**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) 屬性設定為 **ads \_ right \_ ds \_ 讀取 \_** 屬性和/或 **ads \_ right \_ ds \_ 寫入 \_** 屬性。
2.  將 [**IADsAccessControlEntry AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) 屬性設定為 **ADS \_ AceType \_ 存取允許的 \_ \_ 物件** 或 **ads \_ AceType \_ 拒絕存取 \_ \_ 物件**。
3.  將 [ [**IADsAccessControlEntry**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) ] 屬性設定為屬性的 **schemaIDGUID** 。 這是在架構中定義屬性之 **attributeSchema** 物件的 **schemaIDGUID** 。 GUID 必須指定為 COM 程式庫中 [**StringFromGUID2**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2) 函式所產生的格式字串。
4.  將 [**IADsAccessControlEntry**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) 設定為 **ADS \_ 旗標 \_ 物件 \_ 類型 \_**。

如需預先定義之屬性 **schemaIDGUID** 的詳細資訊，請參閱 [Active Directory Domain Services 參考](active-directory-domain-services-reference.md)。

如需可用來取出 schemaIDGUID 的詳細資訊和程式碼範例，請參閱 [讀取 attributeSchema 和 ClassSchema 物件](reading-attributeschema-and-classschema-objects.md)。

如需有關如何建立 ACE 的詳細資訊，請參閱 [設定物件的存取權限](setting-access-rights-on-an-object.md)。

如需可用來設定屬性特定 ACE 的詳細資訊和程式碼範例，請參閱 [在目錄物件上設定 ACE 的範例程式碼](example-code-for-setting-an-ace-on-a-directory-object.md)。

 

 