---
description: 單一矩陣物件可以儲存單一轉換或一連串的轉換。
ms.assetid: 1dc68ff8-6b17-4934-82da-ab2fc612aafa
title: 為何轉換順序很重要
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7350d63456902ff47183faa08170b3b2fef481
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972136"
---
# <a name="why-transformation-order-is-significant"></a><span data-ttu-id="4a9f1-103">為何轉換順序很重要</span><span class="sxs-lookup"><span data-stu-id="4a9f1-103">Why Transformation Order Is Significant</span></span>

<span data-ttu-id="4a9f1-104">單一 [**矩陣**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) 物件可以儲存單一轉換或一連串的轉換。</span><span class="sxs-lookup"><span data-stu-id="4a9f1-104">A single [**Matrix**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) object can store a single transformation or a sequence of transformations.</span></span> <span data-ttu-id="4a9f1-105">後者稱為「 *複合*  *轉換*」。</span><span class="sxs-lookup"><span data-stu-id="4a9f1-105">The latter is called a *composite*  *transformation*.</span></span> <span data-ttu-id="4a9f1-106">複合轉換的矩陣是藉由將個別轉換的矩陣相乘來取得的。</span><span class="sxs-lookup"><span data-stu-id="4a9f1-106">The matrix of a composite transformation is obtained by multiplying the matrices of the individual transformations.</span></span>

<span data-ttu-id="4a9f1-107">在複合轉換中，個別轉換的順序很重要。</span><span class="sxs-lookup"><span data-stu-id="4a9f1-107">In a composite transformation, the order of the individual transformations is important.</span></span> <span data-ttu-id="4a9f1-108">例如，如果您第一次旋轉，然後進行調整，然後轉譯，則會得到不同的結果，而不是您第一次轉譯、接著旋轉然後調整規模。</span><span class="sxs-lookup"><span data-stu-id="4a9f1-108">For example, if you first rotate, then scale, then translate, you get a different result than if you first translate, then rotate, then scale.</span></span> <span data-ttu-id="4a9f1-109">在 Windows GDI + 中，複合轉換是由左至右建立。</span><span class="sxs-lookup"><span data-stu-id="4a9f1-109">In Windows GDI+, composite transformations are built from left to right.</span></span> <span data-ttu-id="4a9f1-110">如果 S、R 和 T 分別是縮放、旋轉和轉譯矩陣，則產品 SRT 會以該順序 () 是第一次調整的複合轉換矩陣，然後旋轉然後轉譯。</span><span class="sxs-lookup"><span data-stu-id="4a9f1-110">If S, R, and T are scale, rotation, and translation matrices respectively, then the product SRT (in that order) is the matrix of the composite transformation that first scales, then rotates, then translates.</span></span> <span data-ttu-id="4a9f1-111">產品 SRT 所產生的矩陣與產品 TRS 所產生的矩陣不同。</span><span class="sxs-lookup"><span data-stu-id="4a9f1-111">The matrix produced by the product SRT is different from the matrix produced by the product TRS.</span></span>

<span data-ttu-id="4a9f1-112">其中一個原因是很重要的是，旋轉和縮放等轉換是針對座標系統的原點進行的。</span><span class="sxs-lookup"><span data-stu-id="4a9f1-112">One reason order is significant is that transformations like rotation and scaling are done with respect to the origin of the coordinate system.</span></span> <span data-ttu-id="4a9f1-113">調整位於原點中央的物件會產生不同的結果，而不是縮放已從原點移出的物件。</span><span class="sxs-lookup"><span data-stu-id="4a9f1-113">Scaling an object that is centered at the origin produces a different result than scaling an object that has been moved away from the origin.</span></span> <span data-ttu-id="4a9f1-114">同樣地，旋轉位於原點中央的物件會產生不同的結果，而不是旋轉離開來源的物件。</span><span class="sxs-lookup"><span data-stu-id="4a9f1-114">Similarly, rotating an object that is centered at the origin produces a different result than rotating an object that has been moved away from the origin.</span></span>

