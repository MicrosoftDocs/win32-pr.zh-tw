---
title: 'glTexCoord3iv 函式 (Gl) '
description: '設定目前的材質座標。 |glTexCoord3iv 函式 (Gl) '
ms.assetid: 1d2f551a-d920-4020-bd51-bff28af83d44
keywords:
- glTexCoord3iv 函式 OpenGL
topic_type:
- apiref
api_name:
- glTexCoord3iv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eef681a41b39ad1cafff1b4a23e4b814dfaab8a7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106981779"
---
# <a name="gltexcoord3iv-function"></a><span data-ttu-id="6c6a0-105">glTexCoord3iv 函式</span><span class="sxs-lookup"><span data-stu-id="6c6a0-105">glTexCoord3iv function</span></span>

<span data-ttu-id="6c6a0-106">設定目前的材質座標。</span><span class="sxs-lookup"><span data-stu-id="6c6a0-106">Sets the current texture coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c6a0-107">語法</span><span class="sxs-lookup"><span data-stu-id="6c6a0-107">Syntax</span></span>


```C++
void WINAPI glTexCoord3iv(
   const GLint *v
);
```



## <a name="parameters"></a><span data-ttu-id="6c6a0-108">參數</span><span class="sxs-lookup"><span data-stu-id="6c6a0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c6a0-109">*V*</span><span class="sxs-lookup"><span data-stu-id="6c6a0-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="6c6a0-110">指標，指向三個元素的陣列，接著指定 s、t 和 r 材質座標。</span><span class="sxs-lookup"><span data-stu-id="6c6a0-110">A pointer to an array of three elements, which in turn specifies the s, t, and r texture coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c6a0-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="6c6a0-111">Return value</span></span>

<span data-ttu-id="6c6a0-112">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="6c6a0-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c6a0-113">備註</span><span class="sxs-lookup"><span data-stu-id="6c6a0-113">Remarks</span></span>

<span data-ttu-id="6c6a0-114">[**GlTexCoord**](gltexcoord-functions.md)函式會將目前的材質座標設定為與多邊形頂點相關聯之資料的一部分。</span><span class="sxs-lookup"><span data-stu-id="6c6a0-114">The [**glTexCoord**](gltexcoord-functions.md) function sets the current texture coordinates that are part of the data associated with polygon vertices.</span></span> <span data-ttu-id="6c6a0-115">**GlTexCoord** 函數會指定一、二、三或四個維度中的材質座標。</span><span class="sxs-lookup"><span data-stu-id="6c6a0-115">The **glTexCoord** function specifies texture coordinates in one, two, three, or four dimensions.</span></span> <span data-ttu-id="6c6a0-116">GlTexCoord1 函式會將目前的材質座標設定為 (s、0、0、1) ;對 glTexCoord2 的呼叫會將它們設定為 (s、t、0、1) 。</span><span class="sxs-lookup"><span data-stu-id="6c6a0-116">The glTexCoord1 function sets the current texture coordinates to (s, 0, 0, 1); a call to glTexCoord2 sets them to (s, t, 0, 1).</span></span> <span data-ttu-id="6c6a0-117">同樣地，glTexCoord3 會將材質座標指定為 (s、t、r、1) ，而 glTexCoord4 會將所有四個元件明確定義為 (s、t、r、q) 。</span><span class="sxs-lookup"><span data-stu-id="6c6a0-117">Similarly, glTexCoord3 specifies the texture coordinates as (s, t, r, 1), and glTexCoord4 defines all four components explicitly as (s, t, r, q).</span></span> <span data-ttu-id="6c6a0-118">您可以隨時更新目前的材質座標。</span><span class="sxs-lookup"><span data-stu-id="6c6a0-118">You can update the current texture coordinates at any time.</span></span> <span data-ttu-id="6c6a0-119">尤其是，您可以呼叫 [**glBegin**](glbegin.md) 的呼叫與 [**glEnd**](glend.md)的對應呼叫之間的 glTexCoord。</span><span class="sxs-lookup"><span data-stu-id="6c6a0-119">In particular, you can call glTexCoord between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="6c6a0-120">下列函式會抓取 **glTexCoord** 的相關資訊：</span><span class="sxs-lookup"><span data-stu-id="6c6a0-120">The following function retrieves information related to **glTexCoord**:</span></span>

<span data-ttu-id="6c6a0-121">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 目前 \_ 材質 \_ COORDS 的 glGet</span><span class="sxs-lookup"><span data-stu-id="6c6a0-121">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_TEXTURE\_COORDS</span></span>

## <a name="requirements"></a><span data-ttu-id="6c6a0-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="6c6a0-122">Requirements</span></span>



| <span data-ttu-id="6c6a0-123">需求</span><span class="sxs-lookup"><span data-stu-id="6c6a0-123">Requirement</span></span> | <span data-ttu-id="6c6a0-124">值</span><span class="sxs-lookup"><span data-stu-id="6c6a0-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6c6a0-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6c6a0-125">Minimum supported client</span></span><br/> | <span data-ttu-id="6c6a0-126">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6c6a0-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="6c6a0-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6c6a0-127">Minimum supported server</span></span><br/> | <span data-ttu-id="6c6a0-128">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6c6a0-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6c6a0-129">標頭</span><span class="sxs-lookup"><span data-stu-id="6c6a0-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c6a0-130"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="6c6a0-130"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="6c6a0-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="6c6a0-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="6c6a0-132"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="6c6a0-132"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="6c6a0-133">DLL</span><span class="sxs-lookup"><span data-stu-id="6c6a0-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6c6a0-134"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c6a0-134"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c6a0-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6c6a0-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c6a0-136">glVertex</span><span class="sxs-lookup"><span data-stu-id="6c6a0-136">glVertex</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





