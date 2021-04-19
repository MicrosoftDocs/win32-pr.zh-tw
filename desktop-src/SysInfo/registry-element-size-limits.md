---
description: 下表將識別各種登錄元素的大小限制。
ms.assetid: a6d3a884-f181-46a5-b655-226c68792e08
title: 登錄元素大小限制
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 262609a64e60536dcfc41f29e5d94ea499158861
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106974717"
---
# <a name="registry-element-size-limits"></a><span data-ttu-id="61cc4-103">登錄元素大小限制</span><span class="sxs-lookup"><span data-stu-id="61cc4-103">Registry Element Size Limits</span></span>

<span data-ttu-id="61cc4-104">下表將識別各種登錄元素的大小限制。</span><span class="sxs-lookup"><span data-stu-id="61cc4-104">The following table identifies the size limits for the various registry elements.</span></span>



| <span data-ttu-id="61cc4-105">Registry 元素</span><span class="sxs-lookup"><span data-stu-id="61cc4-105">Registry Element</span></span> | <span data-ttu-id="61cc4-106">大小限制</span><span class="sxs-lookup"><span data-stu-id="61cc4-106">Size Limit</span></span>                                                                                                                                            |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61cc4-107">索引鍵名稱</span><span class="sxs-lookup"><span data-stu-id="61cc4-107">Key name</span></span>         | <span data-ttu-id="61cc4-108">255個字元。</span><span class="sxs-lookup"><span data-stu-id="61cc4-108">255 characters.</span></span> <span data-ttu-id="61cc4-109">索引鍵名稱包含登錄中金鑰的絕對路徑，一律是從基本金鑰開始，例如 HKEY \_ 本機 \_ 電腦。</span><span class="sxs-lookup"><span data-stu-id="61cc4-109">The key name includes the absolute path of the key in the registry, always starting at a base key, for example, HKEY\_LOCAL\_MACHINE.</span></span> |
| <span data-ttu-id="61cc4-110">值名稱</span><span class="sxs-lookup"><span data-stu-id="61cc4-110">Value name</span></span>       | <span data-ttu-id="61cc4-111">16383字元 **Windows 2000：** 260 ANSI 字元或 16383 Unicode 字元。</span><span class="sxs-lookup"><span data-stu-id="61cc4-111">16,383 characters **Windows 2000:** 260 ANSI characters or 16,383 Unicode characters.</span></span><br/>                                                       |
| <span data-ttu-id="61cc4-112">值</span><span class="sxs-lookup"><span data-stu-id="61cc4-112">Value</span></span>            | <span data-ttu-id="61cc4-113"> (最新格式的可用記憶體) 1 MB (標準格式) </span><span class="sxs-lookup"><span data-stu-id="61cc4-113">Available memory (latest format)1 MB (standard format)</span></span><br/>                                                                                     |
| <span data-ttu-id="61cc4-114">樹狀結構</span><span class="sxs-lookup"><span data-stu-id="61cc4-114">Tree</span></span>             | <span data-ttu-id="61cc4-115">登錄樹狀目錄可以是深512層級。</span><span class="sxs-lookup"><span data-stu-id="61cc4-115">A registry tree can be 512 levels deep.</span></span> <span data-ttu-id="61cc4-116">您可以透過單一登入 API 呼叫，一次最多建立32個層級。</span><span class="sxs-lookup"><span data-stu-id="61cc4-116">You can create up to 32 levels at a time through a single registry API call.</span></span>                                  |



 

<span data-ttu-id="61cc4-117">Long 值 (超過2048個位元組) 應儲存在檔案中，而檔案的位置應儲存在登錄中。</span><span class="sxs-lookup"><span data-stu-id="61cc4-117">Long values (more than 2,048 bytes) should be stored in a file, and the location of the file should be stored in the registry.</span></span> <span data-ttu-id="61cc4-118">這有助於登錄有效率地執行。</span><span class="sxs-lookup"><span data-stu-id="61cc4-118">This helps the registry perform efficiently.</span></span>

<span data-ttu-id="61cc4-119">檔案位置可以是值的名稱或值的資料。</span><span class="sxs-lookup"><span data-stu-id="61cc4-119">The file location can be the name of a value or the data of a value.</span></span> <span data-ttu-id="61cc4-120">位置字串中的每個反斜線前面都必須有另一個反斜線作為 escape 字元。</span><span class="sxs-lookup"><span data-stu-id="61cc4-120">Each backslash in the location string must be preceded by another backslash as an escape character.</span></span> <span data-ttu-id="61cc4-121">例如，指定 "C： \\ \\ mydir \\ \\ myfile.txt" 來儲存字串 "c： \\ mydir \\ myfile.txt"。</span><span class="sxs-lookup"><span data-stu-id="61cc4-121">For example, specify "C:\\\\mydir\\\\myfile" to store the string "C:\\mydir\\myfile".</span></span> <span data-ttu-id="61cc4-122">如果檔案位置是索引鍵名稱255個字元的限制內，而且沒有包含反斜線（不允許用在索引鍵名稱中），則該檔案的名稱也可以是索引鍵的名稱。</span><span class="sxs-lookup"><span data-stu-id="61cc4-122">A file location can also be the name of a key if it is within the 255-character limit for key names and does not contain backslashes, which are not allowed in key names.</span></span>

 

 




