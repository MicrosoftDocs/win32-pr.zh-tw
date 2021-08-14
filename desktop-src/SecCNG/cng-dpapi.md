---
description: Microsoft 在 Windows 2000 中引進了 (DPAPI) 的資料保護應用程式設計介面。
ms.assetid: 048DEA72-39E1-4129-A554-F7D08442C2D9
title: CNG DPAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0273522580c806caa5fe7848ff32a2017cfb37c4499dee21f5a3787ecae57b63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118908627"
---
# <a name="cng-dpapi"></a>CNG DPAPI

Microsoft 在 Windows 2000 中引進了 (DPAPI) 的資料保護應用程式設計介面。 API 包含兩個函數： [**CryptProtectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata) 和 [**CryptUnprotectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectdata)。 DPAPI 是 CryptoAPI 的一部分，適用于只知道使用加密功能的開發人員。 這兩個函數可用來加密和解密單一電腦上的靜態資料。

不過，雲端運算通常需要在一部電腦上加密內容，才能在另一部電腦上解密。 因此，從 Windows 8 開始，Microsoft 擴充了使用相當簡單的 API 來包含雲端案例的概念。 這個新的 API （稱為 DPAPI）可讓您安全地共用秘密 (金鑰、密碼、金鑰材料) 和訊息，方法是保護這些秘密，以在適當的驗證和授權之後，用來在不同電腦上解除保護這些秘密。 目前支援下列主體：

-   Active Directory 樹系中的群組。
-   Web 認證。

如需詳細資訊，請參閱下列主題：

-   [保護提供者](protection-providers.md)
-   [保護描述項](protection-descriptors.md)
-   [受保護的資料格式](protected-data-format.md)

DPAPI-NG 建置於新一代密碼編譯 (CNG) 之上，並包含下列功能：

-   [**NCryptCreateProtectionDescriptor**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcreateprotectiondescriptor)
-   [**NCryptCloseProtectionDescriptor**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcloseprotectiondescriptor)
-   [**NCryptProtectSecret**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptprotectsecret)
-   [**NCryptQueryProtectionDescriptorName**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptqueryprotectiondescriptorname)
-   [**NCryptRegisterProtectionDescriptorName**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptregisterprotectiondescriptorname)
-   [**NCryptStreamClose**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptstreamclose)
-   [**NCryptStreamOpenToProtect**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptstreamopentoprotect)
-   [**NCryptStreamOpenToUnprotect**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptstreamopentounprotect)
-   [**NCryptStreamUpdate**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptstreamupdate)
-   [**NCryptUnprotectSecret**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptunprotectsecret)

 

 
