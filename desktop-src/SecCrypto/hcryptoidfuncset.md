---
description: 表示一組物件識別碼的控制碼， (OID) 可安裝的函式。
ms.assetid: 83b76466-dc55-4269-91a3-17c2e6102126
title: 'HCRYPTOIDFUNCSET (Wincrypt) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 437511de32de97d4fb226d299f224427267381ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975411"
---
# <a name="hcryptoidfuncset"></a><span data-ttu-id="a0931-103">HCRYPTOIDFUNCSET</span><span class="sxs-lookup"><span data-stu-id="a0931-103">HCRYPTOIDFUNCSET</span></span>

<span data-ttu-id="a0931-104">**HCRYPTOIDFUNCSET** 資料類型代表一組 [*物件識別碼*](../secgloss/o-gly.md)的控制碼， (OID) 可安裝的函式。</span><span class="sxs-lookup"><span data-stu-id="a0931-104">The **HCRYPTOIDFUNCSET** data type represents a handle to a set of [*object identifier*](../secgloss/o-gly.md) (OID) installable functions.</span></span> <span data-ttu-id="a0931-105">[**CryptGetDefaultOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetdefaultoidfunctionaddress)、 [**CryptGetOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetoidfunctionaddress)、 [**CryptFreeOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfreeoidfunctionaddress)和 [**CryptInitOIDFunctionSet**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinitoidfunctionset)函數會使用此資料類型。</span><span class="sxs-lookup"><span data-stu-id="a0931-105">The [**CryptGetDefaultOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetdefaultoidfunctionaddress), [**CryptGetOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetoidfunctionaddress), [**CryptFreeOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfreeoidfunctionaddress), and [**CryptInitOIDFunctionSet**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinitoidfunctionset) functions use this data type.</span></span>


```C++
typedef void* HCRYPTOIDFUNCSET;
```



## <a name="requirements"></a><span data-ttu-id="a0931-106">規格需求</span><span class="sxs-lookup"><span data-stu-id="a0931-106">Requirements</span></span>



| <span data-ttu-id="a0931-107">需求</span><span class="sxs-lookup"><span data-stu-id="a0931-107">Requirement</span></span> | <span data-ttu-id="a0931-108">值</span><span class="sxs-lookup"><span data-stu-id="a0931-108">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a0931-109">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a0931-109">Minimum supported client</span></span><br/> | <span data-ttu-id="a0931-110">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a0931-110">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a0931-111">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a0931-111">Minimum supported server</span></span><br/> | <span data-ttu-id="a0931-112">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a0931-112">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a0931-113">標頭</span><span class="sxs-lookup"><span data-stu-id="a0931-113">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0931-114"><dt>Wincrypt。h</dt></span><span class="sxs-lookup"><span data-stu-id="a0931-114"><dt>Wincrypt.h</dt></span></span> </dl> |



 

 
