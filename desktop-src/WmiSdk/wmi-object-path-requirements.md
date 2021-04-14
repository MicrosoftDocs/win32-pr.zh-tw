---
description: WMI 會在關聯類別的參考屬性中使用物件路徑，以識別相關的物件，以及在多個方法的輸入或輸出參數中使用物件路徑。
ms.assetid: 07fee6f8-810e-4dec-8f0f-787756ee3beb
ms.tgt_platform: multiple
title: WMI 物件路徑需求
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2b46195eae3e8351c9c611a34c28cc9d5dd58d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386179"
---
# <a name="wmi-object-path-requirements"></a><span data-ttu-id="68070-103">WMI 物件路徑需求</span><span class="sxs-lookup"><span data-stu-id="68070-103">WMI Object Path Requirements</span></span>

<span data-ttu-id="68070-104">WMI 會在關聯類別的參考屬性中使用物件路徑，以識別相關的物件，以及在多個方法的輸入或輸出參數中使用物件路徑。</span><span class="sxs-lookup"><span data-stu-id="68070-104">WMI uses object paths in the reference properties of association classes to identify related objects, as well as using object paths in input or output parameters for several methods.</span></span> <span data-ttu-id="68070-105">因為會將物件路徑視為字串來進行查閱和比較，所以當做參考屬性使用時，物件路徑的值一律是字串本身，而不是已取值的物件。</span><span class="sxs-lookup"><span data-stu-id="68070-105">Because object paths are treated as strings for the purpose of lookup and comparison, the value of an object path when used as a reference property is always the string itself and not the dereferenced object.</span></span> <span data-ttu-id="68070-106">處理物件路徑的字串比較一律不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="68070-106">String comparisons that deal with object paths are always case-insensitive.</span></span>

<span data-ttu-id="68070-107">物件路徑可以使用下列語法：</span><span class="sxs-lookup"><span data-stu-id="68070-107">An object path can use the following syntax:</span></span>

-   <span data-ttu-id="68070-108">以單引號括住的字串。</span><span class="sxs-lookup"><span data-stu-id="68070-108">Strings contained in single quotation marks.</span></span>
-   <span data-ttu-id="68070-109">斜線作為分隔符號。</span><span class="sxs-lookup"><span data-stu-id="68070-109">Forward slashes as separators.</span></span>
-   <span data-ttu-id="68070-110">以反斜線作為分隔符號。</span><span class="sxs-lookup"><span data-stu-id="68070-110">Backslashes as separators.</span></span>
-   <span data-ttu-id="68070-111">整數的十六進位常數。</span><span class="sxs-lookup"><span data-stu-id="68070-111">Hexadecimal constants for integers.</span></span>
-   <span data-ttu-id="68070-112">具有採用布林值之索引鍵的類別布林常數。</span><span class="sxs-lookup"><span data-stu-id="68070-112">Boolean constants for classes with keys that take Boolean values.</span></span>
-   <span data-ttu-id="68070-113">代表非列印字元的 URL 標記法，例如空白空間的 %20。</span><span class="sxs-lookup"><span data-stu-id="68070-113">URL notation to represent nonprinting characters, such as %20 for a blank space.</span></span>

<span data-ttu-id="68070-114">此外，物件路徑字串必須遵守下列限制：</span><span class="sxs-lookup"><span data-stu-id="68070-114">In addition, an object path string must obey the following restrictions:</span></span>

-   <span data-ttu-id="68070-115">假設的本機伺服器具有部分命名空間路徑。</span><span class="sxs-lookup"><span data-stu-id="68070-115">An assumed local server with a partial namespace path.</span></span> <span data-ttu-id="68070-116">因此，指定根和預設命名空間表示本機伺服器上的根和預設命名空間。</span><span class="sxs-lookup"><span data-stu-id="68070-116">Thus, specifying the root and default namespace implies the root and default namespace on the local server.</span></span>
-   <span data-ttu-id="68070-117">元素內或元素之間沒有空白字元。</span><span class="sxs-lookup"><span data-stu-id="68070-117">No white space either within an element or between elements.</span></span>
-   <span data-ttu-id="68070-118">允許在物件路徑中使用內嵌引號，但必須以 escape 字元分隔引號，如同在 C 或 c + + 應用程式中一樣。</span><span class="sxs-lookup"><span data-stu-id="68070-118">Embedded quotation marks in object paths are allowed but must delimit the quotation mark with escape characters, as in a C or C++ application.</span></span>
-   <span data-ttu-id="68070-119">只有十進位值會被辨識為索引鍵的數位部分。</span><span class="sxs-lookup"><span data-stu-id="68070-119">Only decimal values are recognized as numeric portions of keys.</span></span>

 

 



