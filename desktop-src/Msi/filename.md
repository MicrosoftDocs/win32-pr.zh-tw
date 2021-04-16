---
description: Filename 資料類型是包含檔案名或資料夾的文字字串。
ms.assetid: af59e1b8-0699-4031-895f-415752611e21
title: 檔案名稱
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fc049fa0808efc180afbd715e311a124bfdada9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512788"
---
# <a name="filename"></a><span data-ttu-id="dc858-103">檔案名稱</span><span class="sxs-lookup"><span data-stu-id="dc858-103">Filename</span></span>

<span data-ttu-id="dc858-104">Filename 資料類型是包含檔案名或資料夾的文字字串。</span><span class="sxs-lookup"><span data-stu-id="dc858-104">The Filename data type is a text string containing a file name or folder.</span></span> <span data-ttu-id="dc858-105">根據預設，檔案名會假設使用簡短的檔案名語法;也就是八個字元的名稱、句號 ( ) 和3個字元的副檔名。</span><span class="sxs-lookup"><span data-stu-id="dc858-105">By default, the file name is assumed to use short file name syntax; that is, eight-character name, period (.), and 3-character extension.</span></span> <span data-ttu-id="dc858-106">因為可以設定 [**SHORTFILENAMES**](shortfilenames.md) 屬性，或安裝的目標磁片區可能只支援簡短的檔案名，所以一定要提供簡短的檔案名。</span><span class="sxs-lookup"><span data-stu-id="dc858-106">A short file name must always be provided because the [**SHORTFILENAMES**](shortfilenames.md) property may be set or the target volume for the installation may only support short file names.</span></span>

<span data-ttu-id="dc858-107">若要包含簡短檔案名的長檔名，請使用分隔號將它與短的檔案名分開， (\|) 。</span><span class="sxs-lookup"><span data-stu-id="dc858-107">To include a long file name with the short file name, separate it from the short file name with a vertical bar (\|).</span></span>

<span data-ttu-id="dc858-108">例如，下列兩個字串是有效的：</span><span class="sxs-lookup"><span data-stu-id="dc858-108">For example, the following two strings are valid:</span></span>

-   <span data-ttu-id="dc858-109">status.txt</span><span class="sxs-lookup"><span data-stu-id="dc858-109">status.txt</span></span>
-   <span data-ttu-id="dc858-110">project ~1.txt\| 專案 Status.txt</span><span class="sxs-lookup"><span data-stu-id="dc858-110">projec~1.txt\|Project Status.txt</span></span>

<span data-ttu-id="dc858-111">簡短和完整檔案名不得包含下列字元：</span><span class="sxs-lookup"><span data-stu-id="dc858-111">Short and long file names must not contain the following characters:</span></span>

-   <span data-ttu-id="dc858-112">斜線 (/) 或 (\\) </span><span class="sxs-lookup"><span data-stu-id="dc858-112">slash (/) or (\\)</span></span>
-   <span data-ttu-id="dc858-113">問號 (？ ) </span><span class="sxs-lookup"><span data-stu-id="dc858-113">question mark (?)</span></span>
-   <span data-ttu-id="dc858-114">垂直橫條 (\|) </span><span class="sxs-lookup"><span data-stu-id="dc858-114">vertical bar (\|)</span></span>
-   <span data-ttu-id="dc858-115">右角括弧 (>) </span><span class="sxs-lookup"><span data-stu-id="dc858-115">right angle bracket (>)</span></span>
-   <span data-ttu-id="dc858-116">左角括弧 (<) </span><span class="sxs-lookup"><span data-stu-id="dc858-116">left angle bracket (<)</span></span>
-   <span data-ttu-id="dc858-117">冒號 (:)</span><span class="sxs-lookup"><span data-stu-id="dc858-117">colon (:)</span></span>
-   <span data-ttu-id="dc858-118">星號 (\*) </span><span class="sxs-lookup"><span data-stu-id="dc858-118">asterisk (\*)</span></span>
-   <span data-ttu-id="dc858-119">引號 (")</span><span class="sxs-lookup"><span data-stu-id="dc858-119">quotation mark (")</span></span>

<span data-ttu-id="dc858-120">此外，簡短的檔案名不能包含下列字元：</span><span class="sxs-lookup"><span data-stu-id="dc858-120">In addition, short file names must not contain the following characters:</span></span>

-   <span data-ttu-id="dc858-121">加號 (+)</span><span class="sxs-lookup"><span data-stu-id="dc858-121">plus sign (+)</span></span>
-   <span data-ttu-id="dc858-122">逗號 (,)</span><span class="sxs-lookup"><span data-stu-id="dc858-122">comma (,)</span></span>
-   <span data-ttu-id="dc858-123">分號 (;)</span><span class="sxs-lookup"><span data-stu-id="dc858-123">semicolon (;)</span></span>
-   <span data-ttu-id="dc858-124">等號 (=) </span><span class="sxs-lookup"><span data-stu-id="dc858-124">equals sign (=)</span></span>
-   <span data-ttu-id="dc858-125">左方括弧 (\[) </span><span class="sxs-lookup"><span data-stu-id="dc858-125">left square bracket (\[)</span></span>
-   <span data-ttu-id="dc858-126">右方括弧 (\]) </span><span class="sxs-lookup"><span data-stu-id="dc858-126">right square bracket (\])</span></span>

<span data-ttu-id="dc858-127">在分隔號之前不允許有空格 (\| 短檔案名/完整檔案名語法的) 分隔符號。</span><span class="sxs-lookup"><span data-stu-id="dc858-127">No space is allowed preceding the vertical bar (\|) separator for the short file name/long file name syntax.</span></span> <span data-ttu-id="dc858-128">簡短檔案名不能包含空格，雖然可能會有很長的檔案名。</span><span class="sxs-lookup"><span data-stu-id="dc858-128">Short file names may not include a space, although a long file name may.</span></span> <span data-ttu-id="dc858-129">只有當檔案名的完整檔案名開頭為空格時，才可以在分隔符號之後存在空間。</span><span class="sxs-lookup"><span data-stu-id="dc858-129">A space can exist after the separator only if the long file name of the file name begins with the space.</span></span> <span data-ttu-id="dc858-130">不允許使用完整路徑語法。</span><span class="sxs-lookup"><span data-stu-id="dc858-130">No full-path syntax is allowed.</span></span>

> [!Note]  
> <span data-ttu-id="dc858-131">[MsiEmbeddedUI](msiembeddedui-table.md)資料表的 FileName 資料行格式類似于 filename 資料類型，不同之處在于 \| 不提供簡短的檔案名/完整檔案名語法的垂直列 () 分隔符號。</span><span class="sxs-lookup"><span data-stu-id="dc858-131">The format of the FileName column of the [MsiEmbeddedUI](msiembeddedui-table.md) table is like the format Filename data type except that the vertical bar (\|) separator for the short file name/long file name syntax is not available.</span></span>

 

 

 



