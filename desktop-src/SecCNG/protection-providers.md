---
description: 從 Windows 8 開始，Microsoft 開始散發可讓您安全地在電腦之間共用加密秘密和訊息的提供者。
ms.assetid: C2E62DD2-8316-407B-B879-2617873F8409
title: 保護提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc2c262fcfbfa5ab0842f103849af3d67b20f8e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943930"
---
# <a name="protection-providers"></a>保護提供者

從 Windows 8 開始，Microsoft 開始散發可讓您安全地在電腦之間共用加密秘密和訊息的提供者。 目前有兩個金鑰保護提供者。 Microsoft 金鑰保護提供者可讓您保護 Active Directory 樹系中群組的內容。 Microsoft 用戶端金鑰保護提供者可讓您將內容保護為一組 web 認證。

當 [**NCryptCreateProtectionDescriptor**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcreateprotectiondescriptor) 函式剖析您提供做為輸入的保護描述項規則字串時，會自動為您選擇所要使用的正確保護裝置。 針對以 SID、SDDL 和本機開頭的規則字串選擇 Microsoft 金鑰保護提供者。 Microsoft 用戶端金鑰保護提供者會剖析以 WEBCREDENTIALS 開頭的規則字串。 如需規則字串的詳細資訊，請參閱 [保護描述](protection-descriptors.md)項。

> [!Note]  
> 目前不允許自訂提供者。[CNG DPAPI](cng-dpapi.md)

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[CNG DPAPI](cng-dpapi.md)
</dt> <dt>

[**NCryptCreateProtectionDescriptor**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcreateprotectiondescriptor)
</dt> <dt>

[保護描述項](protection-descriptors.md)
</dt> </dl>

 

 



