---
description: Unicode 標準不規定控制項程式碼的特定意義 0x000D (換行傳回) 和 0x000A (換行字元) 。
ms.assetid: fb8b1a5c-79a4-45a0-b7a1-8217c370d13e
title: 使用 ASCII 控制代碼0x000D 和0x000A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d509c83bfd6349dcceb05ab4a8946aae51feacdc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945423"
---
# <a name="using-ascii-control-codes-0x000d-and-0x000a"></a><span data-ttu-id="a3e78-103">使用 ASCII 控制代碼0x000D 和0x000A</span><span class="sxs-lookup"><span data-stu-id="a3e78-103">Using ASCII Control Codes 0x000D and 0x000A</span></span>

<span data-ttu-id="a3e78-104">Unicode 標準不規定控制項程式碼的特定意義 0x000D (換行傳回) 和 0x000A (換行字元) 。</span><span class="sxs-lookup"><span data-stu-id="a3e78-104">The Unicode standard does not prescribe specific meanings for the control codes 0x000D (carriage return) and 0x000A (linefeed).</span></span> <span data-ttu-id="a3e78-105">這些代碼不一定要用於組合。</span><span class="sxs-lookup"><span data-stu-id="a3e78-105">These codes are not required to be used in combination.</span></span> <span data-ttu-id="a3e78-106">如果個別使用，則這兩個程式碼只能代表本身或兩個程式碼。</span><span class="sxs-lookup"><span data-stu-id="a3e78-106">If used individually, either code can represent itself only or both codes together.</span></span> <span data-ttu-id="a3e78-107">應用程式必須一律決定這些程式碼所代表的意義。</span><span class="sxs-lookup"><span data-stu-id="a3e78-107">The application must always determine what these codes represent.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a3e78-108">相關主題</span><span class="sxs-lookup"><span data-stu-id="a3e78-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3e78-109">使用 Unicode 中的特殊字元</span><span class="sxs-lookup"><span data-stu-id="a3e78-109">Using Special Characters in Unicode</span></span>](using-special-characters-in-unicode.md)
</dt> </dl>

 

 



