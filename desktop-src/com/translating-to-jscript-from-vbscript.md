---
title: 從 VBScript 轉換成 JScript
description: 從 VBScript 轉換成 JScript
ms.assetid: cdf04a01-8bc3-4f37-872b-3a0aae962f26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a18c2ccb11ffa4f5f000d8cfc73f7db6f857cf6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671555"
---
# <a name="translating-to-jscript-from-vbscript"></a><span data-ttu-id="d5dee-103">從 VBScript 轉換成 JScript</span><span class="sxs-lookup"><span data-stu-id="d5dee-103">Translating to JScript from VBScript</span></span>

<span data-ttu-id="d5dee-104">在 VBScript 中，**的 ...\*\*\*\*每個** 迴圈都會列舉集合的成員;在 JScript 中，**的 ...\*\*\*\*in** 迴圈會列舉 JScript 物件或陣列的成員。</span><span class="sxs-lookup"><span data-stu-id="d5dee-104">In VBScript, the **For**...**Each** loop enumerates the members of a collection; in JScript, the **for**...**in** loop enumerates the members of a JScript object or array.</span></span> <span data-ttu-id="d5dee-105">若要列舉 JScript 中的集合，請使用枚舉器物件。</span><span class="sxs-lookup"><span data-stu-id="d5dee-105">To enumerate a collection in JScript, use an Enumerator object.</span></span>

<span data-ttu-id="d5dee-106">在 JScript 中，有數種資料類型，例如數位、字串、布林值、物件，以及 null 屬性。</span><span class="sxs-lookup"><span data-stu-id="d5dee-106">In JScript, there are several data types such as numbers, strings, Booleans, objects, and the null attribute.</span></span> <span data-ttu-id="d5dee-107">VBScript 只使用一種資料類型 **Variant**，可以 subtyped 來表示字串、數位、布林值等等。</span><span class="sxs-lookup"><span data-stu-id="d5dee-107">VBScript only uses one data type, **Variant**, which can be subtyped to represent strings, numbers, Booleans, and so on.</span></span>

<span data-ttu-id="d5dee-108">在 JScript 中，您可以藉由設定陣列 length 屬性的新值來動態展開陣列。</span><span class="sxs-lookup"><span data-stu-id="d5dee-108">In JScript, arrays can be expanded dynamically by setting a new value for the array's length property.</span></span> <span data-ttu-id="d5dee-109">在 VBScript 中，陣列無法放大;您必須使用 **redim** 語句來 redimensioned 它們。</span><span class="sxs-lookup"><span data-stu-id="d5dee-109">In VBScript, arrays cannot be enlarged; they must be redimensioned using the **redim** statement.</span></span>

<span data-ttu-id="d5dee-110">VBScript 和 JScript 都支援函數。</span><span class="sxs-lookup"><span data-stu-id="d5dee-110">Both VBScript and JScript support functions.</span></span> <span data-ttu-id="d5dee-111">但是 VBScript 也支援副程式。</span><span class="sxs-lookup"><span data-stu-id="d5dee-111">VBScript, however, also supports subroutines.</span></span> <span data-ttu-id="d5dee-112">副程式類似于函式，但不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="d5dee-112">Subroutines are similar to functions but do not return a value.</span></span>

<span data-ttu-id="d5dee-113">JScript 會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="d5dee-113">JScript is case-sensitive.</span></span> <span data-ttu-id="d5dee-114">VBScript 不是。</span><span class="sxs-lookup"><span data-stu-id="d5dee-114">VBScript is not.</span></span>

<span data-ttu-id="d5dee-115">Internet Explorer 和 Netscape Navigator 都支援 JScript。</span><span class="sxs-lookup"><span data-stu-id="d5dee-115">JScript is supported by both Internet Explorer and Netscape Navigator.</span></span> <span data-ttu-id="d5dee-116">Netscape Navigator 不支援 VBScript。</span><span class="sxs-lookup"><span data-stu-id="d5dee-116">Netscape Navigator does not support VBScript.</span></span>

<span data-ttu-id="d5dee-117">JScript 提供 Error 物件，可用來攔截和處理錯誤。</span><span class="sxs-lookup"><span data-stu-id="d5dee-117">JScript provides the Error object, which can be used to trap and handle errors.</span></span> <span data-ttu-id="d5dee-118">Error 物件類似于 VBScript Err 物件。</span><span class="sxs-lookup"><span data-stu-id="d5dee-118">The Error object is analogous to the VBScript Err object.</span></span>

<span data-ttu-id="d5dee-119">JScript 陣列不是變數類型 **VARIANT SAFEARRAY** 的陣列。</span><span class="sxs-lookup"><span data-stu-id="d5dee-119">JScript arrays are not arrays of the variable type **VARIANT SAFEARRAY**.</span></span> <span data-ttu-id="d5dee-120">如果您的腳本從 COM 物件或 VBScript 腳本接收 **VARIANT safearray** 變數，它必須使用 VBArray 物件來存取 **variant safearray** 變數。</span><span class="sxs-lookup"><span data-stu-id="d5dee-120">If your script receives a **VARIANT SAFEARRAY** variable from a COM object or VBScript script, it must use a VBArray object to access the **VARIANT SAFEARRAY** variable.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d5dee-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="d5dee-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5dee-122">翻譯為 JScript</span><span class="sxs-lookup"><span data-stu-id="d5dee-122">Translating to JScript</span></span>](translating-to-jscript.md)
</dt> </dl>

 

 




