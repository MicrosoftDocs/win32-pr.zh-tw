---
description: CompleteConnect 方法會通知視窗，轉譯器的輸入針腳已連接。
ms.assetid: 82347ded-eb37-4360-9333-7c837d532115
title: 'CBaseWindow. CompleteConnect 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 15d5719ab78c3e95cd0128d4075797221af1f4c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998383"
---
# <a name="cbasewindowcompleteconnect-method"></a><span data-ttu-id="981f0-103">CBaseWindow. CompleteConnect 方法</span><span class="sxs-lookup"><span data-stu-id="981f0-103">CBaseWindow.CompleteConnect method</span></span>

<span data-ttu-id="981f0-104">`CompleteConnect`方法會通知視窗，轉譯器的輸入針腳已連接。</span><span class="sxs-lookup"><span data-stu-id="981f0-104">The `CompleteConnect` method notifies the window that the renderer's input pin has been connected.</span></span>

## <a name="syntax"></a><span data-ttu-id="981f0-105">語法</span><span class="sxs-lookup"><span data-stu-id="981f0-105">Syntax</span></span>


```C++
HRESULT CompleteConnect();
```



## <a name="parameters"></a><span data-ttu-id="981f0-106">參數</span><span class="sxs-lookup"><span data-stu-id="981f0-106">Parameters</span></span>

<span data-ttu-id="981f0-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="981f0-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="981f0-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="981f0-108">Return value</span></span>

<span data-ttu-id="981f0-109">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="981f0-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="981f0-110">備註</span><span class="sxs-lookup"><span data-stu-id="981f0-110">Remarks</span></span>

<span data-ttu-id="981f0-111">這個方法會重設視窗啟用旗標， ([**CBaseWindow：： m \_ BActivated**](cbasewindow-m-bactivated.md)) 設為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="981f0-111">This method resets the window activation flag ([**CBaseWindow::m\_bActivated**](cbasewindow-m-bactivated.md)) to **FALSE**.</span></span> <span data-ttu-id="981f0-112">當影片轉譯器完成連接的連接時，它可能會呼叫 [**CBaseWindow：： ActivateWindow**](cbasewindow-activatewindow.md) 方法來設定視窗的大小和位置。</span><span class="sxs-lookup"><span data-stu-id="981f0-112">When a video renderer completes a pin connection, it might call the [**CBaseWindow::ActivateWindow**](cbasewindow-activatewindow.md) method to set the window's size and position.</span></span> <span data-ttu-id="981f0-113">若要強制 **ActivateWindow** 重新計算這些屬性，請先呼叫 `CompleteConnect` 方法。</span><span class="sxs-lookup"><span data-stu-id="981f0-113">To force **ActivateWindow** to recalculate these attributes, first call the `CompleteConnect` method.</span></span>

## <a name="requirements"></a><span data-ttu-id="981f0-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="981f0-114">Requirements</span></span>



| <span data-ttu-id="981f0-115">需求</span><span class="sxs-lookup"><span data-stu-id="981f0-115">Requirement</span></span> | <span data-ttu-id="981f0-116">值</span><span class="sxs-lookup"><span data-stu-id="981f0-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="981f0-117">標頭</span><span class="sxs-lookup"><span data-stu-id="981f0-117">Header</span></span><br/>  | <dl> <span data-ttu-id="981f0-118"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="981f0-118"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="981f0-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="981f0-119">Library</span></span><br/> | <dl> <span data-ttu-id="981f0-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="981f0-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="981f0-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="981f0-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="981f0-122">**CBaseWindow 類別**</span><span class="sxs-lookup"><span data-stu-id="981f0-122">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




