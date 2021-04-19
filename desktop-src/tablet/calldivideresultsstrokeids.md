---
description: 抓取筆墨分析所決定之對應單字、線條、段落或繪圖的 IInkStrokeDisp 物件的識別碼屬性。
ms.assetid: f05ffa3b-2a47-46fe-bb8f-e682aa094b69
title: CallDivideResultsStrokeIds 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CallDivideResultsStrokeIds
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: ee690c9564df3b8c75eca6eec8eeb88b7531f4ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970553"
---
# <a name="calldivideresultsstrokeids-function"></a><span data-ttu-id="e9d91-103">CallDivideResultsStrokeIds 函式</span><span class="sxs-lookup"><span data-stu-id="e9d91-103">CallDivideResultsStrokeIds function</span></span>

<span data-ttu-id="e9d91-104">抓取筆墨分析所決定之對應單字、線條、段落或繪圖的 [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)物件的 [**識別碼**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id)屬性。</span><span class="sxs-lookup"><span data-stu-id="e9d91-104">Retrieves the [**Id**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) properties for the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) objects of the corresponding word, line, paragraph, or drawing determined by ink analysis.</span></span>

<span data-ttu-id="e9d91-105">此函式不適合應用程式程式碼使用。</span><span class="sxs-lookup"><span data-stu-id="e9d91-105">This function is not intended to be used by application code.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9d91-106">語法</span><span class="sxs-lookup"><span data-stu-id="e9d91-106">Syntax</span></span>


```C++
HRESULT WINAPI CallDivideResultsStrokeIds(
  _In_  INT_PTR hDivider,
  _Out_ int     aWordStrokeIds[],
  _Out_ int     aLineStrokeIds[],
  _Out_ int     aParagraphStrokeIds[],
  _Out_ int     aDrawingStrokeIds[]
);
```



## <a name="parameters"></a><span data-ttu-id="e9d91-107">參數</span><span class="sxs-lookup"><span data-stu-id="e9d91-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9d91-108">*hDivider* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e9d91-108">*hDivider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9d91-109">[分隔](the-divider-object.md)物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="e9d91-109">A handle to the [Divider](the-divider-object.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="e9d91-110">*\[ aWordStrokeIds \]*\[out\]</span><span class="sxs-lookup"><span data-stu-id="e9d91-110">*aWordStrokeIds\[\]* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e9d91-111">單字中筆墨的筆觸識別碼陣列。</span><span class="sxs-lookup"><span data-stu-id="e9d91-111">An array of the stroke IDs of the ink in the word.</span></span>

</dd> <dt>

<span data-ttu-id="e9d91-112">*\[ aLineStrokeIds \]*\[out\]</span><span class="sxs-lookup"><span data-stu-id="e9d91-112">*aLineStrokeIds\[\]* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e9d91-113">線條中筆墨的筆觸識別碼陣列。</span><span class="sxs-lookup"><span data-stu-id="e9d91-113">An array of the stroke IDs of the ink in the line.</span></span>

</dd> <dt>

<span data-ttu-id="e9d91-114">*\[ aParagraphStrokeIds \]*\[out\]</span><span class="sxs-lookup"><span data-stu-id="e9d91-114">*aParagraphStrokeIds\[\]* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e9d91-115">段落中筆墨的筆觸識別碼陣列。</span><span class="sxs-lookup"><span data-stu-id="e9d91-115">An array of the stroke IDs of the ink in the paragraph.</span></span>

</dd> <dt>

<span data-ttu-id="e9d91-116">*\[ aDrawingStrokeIds \]*\[out\]</span><span class="sxs-lookup"><span data-stu-id="e9d91-116">*aDrawingStrokeIds\[\]* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e9d91-117">繪圖中筆墨的筆觸識別碼陣列。</span><span class="sxs-lookup"><span data-stu-id="e9d91-117">An array of the stroke IDs of the ink in the drawing.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9d91-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="e9d91-118">Return value</span></span>

<span data-ttu-id="e9d91-119">此函數可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="e9d91-119">This function can return one of these values.</span></span>



| <span data-ttu-id="e9d91-120">傳回碼</span><span class="sxs-lookup"><span data-stu-id="e9d91-120">Return code</span></span>                                                                                  | <span data-ttu-id="e9d91-121">Description</span><span class="sxs-lookup"><span data-stu-id="e9d91-121">Description</span></span>                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="e9d91-122"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="e9d91-122"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="e9d91-123">此函數已成功。</span><span class="sxs-lookup"><span data-stu-id="e9d91-123">The function succeeded.</span></span><br/>              |
| <dl> <span data-ttu-id="e9d91-124"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="e9d91-124"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="e9d91-125">*HDivider* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="e9d91-125">The *hDivider* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e9d91-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="e9d91-126">Requirements</span></span>



| <span data-ttu-id="e9d91-127">需求</span><span class="sxs-lookup"><span data-stu-id="e9d91-127">Requirement</span></span> | <span data-ttu-id="e9d91-128">值</span><span class="sxs-lookup"><span data-stu-id="e9d91-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e9d91-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e9d91-129">Minimum supported client</span></span><br/> | <span data-ttu-id="e9d91-130">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e9d91-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="e9d91-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e9d91-131">Minimum supported server</span></span><br/> | <span data-ttu-id="e9d91-132">都不支援</span><span class="sxs-lookup"><span data-stu-id="e9d91-132">None supported</span></span><br/>                                                             |
| <span data-ttu-id="e9d91-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="e9d91-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="e9d91-134"><dt>InkDiv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9d91-134"><dt>InkDiv.dll</dt></span></span> </dl> |



 

 




