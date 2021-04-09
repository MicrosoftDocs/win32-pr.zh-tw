---
title: 關於資源檔
description: 描述如何在 Windows 應用程式中包含 RC 的資源。
ms.assetid: af7c7aed-5d28-40ac-ad00-da0986fd89c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c43e9df59cf0b6507b6c6a53c42299b8792634f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021453"
---
# <a name="about-resource-files"></a><span data-ttu-id="e9b9a-103">關於資源檔</span><span class="sxs-lookup"><span data-stu-id="e9b9a-103">About Resource Files</span></span>

<span data-ttu-id="e9b9a-104">若要在您的 Windows 應用程式中包含 RC 的資源，請執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="e9b9a-104">To include resources in your Windows-based application with RC, do the following:</span></span>

1.  <span data-ttu-id="e9b9a-105">為您的游標、圖示、點陣圖、對話方塊和字型建立個別檔案。</span><span class="sxs-lookup"><span data-stu-id="e9b9a-105">Create individual files for your cursors, icons, bitmaps, dialog boxes, and fonts.</span></span>
2.  <span data-ttu-id="e9b9a-106">建立資源定義腳本 ( .rc 檔) ，以描述您的應用程式所使用的資源。</span><span class="sxs-lookup"><span data-stu-id="e9b9a-106">Create a resource-definition script (.rc file) that describes the resources used by your application.</span></span>
3.  <span data-ttu-id="e9b9a-107">使用 RC 編譯腳本。</span><span class="sxs-lookup"><span data-stu-id="e9b9a-107">Compile the script with RC.</span></span> <span data-ttu-id="e9b9a-108">如需詳細資訊，請參閱 [使用 rc (Rc 命令列) ](using-rc-the-rc-command-line-.md)。</span><span class="sxs-lookup"><span data-stu-id="e9b9a-108">For more information, see [Using RC (The RC Command Line)](using-rc-the-rc-command-line-.md).</span></span>
4.  <span data-ttu-id="e9b9a-109">將已編譯的資源 ( .res) 檔連結至應用程式的可執行檔。</span><span class="sxs-lookup"><span data-stu-id="e9b9a-109">Link the compiled resource (.res) file into the application's executable file with your linker.</span></span>

<span data-ttu-id="e9b9a-110">資源檔是副檔名為 .rc 的文字檔。</span><span class="sxs-lookup"><span data-stu-id="e9b9a-110">A resource file is a text file with the extension .rc.</span></span> <span data-ttu-id="e9b9a-111">檔案可以使用單一位元組、雙位元組或 Unicode 字元。</span><span class="sxs-lookup"><span data-stu-id="e9b9a-111">The file can use single-byte, double-byte, or Unicode characters.</span></span> <span data-ttu-id="e9b9a-112">RC 預處理器的語法和語義類似于 Microsoft C/c + + 編譯器。</span><span class="sxs-lookup"><span data-stu-id="e9b9a-112">The syntax and semantics for the RC preprocessor are similar to those of the Microsoft C/C++ compiler.</span></span> <span data-ttu-id="e9b9a-113">不過，RC 支援在腳本中使用預處理器指示詞、定義和 pragma 的子集。</span><span class="sxs-lookup"><span data-stu-id="e9b9a-113">However, RC supports a subset of the preprocessor directives, defines, and pragmas in a script.</span></span>

<span data-ttu-id="e9b9a-114">腳本檔案會定義資源。</span><span class="sxs-lookup"><span data-stu-id="e9b9a-114">The script file defines resources.</span></span> <span data-ttu-id="e9b9a-115">針對存在於個別檔案中的資源（例如圖示或游標），腳本會指定資源和包含它的檔案。</span><span class="sxs-lookup"><span data-stu-id="e9b9a-115">For a resource that exists in a separate file, such as an icon or cursor, the script specifies the resource and the file that contains it.</span></span> <span data-ttu-id="e9b9a-116">對於某些資源（例如功能表），該資源的整個定義都會存在於腳本中。</span><span class="sxs-lookup"><span data-stu-id="e9b9a-116">For some resources, such as a menu, the entire definition of the resource exists within the script.</span></span>

<span data-ttu-id="e9b9a-117">下列主題描述腳本檔案可以包含的資訊：</span><span class="sxs-lookup"><span data-stu-id="e9b9a-117">The following topics describe the information a script file can contain:</span></span>

-   <span data-ttu-id="e9b9a-118">[批註](comments.md)，也就是 RC 要忽略的附注。</span><span class="sxs-lookup"><span data-stu-id="e9b9a-118">[Comments](comments.md), which are notes to be ignored by RC.</span></span>
-   <span data-ttu-id="e9b9a-119">[預先定義的宏](predefined-macros.md)，不採用任何引數，也無法重新定義。</span><span class="sxs-lookup"><span data-stu-id="e9b9a-119">[Predefined macros](predefined-macros.md), which take no arguments and cannot be redefined.</span></span>
-   <span data-ttu-id="e9b9a-120">[預處理器](preprocessor-directives.md)指示詞，指示 RC 先對腳本執行動作，再進行編譯。</span><span class="sxs-lookup"><span data-stu-id="e9b9a-120">[Preprocessor directives](preprocessor-directives.md), which instruct RC to perform actions on the script before compiling it.</span></span>
-   <span data-ttu-id="e9b9a-121">[預處理器運算子](preprocessor-operators.md)，用於 **\# 定義** 指示詞。</span><span class="sxs-lookup"><span data-stu-id="e9b9a-121">[Preprocessor operators](preprocessor-operators.md), which are used with the **\#define** directive.</span></span>
-   [<span data-ttu-id="e9b9a-122">Pragma 指示詞</span><span class="sxs-lookup"><span data-stu-id="e9b9a-122">Pragma directives</span></span>](pragma-directives.md)
-   <span data-ttu-id="e9b9a-123">[資源定義語句](resource-definition-statements.md)，其名稱和描述資源。</span><span class="sxs-lookup"><span data-stu-id="e9b9a-123">[Resource-definition statements](resource-definition-statements.md), which name and describe resources.</span></span>

 

 




