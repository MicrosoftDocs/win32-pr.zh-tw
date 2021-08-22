---
title: 將許可權設定為特定物件類型的特定屬性
description: 屬性特定的許可權可以與物件特定繼承搭配使用，以提供功能強大且詳細的管理委派。
ms.assetid: d2ebbe3a-78f7-4bb5-bac0-13236031b7b1
ms.tgt_platform: multiple
keywords:
- 將許可權設定為特定物件類型的特定屬性（AD）
- Active Directory，使用，安全性，設定特定屬性的許可權
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86c01070b5c5b23e7524bd3b54293576e578861e0120b431e6dc95b7a5b4cc4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024736"
---
# <a name="setting-rights-to-specific-properties-of-specific-types-of-objects"></a>將許可權設定為特定物件類型的特定屬性

屬性特定的許可權可以與物件特定繼承搭配使用，以提供功能強大且詳細的管理委派。 您可以設定屬性特定的物件-可繼承的 ACE，以允許指定的使用者或群組在容器中的特定子物件類別上讀取和/或寫入特定屬性。 例如，您可以在組織單位上設定 ACE (OU) ，讓群組能夠讀取和寫入 OU 中所有使用者物件的電話號碼屬性。

**設定屬性特定物件-可繼承的 Ace**

1.  將 [**IADsAccessControlEntry AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) 設定為 **ADS \_ AceType \_ 存取 \_ 允許的 \_ 物件** 或 **ads \_ AceType \_ \_ 拒絕存取 \_ 物件**。
2.  將 [**IADsAccessControlEntry**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) 設定為屬性的 **schemaIDGUID** 。 例如， **telephoneNumber** 屬性的 **schemaIDGUID** 是 {bf967a49-0de6-11d0-a285-00aa003049e2}。
3.  將 [**IADsAccessControlEntry AceFlags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) 設定為 **ADS \_ ACEFLAG \_ INHERIT \_ ACE**。
4.  將 [**IADsAccessControlEntry. InheritedObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) 設定為可繼承 ACE 之物件類別的 **schemaIDGUID** 。 例如，**使用者** 類別的 **schemaIDGUID** 是 {bf967aba-0de6-11d0-a285-00aa003049e2}。
5.  將 [**IADsAccessControlEntry**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) 設定為 **ads \_ 旗標 \_ 物件 \_ 類型 \_ 存在** ， **廣告 \_ 旗標繼承的 \_ \_ 物件 \_ 類型 \_ 存在**。

> [!IMPORTANT]
> Set ADS \_ ACEFLAG \_ INHERIT \_ ACE，使 ace 成為繼承的。 此外， \_ \_ \_ \_ 如果套用此 ace 的物件類型不符合指定 ace 之容器的物件類型，則設定 ADS ACEFLAG 只會繼承 ace。 如果未這麼做，ACE 也會在容器上生效，而且可以授與非預期的許可權。

 

如需可用來設定這類 ACE 的詳細資訊和程式碼範例，請參閱 [在目錄物件上設定 ACE 的範例程式碼](example-code-for-setting-an-ace-on-a-directory-object.md)。

 

 