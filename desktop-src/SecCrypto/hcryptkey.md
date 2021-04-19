---
description: HCRYPTKEY 資料類型是用來代表密碼編譯金鑰的控制碼。
ms.assetid: d62f1d40-4f42-4684-96d7-de88db67dceb
title: 'HCRYPTKEY (Wincrypt) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56bda14169aa2f4d7c6e502d3444473ea0f00408
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985031"
---
# <a name="hcryptkey"></a><span data-ttu-id="62c4e-103">HCRYPTKEY</span><span class="sxs-lookup"><span data-stu-id="62c4e-103">HCRYPTKEY</span></span>

<span data-ttu-id="62c4e-104">**HCRYPTKEY** 資料類型是用來代表 [*密碼編譯金鑰*](../secgloss/c-gly.md)的控制碼。</span><span class="sxs-lookup"><span data-stu-id="62c4e-104">The **HCRYPTKEY** data type is used to represent handles to [*cryptographic keys*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="62c4e-105">這些控制碼可用來向 CSP 模組指出特定作業中所使用的金鑰。</span><span class="sxs-lookup"><span data-stu-id="62c4e-105">These handles are used to indicate to the CSP module which key is being used in a specific operation.</span></span> <span data-ttu-id="62c4e-106">CSP 模組不允許直接存取金鑰值。</span><span class="sxs-lookup"><span data-stu-id="62c4e-106">The CSP module does not enable direct access to the key values.</span></span> <span data-ttu-id="62c4e-107">相反地，使用者會透過金鑰控制碼使用索引鍵值來執行函數。</span><span class="sxs-lookup"><span data-stu-id="62c4e-107">Instead, the user performs functions by using the key value through the key handle.</span></span>


```C++
typedef ULONG_PTR HCRYPTKEY;
```



## <a name="requirements"></a><span data-ttu-id="62c4e-108">規格需求</span><span class="sxs-lookup"><span data-stu-id="62c4e-108">Requirements</span></span>



| <span data-ttu-id="62c4e-109">需求</span><span class="sxs-lookup"><span data-stu-id="62c4e-109">Requirement</span></span> | <span data-ttu-id="62c4e-110">值</span><span class="sxs-lookup"><span data-stu-id="62c4e-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="62c4e-111">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="62c4e-111">Minimum supported client</span></span><br/> | <span data-ttu-id="62c4e-112">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="62c4e-112">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="62c4e-113">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="62c4e-113">Minimum supported server</span></span><br/> | <span data-ttu-id="62c4e-114">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="62c4e-114">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="62c4e-115">標頭</span><span class="sxs-lookup"><span data-stu-id="62c4e-115">Header</span></span><br/>                   | <dl> <span data-ttu-id="62c4e-116"><dt>Wincrypt。h</dt></span><span class="sxs-lookup"><span data-stu-id="62c4e-116"><dt>Wincrypt.h</dt></span></span> </dl> |



 

 
