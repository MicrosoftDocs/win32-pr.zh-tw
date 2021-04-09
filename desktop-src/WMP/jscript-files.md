---
title: JScript 檔案
description: JScript 檔案
ms.assetid: 5b862e52-5d49-44b4-811c-3dbca5552167
keywords:
- Windows Media Player 的外觀、JScript 檔案
- 外觀、JScript 檔案
- 外觀、JScript 的檔案
- 適用于面板的 JScript 檔案，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9123ade6b715ee5302925030545140329c06770c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840591"
---
# <a name="jscript-files"></a><span data-ttu-id="2a5c0-107">JScript 檔案</span><span class="sxs-lookup"><span data-stu-id="2a5c0-107">JScript Files</span></span>

<span data-ttu-id="2a5c0-108">JScript 檔案是使用 **VIEW** 專案的 **scriptFile** 屬性載入的。</span><span class="sxs-lookup"><span data-stu-id="2a5c0-108">JScript files are loaded with the **scriptFile** attribute of the **VIEW** element.</span></span> <span data-ttu-id="2a5c0-109">它們必須是文字檔，而且應該使用副檔名 .js。</span><span class="sxs-lookup"><span data-stu-id="2a5c0-109">They must be text files and should use the file name extension .js.</span></span> <span data-ttu-id="2a5c0-110">如果您的 JScript 檔案與面板定義檔的名稱相同，則會同時載入該 JScript 檔案與面板定義檔。</span><span class="sxs-lookup"><span data-stu-id="2a5c0-110">If you have a JScript file that has the same name as the skin definition file, the JScript file will be loaded at the same time as the skin definition file.</span></span> <span data-ttu-id="2a5c0-111">例如，如果您有一個名為 laure 的面板定義檔，而且您有一個稱為 laure.js 的 JScript 檔案，就會自動載入 laure.js 檔。</span><span class="sxs-lookup"><span data-stu-id="2a5c0-111">For example, if you have a skin definition file named laure.wms, and you have a JScript file called laure.js, the laure.js file will be loaded automatically.</span></span>

<span data-ttu-id="2a5c0-112">您可以使用 JScript，在您的面板背後建立詳盡的功能。</span><span class="sxs-lookup"><span data-stu-id="2a5c0-112">You can use JScript to create elaborate functionality behind your skin.</span></span> <span data-ttu-id="2a5c0-113">藉由在 JScript 中建立函式，您幾乎可以使用面板來想像得到任何功能。</span><span class="sxs-lookup"><span data-stu-id="2a5c0-113">By creating functions in JScript, you can do almost anything imaginable with skins.</span></span> <span data-ttu-id="2a5c0-114">例如，您可以在一周的每一天使用不同的播放清單，但在星期五一律有相同的播放清單。</span><span class="sxs-lookup"><span data-stu-id="2a5c0-114">For example, you could use a different playlist for every day of the week, but always have the same one on Friday.</span></span>

<span data-ttu-id="2a5c0-115">如需搭配使用 JScript 與外觀的詳細資訊，請參閱 [使用 jscript](using-jscript.md) 。</span><span class="sxs-lookup"><span data-stu-id="2a5c0-115">See [Using JScript](using-jscript.md) for more information about using JScript with skins.</span></span> <span data-ttu-id="2a5c0-116">請注意，當您在網頁中內嵌 Windows Media Player 控制項時，不支援使用面板來 Visual Basic Scripting Edition (VBScript) 。</span><span class="sxs-lookup"><span data-stu-id="2a5c0-116">Note that Visual Basic Scripting Edition (VBScript), which can be used when embedding the Windows Media Player control in a webpage, is not supported for use with skins.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2a5c0-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="2a5c0-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a5c0-118">**面板檔案**</span><span class="sxs-lookup"><span data-stu-id="2a5c0-118">**Skin Files**</span></span>](skin-files.md)
</dt> </dl>

 

 




