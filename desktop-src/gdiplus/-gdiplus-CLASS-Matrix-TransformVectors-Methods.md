---
description: 本主題列出 Matrix 類別的 TransformVectors 方法。 如需矩陣類別之方法的完整清單，請參閱矩陣方法。
ms.assetid: 6a2ed6a7-825a-422b-b035-b88746f3ab5d
title: 'TransformVectors 方法 (Gdiplusmatrix .h) '
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 3bdb67d839163ffe2d26623a01fc186f8e885ca2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "104974821"
---
# <a name="matrixtransformvectors-methods"></a><span data-ttu-id="39123-104">TransformVectors 方法</span><span class="sxs-lookup"><span data-stu-id="39123-104">Matrix.TransformVectors methods</span></span>

<span data-ttu-id="39123-105">本主題列出 [**Matrix**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) 類別的 TransformVectors 方法。</span><span class="sxs-lookup"><span data-stu-id="39123-105">This topic lists the TransformVectors methods of the [**Matrix**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) class.</span></span> <span data-ttu-id="39123-106">如需 **矩陣** 類別之方法的完整清單，請參閱 [矩陣方法](-gdiplus-class-matrix-methods.md)。</span><span class="sxs-lookup"><span data-stu-id="39123-106">For a complete list of methods for the **Matrix** class, see [Matrix Methods](-gdiplus-class-matrix-methods.md).</span></span>

### <a name="overload-list"></a><span data-ttu-id="39123-107">多載清單</span><span class="sxs-lookup"><span data-stu-id="39123-107">Overload list</span></span>



| <span data-ttu-id="39123-108">方法</span><span class="sxs-lookup"><span data-stu-id="39123-108">Method</span></span>                                                                                                 | <span data-ttu-id="39123-109">描述</span><span class="sxs-lookup"><span data-stu-id="39123-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                      |
|:-------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39123-110">[**TransformVectors (Point \* ，INT)**](/windows/win32/api/gdiplusmatrix/nf-gdiplusmatrix-matrix-transformvectors(inoutpoint_inint))</span><span class="sxs-lookup"><span data-stu-id="39123-110">[**TransformVectors(Point\*,INT)**](/windows/win32/api/gdiplusmatrix/nf-gdiplusmatrix-matrix-transformvectors(inoutpoint_inint))</span></span>   | <span data-ttu-id="39123-111">[**矩陣：： TransformVectors**](/windows/win32/api/gdiplusmatrix/nf-gdiplusmatrix-matrix-transformvectors(inoutpoint_inint))方法會將陣列中的每個向量乘以此矩陣。</span><span class="sxs-lookup"><span data-stu-id="39123-111">The [**Matrix::TransformVectors**](/windows/win32/api/gdiplusmatrix/nf-gdiplusmatrix-matrix-transformvectors(inoutpoint_inint)) method multiplies each vector in an array by this matrix.</span></span> <span data-ttu-id="39123-112">這個矩陣的轉換項目 (第三列) 會被忽略。</span><span class="sxs-lookup"><span data-stu-id="39123-112">The translation elements of this matrix (third row) are ignored.</span></span> <span data-ttu-id="39123-113">每個向量都會被視為資料列矩陣。</span><span class="sxs-lookup"><span data-stu-id="39123-113">Each vector is treated as a row matrix.</span></span> <span data-ttu-id="39123-114">使用左邊的資料列矩陣和右邊的矩陣來執行乘法。</span><span class="sxs-lookup"><span data-stu-id="39123-114">The multiplication is performed with the row matrix on the left and this matrix on the right.</span></span><br/>  |
| <span data-ttu-id="39123-115">[**TransformVectors (PointF \* ，INT)**](/previous-versions//ms535319(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="39123-115">[**TransformVectors(PointF\*,INT)**](/previous-versions//ms535319(v=vs.85))</span></span> | <span data-ttu-id="39123-116">[**矩陣：： TransformVectors**](/previous-versions//ms535319(v=vs.85))方法會將陣列中的每個向量乘以此矩陣。</span><span class="sxs-lookup"><span data-stu-id="39123-116">The [**Matrix::TransformVectors**](/previous-versions//ms535319(v=vs.85)) method multiplies each vector in an array by this matrix.</span></span> <span data-ttu-id="39123-117">這個矩陣的轉換項目 (第三列) 會被忽略。</span><span class="sxs-lookup"><span data-stu-id="39123-117">The translation elements of this matrix (third row) are ignored.</span></span> <span data-ttu-id="39123-118">每個向量都會被視為資料列矩陣。</span><span class="sxs-lookup"><span data-stu-id="39123-118">Each vector is treated as a row matrix.</span></span> <span data-ttu-id="39123-119">使用左邊的資料列矩陣和右邊的矩陣來執行乘法。</span><span class="sxs-lookup"><span data-stu-id="39123-119">The multiplication is performed with the row matrix on the left and this matrix on the right.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="39123-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="39123-120">Requirements</span></span>



| <span data-ttu-id="39123-121">需求</span><span class="sxs-lookup"><span data-stu-id="39123-121">Requirement</span></span> | <span data-ttu-id="39123-122">值</span><span class="sxs-lookup"><span data-stu-id="39123-122">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="39123-123">標頭</span><span class="sxs-lookup"><span data-stu-id="39123-123">Header</span></span><br/> | <dl> <span data-ttu-id="39123-124"><dt>Gdiplusmatrix。h</dt></span><span class="sxs-lookup"><span data-stu-id="39123-124"><dt>Gdiplusmatrix.h</dt></span></span> </dl> |



 

 
