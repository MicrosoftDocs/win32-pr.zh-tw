---
title: 設定屬性群組的許可權
description: 許可權可以套用至屬性的群組。
ms.assetid: cb9f6c04-be94-45b4-ba84-2a79b7625fdd
ms.tgt_platform: multiple
keywords:
- 設定 AD 屬性群組的許可權
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a50fa74cd39353170089bc39940b7bc063e8c94454d46c50bf14a1fa0a9edee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118183417"
---
# <a name="setting-permissions-on-a-group-of-properties"></a>設定屬性群組的許可權

許可權可以套用至屬性的群組。 屬性集是由 [**controlAccessRight**](/windows/desktop/ADSchema/c-controlaccessright)物件之 [**rightsGUID**](/windows/desktop/ADSchema/a-rightsguid)屬性中的 GUID 所識別。 此 GUID 是在群組中每個屬性之 [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema)物件的 [**attributeSecurityGUID**](/windows/desktop/ADSchema/a-attributesecurityguid)屬性中設定。

下列程式示範如何設定適用于物件屬性群組的許可權。

**若要設定適用于物件屬性群組的許可權**

1.  將 [**IADsAccessControlEntry. AccessMask**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) 屬性設定為 [ **ads \_ right \_ ds \_ 讀取 \_**] 屬性、[ **廣告正確的 \_ \_ ds \_ 寫入 \_** ] 屬性或兩個 [值] 組合。
2.  將 [**IADsAccessControlEntry AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) 屬性設定為 **ADS \_ AceType \_ 存取允許的 \_ \_ 物件** 或 **ads \_ AceType \_ 拒絕存取 \_ \_ 物件**。
3.  將 [ [**IADsAccessControlEntry**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) ] 屬性設定為屬性集的 GUID。 這是識別屬性集之 [**controlAccessRight**](/windows/desktop/ADSchema/c-controlaccessright)物件的 [**rightsGUID**](/windows/desktop/ADSchema/a-rightsguid)屬性。 此 GUID 也會設定為群組中每個屬性之 attributeSchema 物件的 [**attributeSecurityGUID**](/windows/desktop/ADSchema/a-attributesecurityguid) 。
4.  將 [ [**IADsAccessControlEntry**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) ] 屬性設定為 [ **ADS \_ 旗標 \_ 物件 \_ 類型 \_**]。

請注意，您不應該在 [**IADsAccessControlEntry. AccessMask**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods)屬性中設定 **ADS 的 \_ 正確 \_ DS \_ 控制 \_ 存取** 旗標。 此旗標只會用來指定控制項存取權限。

如需可用於設定屬性集之存取權限的詳細資訊和程式碼範例，請參閱 [設定屬性群組許可權的範例程式碼](example-code-for-setting-permissions-on-a-group-of-properties.md)。

如需建立 ACE 的詳細資訊，請參閱 [設定物件的存取權限](setting-access-rights-on-an-object.md)。

如需可用於設定屬性集之 ACE 的詳細資訊和程式碼範例，請參閱 [在目錄物件上設定 ace 的範例程式碼](example-code-for-setting-an-ace-on-a-directory-object.md)。

 

 