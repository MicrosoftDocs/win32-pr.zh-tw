---
title: 'glEdgeFlagv 函式 (Gl) '
description: '將邊緣旗標為界限或 nonboundary。 |glEdgeFlagv 函式 (Gl) '
ms.assetid: 69b5ddbd-7c0c-47f0-a358-d8bf81755c88
keywords:
- glEdgeFlagv 函式 OpenGL
topic_type:
- apiref
api_name:
- glEdgeFlagv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe031ab3981e3daa2e6b1aefd51c9eaa62c84483
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322244"
---
# <a name="gledgeflagv-function"></a><span data-ttu-id="40632-105">glEdgeFlagv 函式</span><span class="sxs-lookup"><span data-stu-id="40632-105">glEdgeFlagv function</span></span>

<span data-ttu-id="40632-106">將邊緣旗標為界限或 nonboundary。</span><span class="sxs-lookup"><span data-stu-id="40632-106">Flags edges as either boundary or nonboundary.</span></span>

## <a name="syntax"></a><span data-ttu-id="40632-107">語法</span><span class="sxs-lookup"><span data-stu-id="40632-107">Syntax</span></span>


```C++
void WINAPI glEdgeFlagv(
   const GLboolean *flag
);
```



## <a name="parameters"></a><span data-ttu-id="40632-108">參數</span><span class="sxs-lookup"><span data-stu-id="40632-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40632-109">*旗標*</span><span class="sxs-lookup"><span data-stu-id="40632-109">*flag*</span></span> 
</dt> <dd>

<span data-ttu-id="40632-110">指定陣列的指標，該陣列包含單一布林值元素，其會取代目前的邊緣旗標值。</span><span class="sxs-lookup"><span data-stu-id="40632-110">Specifies a pointer to an array that contains a single Boolean element, which replaces the current edge flag value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40632-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="40632-111">Return value</span></span>

<span data-ttu-id="40632-112">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="40632-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="40632-113">備註</span><span class="sxs-lookup"><span data-stu-id="40632-113">Remarks</span></span>

<span data-ttu-id="40632-114">多邊形、個別三角形或 [**glBegin**](/windows/desktop/OpenGL/glbegin)glEnd 配對之間指定之個別四邊形的每個頂點 / [](/windows/desktop/OpenGL/glend)都會標示為界限或 nonboundary 邊緣的起點。</span><span class="sxs-lookup"><span data-stu-id="40632-114">Each vertex of a polygon, separate triangle, or separate quadrilateral specified between a [**glBegin**](/windows/desktop/OpenGL/glbegin)/[**glEnd**](/windows/desktop/OpenGL/glend) pair is marked as the start of either a boundary or nonboundary edge.</span></span> <span data-ttu-id="40632-115">當指定頂點時，如果目前的邊緣旗標為 **TRUE** ，則會將頂點標示為界限邊緣的起點。</span><span class="sxs-lookup"><span data-stu-id="40632-115">If the current edge flag is **TRUE** when the vertex is specified, the vertex is marked as the start of a boundary edge.</span></span> <span data-ttu-id="40632-116">如果目前的邊緣旗標為 **FALSE**，則會將頂點標示為 nonboundary 邊緣的開頭。</span><span class="sxs-lookup"><span data-stu-id="40632-116">If the current edge flag is **FALSE**, the vertex is marked as the start of a nonboundary edge.</span></span> <span data-ttu-id="40632-117">如果旗標為非零，則 **glEdgeFlagv** 函式會將邊緣旗標設定為 **TRUE** ，否則為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="40632-117">The **glEdgeFlagv** function sets the edge flag to **TRUE** if flag is nonzero, **FALSE** otherwise.</span></span>

<span data-ttu-id="40632-118">無論邊緣旗標的值為何，連接的三角形和連接 quadrilaterals 的頂點一律會標示為界限。</span><span class="sxs-lookup"><span data-stu-id="40632-118">The vertices of connected triangles and connected quadrilaterals are always marked as boundary, regardless of the value of the edge flag.</span></span>

<span data-ttu-id="40632-119">只有當 GL \_ 多邊形 \_ 模式設定為 gl \_ 點或 gl 線時，頂點上的界限和 nonboundary 邊緣旗標才有意義 \_ 。</span><span class="sxs-lookup"><span data-stu-id="40632-119">Boundary and nonboundary edge flags on vertices are significant only if GL\_POLYGON\_MODE is set to GL\_POINT or GL\_LINE.</span></span> <span data-ttu-id="40632-120">請參閱 [**glPolygonMode**](/windows/desktop/OpenGL/glpolygonmode)。</span><span class="sxs-lookup"><span data-stu-id="40632-120">See [**glPolygonMode**](/windows/desktop/OpenGL/glpolygonmode).</span></span>

<span data-ttu-id="40632-121">一開始，邊緣旗標位為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="40632-121">Initially, the edge flag bit is **TRUE**.</span></span>

<span data-ttu-id="40632-122">您可以隨時更新目前的 edge 旗標。</span><span class="sxs-lookup"><span data-stu-id="40632-122">The current edge flag can be updated at any time.</span></span> <span data-ttu-id="40632-123">尤其是，在呼叫 [**glBegin**](/windows/desktop/OpenGL/glbegin)和對應的 [**glEnd**](/windows/desktop/OpenGL/glend)呼叫之間，可以呼叫 **glEdgeFlagv** 。</span><span class="sxs-lookup"><span data-stu-id="40632-123">In particular, **glEdgeFlagv** can be called between a call to [**glBegin**](/windows/desktop/OpenGL/glbegin) and the corresponding call to [**glEnd**](/windows/desktop/OpenGL/glend).</span></span>

<span data-ttu-id="40632-124">下列函式會取出與 **glEdgeFlagv** 相關的資訊：</span><span class="sxs-lookup"><span data-stu-id="40632-124">The following functions retrieve information related to **glEdgeFlagv**:</span></span>

<span data-ttu-id="40632-125">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) 與引數 GL \_ 邊緣 \_ 旗標</span><span class="sxs-lookup"><span data-stu-id="40632-125">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_EDGE\_FLAG</span></span>

## <a name="requirements"></a><span data-ttu-id="40632-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="40632-126">Requirements</span></span>



| <span data-ttu-id="40632-127">需求</span><span class="sxs-lookup"><span data-stu-id="40632-127">Requirement</span></span> | <span data-ttu-id="40632-128">值</span><span class="sxs-lookup"><span data-stu-id="40632-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="40632-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="40632-129">Minimum supported client</span></span><br/> | <span data-ttu-id="40632-130">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="40632-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="40632-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="40632-131">Minimum supported server</span></span><br/> | <span data-ttu-id="40632-132">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="40632-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="40632-133">標頭</span><span class="sxs-lookup"><span data-stu-id="40632-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="40632-134"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="40632-134"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="40632-135">程式庫</span><span class="sxs-lookup"><span data-stu-id="40632-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="40632-136"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="40632-136"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="40632-137">DLL</span><span class="sxs-lookup"><span data-stu-id="40632-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="40632-138"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40632-138"><dt>Opengl32.dll</dt></span></span> </dl> |



 

