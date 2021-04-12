---
description: 設定要在行辨識期間使用的回呼函數。
ms.assetid: 0b07ec80-328a-471b-b554-fa66f56a2871
title: SetLineRecoCallback 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetLineRecoCallback
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: b256a38d6d6ee6ecf43994c6619c369ea6ca2212
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193330"
---
# <a name="setlinerecocallback-function"></a><span data-ttu-id="f1b5a-103">SetLineRecoCallback 函式</span><span class="sxs-lookup"><span data-stu-id="f1b5a-103">SetLineRecoCallback function</span></span>

<span data-ttu-id="f1b5a-104">設定要在行辨識期間使用的回呼函數。</span><span class="sxs-lookup"><span data-stu-id="f1b5a-104">Sets a callback function to be used during line recognition.</span></span>

<span data-ttu-id="f1b5a-105">此 helper 函式不適合應用程式程式碼使用。</span><span class="sxs-lookup"><span data-stu-id="f1b5a-105">This helper function is not intended to be used by application code.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1b5a-106">語法</span><span class="sxs-lookup"><span data-stu-id="f1b5a-106">Syntax</span></span>


```C++
HRESULT WINAPI SetLineRecoCallback(
  _In_ INT_PTR        hDivider,
       GetLineRecoDef pfn
);
```



## <a name="parameters"></a><span data-ttu-id="f1b5a-107">參數</span><span class="sxs-lookup"><span data-stu-id="f1b5a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1b5a-108">*hDivider* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f1b5a-108">*hDivider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1b5a-109">[**InkDivider**](inkdivider-class.md)物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="f1b5a-109">A handle to the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="f1b5a-110">*pfn*</span><span class="sxs-lookup"><span data-stu-id="f1b5a-110">*pfn*</span></span> 
</dt> <dd>

<span data-ttu-id="f1b5a-111">在傳入的 [**InkDivider**](inkdivider-class.md) 上進行辨識時，所呼叫之函式的指標。</span><span class="sxs-lookup"><span data-stu-id="f1b5a-111">A pointer to a function that is called when recognition occurs on the [**InkDivider**](inkdivider-class.md) passed in.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1b5a-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="f1b5a-112">Return value</span></span>

<span data-ttu-id="f1b5a-113">此函數可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="f1b5a-113">This function can return one of these values.</span></span>



| <span data-ttu-id="f1b5a-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="f1b5a-114">Return code</span></span>                                                                                  | <span data-ttu-id="f1b5a-115">Description</span><span class="sxs-lookup"><span data-stu-id="f1b5a-115">Description</span></span>                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="f1b5a-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="f1b5a-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="f1b5a-117">此函數已成功。</span><span class="sxs-lookup"><span data-stu-id="f1b5a-117">The function succeeded.</span></span><br/>              |
| <dl> <span data-ttu-id="f1b5a-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="f1b5a-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="f1b5a-119">*PDivider* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="f1b5a-119">The *pDivider* parameter is invalid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f1b5a-120">備註</span><span class="sxs-lookup"><span data-stu-id="f1b5a-120">Remarks</span></span>

<span data-ttu-id="f1b5a-121">以下是回呼函數的語法。</span><span class="sxs-lookup"><span data-stu-id="f1b5a-121">The following is the syntax for the callback function.</span></span>

``` syntax
public delegate void GetLineRecoDef(
        int cStrokes, 
        [MarshalAs(UnmanagedType.LPArray, ArraySubType = UnmanagedType.I4, SizeParamIndex = 0)]int [] aStrokeIds, 
        float degrees, 
        Point point, 
        [MarshalAs(UnmanagedType.BStr)] out string lineString, 
        out int cSegment, 
        out int[] strokeIdOrdered, 
        out int[] segmentStrokes,
        [MarshalAs(UnmanagedType.LPArray, ArraySubType = UnmanagedType.BStr)] out string [] aSegmentString
    );
```

## <a name="requirements"></a><span data-ttu-id="f1b5a-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="f1b5a-122">Requirements</span></span>



| <span data-ttu-id="f1b5a-123">需求</span><span class="sxs-lookup"><span data-stu-id="f1b5a-123">Requirement</span></span> | <span data-ttu-id="f1b5a-124">值</span><span class="sxs-lookup"><span data-stu-id="f1b5a-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f1b5a-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f1b5a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f1b5a-126">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f1b5a-126">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="f1b5a-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f1b5a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f1b5a-128">都不支援</span><span class="sxs-lookup"><span data-stu-id="f1b5a-128">None supported</span></span><br/>                                                             |
| <span data-ttu-id="f1b5a-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="f1b5a-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="f1b5a-130"><dt>InkDiv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f1b5a-130"><dt>InkDiv.dll</dt></span></span> </dl> |



 

 




