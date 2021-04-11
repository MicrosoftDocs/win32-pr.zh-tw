---
title: Wide-Character 類型
description: Microsoft RPC 支援寬字元類型 wchar \_ t。
ms.assetid: 1a601461-df34-456d-93e8-4cf0b655cf2c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 821d69999a0ec7e175409120f223721defd6cd10
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092988"
---
# <a name="wide-character-types"></a><span data-ttu-id="587f6-103">Wide-Character 類型</span><span class="sxs-lookup"><span data-stu-id="587f6-103">Wide-Character Types</span></span>

<span data-ttu-id="587f6-104">Microsoft RPC 支援寬字元類型 [**wchar \_ t**](/windows/desktop/Midl/wchar-t)。</span><span class="sxs-lookup"><span data-stu-id="587f6-104">Microsoft RPC supports the wide-character type [**wchar\_t**](/windows/desktop/Midl/wchar-t).</span></span> <span data-ttu-id="587f6-105">寬字元類型會針對每個字元使用2個位元組。</span><span class="sxs-lookup"><span data-stu-id="587f6-105">The wide-character type uses 2 bytes for each character.</span></span> <span data-ttu-id="587f6-106">ANSI C 語言定義可讓您將長字元和長字串初始化為：</span><span class="sxs-lookup"><span data-stu-id="587f6-106">The ANSI C-language definition allows you to initialize long characters and long strings as:</span></span>

``` syntax
wchar_t wcInitial = L'a';
wchar_t * pwszString = L"Hello, world";
```

 

 