---
description: 函式方法。
ms.assetid: 9f0b91c4-0364-4c73-b97f-86703ca3ef74
title: 'CBaseWindow. CBaseWindow (Winutil. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.CBaseWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a1741f8596210afac676a7e81f57b46e18fbba9b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983975"
---
# <a name="cbasewindowcbasewindow-constructor"></a><span data-ttu-id="4a917-103">CBaseWindow. CBaseWindow 函數</span><span class="sxs-lookup"><span data-stu-id="4a917-103">CBaseWindow.CBaseWindow constructor</span></span>

<span data-ttu-id="4a917-104">函式方法。</span><span class="sxs-lookup"><span data-stu-id="4a917-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a917-105">語法</span><span class="sxs-lookup"><span data-stu-id="4a917-105">Syntax</span></span>


```C++
CBaseWindow(
   BOOL bDoGetDC = TRUE,
   BOOL bPostToDestroy = FALSE
);
```



## <a name="parameters"></a><span data-ttu-id="4a917-106">參數</span><span class="sxs-lookup"><span data-stu-id="4a917-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a917-107">*bDoGetDC*</span><span class="sxs-lookup"><span data-stu-id="4a917-107">*bDoGetDC*</span></span> 
</dt> <dd>

<span data-ttu-id="4a917-108">指定是否要取出裝置內容的布林值。</span><span class="sxs-lookup"><span data-stu-id="4a917-108">Boolean value that specifies whether to retrieve the device context.</span></span>

</dd> <dt>

<span data-ttu-id="4a917-109">*bPostToDestroy*</span><span class="sxs-lookup"><span data-stu-id="4a917-109">*bPostToDestroy*</span></span> 
</dt> <dd>

<span data-ttu-id="4a917-110">指定 [**CBaseWindow：： m \_ bDoPostToDestroy**](cbasewindow-m-bdoposttodestroy.md) 成員變數的布林值。</span><span class="sxs-lookup"><span data-stu-id="4a917-110">Boolean value that specifies the [**CBaseWindow::m\_bDoPostToDestroy**](cbasewindow-m-bdoposttodestroy.md) member variable.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4a917-111">備註</span><span class="sxs-lookup"><span data-stu-id="4a917-111">Remarks</span></span>

<span data-ttu-id="4a917-112">建立物件之後，請呼叫 [**CBaseWindow：:P reparewindow**](cbasewindow-preparewindow.md) 方法來建立視窗。</span><span class="sxs-lookup"><span data-stu-id="4a917-112">After you create the object, call the [**CBaseWindow::PrepareWindow**](cbasewindow-preparewindow.md) method to create the window.</span></span> <span data-ttu-id="4a917-113">**PrepareWindow** 是虛擬方法。</span><span class="sxs-lookup"><span data-stu-id="4a917-113">**PrepareWindow** is a virtual method.</span></span> <span data-ttu-id="4a917-114">它會呼叫 [**CBaseWindow：： InitialiseWindow**](cbasewindow-initialisewindow.md)，也是虛擬方法。</span><span class="sxs-lookup"><span data-stu-id="4a917-114">It calls [**CBaseWindow::InitialiseWindow**](cbasewindow-initialisewindow.md), also a virtual method.</span></span> <span data-ttu-id="4a917-115">這些方法會與函式分開，讓衍生的類別可以在必要時加以覆寫。</span><span class="sxs-lookup"><span data-stu-id="4a917-115">These methods are separated from the constructor so that derived classes can override them, if necessary.</span></span>

<span data-ttu-id="4a917-116">如果 *bDoGetDC* 參數的值為 **TRUE**，則物件會 `CBaseWindow` (DC) 抓取視窗的裝置內容控制碼，並將其儲存在 [**CBaseWindow：： m \_ hdc**](cbasewindow-m-hdc.md) 成員變數中。</span><span class="sxs-lookup"><span data-stu-id="4a917-116">If the value of the *bDoGetDC* parameter is **TRUE**, the `CBaseWindow` object retrieves a handle to the window's device context (DC) and stores it in the [**CBaseWindow::m\_hdc**](cbasewindow-m-hdc.md) member variable.</span></span> <span data-ttu-id="4a917-117">物件也會建立相容的記憶體 DC，它會儲存在 [**CBaseWindow：： m \_ MemoryDC**](cbasewindow-m-memorydc.md) 成員變數中。</span><span class="sxs-lookup"><span data-stu-id="4a917-117">The object also creates a compatible memory DC, which it stores in the [**CBaseWindow::m\_MemoryDC**](cbasewindow-m-memorydc.md) member variable.</span></span> <span data-ttu-id="4a917-118">這些動作會在 **InitialiseWindow** 方法中進行。</span><span class="sxs-lookup"><span data-stu-id="4a917-118">These actions occur in the **InitialiseWindow** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a917-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="4a917-119">Requirements</span></span>



| <span data-ttu-id="4a917-120">需求</span><span class="sxs-lookup"><span data-stu-id="4a917-120">Requirement</span></span> | <span data-ttu-id="4a917-121">值</span><span class="sxs-lookup"><span data-stu-id="4a917-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a917-122">標頭</span><span class="sxs-lookup"><span data-stu-id="4a917-122">Header</span></span><br/>  | <dl> <span data-ttu-id="4a917-123"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="4a917-123"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4a917-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="4a917-124">Library</span></span><br/> | <dl> <span data-ttu-id="4a917-125"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="4a917-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a917-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4a917-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a917-127">**CBaseWindow 類別**</span><span class="sxs-lookup"><span data-stu-id="4a917-127">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




