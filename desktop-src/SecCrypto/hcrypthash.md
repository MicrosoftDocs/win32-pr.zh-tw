---
description: HCRYPTHASH 資料類型是用來表示雜湊物件的控制碼。
ms.assetid: 3b872bf0-cf1b-465b-82a2-c6fd154e1125
title: 'HCRYPTHASH (Wincrypt) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a009350ed910627c1e6ec9ae33997ed20c7fec2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851296"
---
# <a name="hcrypthash"></a><span data-ttu-id="1e37d-103">HCRYPTHASH</span><span class="sxs-lookup"><span data-stu-id="1e37d-103">HCRYPTHASH</span></span>

<span data-ttu-id="1e37d-104">**HCRYPTHASH** 資料類型是用來表示 [*雜湊物件*](../secgloss/h-gly.md)的控制碼。</span><span class="sxs-lookup"><span data-stu-id="1e37d-104">The **HCRYPTHASH** data type is used to represent handles to [*hash objects*](../secgloss/h-gly.md).</span></span> <span data-ttu-id="1e37d-105">這些控點會向 CSP 模組指出特定作業中使用的雜湊。</span><span class="sxs-lookup"><span data-stu-id="1e37d-105">These handles indicate to the CSP module which hash is being used in a particular operation.</span></span> <span data-ttu-id="1e37d-106">CSP 模組不允許直接操作雜湊值。</span><span class="sxs-lookup"><span data-stu-id="1e37d-106">The CSP module does not enable direct manipulation of the hash values.</span></span> <span data-ttu-id="1e37d-107">相反地，使用者會透過雜湊控制碼來操控雜湊值。</span><span class="sxs-lookup"><span data-stu-id="1e37d-107">Instead, the user manipulates the hash values through the hash handle.</span></span>


```C++
typedef ULONG_PTR HCRYPTHASH;
```



## <a name="requirements"></a><span data-ttu-id="1e37d-108">規格需求</span><span class="sxs-lookup"><span data-stu-id="1e37d-108">Requirements</span></span>



| <span data-ttu-id="1e37d-109">需求</span><span class="sxs-lookup"><span data-stu-id="1e37d-109">Requirement</span></span> | <span data-ttu-id="1e37d-110">值</span><span class="sxs-lookup"><span data-stu-id="1e37d-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1e37d-111">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1e37d-111">Minimum supported client</span></span><br/> | <span data-ttu-id="1e37d-112">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1e37d-112">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="1e37d-113">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1e37d-113">Minimum supported server</span></span><br/> | <span data-ttu-id="1e37d-114">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1e37d-114">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1e37d-115">標頭</span><span class="sxs-lookup"><span data-stu-id="1e37d-115">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e37d-116"><dt>Wincrypt。h</dt></span><span class="sxs-lookup"><span data-stu-id="1e37d-116"><dt>Wincrypt.h</dt></span></span> </dl> |



 

 
