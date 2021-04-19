---
description: Put \_ system.windows.window.windowstyle 方法會設定標準的視窗樣式。
ms.assetid: 3b3aa035-6aa1-4f11-80d8-03268fcf98e1
title: 'CBaseControlWindow.put_WindowStyle 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_WindowStyle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3f98e6205a45530a0dbcce09d095dfaa2267ccbb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983230"
---
# <a name="cbasecontrolwindowput_windowstyle-method"></a><span data-ttu-id="bb70f-103">CBaseControlWindow. put \_ system.windows.window.windowstyle 方法</span><span class="sxs-lookup"><span data-stu-id="bb70f-103">CBaseControlWindow.put\_WindowStyle method</span></span>

<span data-ttu-id="bb70f-104">`put_WindowStyle`方法會設定標準的視窗樣式。</span><span class="sxs-lookup"><span data-stu-id="bb70f-104">The `put_WindowStyle` method sets the standard window styles.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb70f-105">語法</span><span class="sxs-lookup"><span data-stu-id="bb70f-105">Syntax</span></span>


```C++
HRESULT put_WindowStyle(
   long WindowStyle
);
```



## <a name="parameters"></a><span data-ttu-id="bb70f-106">參數</span><span class="sxs-lookup"><span data-stu-id="bb70f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb70f-107">*WindowStyle*</span><span class="sxs-lookup"><span data-stu-id="bb70f-107">*WindowStyle*</span></span> 
</dt> <dd>

<span data-ttu-id="bb70f-108">新的視窗樣式。</span><span class="sxs-lookup"><span data-stu-id="bb70f-108">New window styles.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb70f-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="bb70f-109">Return value</span></span>

<span data-ttu-id="bb70f-110">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="bb70f-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="bb70f-111">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="bb70f-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb70f-112">備註</span><span class="sxs-lookup"><span data-stu-id="bb70f-112">Remarks</span></span>

<span data-ttu-id="bb70f-113">變更視窗樣式時請小心。</span><span class="sxs-lookup"><span data-stu-id="bb70f-113">Take care when changing the window styles.</span></span> <span data-ttu-id="bb70f-114">在大部分的情況下，應用程式應該取出目前的樣式，然後新增或移除不適當的位。</span><span class="sxs-lookup"><span data-stu-id="bb70f-114">In most cases, an application should retrieve the current style and then add or remove the inappropriate bits.</span></span> <span data-ttu-id="bb70f-115">此程式可讓 Windows 使用的各種內部視窗樣式保持不變。</span><span class="sxs-lookup"><span data-stu-id="bb70f-115">This procedure allows various internal window styles used by Windows to remain intact.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb70f-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="bb70f-116">Requirements</span></span>



| <span data-ttu-id="bb70f-117">需求</span><span class="sxs-lookup"><span data-stu-id="bb70f-117">Requirement</span></span> | <span data-ttu-id="bb70f-118">值</span><span class="sxs-lookup"><span data-stu-id="bb70f-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb70f-119">標頭</span><span class="sxs-lookup"><span data-stu-id="bb70f-119">Header</span></span><br/>  | <dl> <span data-ttu-id="bb70f-120"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="bb70f-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="bb70f-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="bb70f-121">Library</span></span><br/> | <dl> <span data-ttu-id="bb70f-122"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="bb70f-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb70f-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bb70f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb70f-124">**CBaseControlWindow 類別**</span><span class="sxs-lookup"><span data-stu-id="bb70f-124">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




