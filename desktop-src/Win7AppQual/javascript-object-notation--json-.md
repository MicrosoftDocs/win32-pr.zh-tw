---
description: .
ms.assetid: 2F6FDE88-C852-46BC-B6B1-630C266AF0AA
title: JavaScript 物件標記法 (JSON)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18b995edc8e83405791a1d96598b827fc77f0204
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193270"
---
# <a name="javascript-object-notation-json"></a><span data-ttu-id="13386-103">JavaScript 物件標記法 (JSON)</span><span class="sxs-lookup"><span data-stu-id="13386-103">JavaScript Object Notation (JSON)</span></span>

<span data-ttu-id="13386-104">[JavaScript 物件標記法 (JSON) ](https://www.json.org/) 是簡單且輕量的資料交換格式，此格式是以 JavaScript 語言的物件常值標記法子集為基礎。</span><span class="sxs-lookup"><span data-stu-id="13386-104">[JavaScript Object Notation (JSON)](https://www.json.org/) is a simple and lightweight data-interchange format that is based on a subset of the object literal notation of the JavaScript language.</span></span> <span data-ttu-id="13386-105">Windows Internet Explorer 8 中的 JavaScript 引擎會為原生 JSON (處理函式（使用[Douglas Crockford 的 json2.js API](https://github.com/douglascrockford/JSON-js/blob/master/json2.js)) ）實行[ECMAScript 3.1 JSON 提案](https://www.ecma-international.org/)。</span><span class="sxs-lookup"><span data-stu-id="13386-105">The JavaScript engine in Windows Internet Explorer 8 implements the [ECMAScript 3.1 JSON proposal](https://www.ecma-international.org/) for native JSON-handling functions (which uses [Douglas Crockford's json2.js API](https://github.com/douglascrockford/JSON-js/blob/master/json2.js)).</span></span>

<span data-ttu-id="13386-106">Internet Explorer 8 包含原生 JSON 物件，此物件符合「 [es 3.1 提案工作草稿](https://www.ecma-international.org/)」中所述的 JSON 支援。</span><span class="sxs-lookup"><span data-stu-id="13386-106">Internet Explorer 8 includes a native JSON object that complies with the JSON support that is described in the [ES3.1 Proposal Working Draft](https://www.ecma-international.org/).</span></span> <span data-ttu-id="13386-107">某些網頁會偵測到原生 JSON 物件，然後以非標準方式使用它。</span><span class="sxs-lookup"><span data-stu-id="13386-107">Some webpages detect the native JSON object, and then use it in a non-standard way.</span></span> <span data-ttu-id="13386-108">此使用通常會導致腳本錯誤，並中斷 AJAX 要求的處理。</span><span class="sxs-lookup"><span data-stu-id="13386-108">This usage typically causes a script error and breaks the handling of AJAX requests.</span></span> <span data-ttu-id="13386-109">下列程式碼範例顯示使用 JSON 物件的錯誤方式。</span><span class="sxs-lookup"><span data-stu-id="13386-109">The following code example shows the wrong way to use the JSON object.</span></span>


```JScript
    if(!window.JSON) JSON = myJSON; 
    JSON.encode(obj); // Not part of the standard
```



<span data-ttu-id="13386-110">相反地，下列程式碼範例會顯示使用 JSON 物件的好方法。</span><span class="sxs-lookup"><span data-stu-id="13386-110">Instead, the following code example shows a good way to use the JSON object.</span></span>


```JScript
    JSON = myJSON; 
    JSON.encode(obj);
```



<span data-ttu-id="13386-111">Windows Internet Explorer 包含原生的 JSON 支援，方法是引進具有兩個內建方法的全域 JSON 物件： **json.stringify** 和 **parse**。</span><span class="sxs-lookup"><span data-stu-id="13386-111">Windows Internet Explorer includes native supports for JSON by introducing a global JSON object that has two built-in methods: **stringify** and **parse**.</span></span> <span data-ttu-id="13386-112">全域 JSON 物件是在 JavaScript 引擎中定義，並且會在引擎初始化階段期間建立。</span><span class="sxs-lookup"><span data-stu-id="13386-112">The global JSON object is defined in the JavaScript engine and is created during the engine initialization phase.</span></span> <span data-ttu-id="13386-113">為了維持回溯相容性，只有當網站使用最新版的 JavaScript 功能時，才能使用「Internet Explorer 8 標準」配置 (檔) 模式。</span><span class="sxs-lookup"><span data-stu-id="13386-113">To maintain backward compatibility, this feature is available only when a website uses the latest version of JavaScript features by using the "Internet Explorer 8 Standards" layout (document) mode.</span></span> <span data-ttu-id="13386-114">這項功能也可能會影響依賴全域變數 JSON 或使用 [json2.js](https://github.com/douglascrockford/JSON-js/blob/master/json2.js)之網頁的行為。</span><span class="sxs-lookup"><span data-stu-id="13386-114">This feature also might affect the behavior of webpages that depend on a global variable JSON or use [json2.js](https://github.com/douglascrockford/JSON-js/blob/master/json2.js).</span></span>

<span data-ttu-id="13386-115">您可以覆寫全域 JSON 物件。</span><span class="sxs-lookup"><span data-stu-id="13386-115">You can override the global JSON object.</span></span> <span data-ttu-id="13386-116">但是，當網頁使用「Internet Explorer 8 標準」配置 (檔) 模式時，它再也不是未定義的物件。</span><span class="sxs-lookup"><span data-stu-id="13386-116">But when a webpage uses the “Internet Explorer 8 Standards” layout (document) mode, it is not an undefined object anymore.</span></span> <span data-ttu-id="13386-117">因為 JavaScript 引擎會將 JSON 具現化為全域名稱，所以會檢查「如果 (！ this.JSON) 」是否評估為 False，而且必須在使用者程式碼中變更。</span><span class="sxs-lookup"><span data-stu-id="13386-117">Because JSON is instantiated as a global name by the JavaScript engine, checks like "if(!this.JSON)" evaluate to False and must be changed in the user code.</span></span>

<span data-ttu-id="13386-118">使用 [json2.js](https://github.com/douglascrockford/JSON-js/blob/master/json2.js) 的網頁可能不會受到影響。</span><span class="sxs-lookup"><span data-stu-id="13386-118">Webpages that use [json2.js](https://github.com/douglascrockford/JSON-js/blob/master/json2.js) are likely not affected.</span></span> <span data-ttu-id="13386-119">有幾個例外狀況，這些頁面應該可以更快速地運作。</span><span class="sxs-lookup"><span data-stu-id="13386-119">With few exceptions, these pages should work faster.</span></span> <span data-ttu-id="13386-120">例外狀況是因為 Internet Explorer 原生 JSON 執行和 json2.js 之間的差異。</span><span class="sxs-lookup"><span data-stu-id="13386-120">The exceptions are because of the differences between the Internet Explorer native JSON implementation and json2.js.</span></span> <span data-ttu-id="13386-121">例如，在序列化期間，原生 JSON 實作為偵測迴圈，而不會進入無限遞迴（例如 json.js）。</span><span class="sxs-lookup"><span data-stu-id="13386-121">For example, during serialization, the native JSON implementation detects cycles and does not go in infinite recursion like json.js.</span></span> <span data-ttu-id="13386-122">如需這些例外狀況的詳細資訊，請參閱 [JavaScript blog](/archive/blogs/jscript/)。</span><span class="sxs-lookup"><span data-stu-id="13386-122">For more information about these exceptions, see the [JavaScript Blogs](/archive/blogs/jscript/).</span></span>

<span data-ttu-id="13386-123">如需詳細資訊，請參閱 [JSON 檔](https://msdn.microsoft.com/library/cc836458(VS.85).aspx) 和 [版本控制和 JavaScript 引擎的版本支援](https://www.microsoft.com/windows/internet-explorer/readiness/developers-new.aspx)。</span><span class="sxs-lookup"><span data-stu-id="13386-123">For more information, see [JSON Documentation](https://msdn.microsoft.com/library/cc836458(VS.85).aspx) and [Versioning and JavaScript Engine’s Version Support](https://www.microsoft.com/windows/internet-explorer/readiness/developers-new.aspx).</span></span>

## <a name="related-topics"></a><span data-ttu-id="13386-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="13386-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="13386-125">使用相容性檢視修正 Web 應用程式中的相容性問題</span><span class="sxs-lookup"><span data-stu-id="13386-125">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
