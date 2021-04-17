---
description: 您的應用程式應該使用換行字元 (0x2028) 和段落分隔符號 (0x2029) 來分隔純文字。 在每個行分隔字元後方會開始新行。 在每個段落分隔字元後方會開始新段落。
ms.assetid: 086aca6c-8d1f-4e54-9e1c-642be50b303c
title: 使用線條和段落分隔符號
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2c9511ba2a8889b3c9139daf1d088d91ed746db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195434"
---
# <a name="using-line-and-paragraph-separators"></a><span data-ttu-id="a46c6-105">使用線條和段落分隔符號</span><span class="sxs-lookup"><span data-stu-id="a46c6-105">Using Line and Paragraph Separators</span></span>

<span data-ttu-id="a46c6-106">您的應用程式應該使用換行字元 (0x2028) 和段落分隔符號 (0x2029) 來分隔純文字。</span><span class="sxs-lookup"><span data-stu-id="a46c6-106">Your applications should use the line separator character (0x2028) and the paragraph separator character (0x2029) to divide plain text.</span></span> <span data-ttu-id="a46c6-107">在每個行分隔字元後方會開始新行。</span><span class="sxs-lookup"><span data-stu-id="a46c6-107">A new line is begun after each line separator.</span></span> <span data-ttu-id="a46c6-108">在每個段落分隔字元後方會開始新段落。</span><span class="sxs-lookup"><span data-stu-id="a46c6-108">A new paragraph is begun after each paragraph separator.</span></span>

<span data-ttu-id="a46c6-109">您不需要以這些字元來啟動檔案中的第一行或段落，也不需要用它們來結束最後一行或段落。</span><span class="sxs-lookup"><span data-stu-id="a46c6-109">It is not necessary to start the first line or paragraph in a file with these characters, or to end the last line or paragraph with them.</span></span> <span data-ttu-id="a46c6-110">這麼做會指出該位置中有空白行或段落。</span><span class="sxs-lookup"><span data-stu-id="a46c6-110">Doing so indicates that there is an empty line or paragraph in that location.</span></span>

<span data-ttu-id="a46c6-111">應用程式可以使用行分隔符號來表示無條件的行尾。</span><span class="sxs-lookup"><span data-stu-id="a46c6-111">The application can use the line separator to indicate an unconditional end of line.</span></span> <span data-ttu-id="a46c6-112">不過，行分隔字元不會對應至個別的歸位字元與換行字元，或是對應至這些字元的組合。</span><span class="sxs-lookup"><span data-stu-id="a46c6-112">However, line separators do not correspond to the separate carriage return and linefeed characters, or to a combination of these characters.</span></span> <span data-ttu-id="a46c6-113">行分隔字元必須與歸位字元和換行字元分開個別處理。</span><span class="sxs-lookup"><span data-stu-id="a46c6-113">Line separators must be processed separately from carriage return and linefeed characters.</span></span>

<span data-ttu-id="a46c6-114">應用程式可以在文欄位落之間插入段落分隔符號。</span><span class="sxs-lookup"><span data-stu-id="a46c6-114">The application can insert a paragraph separator between paragraphs of text.</span></span> <span data-ttu-id="a46c6-115">使用此分隔字元可讓您建立純文字檔案，以在不同作業系統上使用各種不同的行寬度進行格式化。</span><span class="sxs-lookup"><span data-stu-id="a46c6-115">Use of this separator allows creation of plain text files that can be formatted with different line widths on different operating systems.</span></span> <span data-ttu-id="a46c6-116">目標系統可以忽略任何行分隔符號，而只在段落分格符號所在位置分段。</span><span class="sxs-lookup"><span data-stu-id="a46c6-116">The target system can ignore any line separators and break paragraphs only at the paragraph separators.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a46c6-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="a46c6-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a46c6-118">使用 Unicode 中的特殊字元</span><span class="sxs-lookup"><span data-stu-id="a46c6-118">Using Special Characters in Unicode</span></span>](using-special-characters-in-unicode.md)
</dt> </dl>

 

 



