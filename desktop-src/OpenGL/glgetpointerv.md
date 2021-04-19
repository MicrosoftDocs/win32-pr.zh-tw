---
title: 'glGetPointerv 函式 (Gl) '
description: GlGetPointerv 函數會傳回頂點資料陣列的位址。
ms.assetid: 6f85c508-9335-4474-8cc5-e67c7421a8e4
keywords:
- glGetPointerv 函式 OpenGL
topic_type:
- apiref
api_name:
- glGetPointerv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 569861922514af88835fbb4e313dab3286b7c47d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969190"
---
# <a name="glgetpointerv-function"></a><span data-ttu-id="a7cd7-104">glGetPointerv 函式</span><span class="sxs-lookup"><span data-stu-id="a7cd7-104">glGetPointerv function</span></span>

<span data-ttu-id="a7cd7-105">**GlGetPointerv** 函數會傳回頂點資料陣列的位址。</span><span class="sxs-lookup"><span data-stu-id="a7cd7-105">The **glGetPointerv** function returns the address of a vertex data array.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7cd7-106">語法</span><span class="sxs-lookup"><span data-stu-id="a7cd7-106">Syntax</span></span>


```C++
void WINAPI glGetPointerv(
   GLenum pname,
   GLvoid **params
);
```



## <a name="parameters"></a><span data-ttu-id="a7cd7-107">參數</span><span class="sxs-lookup"><span data-stu-id="a7cd7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7cd7-108">*pname*</span><span class="sxs-lookup"><span data-stu-id="a7cd7-108">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="a7cd7-109">要從下列符號常數傳回的陣列指標類型： GL \_ 色彩 \_ 陣列 \_ 指標、gl \_ EDGE 旗標 \_ \_ 陣列 \_ 指標、gl \_ 意見反應 \_ 緩衝區 \_ 指標、GL \_ 索引 \_ 陣列 \_ 指標、gl \_ 標準 \_ 陣列 \_ 指標、gl \_ 材質 \_ COORD \_ 陣列 \_ 指標、gl \_ 選取 \_ 緩衝區 \_ 指標，以及 gl \_ 頂點 \_ 陣列 \_ 指標。</span><span class="sxs-lookup"><span data-stu-id="a7cd7-109">The type of array pointer to return from the following symbolic constants: GL\_COLOR\_ARRAY\_POINTER, GL\_EDGE\_FLAG\_ARRAY\_POINTER, GL\_FEEDBACK\_BUFFER\_POINTER, GL\_INDEX\_ARRAY\_POINTER, GL\_NORMAL\_ARRAY\_POINTER, GL\_TEXTURE\_COORD\_ARRAY\_POINTER, GL\_SELECTION\_BUFFER\_POINTER, and GL\_VERTEX\_ARRAY\_POINTER.</span></span>

</dd> <dt>

<span data-ttu-id="a7cd7-110">*params*</span><span class="sxs-lookup"><span data-stu-id="a7cd7-110">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="a7cd7-111">傳回 *pname* 所指定陣列指標的值。</span><span class="sxs-lookup"><span data-stu-id="a7cd7-111">Returns the value of the array pointer specified by *pname*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7cd7-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="a7cd7-112">Return value</span></span>

<span data-ttu-id="a7cd7-113">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="a7cd7-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a7cd7-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="a7cd7-114">Error codes</span></span>

<span data-ttu-id="a7cd7-115">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="a7cd7-115">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="a7cd7-116">Name</span><span class="sxs-lookup"><span data-stu-id="a7cd7-116">Name</span></span>                                                                                             | <span data-ttu-id="a7cd7-117">意義</span><span class="sxs-lookup"><span data-stu-id="a7cd7-117">Meaning</span></span>                                       |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="a7cd7-118"><dt>**GL \_ 無效 \_ 列舉**</dt></span><span class="sxs-lookup"><span data-stu-id="a7cd7-118"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl> | <span data-ttu-id="a7cd7-119">*pname* 不是可接受的值。</span><span class="sxs-lookup"><span data-stu-id="a7cd7-119">*pname* was not an accepted value.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="a7cd7-120">備註</span><span class="sxs-lookup"><span data-stu-id="a7cd7-120">Remarks</span></span>

<span data-ttu-id="a7cd7-121">**GlGetPointerv** 函式會傳回陣列指標資訊。</span><span class="sxs-lookup"><span data-stu-id="a7cd7-121">The **glGetPointerv** function returns array pointer information.</span></span> <span data-ttu-id="a7cd7-122">*Pname* 參數是指定要傳回之陣列指標類型的符號常數，而 *params* 是指向放置傳回資料之位置的指標。</span><span class="sxs-lookup"><span data-stu-id="a7cd7-122">The *pname* parameter is a symbolic constant specifying the kind of array pointer to return, and *params* is a pointer to a location to place the returned data.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7cd7-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="a7cd7-123">Requirements</span></span>



| <span data-ttu-id="a7cd7-124">需求</span><span class="sxs-lookup"><span data-stu-id="a7cd7-124">Requirement</span></span> | <span data-ttu-id="a7cd7-125">值</span><span class="sxs-lookup"><span data-stu-id="a7cd7-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a7cd7-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a7cd7-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a7cd7-127">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a7cd7-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a7cd7-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a7cd7-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a7cd7-129">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a7cd7-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a7cd7-130">標頭</span><span class="sxs-lookup"><span data-stu-id="a7cd7-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7cd7-131"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="a7cd7-131"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="a7cd7-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="a7cd7-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="a7cd7-133"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a7cd7-133"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="a7cd7-134">DLL</span><span class="sxs-lookup"><span data-stu-id="a7cd7-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a7cd7-135"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a7cd7-135"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7cd7-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a7cd7-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7cd7-137">**glArrayElement**</span><span class="sxs-lookup"><span data-stu-id="a7cd7-137">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="a7cd7-138">**glColorPointer**</span><span class="sxs-lookup"><span data-stu-id="a7cd7-138">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="a7cd7-139">**glDrawArrays**</span><span class="sxs-lookup"><span data-stu-id="a7cd7-139">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="a7cd7-140">**glEdgeFlagPointer**</span><span class="sxs-lookup"><span data-stu-id="a7cd7-140">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="a7cd7-141">**glGetString**</span><span class="sxs-lookup"><span data-stu-id="a7cd7-141">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="a7cd7-142">**glIndexPointer**</span><span class="sxs-lookup"><span data-stu-id="a7cd7-142">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="a7cd7-143">**glNormalPointer**</span><span class="sxs-lookup"><span data-stu-id="a7cd7-143">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="a7cd7-144">**glTexCoordPointer**</span><span class="sxs-lookup"><span data-stu-id="a7cd7-144">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="a7cd7-145">**glVertexPointer**</span><span class="sxs-lookup"><span data-stu-id="a7cd7-145">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 





