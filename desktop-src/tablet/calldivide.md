---
description: 從 InkDivider 物件中取出分析資訊。
ms.assetid: 1b073da4-80f4-48f4-8ff6-b21793c173a8
title: CallDivide 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CallDivide
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: 0084811ee471bee8fe67653dace49fa83642a7fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510762"
---
# <a name="calldivide-function"></a><span data-ttu-id="c1cd2-103">CallDivide 函式</span><span class="sxs-lookup"><span data-stu-id="c1cd2-103">CallDivide function</span></span>

<span data-ttu-id="c1cd2-104">從 [**InkDivider**](inkdivider-class.md) 物件中取出分析資訊。</span><span class="sxs-lookup"><span data-stu-id="c1cd2-104">Retrieves analysis information from the [**InkDivider**](inkdivider-class.md) object.</span></span>

<span data-ttu-id="c1cd2-105">此函式不適合應用程式程式碼使用。</span><span class="sxs-lookup"><span data-stu-id="c1cd2-105">This function is not intended to be used by application code.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1cd2-106">語法</span><span class="sxs-lookup"><span data-stu-id="c1cd2-106">Syntax</span></span>


```C++
HRESULT WINAPI CallDivide(
  _In_  INT_PTR hDivider,
  _In_  int     *pWordSize,
  _In_  int     *pLineSize,
  _In_  int     *pParagraphSize,
  _In_  int     *pDrawingSize,
  _Out_ int     *pWordCount,
  _Out_ int     *pLineCount,
  _Out_ int     *pParagraphCount
);
```



## <a name="parameters"></a><span data-ttu-id="c1cd2-107">參數</span><span class="sxs-lookup"><span data-stu-id="c1cd2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1cd2-108">*hDivider* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c1cd2-108">*hDivider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1cd2-109">[**InkDivider**](inkdivider-class.md)物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="c1cd2-109">A handle to the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="c1cd2-110">*pWordSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c1cd2-110">*pWordSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1cd2-111">[**InkDivider**](inkdivider-class.md)物件所傳回的單字大小。</span><span class="sxs-lookup"><span data-stu-id="c1cd2-111">The size of the word returned by the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="c1cd2-112">*pLineSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c1cd2-112">*pLineSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1cd2-113">[**InkDivider**](inkdivider-class.md)物件所傳回的行大小。</span><span class="sxs-lookup"><span data-stu-id="c1cd2-113">The size of the line returned by the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="c1cd2-114">*pParagraphSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c1cd2-114">*pParagraphSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1cd2-115">[**InkDivider**](inkdivider-class.md)物件所傳回之段落的大小。</span><span class="sxs-lookup"><span data-stu-id="c1cd2-115">The size of the paragraph returned by the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="c1cd2-116">*pDrawingSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c1cd2-116">*pDrawingSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1cd2-117">[**InkDivider**](inkdivider-class.md)物件所傳回之繪圖的大小。</span><span class="sxs-lookup"><span data-stu-id="c1cd2-117">The size of the drawing returned by the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="c1cd2-118">*pWordCount* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c1cd2-118">*pWordCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c1cd2-119">筆墨分析所傳回的文字數目。</span><span class="sxs-lookup"><span data-stu-id="c1cd2-119">The number of words returned by ink analysis.</span></span>

</dd> <dt>

<span data-ttu-id="c1cd2-120">*pLineCount* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c1cd2-120">*pLineCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c1cd2-121">筆墨分析所傳回的行數。</span><span class="sxs-lookup"><span data-stu-id="c1cd2-121">The number of lines returned by ink analysis.</span></span>

</dd> <dt>

<span data-ttu-id="c1cd2-122">*pParagraphCount* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c1cd2-122">*pParagraphCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c1cd2-123">筆墨分析傳回的段落數目。</span><span class="sxs-lookup"><span data-stu-id="c1cd2-123">The number of paragraphs returned by ink analysis.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1cd2-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="c1cd2-124">Return value</span></span>

<span data-ttu-id="c1cd2-125">此函數可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="c1cd2-125">This function can return one of these values.</span></span>



| <span data-ttu-id="c1cd2-126">傳回碼</span><span class="sxs-lookup"><span data-stu-id="c1cd2-126">Return code</span></span>                                                                                  | <span data-ttu-id="c1cd2-127">Description</span><span class="sxs-lookup"><span data-stu-id="c1cd2-127">Description</span></span>                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="c1cd2-128"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="c1cd2-128"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="c1cd2-129">函數成功。</span><span class="sxs-lookup"><span data-stu-id="c1cd2-129">The function suceeded.</span></span><br/>              |
| <dl> <span data-ttu-id="c1cd2-130"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="c1cd2-130"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="c1cd2-131">一或多個參數無效。</span><span class="sxs-lookup"><span data-stu-id="c1cd2-131">One or more parameters are invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c1cd2-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="c1cd2-132">Requirements</span></span>



| <span data-ttu-id="c1cd2-133">需求</span><span class="sxs-lookup"><span data-stu-id="c1cd2-133">Requirement</span></span> | <span data-ttu-id="c1cd2-134">值</span><span class="sxs-lookup"><span data-stu-id="c1cd2-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c1cd2-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c1cd2-135">Minimum supported client</span></span><br/> | <span data-ttu-id="c1cd2-136">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c1cd2-136">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="c1cd2-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c1cd2-137">Minimum supported server</span></span><br/> | <span data-ttu-id="c1cd2-138">都不支援</span><span class="sxs-lookup"><span data-stu-id="c1cd2-138">None supported</span></span><br/>                                                             |
| <span data-ttu-id="c1cd2-139">程式庫</span><span class="sxs-lookup"><span data-stu-id="c1cd2-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="c1cd2-140"><dt>InkDiv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c1cd2-140"><dt>InkDiv.dll</dt></span></span> </dl> |



 

 




