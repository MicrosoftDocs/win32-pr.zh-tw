---
title: 設定特定物件類型的許可權
description: 下列程式顯示如何設定只能由特定物件類別繼承的 ACE。
ms.assetid: 42712458-69c7-4fe1-bfb3-b3fb28092a56
ms.tgt_platform: multiple
keywords:
- 將許可權設定為物件的類型
- 物件 AD，將許可權設定為
- Active Directory，使用，安全性，將許可權設定為物件的類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6f44cfbe753e6f92787f8269eab1f4eab4c2e98
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103933042"
---
# <a name="setting-rights-to-specific-types-of-objects"></a>設定特定物件類型的許可權

下列程式顯示如何設定只能由特定物件類別繼承的 ACE。

 **設定只能由特定物件類別繼承的 ACE**

1.  將 [**IADsAccessControlEntry AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) 屬性設定為 **ADS \_ AceType \_ 存取允許的 \_ \_ 物件** 或 **ads \_ AceType \_ 拒絕存取 \_ \_ 物件**。
2.  將 [**IADsAccessControlEntry AceFlags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) 屬性設定為包含 ADS \_ ACEFLAG \_ INHERIT \_ ACE 旗標。
3.  將 [**IADsAccessControlEntry. InheritedObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) 屬性設定為可以繼承 ACE 之物件類別的 **schemaIDGUID** 。
4.  將 [ [**IADsAccessControlEntry**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) ] 屬性設定為 [ **ADS \_ 旗標繼承的 \_ 物件 \_ 類型 \_**]。

> [!IMPORTANT]
> Set **ADS \_ ACEFLAG \_ INHERIT \_ ace** ，使 ace 成為繼承的。 此外，如果套用此 ACE 的物件類型不符合指定 ACE 之容器的物件類型，則您必須設定 **ADS \_ ACEFLAG \_ \_ 僅繼承 \_ ace** 。 如果未這麼做，ACE 也會在容器上生效，而且可以授與非預期的許可權。

 

如需可用來設定這類 ACE 的詳細資訊和程式碼範例，請參閱 [在目錄物件上設定 ACE 的範例程式碼](example-code-for-setting-an-ace-on-a-directory-object.md)。

 

 