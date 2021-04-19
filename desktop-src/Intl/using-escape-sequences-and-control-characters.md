---
description: 當應用程式將字串從 ASCII 或 Windows (ANSI) 字碼頁轉換為 Unicode 時，它應該會逐字元將 escape 序列轉譯成 Unicode。
ms.assetid: 4be0fd47-0903-44d3-a323-0adc6e9c0cc9
title: 使用 Escape 序列和控制字元
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4211a487a31d5a79454d7be15159f48cdc3d5beb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106999948"
---
# <a name="using-escape-sequences-and-control-characters"></a><span data-ttu-id="e95be-103">使用 Escape 序列和控制字元</span><span class="sxs-lookup"><span data-stu-id="e95be-103">Using Escape Sequences and Control Characters</span></span>

<span data-ttu-id="e95be-104">當應用程式將字串從 ASCII 或 [Windows (ANSI) 字碼頁](code-pages.md) 轉換為 unicode 時，它應該會逐字元將 escape 序列轉譯成 unicode。</span><span class="sxs-lookup"><span data-stu-id="e95be-104">When an application converts strings from ASCII or from a [Windows (ANSI) code page](code-pages.md) to Unicode, it should translate escape sequences character-by-character into Unicode.</span></span> <span data-ttu-id="e95be-105">將 ASCII 或其他8位文字檔轉換成 Unicode 時，稍後可能會將它轉換回來。</span><span class="sxs-lookup"><span data-stu-id="e95be-105">When an ASCII or other 8-bit text file is converted to Unicode, there is a chance that it will subsequently be converted back.</span></span> <span data-ttu-id="e95be-106">以逐字元為基礎將 escape 序列轉換成 Unicode，而不是將它們組合成單一 Unicode 字元，就可以執行反向轉換，而不需要辨識和剖析 escape 序列。</span><span class="sxs-lookup"><span data-stu-id="e95be-106">Converting escape sequences into Unicode on a character-by-character basis, instead of combining them as a single Unicode character, makes it possible to perform the reverse conversion without needing to recognize and parse the escape sequences as such.</span></span> <span data-ttu-id="e95be-107">例如，ESC + A 應該變成 0x001B (ESC) ，0x0041 () ，而不是0x411B。</span><span class="sxs-lookup"><span data-stu-id="e95be-107">For example, ESC+A should become 0x001B (ESC), 0x0041 (A), instead of 0x411B.</span></span>

<span data-ttu-id="e95be-108">Unicode 中的第一個 32 16 位代碼值適用于32控制字元。</span><span class="sxs-lookup"><span data-stu-id="e95be-108">The first 32 16-bit code values in Unicode are intended for the 32 control characters.</span></span> <span data-ttu-id="e95be-109">此規格支援現有的控制字元使用，以做為格式化用途。</span><span class="sxs-lookup"><span data-stu-id="e95be-109">This specification supports the existing use of control characters for formatting purposes.</span></span> <span data-ttu-id="e95be-110">Unicode 應用程式可以將這些控制字元視為處理其 ASCII 對等專案的方式，完全相同。</span><span class="sxs-lookup"><span data-stu-id="e95be-110">Unicode applications can treat these control characters in exactly the same way as they treat their ASCII equivalents.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e95be-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="e95be-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e95be-112">使用 Unicode 中的特殊字元</span><span class="sxs-lookup"><span data-stu-id="e95be-112">Using Special Characters in Unicode</span></span>](using-special-characters-in-unicode.md)
</dt> </dl>

 

 



