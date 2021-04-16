---
title: LANGUAGE 語句
description: 定義所有資源的語言，直到下一個語言語句或檔案結尾為止。
ms.assetid: 175e27e2-903a-4aaf-89ef-532166b167e8
keywords:
- 語言語句功能表與其他資源
topic_type:
- apiref
api_name:
- LANGUAGE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9563ba2ec00362a3b9caa3911a701919a81cae1e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104507911"
---
# <a name="language-statement"></a><span data-ttu-id="256fb-104">LANGUAGE 語句</span><span class="sxs-lookup"><span data-stu-id="256fb-104">LANGUAGE statement</span></span>

<span data-ttu-id="256fb-105">定義所有資源的語言，直到下一個 **語言** 語句或檔案結尾為止。</span><span class="sxs-lookup"><span data-stu-id="256fb-105">Defines the language for all resources up to the next **LANGUAGE** statement or to the end of the file.</span></span>

<span data-ttu-id="256fb-106">當 **LANGUAGE** 語句出現在 [**加速器**](accelerators-resource.md)、 [**DIALOGEX**](dialogex-resource.md)、 [**MENU**](menu-resource.md)、 [**RCDATA**](rcdata-resource.md)或 [**STRINGTABLE**](stringtable-resource.md) 資源定義的主體開頭之前，指定的語言只適用于該資源。</span><span class="sxs-lookup"><span data-stu-id="256fb-106">When the **LANGUAGE** statement appears before the beginning of the body of an [**ACCELERATORS**](accelerators-resource.md), [**DIALOGEX**](dialogex-resource.md), [**MENU**](menu-resource.md), [**RCDATA**](rcdata-resource.md), or [**STRINGTABLE**](stringtable-resource.md) resource definition, the specified language applies only to that resource.</span></span>

``` syntax
LANGUAGE language, sublanguage
```

<dl> <dt>

<span data-ttu-id="256fb-107"><span id="language"></span><span id="LANGUAGE"></span>*語言*</span><span class="sxs-lookup"><span data-stu-id="256fb-107"><span id="language"></span><span id="LANGUAGE"></span>*language*</span></span>
</dt> <dd>

<span data-ttu-id="256fb-108">語言識別項。</span><span class="sxs-lookup"><span data-stu-id="256fb-108">Language identifier.</span></span>

</dd> <dt>

<span data-ttu-id="256fb-109"><span id="sublanguage"></span><span id="SUBLANGUAGE"></span>*語言*</span><span class="sxs-lookup"><span data-stu-id="256fb-109"><span id="sublanguage"></span><span id="SUBLANGUAGE"></span>*sublanguage*</span></span>
</dt> <dd>

<span data-ttu-id="256fb-110">子語言識別項。</span><span class="sxs-lookup"><span data-stu-id="256fb-110">Sublanguage identifier.</span></span>

</dd> </dl>

<span data-ttu-id="256fb-111">如需詳細資訊，請參閱 [語言識別項常數和字串](/windows/desktop/Intl/language-identifier-constants-and-strings)。</span><span class="sxs-lookup"><span data-stu-id="256fb-111">For more information, see [Language Identifier Constants and Strings](/windows/desktop/Intl/language-identifier-constants-and-strings).</span></span>

## <a name="see-also"></a><span data-ttu-id="256fb-112">另請參閱</span><span class="sxs-lookup"><span data-stu-id="256fb-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="256fb-113">**加速器**</span><span class="sxs-lookup"><span data-stu-id="256fb-113">**ACCELERATORS**</span></span>](accelerators-resource.md)
</dt> <dt>

[<span data-ttu-id="256fb-114">**特徵**</span><span class="sxs-lookup"><span data-stu-id="256fb-114">**CHARACTERISTICS**</span></span>](characteristics-statement.md)
</dt> <dt>

[<span data-ttu-id="256fb-115">**功能表**</span><span class="sxs-lookup"><span data-stu-id="256fb-115">**MENU**</span></span>](menu-resource.md)
</dt> <dt>

[<span data-ttu-id="256fb-116">**RCDATA**</span><span class="sxs-lookup"><span data-stu-id="256fb-116">**RCDATA**</span></span>](rcdata-resource.md)
</dt> <dt>

[<span data-ttu-id="256fb-117">**STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="256fb-117">**STRINGTABLE**</span></span>](stringtable-resource.md)
</dt> <dt>

[<span data-ttu-id="256fb-118">**版本**</span><span class="sxs-lookup"><span data-stu-id="256fb-118">**VERSION**</span></span>](version-statement.md)
</dt> </dl>

 

 