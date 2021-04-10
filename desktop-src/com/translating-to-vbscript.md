---
title: 翻譯為 VBScript
description: 翻譯為 VBScript
ms.assetid: 12eac4bd-06d9-45db-81c2-0591200cbacc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14b9f64e25a22ffe83c148c1fd1b7a7603b8f3f8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183304"
---
# <a name="translating-to-vbscript"></a><span data-ttu-id="d3ee1-103">翻譯為 VBScript</span><span class="sxs-lookup"><span data-stu-id="d3ee1-103">Translating to VBScript</span></span>

<span data-ttu-id="d3ee1-104">VBScript 是 Microsoft Visual Basic for Applications 語言的子集。</span><span class="sxs-lookup"><span data-stu-id="d3ee1-104">VBScript is a subset of the Microsoft Visual Basic for Applications language.</span></span> <span data-ttu-id="d3ee1-105">由於 VBScript 的目的是要在用戶端應用程式（例如網頁）中安全地使用，因此不會提供檔案輸入和輸出，也不會直接存取基礎作業系統。</span><span class="sxs-lookup"><span data-stu-id="d3ee1-105">Because VBScript is intended to be safe for use in client-side applications such as webpages, it does not provide file input and output or direct access to the underlying operating system.</span></span> <span data-ttu-id="d3ee1-106">這可防止 Web 腳本刪除或改變電腦上的檔案。</span><span class="sxs-lookup"><span data-stu-id="d3ee1-106">This prevents a Web-based script from deleting or altering files on your computer.</span></span> <span data-ttu-id="d3ee1-107">如需 VBScript 中不支援之 Visual Basic 功能的完整清單，請參閱 Visual Basic for Applications 檔。</span><span class="sxs-lookup"><span data-stu-id="d3ee1-107">For a complete list of Visual Basic features that are not supported in VBScript, see the Visual Basic for Applications documentation.</span></span>

<span data-ttu-id="d3ee1-108">除了 VBScript 所提供的語言功能之外，腳本主機也可能會公開您的腳本可以存取的 VBScript 物件模型。</span><span class="sxs-lookup"><span data-stu-id="d3ee1-108">In addition to the language features provided by VBScript, the scripting host may also expose a VBScript object model that your script can access.</span></span> <span data-ttu-id="d3ee1-109">例如，Internet Explorer 會公開物件模型，讓腳本能夠與互動並以程式設計方式控制瀏覽器。</span><span class="sxs-lookup"><span data-stu-id="d3ee1-109">For example, Internet Explorer exposes an object model that enables scripts to interact with and programmatically control the browser.</span></span> <span data-ttu-id="d3ee1-110">如需有關使用這類物件模型的詳細資訊，請參閱腳本主機上的檔。</span><span class="sxs-lookup"><span data-stu-id="d3ee1-110">For more information about working with such object models, see the documentation on your scripting host.</span></span>

<span data-ttu-id="d3ee1-111">下列主題描述當您從 JavaScript 或 JScript 將腳本轉譯為 VBScript 時，應該考慮的問題：</span><span class="sxs-lookup"><span data-stu-id="d3ee1-111">The following topics describe issues you should consider when translating a script to VBScript from JavaScript or JScript:</span></span>

-   [<span data-ttu-id="d3ee1-112">從 JScript 轉換成 VBScript</span><span class="sxs-lookup"><span data-stu-id="d3ee1-112">Translating to VBScript from JScript</span></span>](translating-to-vbscript-from-jscript.md)
-   [<span data-ttu-id="d3ee1-113">從 JavaScript 轉換成 VBScript</span><span class="sxs-lookup"><span data-stu-id="d3ee1-113">Translating to VBScript from JavaScript</span></span>](translating-to-vbscript-from-javascript.md)

## <a name="related-topics"></a><span data-ttu-id="d3ee1-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="d3ee1-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3ee1-115">翻譯為 JavaScript</span><span class="sxs-lookup"><span data-stu-id="d3ee1-115">Translating to JavaScript</span></span>](translating-to-javascript.md)
</dt> <dt>

[<span data-ttu-id="d3ee1-116">翻譯為 JScript</span><span class="sxs-lookup"><span data-stu-id="d3ee1-116">Translating to JScript</span></span>](translating-to-jscript.md)
</dt> </dl>

 

 




