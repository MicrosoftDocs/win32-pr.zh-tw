---
title: 從 JScript 轉換成 JavaScript
description: 從 JScript 轉換成 JavaScript
ms.assetid: 11d31c8c-868d-4220-9298-6d24a209dc47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71b18972f407cf008626245798b3f7740d98058e
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/20/2020
ms.locfileid: "104374650"
---
# <a name="translating-to-javascript-from-jscript"></a><span data-ttu-id="23423-103">從 JScript 轉換成 JavaScript</span><span class="sxs-lookup"><span data-stu-id="23423-103">Translating to JavaScript from JScript</span></span>

<span data-ttu-id="23423-104">JScript 大多與 JavaScript 相容。</span><span class="sxs-lookup"><span data-stu-id="23423-104">JScript is largely compatible with JavaScript.</span></span> <span data-ttu-id="23423-105">但是，JScript 包含一些 JavaScript 目前不支援的物件，例如 ActiveXObject、列舉值、Error、Global 和 VBArray。</span><span class="sxs-lookup"><span data-stu-id="23423-105">However, JScript includes some objects not currently supported by JavaScript, such as ActiveXObject, Enumerator, Error, Global, and VBArray.</span></span>

<span data-ttu-id="23423-106">JScript version 5.0 透過 **try** 支援例外狀況處理 .。。**catch** 語句。</span><span class="sxs-lookup"><span data-stu-id="23423-106">JScript version 5.0 supports exception handling through **try**...**catch** statements.</span></span> <span data-ttu-id="23423-107">JavaScript 目前未提供錯誤處理機制。</span><span class="sxs-lookup"><span data-stu-id="23423-107">JavaScript does not currently provide an error-handing mechanism.</span></span>

<span data-ttu-id="23423-108">使用 JScript 或 JavaScript 時，各種網頁瀏覽器支援的物件模型執行之間有一些細微的差異。</span><span class="sxs-lookup"><span data-stu-id="23423-108">When working with either JScript or JavaScript, there are some subtle differences between the object model implementations supported by various Web browsers.</span></span> <span data-ttu-id="23423-109">若要撰寫在 Internet Explorer 和 Netscape Navigator 上執行的腳本，請將腳本所使用的功能限制為全球資訊網協會 (W3C) [standard FOR HTML 3.2 版](https://www.w3.org/tr/rec-html32.html)中指定的功能。</span><span class="sxs-lookup"><span data-stu-id="23423-109">To write script that runs on both Internet Explorer and Netscape Navigator, limit the features used by your scripts to those specified in the World Wide Web Consortium (W3C) [standard for HTML version 3.2](https://www.w3.org/tr/rec-html32.html).</span></span>

## <a name="related-topics"></a><span data-ttu-id="23423-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="23423-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23423-111">翻譯為 JavaScript</span><span class="sxs-lookup"><span data-stu-id="23423-111">Translating to JavaScript</span></span>](translating-to-javascript.md)
</dt> </dl>

 

 




