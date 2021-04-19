---
description: GetClassWindowStyles 方法會抓取視窗的類別樣式和視窗樣式。
ms.assetid: 6eec7912-c654-4e4f-b6f1-ec94c7284575
title: 'CBaseWindow. GetClassWindowStyles 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.GetClassWindowStyles
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a34332f84a91ee88d61ee5f29f0b6a0b0cc44714
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001821"
---
# <a name="cbasewindowgetclasswindowstyles-method"></a><span data-ttu-id="1f0ab-103">CBaseWindow. GetClassWindowStyles 方法</span><span class="sxs-lookup"><span data-stu-id="1f0ab-103">CBaseWindow.GetClassWindowStyles method</span></span>

<span data-ttu-id="1f0ab-104">方法會抓取 `GetClassWindowStyles` 視窗的類別樣式和視窗樣式。</span><span class="sxs-lookup"><span data-stu-id="1f0ab-104">The `GetClassWindowStyles` method retrieves the window's class styles and window styles.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f0ab-105">語法</span><span class="sxs-lookup"><span data-stu-id="1f0ab-105">Syntax</span></span>


```C++
virtual LPTSTR GetClassWindowStyles(
   DWORD *pClassStyles,
   DWORD *pWindowStyles,
   DWORD *pWindowStylesEx
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="1f0ab-106">參數</span><span class="sxs-lookup"><span data-stu-id="1f0ab-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f0ab-107">*pClassStyles*</span><span class="sxs-lookup"><span data-stu-id="1f0ab-107">*pClassStyles*</span></span> 
</dt> <dd>

<span data-ttu-id="1f0ab-108">接收類別樣式之變數的指標。</span><span class="sxs-lookup"><span data-stu-id="1f0ab-108">Pointer to a variable that receives the class styles.</span></span>

</dd> <dt>

<span data-ttu-id="1f0ab-109">*pWindowStyles*</span><span class="sxs-lookup"><span data-stu-id="1f0ab-109">*pWindowStyles*</span></span> 
</dt> <dd>

<span data-ttu-id="1f0ab-110">接收視窗樣式之變數的指標。</span><span class="sxs-lookup"><span data-stu-id="1f0ab-110">Pointer to a variable that receives the window styles.</span></span>

</dd> <dt>

<span data-ttu-id="1f0ab-111">*pWindowStylesEx*</span><span class="sxs-lookup"><span data-stu-id="1f0ab-111">*pWindowStylesEx*</span></span> 
</dt> <dd>

<span data-ttu-id="1f0ab-112">接收延伸視窗樣式之變數的指標。</span><span class="sxs-lookup"><span data-stu-id="1f0ab-112">Pointer to a variable that receives the extended window styles.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f0ab-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="1f0ab-113">Return value</span></span>

<span data-ttu-id="1f0ab-114">傳回包含類別名稱的靜態文字字串。</span><span class="sxs-lookup"><span data-stu-id="1f0ab-114">Returns a static text string that contains the class name.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f0ab-115">備註</span><span class="sxs-lookup"><span data-stu-id="1f0ab-115">Remarks</span></span>

<span data-ttu-id="1f0ab-116">[**CBaseWindow：:P reparewindow**](cbasewindow-preparewindow.md)方法會呼叫這個方法，以取得視窗的類別樣式和視窗樣式。</span><span class="sxs-lookup"><span data-stu-id="1f0ab-116">The [**CBaseWindow::PrepareWindow**](cbasewindow-preparewindow.md) method calls this method to retrieve the window's class styles and window styles.</span></span>

<span data-ttu-id="1f0ab-117">這個方法是純虛擬的;衍生的類別必須加以執行。</span><span class="sxs-lookup"><span data-stu-id="1f0ab-117">This method is pure virtual; the derived class must implement it.</span></span> <span data-ttu-id="1f0ab-118">下列範例顯示可能的實作為：</span><span class="sxs-lookup"><span data-stu-id="1f0ab-118">The following example shows a possible implementation:</span></span>


```C++
LPTSTR CMyWindowClass::GetClassWindowStyles(DWORD *pClassStyles,
                                            DWORD *pWindowStyles,
                                            DWORD *pWindowStylesEx)
{
    *pClassStyles = CS_HREDRAW | CS_VREDRAW;
    *pWindowStyles = WS_OVERLAPPEDWINDOW | WS_CLIPCHILDREN;
    *pWindowStylesEx = WS_EX_WINDOWEDGE;
    return TEXT("MyWindowClass");
}
```



<span data-ttu-id="1f0ab-119">物件會針對 WNDCLASS 結構的 **lpszClassName** 成員（其會傳遞至 **RegisterClass** 函數）使用類別樣式。</span><span class="sxs-lookup"><span data-stu-id="1f0ab-119">The object uses the class style for the **lpszClassName** member of a WNDCLASS structure, which it passes to the **RegisterClass** function.</span></span> <span data-ttu-id="1f0ab-120">物件使用 **CreateWindowEx** 函式的 *dwExStyle* 和 *dwStyle* 參數的視窗樣式。</span><span class="sxs-lookup"><span data-stu-id="1f0ab-120">The object uses the window styles for the *dwExStyle* and *dwStyle* parameters of the **CreateWindowEx** function.</span></span> <span data-ttu-id="1f0ab-121">如需詳細資訊，請參閱 Platform SDK。</span><span class="sxs-lookup"><span data-stu-id="1f0ab-121">For more information, see the Platform SDK.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f0ab-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="1f0ab-122">Requirements</span></span>



| <span data-ttu-id="1f0ab-123">需求</span><span class="sxs-lookup"><span data-stu-id="1f0ab-123">Requirement</span></span> | <span data-ttu-id="1f0ab-124">值</span><span class="sxs-lookup"><span data-stu-id="1f0ab-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f0ab-125">標頭</span><span class="sxs-lookup"><span data-stu-id="1f0ab-125">Header</span></span><br/>  | <dl> <span data-ttu-id="1f0ab-126"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="1f0ab-126"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1f0ab-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="1f0ab-127">Library</span></span><br/> | <dl> <span data-ttu-id="1f0ab-128"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="1f0ab-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f0ab-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1f0ab-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f0ab-130">**CBaseWindow 類別**</span><span class="sxs-lookup"><span data-stu-id="1f0ab-130">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




