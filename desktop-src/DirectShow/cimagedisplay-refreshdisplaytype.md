---
description: RefreshDisplayType 方法會更新物件的影片格式，以符合指定的顯示。
ms.assetid: cc2bdfeb-80f1-4fb6-859d-977d644a5e08
title: 'CImageDisplay. RefreshDisplayType 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.RefreshDisplayType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9f8010dcfe490363903ff455bedb61254b69b825
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981368"
---
# <a name="cimagedisplayrefreshdisplaytype-method"></a><span data-ttu-id="2d600-103">CImageDisplay. RefreshDisplayType 方法</span><span class="sxs-lookup"><span data-stu-id="2d600-103">CImageDisplay.RefreshDisplayType method</span></span>

<span data-ttu-id="2d600-104">`RefreshDisplayType`方法會更新物件的影片格式，以符合指定的顯示。</span><span class="sxs-lookup"><span data-stu-id="2d600-104">The `RefreshDisplayType` method updates the object's video format to match the specified display.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d600-105">語法</span><span class="sxs-lookup"><span data-stu-id="2d600-105">Syntax</span></span>


```C++
HRESULT RefreshDisplayType(
   LPSTR szDeviceName
);
```



## <a name="parameters"></a><span data-ttu-id="2d600-106">參數</span><span class="sxs-lookup"><span data-stu-id="2d600-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d600-107">*szDeviceName*</span><span class="sxs-lookup"><span data-stu-id="2d600-107">*szDeviceName*</span></span> 
</dt> <dd>

<span data-ttu-id="2d600-108">字串的指標，其中包含由 GDI **EnumDisplayDevices** 函式所傳回之顯示裝置的名稱。</span><span class="sxs-lookup"><span data-stu-id="2d600-108">Pointer to a string that contains the name of the display device, as returned by the GDI **EnumDisplayDevices** function.</span></span> <span data-ttu-id="2d600-109">若要使用主顯示器裝置，請將此參數設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="2d600-109">To use the main display device, set this parameter to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d600-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="2d600-110">Return value</span></span>

<span data-ttu-id="2d600-111">\_如果成功，則傳回 [確定]，如果失敗，則傳回 E \_ 失敗。</span><span class="sxs-lookup"><span data-stu-id="2d600-111">Returns S\_OK if successful, or E\_FAIL if unsuccessful.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d600-112">備註</span><span class="sxs-lookup"><span data-stu-id="2d600-112">Remarks</span></span>

<span data-ttu-id="2d600-113">這個方法會將 **m \_ 顯示** 成員初始化為與指定裝置上的顯示模式相對應的影片類型。</span><span class="sxs-lookup"><span data-stu-id="2d600-113">This method initializes the **m\_Display** member to a video type that corresponds to the display mode on the specified device.</span></span>

<span data-ttu-id="2d600-114">每次收到 WM DISPLAYCHANGED 訊息時呼叫此方法 \_ ，或指定次要顯示裝置。</span><span class="sxs-lookup"><span data-stu-id="2d600-114">Call this method whenever a WM\_DISPLAYCHANGED message is received, or to specify a secondary display device.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d600-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="2d600-115">Requirements</span></span>



| <span data-ttu-id="2d600-116">需求</span><span class="sxs-lookup"><span data-stu-id="2d600-116">Requirement</span></span> | <span data-ttu-id="2d600-117">值</span><span class="sxs-lookup"><span data-stu-id="2d600-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d600-118">標頭</span><span class="sxs-lookup"><span data-stu-id="2d600-118">Header</span></span><br/>  | <dl> <span data-ttu-id="2d600-119"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="2d600-119"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2d600-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="2d600-120">Library</span></span><br/> | <dl> <span data-ttu-id="2d600-121"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="2d600-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d600-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2d600-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d600-123">**CImageDisplay 類別**</span><span class="sxs-lookup"><span data-stu-id="2d600-123">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




