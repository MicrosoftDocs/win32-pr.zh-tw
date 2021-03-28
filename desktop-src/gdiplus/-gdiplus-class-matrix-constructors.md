---
description: 本主題列出矩陣類別的函式。 如需完整的類別清單，請參閱矩陣類別。
ms.assetid: a1411b9c-69e9-441e-a476-b0eb6ec30bf2
title: Matrix. 矩陣函數
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name: ''
api_type:
- NA
api_location: ''
ms.openlocfilehash: e2f8b4a58a6a1257be4c28cc6aa6bc5400bb81bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943953"
---
# <a name="matrixmatrix-constructors"></a><span data-ttu-id="7eee0-104">Matrix. 矩陣函數</span><span class="sxs-lookup"><span data-stu-id="7eee0-104">Matrix.Matrix constructors</span></span>

<span data-ttu-id="7eee0-105">本主題列出 [**矩陣**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) 類別的函式。</span><span class="sxs-lookup"><span data-stu-id="7eee0-105">This topic lists the constructors of the [**Matrix**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) class.</span></span> <span data-ttu-id="7eee0-106">如需完整的類別清單，請參閱 **矩陣類別**。</span><span class="sxs-lookup"><span data-stu-id="7eee0-106">For a complete class listing, see **Matrix Class**.</span></span>

### <a name="overload-list"></a><span data-ttu-id="7eee0-107">多載清單</span><span class="sxs-lookup"><span data-stu-id="7eee0-107">Overload list</span></span>



| <span data-ttu-id="7eee0-108">建構函式</span><span class="sxs-lookup"><span data-stu-id="7eee0-108">Constructor</span></span>                                                                                          | <span data-ttu-id="7eee0-109">描述</span><span class="sxs-lookup"><span data-stu-id="7eee0-109">Description</span></span>                                                                                                                                                                          |
|:-----------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7eee0-110">[**矩陣 (Rect&、點 \*)**](/windows/win32/api/gdiplusmatrix/nf-gdiplusmatrix-matrix-matrix(inconstrect__inconstpoint))</span><span class="sxs-lookup"><span data-stu-id="7eee0-110">[**Matrix(Rect&,Point\*)**](/windows/win32/api/gdiplusmatrix/nf-gdiplusmatrix-matrix-matrix(inconstrect__inconstpoint))</span></span>                | <span data-ttu-id="7eee0-111">根據矩形和點建立 [**矩陣：：矩陣**](/windows/win32/api/gdiplusmatrix/nf-gdiplusmatrix-matrix-matrix(inconstrect__inconstpoint)) 物件。</span><span class="sxs-lookup"><span data-stu-id="7eee0-111">Creates a [**Matrix::Matrix**](/windows/win32/api/gdiplusmatrix/nf-gdiplusmatrix-matrix-matrix(inconstrect__inconstpoint)) object based on a rectangle and a point.</span></span><br/>                                         |
| <span data-ttu-id="7eee0-112">[**矩陣 (RectF&、PointF \*)**](/windows/win32/api/gdiplusmatrix/nf-gdiplusmatrix-matrix-matrix(inconstrectf__inconstpointf))</span><span class="sxs-lookup"><span data-stu-id="7eee0-112">[**Matrix(RectF&,PointF\*)**](/windows/win32/api/gdiplusmatrix/nf-gdiplusmatrix-matrix-matrix(inconstrectf__inconstpointf))</span></span>            | <span data-ttu-id="7eee0-113">根據矩形和點建立 [**矩陣：：矩陣**](/windows/win32/api/gdiplusmatrix/nf-gdiplusmatrix-matrix-matrix(inconstrectf__inconstpointf)) 物件。</span><span class="sxs-lookup"><span data-stu-id="7eee0-113">Creates a [**Matrix::Matrix**](/windows/win32/api/gdiplusmatrix/nf-gdiplusmatrix-matrix-matrix(inconstrectf__inconstpointf)) object based on a rectangle and a point.</span></span><br/>                                       |
| <span data-ttu-id="7eee0-114">[**矩陣 (REAL、REAL、REAL、REAL、real)**](/windows/win32/api/gdiplusmatrix/nf-gdiplusmatrix-matrix-matrix(inreal_inreal_inreal_inreal_inreal_inreal))</span><span class="sxs-lookup"><span data-stu-id="7eee0-114">[**Matrix(REAL,REAL,REAL,REAL,REAL,REAL)**](/windows/win32/api/gdiplusmatrix/nf-gdiplusmatrix-matrix-matrix(inreal_inreal_inreal_inreal_inreal_inreal))</span></span> | <span data-ttu-id="7eee0-115">根據定義仿射轉換的六個數字，建立及初始化 [**矩陣：：矩陣**](/windows/win32/api/gdiplusmatrix/nf-gdiplusmatrix-matrix-matrix(inreal_inreal_inreal_inreal_inreal_inreal)) 物件。</span><span class="sxs-lookup"><span data-stu-id="7eee0-115">Creates and initializes a [**Matrix::Matrix**](/windows/win32/api/gdiplusmatrix/nf-gdiplusmatrix-matrix-matrix(inreal_inreal_inreal_inreal_inreal_inreal)) object based on six numbers that define an affine transformation.</span></span><br/> |
| <span data-ttu-id="7eee0-116">[**矩陣 ()**](/windows/win32/api/gdiplusmatrix/nf-gdiplusmatrix-matrix-matrix(constmatrix_))</span><span class="sxs-lookup"><span data-stu-id="7eee0-116">[**Matrix()**](/windows/win32/api/gdiplusmatrix/nf-gdiplusmatrix-matrix-matrix(constmatrix_))</span></span>                                                    | <span data-ttu-id="7eee0-117">建立並初始化 [**矩陣：：矩陣**](/windows/win32/api/gdiplusmatrix/nf-gdiplusmatrix-matrix-matrix(constmatrix_)) 物件，該物件代表識別矩陣。</span><span class="sxs-lookup"><span data-stu-id="7eee0-117">Creates and initializes a [**Matrix::Matrix**](/windows/win32/api/gdiplusmatrix/nf-gdiplusmatrix-matrix-matrix(constmatrix_)) object that represents the identity matrix.</span></span><br/>                                             |



 

 
