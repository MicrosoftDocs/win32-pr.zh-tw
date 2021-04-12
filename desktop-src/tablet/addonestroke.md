---
description: 將新的 IInkStrokeDisp 物件加入至傳入的 InkDivider 物件。
ms.assetid: d5b82244-68d5-4137-aaf4-d3232f7c0779
title: AddOneStroke 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddOneStroke
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: 0af3913f2579363afbb0c3985ad0f40f58051eac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468585"
---
# <a name="addonestroke-function"></a><span data-ttu-id="e3073-103">AddOneStroke 函式</span><span class="sxs-lookup"><span data-stu-id="e3073-103">AddOneStroke function</span></span>

<span data-ttu-id="e3073-104">將新的 [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) 物件加入至傳入的 [**InkDivider**](inkdivider-class.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="e3073-104">Adds a new [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object to the [**InkDivider**](inkdivider-class.md) object that was passed in.</span></span>

<span data-ttu-id="e3073-105">此函式不適合應用程式程式碼使用。</span><span class="sxs-lookup"><span data-stu-id="e3073-105">This function is not intended to be used by application code.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3073-106">語法</span><span class="sxs-lookup"><span data-stu-id="e3073-106">Syntax</span></span>


```C++
HRESULT WINAPI AddOneStroke(
  _In_ INT_PTR hDivider,
  _In_ int     strokeId,
  _In_ int     cPoints,
  _In_ POINT   *aPoints
);
```



## <a name="parameters"></a><span data-ttu-id="e3073-107">參數</span><span class="sxs-lookup"><span data-stu-id="e3073-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3073-108">*hDivider* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e3073-108">*hDivider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3073-109">[**InkDivider**](inkdivider-class.md)物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="e3073-109">A handle to the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="e3073-110">*strokeId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e3073-110">*strokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3073-111">要加入至 [**InkDivider**](inkdivider-class.md)物件之 [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)物件的 [**識別碼**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id)。</span><span class="sxs-lookup"><span data-stu-id="e3073-111">The [**Id**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) of the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object to be added to the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="e3073-112">*cPoints* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e3073-112">*cPoints* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3073-113">組成新 [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) 物件的封包數目。</span><span class="sxs-lookup"><span data-stu-id="e3073-113">The number of packets that make up the new [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object.</span></span>

</dd> <dt>

<span data-ttu-id="e3073-114">*aPoints* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e3073-114">*aPoints* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3073-115">組成 *strokeId* 中 [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)物件的封包陣列。</span><span class="sxs-lookup"><span data-stu-id="e3073-115">The array of packets that make up the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object in *strokeId*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3073-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="e3073-116">Return value</span></span>

<span data-ttu-id="e3073-117">此函數可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="e3073-117">This function can return one of these values.</span></span>



| <span data-ttu-id="e3073-118">傳回碼</span><span class="sxs-lookup"><span data-stu-id="e3073-118">Return code</span></span>                                                                                  | <span data-ttu-id="e3073-119">Description</span><span class="sxs-lookup"><span data-stu-id="e3073-119">Description</span></span>                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="e3073-120"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="e3073-120"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="e3073-121">此函數已成功。</span><span class="sxs-lookup"><span data-stu-id="e3073-121">The function succeeded.</span></span><br/>              |
| <dl> <span data-ttu-id="e3073-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="e3073-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="e3073-123">*HDivider* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="e3073-123">The *hDivider* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e3073-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="e3073-124">Requirements</span></span>



| <span data-ttu-id="e3073-125">需求</span><span class="sxs-lookup"><span data-stu-id="e3073-125">Requirement</span></span> | <span data-ttu-id="e3073-126">值</span><span class="sxs-lookup"><span data-stu-id="e3073-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e3073-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e3073-127">Minimum supported client</span></span><br/> | <span data-ttu-id="e3073-128">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e3073-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="e3073-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e3073-129">Minimum supported server</span></span><br/> | <span data-ttu-id="e3073-130">都不支援</span><span class="sxs-lookup"><span data-stu-id="e3073-130">None supported</span></span><br/>                                                             |
| <span data-ttu-id="e3073-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="e3073-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="e3073-132"><dt>InkDiv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e3073-132"><dt>InkDiv.dll</dt></span></span> </dl> |



 

 