<span data-ttu-id="4a9f1-115">下列範例結合了調整、旋轉和轉譯 (順序) 形成複合轉換。</span><span class="sxs-lookup"><span data-stu-id="4a9f1-115">The following example combines scaling, rotation and translation (in that order) to form a composite transformation.</span></span> <span data-ttu-id="4a9f1-116">傳遞至 [**Graphics：： RotateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-rotatetransform)方法的引數 [\* \* \* \* MatrixOrderAppend \*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder) \* 會指定旋轉將遵循調整。</span><span class="sxs-lookup"><span data-stu-id="4a9f1-116">The argument [\*\*\*\*MatrixOrderAppend\*\*\*\*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder) passed to the [**Graphics::RotateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-rotatetransform) method specifies that the rotation will follow the scaling.</span></span> <span data-ttu-id="4a9f1-117">同樣地，傳遞給 [**Graphics：： TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform)方法的引數 [\* \* \* \* MatrixOrderAppend \*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder) \* \* 會指定轉譯會在旋轉之後。</span><span class="sxs-lookup"><span data-stu-id="4a9f1-117">Likewise, the argument [\*\*\*\*MatrixOrderAppend\*\*\*\*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder) passed to the [**Graphics::TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform) method specifies that the translation will follow the rotation.</span></span>


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.ScaleTransform(1.75f, 0.5f);
graphics.RotateTransform(28.0f, MatrixOrderAppend);
graphics.TranslateTransform(150.0f, 150.0f, MatrixOrderAppend);
graphics.DrawRectangle(&pen, rect);
```



<span data-ttu-id="4a9f1-118">下列範例會執行與上述範例相同的方法呼叫，但是呼叫的順序會反轉。</span><span class="sxs-lookup"><span data-stu-id="4a9f1-118">The following example makes the same method calls as the previous example, but the order of the calls is reversed.</span></span> <span data-ttu-id="4a9f1-119">產生的作業順序會先轉譯，然後再旋轉，然後調整，以產生與第一個尺規不同的結果，然後再旋轉，然後轉譯：</span><span class="sxs-lookup"><span data-stu-id="4a9f1-119">The resulting order of operations is first translate, then rotate, then scale, which produces a very different result than first scale, then rotate, then translate:</span></span>


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.TranslateTransform(150.0f, 150.0f);
graphics.RotateTransform(28.0f, MatrixOrderAppend);
graphics.ScaleTransform(1.75f, 0.5f, MatrixOrderAppend);
graphics.DrawRectangle(&pen, rect);
```



<span data-ttu-id="4a9f1-120">在複合轉換中反轉個別轉換順序的其中一種方式，是反轉方法呼叫序列的順序。</span><span class="sxs-lookup"><span data-stu-id="4a9f1-120">One way to reverse the order of the individual transformations in a composite transformation is to reverse the order of a sequence of method calls.</span></span> <span data-ttu-id="4a9f1-121">控制作業順序的第二種方式是變更矩陣順序引數。</span><span class="sxs-lookup"><span data-stu-id="4a9f1-121">A second way to control the order of operations is to change the matrix order argument.</span></span> <span data-ttu-id="4a9f1-122">下列範例與上一個範例相同，不同之處在于 [\* \* \* \* MatrixOrderAppend \* \*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder) \* \* 已變更為 [\* \* \* \* MatrixOrderPrepend \* \*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder)\* \*。</span><span class="sxs-lookup"><span data-stu-id="4a9f1-122">The following example is the same as the previous example, except that [\*\*\*\*MatrixOrderAppend\*\*\*\*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder) has been changed to [\*\*\*\*MatrixOrderPrepend\*\*\*\*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder).</span></span> <span data-ttu-id="4a9f1-123">矩陣乘法是在 order SRT 中完成，其中 S、R 和 T 分別是調整、旋轉和轉譯的矩陣。</span><span class="sxs-lookup"><span data-stu-id="4a9f1-123">The matrix multiplication is done in the order SRT, where S, R, and T are the matrices for scale, rotate, and translate, respectively.</span></span> <span data-ttu-id="4a9f1-124">複合轉換的順序是先進行調整，然後再旋轉，然後轉譯。</span><span class="sxs-lookup"><span data-stu-id="4a9f1-124">The order of the composite transformation is first scale, then rotate, then translate.</span></span>


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.TranslateTransform(150.0f, 150.0f,MatrixOrderPrepend);
graphics.RotateTransform(28.0f, MatrixOrderPrepend);
graphics.ScaleTransform(1.75f, 0.5f, MatrixOrderPrepend);
graphics.DrawRectangle(&pen, rect);
```



<span data-ttu-id="4a9f1-125">上述範例的結果與我們在本節的第一個範例中達成的結果相同。</span><span class="sxs-lookup"><span data-stu-id="4a9f1-125">The result of the preceding example is the same result that we achieved in the first example of this section.</span></span> <span data-ttu-id="4a9f1-126">這是因為我們反轉方法呼叫的順序和矩陣相乘的順序。</span><span class="sxs-lookup"><span data-stu-id="4a9f1-126">This is because we reversed both the order of the method calls and the order of the matrix multiplication.</span></span>

 

 



