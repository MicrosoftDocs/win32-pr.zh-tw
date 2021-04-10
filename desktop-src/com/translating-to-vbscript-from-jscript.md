---
title: 從 JScript 轉換成 VBScript
description: 從 JScript 轉換成 VBScript
ms.assetid: db1115e1-2abd-4b06-ad8d-c1f917cd3087
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 704f5ac608e94f883edc3b319fd04625e9a08d18
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021138"
---
# <a name="translating-to-vbscript-from-jscript"></a><span data-ttu-id="dc078-103">從 JScript 轉換成 VBScript</span><span class="sxs-lookup"><span data-stu-id="dc078-103">Translating to VBScript from JScript</span></span>

<span data-ttu-id="dc078-104">在 VBScript 中，**的 ...\*\*\*\*每個** 迴圈都會列舉集合的成員;在 JScript 中，**的 ...\*\*\*\*in** 迴圈會列舉 JScript 物件或陣列的成員。</span><span class="sxs-lookup"><span data-stu-id="dc078-104">In VBScript, the **For**...**Each** loop enumerates the members of a collection; in JScript, the **for**...**in** loop enumerates the members of a JScript object or array.</span></span> <span data-ttu-id="dc078-105">若要列舉 JScript 中的集合，請使用枚舉器物件。</span><span class="sxs-lookup"><span data-stu-id="dc078-105">To enumerate a collection in JScript, use an Enumerator object.</span></span>

<span data-ttu-id="dc078-106">JScript 提供 Error 物件，可用來攔截和處理錯誤。</span><span class="sxs-lookup"><span data-stu-id="dc078-106">JScript provides the Error object, which can be used to trap and handle errors.</span></span> <span data-ttu-id="dc078-107">Error 物件類似于 VBScript Err 物件。</span><span class="sxs-lookup"><span data-stu-id="dc078-107">The Error object is analogous to the VBScript Err object.</span></span>

<span data-ttu-id="dc078-108">在 JScript 中，有數種資料類型，例如數位、字串、布林值、物件，以及 null 屬性。</span><span class="sxs-lookup"><span data-stu-id="dc078-108">In JScript, there are several data types such as numbers, strings, Booleans, objects, and the null attribute.</span></span> <span data-ttu-id="dc078-109">VBScript 只使用一種資料類型 **Variant**，可以 subtyped 來表示字串、數位、布林值等等。</span><span class="sxs-lookup"><span data-stu-id="dc078-109">VBScript only uses one data type, **Variant**, which can be subtyped to represent strings, numbers, Booleans, and so on.</span></span>

<span data-ttu-id="dc078-110">在 JScript 中，您可以藉由設定陣列 length 屬性的新值來動態展開陣列。</span><span class="sxs-lookup"><span data-stu-id="dc078-110">In JScript, arrays can be expanded dynamically by setting a new value for the array's length property.</span></span> <span data-ttu-id="dc078-111">在 VBScript 中，陣列無法放大;您必須使用 **redim** 語句來 redimensioned 它們。</span><span class="sxs-lookup"><span data-stu-id="dc078-111">In VBScript, arrays cannot be enlarged; they must be redimensioned using the **redim** statement.</span></span>

<span data-ttu-id="dc078-112">VBScript 和 JScript 都支援函數。</span><span class="sxs-lookup"><span data-stu-id="dc078-112">Both VBScript and JScript support functions.</span></span> <span data-ttu-id="dc078-113">但是 VBScript 也支援副程式。</span><span class="sxs-lookup"><span data-stu-id="dc078-113">VBScript, however, also supports subroutines.</span></span> <span data-ttu-id="dc078-114">副程式類似于函式，但不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="dc078-114">Subroutines are similar to functions but do not return a value.</span></span>

<span data-ttu-id="dc078-115">JScript 會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="dc078-115">JScript is case-sensitive.</span></span> <span data-ttu-id="dc078-116">VBScript 不是。</span><span class="sxs-lookup"><span data-stu-id="dc078-116">VBScript is not.</span></span>

<span data-ttu-id="dc078-117">JScript 是由各式各樣的網頁瀏覽器所支援，包括 Internet Explorer 和 Netscape Navigator。</span><span class="sxs-lookup"><span data-stu-id="dc078-117">JScript is supported by a wide variety of Web browsers, including both Internet Explorer and Netscape Navigator.</span></span> <span data-ttu-id="dc078-118">Netscape Navigator 不支援 VBScript。</span><span class="sxs-lookup"><span data-stu-id="dc078-118">Netscape Navigator does not support VBScript.</span></span>

<span data-ttu-id="dc078-119">JScript 陣列不是變數類型 **VARIANT SAFEARRAY** 的陣列。</span><span class="sxs-lookup"><span data-stu-id="dc078-119">JScript arrays are not arrays of the variable type **VARIANT SAFEARRAY**.</span></span> <span data-ttu-id="dc078-120">JScript 腳本必須使用 VBArray 物件來存取 **VARIANT SAFEARRAY** 變數。</span><span class="sxs-lookup"><span data-stu-id="dc078-120">A JScript script must use a VBArray object to access the **VARIANT SAFEARRAY** variable.</span></span> <span data-ttu-id="dc078-121">VBScript 腳本可以直接存取 **VARIANT SAFEARRAY** 變數。</span><span class="sxs-lookup"><span data-stu-id="dc078-121">VBScript scripts can access **VARIANT SAFEARRAY** variables directly.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dc078-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="dc078-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dc078-123">翻譯為 VBScript</span><span class="sxs-lookup"><span data-stu-id="dc078-123">Translating to VBScript</span></span>](translating-to-vbscript.md)
</dt> </dl>

 

 




