---
title: 物件名稱和身分識別
description: Active Directory Domain Services 中的物件有數個身分識別，包括下列各項。
ms.assetid: ad8bc74d-45a8-4df3-bfb8-35dd376b9c0b
ms.tgt_platform: multiple
keywords:
- 物件名稱和身分識別 Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a803b4cc068a3ee0f9e2a75f61ff239c1d971bf3
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104462844"
---
# <a name="object-names-and-identities"></a>物件名稱和身分識別

Active Directory Domain Services 中的物件有數個身分識別，包括下列各項。

## <a name="relative-distinguished-name"></a>相對辨別名稱

相對分辨名稱是物件命名屬性所定義的名稱。 **ClassSchema** 物件的 **rDnAttID** 屬性會識別類別實例的命名屬性。 大部分的物件類別都會使用 **cn** (一般名稱) 屬性做為命名屬性。 物件的相對辨別名稱在物件所在的容器中必須是唯一的。 您可以有多個具有相同相對分辨名稱的物件實例，但在相同的容器中不能有兩個。 如需 **rDnAttID** 屬性和 **classSchema** 物件的詳細資訊，請參閱 [物件類別的特性](characteristics-of-object-classes.md)。

## <a name="distinguished-name"></a>辨別名稱

[*辨別名稱*](/previous-versions/windows/desktop/legacy/ms681901(v=vs.85))是物件的目前名稱，並且包含在物件的 **distinguishedName** 屬性中。 辨別名稱是一個字串，其中包含物件的位置，而是藉由將物件的相對辨別名稱和每個祖系串連至根目錄來形成。 例如，Fabrikam.com 網域中使用者容器的分辨名稱將會是 "CN = Users，DC = Fabrikam，DC = com"。 辨別名稱在樹系中是唯一的。 移動或重新命名物件時，物件的辨別名稱會變更。

## <a name="object-guid"></a>物件 GUID

物件 GUID 是物件實例建立時，由 Active Directory Domain Services 指派的全域唯一識別碼。 物件 GUID 包含在物件的 **objectGUID** 屬性中。 GUID 是在空間和時間中保證是唯一的128位數位。 物件 Guid 永遠不會變更，因此，如果物件已重新命名或移至企業樹系中的任何位置，物件 GUID 會維持不變。 在 Active Directory Domain Services 中儲存物件參考的應用程式必須使用物件 GUID，以確保物件參考在物件重新命名後仍然存在。 物件的分辨名稱可能會變更，但物件 GUID 則不會變更。

## <a name="other-identities"></a>其他身分識別

物件實例可以有許多其他屬性，而這些屬性可用於應用程式的識別。 例如， **使用者**、 **電腦** 和 **群組** 物件類別 (實例的安全性主體物件) 有 **userPrincipalName**、 **sAMAccountName** 和 **objectSid** 屬性。 這些屬性對於 Windows 2000 而言是很重要的「名稱」，但是這些屬性不是來自目錄觀點的物件身分識別的一部分。

 

 