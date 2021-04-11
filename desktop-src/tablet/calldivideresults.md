---
description: 從 InkDivider 物件取出分析結果。
ms.assetid: 7fc2bb5a-172f-4f4e-84dd-e31925f86982
title: CallDivideResults 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CallDivideResults
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: 11878e6a0ac953b9b7eb27ce21bb67001f9d88d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111704"
---
# <a name="calldivideresults-function"></a><span data-ttu-id="722c5-103">CallDivideResults 函式</span><span class="sxs-lookup"><span data-stu-id="722c5-103">CallDivideResults function</span></span>

<span data-ttu-id="722c5-104">從 [**InkDivider**](inkdivider-class.md) 物件取出分析結果。</span><span class="sxs-lookup"><span data-stu-id="722c5-104">Retrieves analysis results from the [**InkDivider**](inkdivider-class.md) object.</span></span>

<span data-ttu-id="722c5-105">此函式不適合應用程式程式碼使用。</span><span class="sxs-lookup"><span data-stu-id="722c5-105">This function is not intended to be used by application code.</span></span>

## <a name="syntax"></a><span data-ttu-id="722c5-106">語法</span><span class="sxs-lookup"><span data-stu-id="722c5-106">Syntax</span></span>


```C++
HRESULT WINAPI CallDivideResults(
  _In_  INT_PTR   hDivider,
  _Out_ int       aWordStrokeIds[],
  _Out_ int       aLineStrokeIds[],
  _Out_ int       aParagraphStrokeIds[],
  _Out_ int       aDrawingStrokeIds[],
  _Out_ SAFEARRAY **pastrWords,
  _Out_ SAFEARRAY **pastrLines,
  _Out_ SAFEARRAY **pastrParagraphs,
  _Out_ int       *aWordRotationCenterX,
  _Out_ int       *aWordRotationCenterY,
  _Out_ float     *aWordAngle,
  _Out_ int       *aLineRotationCenterX,
  _Out_ int       *aLineRotationCenterY,
  _Out_ float     *aLineAngle
);
```



## <a name="parameters"></a><span data-ttu-id="722c5-107">參數</span><span class="sxs-lookup"><span data-stu-id="722c5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="722c5-108">*hDivider* \[在\]</span><span class="sxs-lookup"><span data-stu-id="722c5-108">*hDivider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="722c5-109">[**InkDivider**](inkdivider-class.md)物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="722c5-109">A handle to the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="722c5-110">*aWordStrokeIds* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="722c5-110">*aWordStrokeIds* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="722c5-111">與傳遞給 [**InkDivider**](inkdivider-class.md) 類別的單字相關聯的識別碼陣列。</span><span class="sxs-lookup"><span data-stu-id="722c5-111">An array of identifiers associated with the word that is passed in to the [**InkDivider**](inkdivider-class.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="722c5-112">*aLineStrokeIds* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="722c5-112">*aLineStrokeIds* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="722c5-113">[**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)物件的 [**識別碼**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id)屬性陣列，這些物件與傳遞給 [**InkDivider**](inkdivider-class.md)類別的行相關聯。</span><span class="sxs-lookup"><span data-stu-id="722c5-113">An array of [**ID**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) properties for the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) objects associated with the line that is passed in to the [**InkDivider**](inkdivider-class.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="722c5-114">*aParagraphStrokeIds* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="722c5-114">*aParagraphStrokeIds* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="722c5-115">與 [**InkDivider**](inkdivider-class.md)類別中的段落相關聯之 [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)物件的 [**識別碼**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id)屬性陣列。</span><span class="sxs-lookup"><span data-stu-id="722c5-115">An array of the [**ID**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) properties for the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) objects associated with the paragraph from the [**InkDivider**](inkdivider-class.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="722c5-116">*aDrawingStrokeIds* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="722c5-116">*aDrawingStrokeIds* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="722c5-117">與 [**InkDivider**](inkdivider-class.md)類別中的繪圖相關聯之 [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)物件的 [**識別碼**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id)屬性陣列。</span><span class="sxs-lookup"><span data-stu-id="722c5-117">An array of [**ID**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) properties for the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) objects associated with the drawing from the [**InkDivider**](inkdivider-class.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="722c5-118">*pastrWords* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="722c5-118">*pastrWords* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="722c5-119">從筆墨分析傳回的單字陣列。</span><span class="sxs-lookup"><span data-stu-id="722c5-119">An array of words returned from ink analysis.</span></span>

</dd> <dt>

<span data-ttu-id="722c5-120">*pastrLines* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="722c5-120">*pastrLines* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="722c5-121">從筆墨分析傳回的行陣列。</span><span class="sxs-lookup"><span data-stu-id="722c5-121">An array of lines returned from ink analysis.</span></span>

</dd> <dt>

<span data-ttu-id="722c5-122">*pastrParagraphs* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="722c5-122">*pastrParagraphs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="722c5-123">從筆墨分析傳回的段落陣列。</span><span class="sxs-lookup"><span data-stu-id="722c5-123">An array of paragraphs returned from ink analysis.</span></span>

