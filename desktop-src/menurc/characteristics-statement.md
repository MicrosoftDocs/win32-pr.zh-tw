---
title: 特性語句
description: 定義可供讀取和寫入資源定義檔的工具使用之資源的相關資訊。
ms.assetid: 07834b02-a36e-40cc-8907-bff6631842f3
keywords:
- 特性語句功能表和其他資源
topic_type:
- apiref
api_name:
- CHARACTERISTICS
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de681785fa2ec815b1edbdda913dd8032f8feb8e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104022454"
---
# <a name="characteristics-statement"></a><span data-ttu-id="01c47-104">特性語句</span><span class="sxs-lookup"><span data-stu-id="01c47-104">CHARACTERISTICS statement</span></span>

<span data-ttu-id="01c47-105">定義可供讀取和寫入資源定義檔的工具使用之資源的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="01c47-105">Defines information about a resource that can be used by tools that read and write resource-definition files.</span></span> <span data-ttu-id="01c47-106">在編譯的 .res 檔中，會顯示指定的 **DWORD** 值與資源。</span><span class="sxs-lookup"><span data-stu-id="01c47-106">The specified **DWORD** value appears with the resource in the compiled .res file.</span></span> <span data-ttu-id="01c47-107">不過，此值不會儲存在可執行檔中，而且對系統沒有任何意義。</span><span class="sxs-lookup"><span data-stu-id="01c47-107">However, the value is not stored in the executable file and has no significance to the system.</span></span>

<span data-ttu-id="01c47-108">**特性** 語句會出現在 [**加速器**](accelerators-resource.md)、[**對話方塊**](dialog-resource.md)、[**功能表**](menu-resource.md)、 [**RCDATA**](rcdata-resource.md)或 [**STRINGTABLE**](stringtable-resource.md)資源定義的主體開頭之前。</span><span class="sxs-lookup"><span data-stu-id="01c47-108">The **CHARACTERISTICS** statement appears before the beginning of the body of an [**ACCELERATORS**](accelerators-resource.md), [**DIALOG**](dialog-resource.md), [**MENU**](menu-resource.md), [**RCDATA**](rcdata-resource.md), or [**STRINGTABLE**](stringtable-resource.md) resource definition.</span></span> <span data-ttu-id="01c47-109">指定的值僅適用于該資源。</span><span class="sxs-lookup"><span data-stu-id="01c47-109">The specified value applies only to that resource.</span></span>

``` syntax
CHARACTERISTICS dword
```

<dl> <dt>

<span data-ttu-id="01c47-110"><span id="dword"></span><span id="DWORD"></span>*Dword*</span><span class="sxs-lookup"><span data-stu-id="01c47-110"><span id="dword"></span><span id="DWORD"></span>*dword*</span></span>
</dt> <dd>

<span data-ttu-id="01c47-111">使用者定義的 **DWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="01c47-111">User-defined **DWORD** value.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="01c47-112">另請參閱</span><span class="sxs-lookup"><span data-stu-id="01c47-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01c47-113">**加速器**</span><span class="sxs-lookup"><span data-stu-id="01c47-113">**ACCELERATORS**</span></span>](accelerators-resource.md)
</dt> <dt>

[<span data-ttu-id="01c47-114">**對話 框**</span><span class="sxs-lookup"><span data-stu-id="01c47-114">**DIALOG**</span></span>](dialog-resource.md)
</dt> <dt>

[<span data-ttu-id="01c47-115">**語言**</span><span class="sxs-lookup"><span data-stu-id="01c47-115">**LANGUAGE**</span></span>](language-statement.md)
</dt> <dt>

[<span data-ttu-id="01c47-116">**功能表**</span><span class="sxs-lookup"><span data-stu-id="01c47-116">**MENU**</span></span>](menu-resource.md)
</dt> <dt>

[<span data-ttu-id="01c47-117">**RCDATA**</span><span class="sxs-lookup"><span data-stu-id="01c47-117">**RCDATA**</span></span>](rcdata-resource.md)
</dt> <dt>

[<span data-ttu-id="01c47-118">**STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="01c47-118">**STRINGTABLE**</span></span>](stringtable-resource.md)
</dt> </dl>

 

 




