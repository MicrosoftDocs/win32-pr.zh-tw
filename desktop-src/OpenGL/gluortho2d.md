---
title: 'gluOrtho2D 函式 (X.glu 隊) '
description: GluOrtho2D 函式會定義2D 正向投射矩陣。
ms.assetid: ba83fb5c-e5c7-4486-a815-a1aff0469757
keywords:
- gluOrtho2D 函式 OpenGL
topic_type:
- apiref
api_name:
- gluOrtho2D
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a36b321f312a074a5dd78340968f1c9b2b844c6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383834"
---
# <a name="gluortho2d-function"></a><span data-ttu-id="cbc48-104">gluOrtho2D 函式</span><span class="sxs-lookup"><span data-stu-id="cbc48-104">gluOrtho2D function</span></span>

<span data-ttu-id="cbc48-105">**GluOrtho2D** 函式會定義2d 正向投射矩陣。</span><span class="sxs-lookup"><span data-stu-id="cbc48-105">The **gluOrtho2D** function defines a 2-D orthographic projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbc48-106">語法</span><span class="sxs-lookup"><span data-stu-id="cbc48-106">Syntax</span></span>


```C++
void WINAPI gluOrtho2D(
   GLdouble left,
   GLdouble right,
   GLdouble top,
   GLdouble bottom
);
```



## <a name="parameters"></a><span data-ttu-id="cbc48-107">參數</span><span class="sxs-lookup"><span data-stu-id="cbc48-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cbc48-108">*離開*</span><span class="sxs-lookup"><span data-stu-id="cbc48-108">*left*</span></span> 
</dt> <dd>

<span data-ttu-id="cbc48-109">左方垂直裁剪平面的座標。</span><span class="sxs-lookup"><span data-stu-id="cbc48-109">The coordinate for the left vertical clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="cbc48-110">*對*</span><span class="sxs-lookup"><span data-stu-id="cbc48-110">*right*</span></span> 
</dt> <dd>

<span data-ttu-id="cbc48-111">右垂直裁剪平面的座標。</span><span class="sxs-lookup"><span data-stu-id="cbc48-111">The coordinate for the right vertical clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="cbc48-112">*top*</span><span class="sxs-lookup"><span data-stu-id="cbc48-112">*top*</span></span> 
</dt> <dd>

<span data-ttu-id="cbc48-113">上方水準裁剪平面的座標。</span><span class="sxs-lookup"><span data-stu-id="cbc48-113">The coordinate for the top horizontal clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="cbc48-114">*底部*</span><span class="sxs-lookup"><span data-stu-id="cbc48-114">*bottom*</span></span> 
</dt> <dd>

<span data-ttu-id="cbc48-115">底部水準裁剪平面的座標。</span><span class="sxs-lookup"><span data-stu-id="cbc48-115">The coordinate for the bottom horizontal clipping plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cbc48-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="cbc48-116">Return value</span></span>

<span data-ttu-id="cbc48-117">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="cbc48-117">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cbc48-118">備註</span><span class="sxs-lookup"><span data-stu-id="cbc48-118">Remarks</span></span>

<span data-ttu-id="cbc48-119">**GluOrtho2D** 函式會設定二維正交的視圖區域。</span><span class="sxs-lookup"><span data-stu-id="cbc48-119">The **gluOrtho2D** function sets up a two-dimensional orthographic viewing region.</span></span> <span data-ttu-id="cbc48-120">這相當於使用 near = 1 和 far = 1 呼叫 [**glOrtho**](glortho.md) 。</span><span class="sxs-lookup"><span data-stu-id="cbc48-120">This is equivalent to calling [**glOrtho**](glortho.md) with near =  1 and far = 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="cbc48-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="cbc48-121">Requirements</span></span>



| <span data-ttu-id="cbc48-122">需求</span><span class="sxs-lookup"><span data-stu-id="cbc48-122">Requirement</span></span> | <span data-ttu-id="cbc48-123">值</span><span class="sxs-lookup"><span data-stu-id="cbc48-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cbc48-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cbc48-124">Minimum supported client</span></span><br/> | <span data-ttu-id="cbc48-125">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cbc48-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="cbc48-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cbc48-126">Minimum supported server</span></span><br/> | <span data-ttu-id="cbc48-127">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cbc48-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="cbc48-128">標頭</span><span class="sxs-lookup"><span data-stu-id="cbc48-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="cbc48-129"><dt>X.glu 隊。h</dt></span><span class="sxs-lookup"><span data-stu-id="cbc48-129"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="cbc48-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="cbc48-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="cbc48-131"><dt>Glu32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="cbc48-131"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="cbc48-132">DLL</span><span class="sxs-lookup"><span data-stu-id="cbc48-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cbc48-133"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cbc48-133"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cbc48-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cbc48-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbc48-135">**glOrtho**</span><span class="sxs-lookup"><span data-stu-id="cbc48-135">**glOrtho**</span></span>](glortho.md)
</dt> <dt>

[<span data-ttu-id="cbc48-136">**gluPerspective**</span><span class="sxs-lookup"><span data-stu-id="cbc48-136">**gluPerspective**</span></span>](gluperspective.md)
</dt> </dl>

 

 





