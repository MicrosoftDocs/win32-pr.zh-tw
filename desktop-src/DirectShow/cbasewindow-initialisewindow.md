---
description: InitialiseWindow 方法會初始化視窗。
ms.assetid: 0cf07714-6846-4271-8095-bc4ab865171f
title: " (Winutil 的 CBaseWindow.InitialiseWindow 方法) "
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.InitialiseWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 75668846c700c33a26b7bb7ad2af2a3fd6e8eea2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989600"
---
# <a name="cbasewindowinitialisewindow-method"></a><span data-ttu-id="d17bb-103">CBaseWindow.InitialiseWindow 方法</span><span class="sxs-lookup"><span data-stu-id="d17bb-103">CBaseWindow.InitialiseWindow method</span></span>

<span data-ttu-id="d17bb-104">`InitialiseWindow`方法會初始化視窗。</span><span class="sxs-lookup"><span data-stu-id="d17bb-104">The `InitialiseWindow` method initializes the window.</span></span>

## <a name="syntax"></a><span data-ttu-id="d17bb-105">語法</span><span class="sxs-lookup"><span data-stu-id="d17bb-105">Syntax</span></span>


```C++
virtual HRESULT InitialiseWindow(
   HWND hwnd
);
```



## <a name="parameters"></a><span data-ttu-id="d17bb-106">參數</span><span class="sxs-lookup"><span data-stu-id="d17bb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d17bb-107">*hwnd*</span><span class="sxs-lookup"><span data-stu-id="d17bb-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="d17bb-108">視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="d17bb-108">Handle to the window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d17bb-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="d17bb-109">Return value</span></span>

<span data-ttu-id="d17bb-110">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="d17bb-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="d17bb-111">備註</span><span class="sxs-lookup"><span data-stu-id="d17bb-111">Remarks</span></span>

<span data-ttu-id="d17bb-112">根據預設，這個方法會抓取視窗的裝置內容 (DC) 的控制碼，並建立相容的記憶體 DC。</span><span class="sxs-lookup"><span data-stu-id="d17bb-112">By default, this method retrieves a handle to the window's device context (DC) and creates a compatible memory DC.</span></span> <span data-ttu-id="d17bb-113">但是，如果 [**CBaseWindow：： m \_ bDoGetDC**](cbasewindow-m-bdogetdc.md) 旗標的值為 **FALSE**，則這個方法不會取出裝置內容。</span><span class="sxs-lookup"><span data-stu-id="d17bb-113">If the value of the [**CBaseWindow::m\_bDoGetDC**](cbasewindow-m-bdogetdc.md) flag is **FALSE**, however, this method does not retrieve the device contexts.</span></span> <span data-ttu-id="d17bb-114">記憶體 DC 在將點陣圖 blitting 至視窗之前，很適合用來選取點陣圖。</span><span class="sxs-lookup"><span data-stu-id="d17bb-114">The memory DC is useful for selecting bitmaps before blitting them to the window.</span></span>

<span data-ttu-id="d17bb-115">[**CBaseWindow：:D ocreatewindow**](cbasewindow-docreatewindow.md)方法會呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="d17bb-115">The [**CBaseWindow::DoCreateWindow**](cbasewindow-docreatewindow.md) method calls this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="d17bb-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="d17bb-116">Requirements</span></span>



| <span data-ttu-id="d17bb-117">需求</span><span class="sxs-lookup"><span data-stu-id="d17bb-117">Requirement</span></span> | <span data-ttu-id="d17bb-118">值</span><span class="sxs-lookup"><span data-stu-id="d17bb-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d17bb-119">標頭</span><span class="sxs-lookup"><span data-stu-id="d17bb-119">Header</span></span><br/>  | <dl> <span data-ttu-id="d17bb-120"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="d17bb-120"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d17bb-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="d17bb-121">Library</span></span><br/> | <dl> <span data-ttu-id="d17bb-122"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="d17bb-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d17bb-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d17bb-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d17bb-124">**CBaseWindow 類別**</span><span class="sxs-lookup"><span data-stu-id="d17bb-124">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




