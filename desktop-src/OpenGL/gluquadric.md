---
title: 'gluQuadricCallback 函式 (X.glu 隊) '
description: GluQuadricCallback 函數會定義 quadric 物件的回呼。
ms.assetid: 1f1e9fe9-7239-419c-92b6-af2534850ac5
keywords:
- gluQuadricCallback 函式 OpenGL
topic_type:
- apiref
api_name:
- gluQuadricCallback
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c0c92e3cd4e723b59ee9060c5e2f33b710e7f69
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508999"
---
# <a name="gluquadriccallback-function"></a><span data-ttu-id="2c293-104">gluQuadricCallback 函式</span><span class="sxs-lookup"><span data-stu-id="2c293-104">gluQuadricCallback function</span></span>

<span data-ttu-id="2c293-105">**GluQuadricCallback** 函數會定義 quadric 物件的回呼。</span><span class="sxs-lookup"><span data-stu-id="2c293-105">The **gluQuadricCallback** function defines a callback for a quadric object.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c293-106">語法</span><span class="sxs-lookup"><span data-stu-id="2c293-106">Syntax</span></span>


```C++
void WINAPI gluQuadricCallback(
   GLUquadric *qobj,
   GLenum     which,
   void (CALLBACK *fn)()
);
```



## <a name="parameters"></a><span data-ttu-id="2c293-107">參數</span><span class="sxs-lookup"><span data-stu-id="2c293-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c293-108">*qobj*</span><span class="sxs-lookup"><span data-stu-id="2c293-108">*qobj*</span></span> 
</dt> <dd>

<span data-ttu-id="2c293-109">Quadric 物件 (使用 [**gluNewQuadric**](glunewquadric.md)) 建立。</span><span class="sxs-lookup"><span data-stu-id="2c293-109">The quadric object (created with [**gluNewQuadric**](glunewquadric.md)).</span></span>

</dd> <dt>

<span data-ttu-id="2c293-110">*頻率*</span><span class="sxs-lookup"><span data-stu-id="2c293-110">*which*</span></span> 
</dt> <dd>

<span data-ttu-id="2c293-111">要定義的回呼。</span><span class="sxs-lookup"><span data-stu-id="2c293-111">The callback being defined.</span></span> <span data-ttu-id="2c293-112">唯一有效的值為 X.GLU 隊 \_ 錯誤。</span><span class="sxs-lookup"><span data-stu-id="2c293-112">The only valid value is GLU\_ERROR.</span></span>



| <span data-ttu-id="2c293-113">值</span><span class="sxs-lookup"><span data-stu-id="2c293-113">Value</span></span>                                                                                                                                             | <span data-ttu-id="2c293-114">意義</span><span class="sxs-lookup"><span data-stu-id="2c293-114">Meaning</span></span>                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_ERROR"></span><span id="glu_error"></span><dl> <span data-ttu-id="2c293-115"><dt>**X.GLU 隊 \_ 錯誤**</dt></span><span class="sxs-lookup"><span data-stu-id="2c293-115"><dt>**GLU\_ERROR**</dt></span></span> </dl> | <span data-ttu-id="2c293-116">遇到錯誤時，會呼叫 **gluQuadricCallback** 函數。</span><span class="sxs-lookup"><span data-stu-id="2c293-116">The **gluQuadricCallback** function is called when an error is encountered.</span></span> <span data-ttu-id="2c293-117">其單一引數的類型為 **GLenum**，它會指出發生的特定錯誤。</span><span class="sxs-lookup"><span data-stu-id="2c293-117">Its single argument is of type **GLenum**, and it indicates the specific error that occurred.</span></span> <span data-ttu-id="2c293-118">描述這些錯誤的字元字串可以使用 [**gluErrorString**](gluerrorstring.md) 呼叫來抓取。</span><span class="sxs-lookup"><span data-stu-id="2c293-118">Character strings describing these errors can be retrieved with the [**gluErrorString**](gluerrorstring.md) call.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2c293-119">*Fn*</span><span class="sxs-lookup"><span data-stu-id="2c293-119">*fn*</span></span> 
</dt> <dd>

<span data-ttu-id="2c293-120">要呼叫的函式。</span><span class="sxs-lookup"><span data-stu-id="2c293-120">The function to be called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c293-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="2c293-121">Return value</span></span>

<span data-ttu-id="2c293-122">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="2c293-122">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c293-123">備註</span><span class="sxs-lookup"><span data-stu-id="2c293-123">Remarks</span></span>

<span data-ttu-id="2c293-124">使用 **gluQuadricCallback** 來定義 quadric 物件所要使用的新回呼。</span><span class="sxs-lookup"><span data-stu-id="2c293-124">Use **gluQuadricCallback** to define a new callback to be used by a quadric object.</span></span> <span data-ttu-id="2c293-125">如果已定義指定的回呼，則會予以取代。</span><span class="sxs-lookup"><span data-stu-id="2c293-125">If the specified callback is already defined, it is replaced.</span></span> <span data-ttu-id="2c293-126">如果 *fn* 為 **Null**，則會清除任何現有的回呼。</span><span class="sxs-lookup"><span data-stu-id="2c293-126">If *fn* is **NULL**, any existing callback is erased.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c293-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="2c293-127">Requirements</span></span>



| <span data-ttu-id="2c293-128">需求</span><span class="sxs-lookup"><span data-stu-id="2c293-128">Requirement</span></span> | <span data-ttu-id="2c293-129">值</span><span class="sxs-lookup"><span data-stu-id="2c293-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2c293-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2c293-130">Minimum supported client</span></span><br/> | <span data-ttu-id="2c293-131">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2c293-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="2c293-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2c293-132">Minimum supported server</span></span><br/> | <span data-ttu-id="2c293-133">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2c293-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="2c293-134">標頭</span><span class="sxs-lookup"><span data-stu-id="2c293-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c293-135"><dt>X.glu 隊。h</dt></span><span class="sxs-lookup"><span data-stu-id="2c293-135"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="2c293-136">程式庫</span><span class="sxs-lookup"><span data-stu-id="2c293-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="2c293-137"><dt>Glu32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="2c293-137"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="2c293-138">DLL</span><span class="sxs-lookup"><span data-stu-id="2c293-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c293-139"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c293-139"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c293-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2c293-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c293-141">**gluErrorString**</span><span class="sxs-lookup"><span data-stu-id="2c293-141">**gluErrorString**</span></span>](gluerrorstring.md)
</dt> <dt>

[<span data-ttu-id="2c293-142">**gluNewQuadric**</span><span class="sxs-lookup"><span data-stu-id="2c293-142">**gluNewQuadric**</span></span>](glunewquadric.md)
</dt> </dl>

 

 





