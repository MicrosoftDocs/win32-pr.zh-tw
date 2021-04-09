---
title: VERSION 語句
description: 定義可供讀取和寫入資源檔的工具使用之資源的版本資訊。
ms.assetid: 3a33cff3-b8b3-43f4-b43a-ff1d1728cdc1
keywords:
- 版本語句功能表和其他資源
topic_type:
- apiref
api_name:
- VERSION
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 302ffcee38b287afff2697b9c5a5241fa406b55c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678540"
---
# <a name="version-statement"></a><span data-ttu-id="0255a-104">VERSION 語句</span><span class="sxs-lookup"><span data-stu-id="0255a-104">VERSION statement</span></span>

<span data-ttu-id="0255a-105">定義可供讀取和寫入資源檔的工具使用之資源的版本資訊。</span><span class="sxs-lookup"><span data-stu-id="0255a-105">Defines version information about a resource that can be used by tools that read and write resource files.</span></span> <span data-ttu-id="0255a-106">指定的 *dword* 值會隨著資源出現在已編譯的中。RES 檔。</span><span class="sxs-lookup"><span data-stu-id="0255a-106">The specified *dword* value appears with the resource in the compiled .RES file.</span></span> <span data-ttu-id="0255a-107">不過，此值不會儲存在可執行檔中，而且對系統沒有任何意義。</span><span class="sxs-lookup"><span data-stu-id="0255a-107">However, the value is not stored in the executable file and has no significance to the system.</span></span>

<span data-ttu-id="0255a-108">**版本** 語句會出現在 [**加速器**](accelerators-resource.md)、 [**DIALOGEX**](dialogex-resource.md)、[**功能表**](menu-resource.md)、 [**RCDATA**](rcdata-resource.md)或 [**STRINGTABLE**](stringtable-resource.md)資源定義的主體開頭之前。</span><span class="sxs-lookup"><span data-stu-id="0255a-108">The **VERSION** statement appears before the beginning of the body of an [**ACCELERATORS**](accelerators-resource.md), [**DIALOGEX**](dialogex-resource.md), [**MENU**](menu-resource.md), [**RCDATA**](rcdata-resource.md), or [**STRINGTABLE**](stringtable-resource.md) resource definition.</span></span> <span data-ttu-id="0255a-109">指定的值僅適用于該資源。</span><span class="sxs-lookup"><span data-stu-id="0255a-109">The specified value applies only to that resource.</span></span>

``` syntax
VERSION dword
```

<dl> <dt>

<span data-ttu-id="0255a-110"><span id="dword"></span><span id="DWORD"></span>*Dword*</span><span class="sxs-lookup"><span data-stu-id="0255a-110"><span id="dword"></span><span id="DWORD"></span>*dword*</span></span>
</dt> <dd>

<span data-ttu-id="0255a-111">使用者定義的 **DWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="0255a-111">A user-defined **DWORD** value.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="0255a-112">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0255a-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0255a-113">**加速器**</span><span class="sxs-lookup"><span data-stu-id="0255a-113">**ACCELERATORS**</span></span>](accelerators-resource.md)
</dt> <dt>

[<span data-ttu-id="0255a-114">**特徵**</span><span class="sxs-lookup"><span data-stu-id="0255a-114">**CHARACTERISTICS**</span></span>](characteristics-statement.md)
</dt> <dt>

[<span data-ttu-id="0255a-115">**語言**</span><span class="sxs-lookup"><span data-stu-id="0255a-115">**LANGUAGE**</span></span>](language-statement.md)
</dt> <dt>

[<span data-ttu-id="0255a-116">**功能表**</span><span class="sxs-lookup"><span data-stu-id="0255a-116">**MENU**</span></span>](menu-resource.md)
</dt> <dt>

[<span data-ttu-id="0255a-117">**RCDATA**</span><span class="sxs-lookup"><span data-stu-id="0255a-117">**RCDATA**</span></span>](rcdata-resource.md)
</dt> <dt>

[<span data-ttu-id="0255a-118">**STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="0255a-118">**STRINGTABLE**</span></span>](stringtable-resource.md)
</dt> </dl>

 

 




