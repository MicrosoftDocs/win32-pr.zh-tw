---
title: 設定子物件作業的許可權
description: 您也可以針對特定類別的所有子系或子系上的作業，授與或拒絕許可權，例如「建立子系」和「刪除子系」。
ms.assetid: fe2f8939-7562-4c03-a7a9-3ac5fc3e81bb
ms.tgt_platform: multiple
keywords:
- 設定子物件作業的許可權 AD
- 物件 AD、子系、設定子物件作業的許可權
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f136119d5e61ea312748d5cd64cabb8c0aee0b651d8b192519dc2d74e2045cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024766"
---
# <a name="setting-permissions-on-child-object-operations"></a>設定子物件作業的許可權

您也可以針對特定類別的所有子系或子系上的作業，授與或拒絕許可權，例如「建立子系」和「刪除子系」。

下列程式可以用來設定特定子物件類型的許可權。

**若要設定特定子物件類型的許可權**

1.  將 [**IADsAccessControlEntry AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) 屬性設定為 **ADS \_ AceType \_ 存取允許的 \_ \_ 物件** 或 **ads \_ AceType \_ 拒絕存取 \_ \_ 物件**。
2.  將 [ [**IADsAccessControlEntry**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) ] 屬性設定為物件類別的 GUID。 這是定義物件類別之 classSchema 物件的 **schemaIDGUID** 屬性。 如果 **ObjectType** 屬性為 **Null**，ACE 會套用至任何類別的子物件。
3.  將 [ [**IADsAccessControlEntry**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) ] 屬性設定為 [ **ADS \_ 旗標 \_ 物件 \_ 類型 \_**]。

如需建立 ACE 的詳細資訊和程式，請參閱 [設定物件的存取權限](setting-access-rights-on-an-object.md)。

如需可用於設定可控制子物件作業之 ACE 的詳細資訊和程式碼範例，請參閱 [在目錄物件上設定 ace 的範例程式碼](example-code-for-setting-an-ace-on-a-directory-object.md)。

 

 