</dd> <dt>

<span data-ttu-id="722c5-124">*aWordRotationCenterX* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="722c5-124">*aWordRotationCenterX* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="722c5-125">從筆墨分析沿著 X 軸的單字中心點陣列。</span><span class="sxs-lookup"><span data-stu-id="722c5-125">An array of the center points of the words along the x-axis from ink analysis.</span></span>

</dd> <dt>

<span data-ttu-id="722c5-126">*aWordRotationCenterY* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="722c5-126">*aWordRotationCenterY* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="722c5-127">從筆墨分析沿著 y 軸的單字中心點陣列。</span><span class="sxs-lookup"><span data-stu-id="722c5-127">An array of the center points of the words along the y-axis from ink analysis.</span></span>

</dd> <dt>

<span data-ttu-id="722c5-128">*aWordAngle* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="722c5-128">*aWordAngle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="722c5-129">陣列，其中包含用來旋轉最佳分析結果之單字的角度。</span><span class="sxs-lookup"><span data-stu-id="722c5-129">An array containing the angles by which to rotate the words for best analysis results.</span></span>

</dd> <dt>

<span data-ttu-id="722c5-130">*aLineRotationCenterX* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="722c5-130">*aLineRotationCenterX* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="722c5-131">陣列，包含沿著 X 軸之線條的中心點。</span><span class="sxs-lookup"><span data-stu-id="722c5-131">An array containing the center points of the lines along the x-axis.</span></span>

</dd> <dt>

<span data-ttu-id="722c5-132">*aLineRotationCenterY* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="722c5-132">*aLineRotationCenterY* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="722c5-133">陣列，其中包含沿著 y 軸之線條的中心點。</span><span class="sxs-lookup"><span data-stu-id="722c5-133">An array containing the center points of the lines along the y-axis.</span></span>

</dd> <dt>

<span data-ttu-id="722c5-134">*aLineAngle* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="722c5-134">*aLineAngle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="722c5-135">陣列，其中包含用來旋轉最佳分析結果之線條的角度。</span><span class="sxs-lookup"><span data-stu-id="722c5-135">An array containing the angles by which to rotate the lines for best analysis results.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="722c5-136">傳回值</span><span class="sxs-lookup"><span data-stu-id="722c5-136">Return value</span></span>

<span data-ttu-id="722c5-137">此函數可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="722c5-137">This function can return one of these values.</span></span>



| <span data-ttu-id="722c5-138">傳回碼</span><span class="sxs-lookup"><span data-stu-id="722c5-138">Return code</span></span>                                                                                   | <span data-ttu-id="722c5-139">Description</span><span class="sxs-lookup"><span data-stu-id="722c5-139">Description</span></span>                                                       |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <span data-ttu-id="722c5-140"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="722c5-140"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="722c5-141">此函數已成功。</span><span class="sxs-lookup"><span data-stu-id="722c5-141">The function succeeded.</span></span><br/>                                |
| <dl> <span data-ttu-id="722c5-142"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="722c5-142"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="722c5-143">*HDivider* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="722c5-143">The *hDivider* parameter is invalid.</span></span><br/>                   |
| <dl> <span data-ttu-id="722c5-144"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="722c5-144"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="722c5-145">無法配置足夠的記憶體來儲存結果。</span><span class="sxs-lookup"><span data-stu-id="722c5-145">Could not allocate enough memory to store the results.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="722c5-146">備註</span><span class="sxs-lookup"><span data-stu-id="722c5-146">Remarks</span></span>

<span data-ttu-id="722c5-147">若要避免記憶體流失，您必須釋放 *pastrWords*、 *pastrLines* 和 *pastrParagraphs* 的資源。</span><span class="sxs-lookup"><span data-stu-id="722c5-147">To avoid memory leaks you must release the resources for *pastrWords*, *pastrLines*, and *pastrParagraphs*.</span></span>

## <a name="requirements"></a><span data-ttu-id="722c5-148">規格需求</span><span class="sxs-lookup"><span data-stu-id="722c5-148">Requirements</span></span>



| <span data-ttu-id="722c5-149">需求</span><span class="sxs-lookup"><span data-stu-id="722c5-149">Requirement</span></span> | <span data-ttu-id="722c5-150">值</span><span class="sxs-lookup"><span data-stu-id="722c5-150">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="722c5-151">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="722c5-151">Minimum supported client</span></span><br/> | <span data-ttu-id="722c5-152">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="722c5-152">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="722c5-153">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="722c5-153">Minimum supported server</span></span><br/> | <span data-ttu-id="722c5-154">都不支援</span><span class="sxs-lookup"><span data-stu-id="722c5-154">None supported</span></span><br/>                                                             |
| <span data-ttu-id="722c5-155">程式庫</span><span class="sxs-lookup"><span data-stu-id="722c5-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="722c5-156"><dt>InkDiv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="722c5-156"><dt>InkDiv.dll</dt></span></span> </dl> |



 

 




