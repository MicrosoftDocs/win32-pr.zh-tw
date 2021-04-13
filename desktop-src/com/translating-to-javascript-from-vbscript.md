---
title: 從 VBScript 轉換成 JavaScript
description: 從 VBScript 轉換成 JavaScript
ms.assetid: 39a712c5-f8d7-4441-a602-93cda43c24d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ff950c58c87e926c8593e5c009db4efbce0a371
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300204"
---
# <a name="translating-to-javascript-from-vbscript"></a><span data-ttu-id="13c90-103">從 VBScript 轉換成 JavaScript</span><span class="sxs-lookup"><span data-stu-id="13c90-103">Translating to JavaScript from VBScript</span></span>

<span data-ttu-id="13c90-104">在 JavaScript 中，有數種資料類型，例如數位、字串、布林值、物件，以及 null 屬性。</span><span class="sxs-lookup"><span data-stu-id="13c90-104">In JavaScript, there are several data types such as numbers, strings, Booleans, objects, and the null attribute.</span></span> <span data-ttu-id="13c90-105">VBScript 只使用一種資料類型 **Variant**，可以 subtyped 來表示字串、數位、布林值等等。</span><span class="sxs-lookup"><span data-stu-id="13c90-105">VBScript only uses one data type, **Variant**, which can be subtyped to represent strings, numbers, Booleans, and so on.</span></span>

<span data-ttu-id="13c90-106">在 JavaScript 中，您可以藉由設定陣列 length 屬性的新值來動態展開陣列。</span><span class="sxs-lookup"><span data-stu-id="13c90-106">In JavaScript, arrays can be expanded dynamically by setting a new value for the array's length property.</span></span> <span data-ttu-id="13c90-107">在 VBScript 中，陣列無法放大;您必須使用 **redim** 語句來 redimensioned 它們。</span><span class="sxs-lookup"><span data-stu-id="13c90-107">In VBScript, arrays cannot be enlarged; they must be redimensioned using the **redim** statement.</span></span>

<span data-ttu-id="13c90-108">VBScript 和 JavaScript 都支援函數。</span><span class="sxs-lookup"><span data-stu-id="13c90-108">Both VBScript and JavaScript support functions.</span></span> <span data-ttu-id="13c90-109">但是 VBScript 也支援副程式。</span><span class="sxs-lookup"><span data-stu-id="13c90-109">VBScript, however, also supports subroutines.</span></span> <span data-ttu-id="13c90-110">副程式類似于函式，但不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="13c90-110">Subroutines are similar to functions but do not return a value.</span></span>

<span data-ttu-id="13c90-111">JavaScript 會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="13c90-111">JavaScript is case-sensitive.</span></span> <span data-ttu-id="13c90-112">VBScript 不是。</span><span class="sxs-lookup"><span data-stu-id="13c90-112">VBScript is not.</span></span>

<span data-ttu-id="13c90-113">JavaScript 是由各式各樣的網頁瀏覽器所支援，包括 Internet Explorer 和 Netscape Navigator。</span><span class="sxs-lookup"><span data-stu-id="13c90-113">JavaScript is supported by a wide variety of Web browsers, including both Internet Explorer and Netscape Navigator.</span></span> <span data-ttu-id="13c90-114">只有 Internet Explorer 才支援 VBScript。</span><span class="sxs-lookup"><span data-stu-id="13c90-114">VBScript is only supported by Internet Explorer.</span></span>

<span data-ttu-id="13c90-115">VBScript 透過其 Err 物件提供錯誤處理支援。</span><span class="sxs-lookup"><span data-stu-id="13c90-115">VBScript provides error handling support through its Err object.</span></span> <span data-ttu-id="13c90-116">JavaScript 目前並不提供一種方式來捕捉和處理錯誤。</span><span class="sxs-lookup"><span data-stu-id="13c90-116">JavaScript does not currently provide a means of trapping and handling errors.</span></span>

## <a name="related-topics"></a><span data-ttu-id="13c90-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="13c90-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="13c90-118">翻譯為 JavaScript</span><span class="sxs-lookup"><span data-stu-id="13c90-118">Translating to JavaScript</span></span>](translating-to-javascript.md)
</dt> </dl>

 

 




