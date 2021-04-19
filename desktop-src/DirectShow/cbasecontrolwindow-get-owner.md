---
description: 取得擁有者方法會抓取 \_ 目前的視窗擁有者。
ms.assetid: f0eea5e7-4dfa-4973-ae12-487657e6be80
title: 'CBaseControlWindow.get_Owner 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_Owner
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c8f8e3d4a331dbc66397a7b0058fcefcede2cdbb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982619"
---
# <a name="cbasecontrolwindowget_owner-method"></a><span data-ttu-id="24d0c-103">CBaseControlWindow 取得 \_ Owner 方法</span><span class="sxs-lookup"><span data-stu-id="24d0c-103">CBaseControlWindow.get\_Owner method</span></span>

<span data-ttu-id="24d0c-104">方法會抓取 `get_Owner` 目前的視窗擁有者。</span><span class="sxs-lookup"><span data-stu-id="24d0c-104">The `get_Owner` method retrieves the current window owner.</span></span>

## <a name="syntax"></a><span data-ttu-id="24d0c-105">語法</span><span class="sxs-lookup"><span data-stu-id="24d0c-105">Syntax</span></span>


```C++
HRESULT get_Owner(
   OAHWND *Owner
);
```



## <a name="parameters"></a><span data-ttu-id="24d0c-106">參數</span><span class="sxs-lookup"><span data-stu-id="24d0c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24d0c-107">*擁有者*</span><span class="sxs-lookup"><span data-stu-id="24d0c-107">*Owner*</span></span> 
</dt> <dd>

<span data-ttu-id="24d0c-108">視窗擁有者的指標。</span><span class="sxs-lookup"><span data-stu-id="24d0c-108">Pointer to the window owner.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24d0c-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="24d0c-109">Return value</span></span>

<span data-ttu-id="24d0c-110">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="24d0c-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="24d0c-111">備註</span><span class="sxs-lookup"><span data-stu-id="24d0c-111">Remarks</span></span>

<span data-ttu-id="24d0c-112">影片視窗可以在檔環境內播放。</span><span class="sxs-lookup"><span data-stu-id="24d0c-112">The video window can play back within a document environment.</span></span> <span data-ttu-id="24d0c-113">若要這樣做，必須將視窗設為另一個視窗 (的子系，以便將其裁剪並適當地移) 。</span><span class="sxs-lookup"><span data-stu-id="24d0c-113">To do this, the window must be made a child of another window (so that it is clipped and moved appropriately).</span></span> <span data-ttu-id="24d0c-114">這個屬性可讓您設定和取出視窗的擁有者。</span><span class="sxs-lookup"><span data-stu-id="24d0c-114">This property allows the owner of the window to be set and retrieved.</span></span> <span data-ttu-id="24d0c-115">當視窗由另一個視窗所擁有時，它只會呼叫 Microsoft Win32 **SetParent** 函式。</span><span class="sxs-lookup"><span data-stu-id="24d0c-115">When the window is owned by another window, it simply calls the Microsoft Win32 **SetParent** function.</span></span> <span data-ttu-id="24d0c-116">呼叫此函式的應用程式將會變更視窗樣式，以 \_ 在上設定 WS 子位。</span><span class="sxs-lookup"><span data-stu-id="24d0c-116">An application calling this function will change the window styles to set the WS\_CHILD bit on.</span></span>

<span data-ttu-id="24d0c-117">當視窗由另一個視窗所擁有時，會自動將特定的訊息集轉寄 (特別是) 的滑鼠和鍵盤訊息。</span><span class="sxs-lookup"><span data-stu-id="24d0c-117">When the window is owned by another window, it will automatically forward certain sets of messages (in particular, mouse and keyboard messages).</span></span> <span data-ttu-id="24d0c-118">這可讓應用程式進行簡單的熱點編輯和其他互動。</span><span class="sxs-lookup"><span data-stu-id="24d0c-118">This allows an application to do simple hot-spot editing and other interactions.</span></span>

<span data-ttu-id="24d0c-119">此成員函式的目的是要透過 [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) 介面呼叫外部物件，因此會鎖定重要區段以與相關聯的篩選進行同步處理。</span><span class="sxs-lookup"><span data-stu-id="24d0c-119">This member function is meant to be called by external objects through the [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) interface, and therefore locks the critical section to synchronize with the associated filter.</span></span> <span data-ttu-id="24d0c-120">呼叫 [**CBaseControlWindow：： GetOwnerWindow**](cbasecontrolwindow-getownerwindow.md) 成員函式，以取得此屬性（如果不是從外部物件呼叫）。</span><span class="sxs-lookup"><span data-stu-id="24d0c-120">Call the [**CBaseControlWindow::GetOwnerWindow**](cbasecontrolwindow-getownerwindow.md) member function to retrieve this property if not calling from an external object.</span></span>

## <a name="requirements"></a><span data-ttu-id="24d0c-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="24d0c-121">Requirements</span></span>



| <span data-ttu-id="24d0c-122">需求</span><span class="sxs-lookup"><span data-stu-id="24d0c-122">Requirement</span></span> | <span data-ttu-id="24d0c-123">值</span><span class="sxs-lookup"><span data-stu-id="24d0c-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24d0c-124">標頭</span><span class="sxs-lookup"><span data-stu-id="24d0c-124">Header</span></span><br/>  | <dl> <span data-ttu-id="24d0c-125"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="24d0c-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="24d0c-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="24d0c-126">Library</span></span><br/> | <dl> <span data-ttu-id="24d0c-127"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="24d0c-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24d0c-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="24d0c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24d0c-129">**CBaseControlWindow 類別**</span><span class="sxs-lookup"><span data-stu-id="24d0c-129">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




