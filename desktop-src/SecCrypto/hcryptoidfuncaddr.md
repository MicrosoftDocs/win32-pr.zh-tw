---
description: 代表物件識別碼的控制碼， (OID) 可安裝的函式。
ms.assetid: 06492b94-9717-40e0-be96-f97f42ac34af
title: 'HCRYPTOIDFUNCADDR (Wincrypt) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4f083d87234e598e8464491f2968868fa2b3c8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984648"
---
# <a name="hcryptoidfuncaddr"></a><span data-ttu-id="90d69-103">HCRYPTOIDFUNCADDR</span><span class="sxs-lookup"><span data-stu-id="90d69-103">HCRYPTOIDFUNCADDR</span></span>

<span data-ttu-id="90d69-104">**HCRYPTOIDFUNCADDR** 資料類型代表 [*物件識別碼*](../secgloss/o-gly.md)的控制碼， (OID) 可安裝的函式。</span><span class="sxs-lookup"><span data-stu-id="90d69-104">The **HCRYPTOIDFUNCADDR** data type represents a handle to an [*object identifier*](../secgloss/o-gly.md) (OID) installable function.</span></span> <span data-ttu-id="90d69-105">[**CryptGetDefaultOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetdefaultoidfunctionaddress)、 [**CryptGetOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetoidfunctionaddress)和 [**CryptFreeOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfreeoidfunctionaddress)函數以及 [**CERT \_ STORE \_ >prov \_ 資訊**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_info)結構都會使用此資料類型。</span><span class="sxs-lookup"><span data-stu-id="90d69-105">The [**CryptGetDefaultOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetdefaultoidfunctionaddress), [**CryptGetOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetoidfunctionaddress), and [**CryptFreeOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfreeoidfunctionaddress) functions, and the [**CERT\_STORE\_PROV\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_info) structure use this data type.</span></span>


```C++
typedef void* HCRYPTOIDFUNCADDR;
```



## <a name="requirements"></a><span data-ttu-id="90d69-106">規格需求</span><span class="sxs-lookup"><span data-stu-id="90d69-106">Requirements</span></span>



| <span data-ttu-id="90d69-107">需求</span><span class="sxs-lookup"><span data-stu-id="90d69-107">Requirement</span></span> | <span data-ttu-id="90d69-108">值</span><span class="sxs-lookup"><span data-stu-id="90d69-108">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="90d69-109">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="90d69-109">Minimum supported client</span></span><br/> | <span data-ttu-id="90d69-110">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="90d69-110">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="90d69-111">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="90d69-111">Minimum supported server</span></span><br/> | <span data-ttu-id="90d69-112">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="90d69-112">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="90d69-113">標頭</span><span class="sxs-lookup"><span data-stu-id="90d69-113">Header</span></span><br/>                   | <dl> <span data-ttu-id="90d69-114"><dt>Wincrypt。h</dt></span><span class="sxs-lookup"><span data-stu-id="90d69-114"><dt>Wincrypt.h</dt></span></span> </dl> |



 

 
