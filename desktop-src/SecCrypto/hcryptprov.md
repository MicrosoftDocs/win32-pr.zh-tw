---
description: HCRYPTPROV 資料類型是用來表示 Csp 的控制碼。 這些控制碼可用來指出哪個 CSP 模組會執行特定的作業。
ms.assetid: 8ec6b392-06bc-4717-8657-7ea9a43d03fb
title: 'HCRYPTPROV (Wincrypt) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c14c74770b0cca86adaaa72ad38bff3397fa15b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944871"
---
# <a name="hcryptprov"></a><span data-ttu-id="4a979-104">HCRYPTPROV</span><span class="sxs-lookup"><span data-stu-id="4a979-104">HCRYPTPROV</span></span>

<span data-ttu-id="4a979-105">**HCRYPTPROV** 資料類型是用來表示 csp 的控制碼。</span><span class="sxs-lookup"><span data-stu-id="4a979-105">The **HCRYPTPROV** data type is used to represent handles to CSPs.</span></span> <span data-ttu-id="4a979-106">這些控制碼可用來指出哪個 CSP 模組會執行特定的作業。</span><span class="sxs-lookup"><span data-stu-id="4a979-106">These handles are used to indicate which CSP module performs specific operations.</span></span>


```C++
typedef ULONG_PTR HCRYPTPROV;
```



## <a name="requirements"></a><span data-ttu-id="4a979-107">規格需求</span><span class="sxs-lookup"><span data-stu-id="4a979-107">Requirements</span></span>



| <span data-ttu-id="4a979-108">需求</span><span class="sxs-lookup"><span data-stu-id="4a979-108">Requirement</span></span> | <span data-ttu-id="4a979-109">值</span><span class="sxs-lookup"><span data-stu-id="4a979-109">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4a979-110">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4a979-110">Minimum supported client</span></span><br/> | <span data-ttu-id="4a979-111">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4a979-111">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="4a979-112">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4a979-112">Minimum supported server</span></span><br/> | <span data-ttu-id="4a979-113">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4a979-113">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4a979-114">標頭</span><span class="sxs-lookup"><span data-stu-id="4a979-114">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a979-115"><dt>Wincrypt。h</dt></span><span class="sxs-lookup"><span data-stu-id="4a979-115"><dt>Wincrypt.h</dt></span></span> </dl> |



 

 




