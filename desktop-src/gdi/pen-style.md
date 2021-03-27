---
description: Style 屬性會指定使用特定表面或幾何畫筆時所顯示的線條模式。 預先定義的畫筆樣式有八個。 下圖顯示由系統定義的七個樣式。
ms.assetid: a9aaa999-529c-46e1-9a3f-b6fdcbeb5b51
title: 畫筆樣式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f447839627f97d7662fdef35bd7088ef7b0dcba5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943800"
---
# <a name="pen-style"></a><span data-ttu-id="b21fd-105">畫筆樣式</span><span class="sxs-lookup"><span data-stu-id="b21fd-105">Pen Style</span></span>

<span data-ttu-id="b21fd-106">Style 屬性會指定使用特定表面或幾何畫筆時所顯示的線條模式。</span><span class="sxs-lookup"><span data-stu-id="b21fd-106">The style attribute specifies the line pattern that appears when a particular cosmetic or geometric pen is used.</span></span> <span data-ttu-id="b21fd-107">預先定義的畫筆樣式有八個。</span><span class="sxs-lookup"><span data-stu-id="b21fd-107">There are eight predefined pen styles.</span></span> <span data-ttu-id="b21fd-108">下圖顯示由系統定義的七個樣式。</span><span class="sxs-lookup"><span data-stu-id="b21fd-108">The following illustration shows the seven of these styles that are defined by the system.</span></span>

![圖例顯示七行，每個線條使用不同的預先定義樣式繪製](images/cspen-01.png)

<span data-ttu-id="b21fd-110">內框架樣式與表面畫筆的純色樣式相同。</span><span class="sxs-lookup"><span data-stu-id="b21fd-110">The inside-frame style is identical to the solid style for cosmetic pens.</span></span> <span data-ttu-id="b21fd-111">不過，與幾何畫筆搭配使用時，它的運作方式不同。</span><span class="sxs-lookup"><span data-stu-id="b21fd-111">However, it operates differently when used with a geometric pen.</span></span> <span data-ttu-id="b21fd-112">如果幾何畫筆的寬度超過單一圖元，而繪圖函式使用畫筆在填滿的物件周圍繪製框線，系統就會在物件的框架內繪製框線。</span><span class="sxs-lookup"><span data-stu-id="b21fd-112">If the geometric pen is wider than a single pixel and a drawing function uses the pen to draw a border around a filled object, the system draws the border inside the object's frame.</span></span> <span data-ttu-id="b21fd-113">藉由使用內建的樣式，應用程式可以確保物件完全出現在指定的維度內，無論幾何畫筆的寬度為何。</span><span class="sxs-lookup"><span data-stu-id="b21fd-113">By using the inside-frame style, an application can ensure that an object appears entirely within the specified dimensions, regardless of the geometric pen width.</span></span>

<span data-ttu-id="b21fd-114">除了系統所定義的七種樣式之外，還有第八種樣式，也就是使用者 (或應用程式) 定義。</span><span class="sxs-lookup"><span data-stu-id="b21fd-114">In addition to the seven styles defined by the system, there is an eighth style that is user (or application) defined.</span></span> <span data-ttu-id="b21fd-115">使用者定義樣式會產生具有自訂一連串虛線和點的行。</span><span class="sxs-lookup"><span data-stu-id="b21fd-115">A user-defined style generates lines with a customized series of dashes and dots.</span></span>

<span data-ttu-id="b21fd-116">您可以使用 [**CreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-createpen)、 [**CreatePenIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createpenindirect)或 [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) 函數來建立具有系統定義樣式的畫筆。</span><span class="sxs-lookup"><span data-stu-id="b21fd-116">Use the [**CreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-createpen), [**CreatePenIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createpenindirect), or [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) function to create a pen that has the system-defined styles.</span></span> <span data-ttu-id="b21fd-117">您可以使用 **ExtCreatePen** 函式來建立具有使用者定義樣式的畫筆。</span><span class="sxs-lookup"><span data-stu-id="b21fd-117">Use the **ExtCreatePen** function to create a pen that has a user-defined style.</span></span>

 

 



