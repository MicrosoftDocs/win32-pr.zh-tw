---
description: 不透明的資料類型。
ms.assetid: 384dd6e0-726f-4100-a036-1cca6a332a64
title: 'PLSA_CLIENT_REQUEST (Ntsecpkg) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a3685c3cd38843edfd4ae708a18761b6ee698c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104192951"
---
# <a name="plsa_client_request"></a><span data-ttu-id="4ea6d-103">PLSA \_ 用戶端 \_ 要求</span><span class="sxs-lookup"><span data-stu-id="4ea6d-103">PLSA\_CLIENT\_REQUEST</span></span>

<span data-ttu-id="4ea6d-104">**PLSA \_ 用戶端 \_ 要求** 資料類型是不透明的資料類型。</span><span class="sxs-lookup"><span data-stu-id="4ea6d-104">The **PLSA\_CLIENT\_REQUEST** data type is an opaque data type.</span></span>

<span data-ttu-id="4ea6d-105">[*本地安全機構*](../secgloss/l-gly.md) (LSA) 在內部使用它來維護與個別要求相關的用戶端資訊。</span><span class="sxs-lookup"><span data-stu-id="4ea6d-105">The [*Local Security Authority*](../secgloss/l-gly.md) (LSA) uses it internally to maintain client information related to individual requests.</span></span>


```C++
#include <windows.h>

typedef PVOID *PLSA_CLIENT_REQUEST;
```



## <a name="requirements"></a><span data-ttu-id="4ea6d-106">規格需求</span><span class="sxs-lookup"><span data-stu-id="4ea6d-106">Requirements</span></span>



| <span data-ttu-id="4ea6d-107">需求</span><span class="sxs-lookup"><span data-stu-id="4ea6d-107">Requirement</span></span> | <span data-ttu-id="4ea6d-108">值</span><span class="sxs-lookup"><span data-stu-id="4ea6d-108">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4ea6d-109">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4ea6d-109">Minimum supported client</span></span><br/> | <span data-ttu-id="4ea6d-110">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4ea6d-110">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="4ea6d-111">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4ea6d-111">Minimum supported server</span></span><br/> | <span data-ttu-id="4ea6d-112">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4ea6d-112">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4ea6d-113">標頭</span><span class="sxs-lookup"><span data-stu-id="4ea6d-113">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ea6d-114"><dt>Ntsecpkg。h</dt></span><span class="sxs-lookup"><span data-stu-id="4ea6d-114"><dt>Ntsecpkg.h</dt></span></span> </dl> |



 

 
