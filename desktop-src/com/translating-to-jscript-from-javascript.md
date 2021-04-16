---
title: 從 JavaScript 翻譯為 JScript
description: 從 JavaScript 翻譯為 JScript
ms.assetid: 86067a69-a6a1-474f-b8d8-85caf384a311
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45535807a5ef2baf59c2e068007a5a8df8bf4863
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/20/2020
ms.locfileid: "104507817"
---
# <a name="translating-to-jscript-from-javascript"></a><span data-ttu-id="bb2ee-103">從 JavaScript 翻譯為 JScript</span><span class="sxs-lookup"><span data-stu-id="bb2ee-103">Translating to JScript from JavaScript</span></span>

<span data-ttu-id="bb2ee-104">JScript 大多與 JavaScript 相容。</span><span class="sxs-lookup"><span data-stu-id="bb2ee-104">JScript is largely compatible with JavaScript.</span></span> <span data-ttu-id="bb2ee-105">不過，JScript 5.0 版包含了一些 JavaScript 目前不支援的物件，例如 ActiveXObject、列舉值、Error、Global 和 VBArray。</span><span class="sxs-lookup"><span data-stu-id="bb2ee-105">However, JScript version 5.0 includes some objects not currently supported by JavaScript, such as ActiveXObject, Enumerator, Error, Global, and VBArray.</span></span>

<span data-ttu-id="bb2ee-106">JScript 5.0 透過 **try** 支援例外狀況處理 .。。**catch** 語句。</span><span class="sxs-lookup"><span data-stu-id="bb2ee-106">JScript 5.0 supports exception handling through **try**...**catch** statements.</span></span> <span data-ttu-id="bb2ee-107">JavaScript 目前未提供錯誤處理機制。</span><span class="sxs-lookup"><span data-stu-id="bb2ee-107">JavaScript does not currently provide an error-handing mechanism.</span></span>

<span data-ttu-id="bb2ee-108">使用 JScript 或 JavaScript 時，各種網頁瀏覽器支援的物件模型執行之間有一些細微的差異。</span><span class="sxs-lookup"><span data-stu-id="bb2ee-108">When working with either JScript or JavaScript, there are some subtle differences between the object model implementations supported by various Web browsers.</span></span> <span data-ttu-id="bb2ee-109">若要撰寫在 Internet Explorer 和 Netscape Navigator 上執行的腳本，請將腳本所使用的功能限制為全球資訊網協會 (W3C) standard for HTML 3.2 版中指定的功能。</span><span class="sxs-lookup"><span data-stu-id="bb2ee-109">To write script that runs on both Internet Explorer and Netscape Navigator, limit the features used by your scripts to those specified in the World Wide Web Consortium (W3C) standard for HTML version 3.2.</span></span> <span data-ttu-id="bb2ee-110">如需此標準的詳細資訊，請參閱 [HTML 3.2 參考規格](https://www.w3.org/TR/REC-html32.html)。</span><span class="sxs-lookup"><span data-stu-id="bb2ee-110">For more information about this standard, see [HTML 3.2 Reference Specification](https://www.w3.org/TR/REC-html32.html).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bb2ee-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="bb2ee-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bb2ee-112">翻譯為 JScript</span><span class="sxs-lookup"><span data-stu-id="bb2ee-112">Translating to JScript</span></span>](translating-to-jscript.md)
</dt> </dl>

 

 




