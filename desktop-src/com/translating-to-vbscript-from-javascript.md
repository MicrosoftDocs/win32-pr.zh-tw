---
title: 從 JavaScript 轉換成 VBScript
description: 從 JavaScript 轉換成 VBScript
ms.assetid: f302e032-4e94-42f1-839b-022dab538760
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2eda8169a665dc93133f7ac933de12ecc612f3e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106966184"
---
# <a name="translating-to-vbscript-from-javascript"></a><span data-ttu-id="b7779-103">從 JavaScript 轉換成 VBScript</span><span class="sxs-lookup"><span data-stu-id="b7779-103">Translating to VBScript from JavaScript</span></span>

<span data-ttu-id="b7779-104">在 JavaScript 中，有數種資料類型，例如數位、字串、布林值、物件，以及 null 屬性。</span><span class="sxs-lookup"><span data-stu-id="b7779-104">In JavaScript, there are several data types, such as numbers, strings, Booleans, objects, and the null attribute.</span></span> <span data-ttu-id="b7779-105">VBScript 只使用一種資料類型 **Variant**，可以 subtyped 來表示字串、數位、布林值等等。</span><span class="sxs-lookup"><span data-stu-id="b7779-105">VBScript only uses one data type, **Variant**, which can be subtyped to represent strings, numbers, Booleans, and so on.</span></span>

<span data-ttu-id="b7779-106">在 JavaScript 中，您可以藉由設定陣列 length 屬性的新值來動態展開陣列。</span><span class="sxs-lookup"><span data-stu-id="b7779-106">In JavaScript, arrays can be expanded dynamically by setting a new value for the array's length property.</span></span> <span data-ttu-id="b7779-107">在 VBScript 中，陣列無法放大;您必須使用 **redim** 語句來 redimensioned 它們。</span><span class="sxs-lookup"><span data-stu-id="b7779-107">In VBScript, arrays cannot be enlarged; they must be redimensioned using the **redim** statement.</span></span>

<span data-ttu-id="b7779-108">VBScript 和 JavaScript 都支援函數。</span><span class="sxs-lookup"><span data-stu-id="b7779-108">Both VBScript and JavaScript support functions.</span></span> <span data-ttu-id="b7779-109">但是 VBScript 也支援副程式。</span><span class="sxs-lookup"><span data-stu-id="b7779-109">VBScript, however, also supports subroutines.</span></span> <span data-ttu-id="b7779-110">副程式類似于函式，不同之處在于它們不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="b7779-110">Subroutines are similar to functions, except they do not return a value.</span></span>

<span data-ttu-id="b7779-111">JavaScript 會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="b7779-111">JavaScript is case-sensitive.</span></span> <span data-ttu-id="b7779-112">VBScript 不是。</span><span class="sxs-lookup"><span data-stu-id="b7779-112">VBScript is not.</span></span>

<span data-ttu-id="b7779-113">JavaScript 是由各式各樣的網頁瀏覽器所支援，包括 Internet Explorer 和 Netscape Navigator。</span><span class="sxs-lookup"><span data-stu-id="b7779-113">JavaScript is supported by a wide variety of Web browsers, including both Internet Explorer and Netscape Navigator.</span></span> <span data-ttu-id="b7779-114">Netscape Navigator 不支援 VBScript。</span><span class="sxs-lookup"><span data-stu-id="b7779-114">Netscape Navigator does not support VBScript.</span></span>

<span data-ttu-id="b7779-115">VBScript 透過其 Err 物件支援錯誤處理。</span><span class="sxs-lookup"><span data-stu-id="b7779-115">VBScript supports error handling through its Err object.</span></span> <span data-ttu-id="b7779-116">JavaScript 目前並不提供一種方式來捕捉和處理錯誤。</span><span class="sxs-lookup"><span data-stu-id="b7779-116">JavaScript does not currently provide a means of trapping and handling errors.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b7779-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="b7779-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7779-118">翻譯為 VBScript</span><span class="sxs-lookup"><span data-stu-id="b7779-118">Translating to VBScript</span></span>](translating-to-vbscript.md)
</dt> </dl>

 

 




