---
title: 預設安全描述項
description: 使用 Active Directory Domain Services，您也可以為每種類型的物件指定預設的安全性。
ms.assetid: 6642c966-c163-4d63-8707-62a545d15094
ms.tgt_platform: multiple
keywords:
- 預設安全描述項 AD
- 安全描述項 AD、預設
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 372f285c3e8c17b481811d7356c40ae07316801d
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104023261"
---
# <a name="default-security-descriptor"></a>預設安全描述項

使用 Active Directory Domain Services，您也可以為每種類型的物件指定預設的安全性。 這是在 [Active Directory 架構](active-directory-schema.md)中 [**classSchema**](/windows/desktop/ADSchema/c-classschema)物件定義的 [**defaultSecurityDescriptor**](/windows/desktop/ADSchema/a-defaultsecuritydescriptor)屬性中指定。 如果在建立物件期間未指定任何安全描述項，則會使用這個安全描述項來提供物件的預設保護。

> [!Note]  
> 預設安全描述項中的 Ace 會以在建立物件時所指定的方式來處理。 因此，預設 Ace 會放置在繼承的 Ace 前面，並視需要加以覆寫。 如需詳細資訊，請參閱 [DACL 中的 Ace 順序](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl)。

 

[**DefaultSecurityDescriptor**](/windows/desktop/ADSchema/a-defaultsecuritydescriptor)是使用 [安全描述項定義語言](/windows/desktop/SecAuthZ/security-descriptor-definition-language) (SDDL) 以特殊字元串格式指定。 您可以使用兩個函式，將安全描述項的二進位形式轉換成字串格式，反之亦然。 這些函式是：

-   [ConvertSecurityDescriptorToStringSecurityDescriptor](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora)
-   [ConvertStringSecurityDescriptorToSecurityDescriptor](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora)

如需預先定義之物件類別的詳細資訊和預設安全描述項，請參閱 [Active Directory Domain Services 參考](active-directory-domain-services-reference.md)的 Active Directory 架構參考中的類別參考頁面。

如需讀取或修改物件類別之 [**defaultSecurityDescriptor**](/windows/desktop/ADSchema/a-defaultsecuritydescriptor) 屬性的詳細資訊和程式碼範例，請參閱 [讀取物件類別的 DefaultSecurityDescriptor](reading-the-defaultsecuritydescriptor-for-an-object-class.md) ，以及 [修改物件類別的 defaultSecurityDescriptor](modifying-the-defaultsecuritydescriptor-for-an-object-class.md)。

 

 