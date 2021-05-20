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
ms.openlocfilehash: 1bf07fea583c5ae46680d888f6bf6c0a9c5aa9a0
ms.sourcegitcommit: 88049609e29f91a42442235885abf56f598b06b3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/19/2021
ms.locfileid: "110153551"
---
# <a name="gluortho2d-function"></a><span data-ttu-id="0c84f-104">gluOrtho2D 函式</span><span class="sxs-lookup"><span data-stu-id="0c84f-104">gluOrtho2D function</span></span>

<span data-ttu-id="0c84f-105">**GluOrtho2D** 函式會定義2d 正向投射矩陣。</span><span class="sxs-lookup"><span data-stu-id="0c84f-105">The **gluOrtho2D** function defines a 2-D orthographic projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c84f-106">語法</span><span class="sxs-lookup"><span data-stu-id="0c84f-106">Syntax</span></span>


```C++
void WINAPI gluOrtho2D(
   GLdouble left,
   GLdouble right,
   GLdouble top,
   GLdouble bottom
);
```



## <a name="parameters"></a><span data-ttu-id="0c84f-107">參數</span><span class="sxs-lookup"><span data-stu-id="0c84f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c84f-108">*離開*</span><span class="sxs-lookup"><span data-stu-id="0c84f-108">*left*</span></span> 
</dt> <dd>

<span data-ttu-id="0c84f-109">左方垂直裁剪平面的座標。</span><span class="sxs-lookup"><span data-stu-id="0c84f-109">The coordinate for the left vertical clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="0c84f-110">*對*</span><span class="sxs-lookup"><span data-stu-id="0c84f-110">*right*</span></span> 
</dt> <dd>

<span data-ttu-id="0c84f-111">右垂直裁剪平面的座標。</span><span class="sxs-lookup"><span data-stu-id="0c84f-111">The coordinate for the right vertical clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="0c84f-112">*top*</span><span class="sxs-lookup"><span data-stu-id="0c84f-112">*top*</span></span> 
</dt> <dd>

<span data-ttu-id="0c84f-113">上方水準裁剪平面的座標。</span><span class="sxs-lookup"><span data-stu-id="0c84f-113">The coordinate for the top horizontal clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="0c84f-114">*底部*</span><span class="sxs-lookup"><span data-stu-id="0c84f-114">*bottom*</span></span> 
</dt> <dd>

<span data-ttu-id="0c84f-115">底部水準裁剪平面的座標。</span><span class="sxs-lookup"><span data-stu-id="0c84f-115">The coordinate for the bottom horizontal clipping plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c84f-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="0c84f-116">Return value</span></span>

<span data-ttu-id="0c84f-117">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="0c84f-117">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0c84f-118">備註</span><span class="sxs-lookup"><span data-stu-id="0c84f-118">Remarks</span></span>

<span data-ttu-id="0c84f-119">**GluOrtho2D** 函式會設定二維正交的視圖區域。</span><span class="sxs-lookup"><span data-stu-id="0c84f-119">The **gluOrtho2D** function sets up a two-dimensional orthographic viewing region.</span></span> <span data-ttu-id="0c84f-120">這相當於呼叫 [**glOrtho**](glortho.md) 搭配 zNear =-1 和 zFar = 1。</span><span class="sxs-lookup"><span data-stu-id="0c84f-120">This is equivalent to calling [**glOrtho**](glortho.md) with zNear = -1 and zFar = 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c84f-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="0c84f-121">Requirements</span></span>



| <span data-ttu-id="0c84f-122">需求</span><span class="sxs-lookup"><span data-stu-id="0c84f-122">Requirement</span></span> | <span data-ttu-id="0c84f-123">值</span><span class="sxs-lookup"><span data-stu-id="0c84f-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0c84f-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0c84f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="0c84f-125">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0c84f-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="0c84f-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0c84f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="0c84f-127">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0c84f-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="0c84f-128">標頭</span><span class="sxs-lookup"><span data-stu-id="0c84f-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c84f-129"><dt>X.glu 隊。h</dt></span><span class="sxs-lookup"><span data-stu-id="0c84f-129"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="0c84f-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="0c84f-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="0c84f-131"><dt>Glu32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="0c84f-131"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="0c84f-132">DLL</span><span class="sxs-lookup"><span data-stu-id="0c84f-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0c84f-133"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0c84f-133"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c84f-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0c84f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c84f-135">**glOrtho**</span><span class="sxs-lookup"><span data-stu-id="0c84f-135">**glOrtho**</span></span>](glortho.md)
</dt> <dt>

[<span data-ttu-id="0c84f-136">**gluPerspective**</span><span class="sxs-lookup"><span data-stu-id="0c84f-136">**gluPerspective**</span></span>](gluperspective.md)
</dt> </dl>

 

 





