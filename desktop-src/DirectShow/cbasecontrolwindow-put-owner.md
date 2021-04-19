---
description: Put \_ Owner 方法會設定影片視窗的父視窗; 父視窗接著會將某些訊息轉送至影片視窗。
ms.assetid: 8ed85cb0-47be-40c1-947a-dd9f7850d867
title: 'CBaseControlWindow.put_Owner 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_Owner
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 16817d1c3f0fbdf756f6c054b875b8507fd1172a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995452"
---
# <a name="cbasecontrolwindowput_owner-method"></a><span data-ttu-id="df4e5-103">CBaseControlWindow put \_ Owner 方法</span><span class="sxs-lookup"><span data-stu-id="df4e5-103">CBaseControlWindow.put\_Owner method</span></span>

<span data-ttu-id="df4e5-104">`put_Owner`方法會設定影片視窗的父視窗; 父視窗接著會將某些訊息轉送至影片視窗。</span><span class="sxs-lookup"><span data-stu-id="df4e5-104">The `put_Owner` method sets the video window's parent window; the parent window then forwards certain messages to the video window.</span></span>

## <a name="syntax"></a><span data-ttu-id="df4e5-105">語法</span><span class="sxs-lookup"><span data-stu-id="df4e5-105">Syntax</span></span>


```C++
HRESULT put_Owner(
   OAHWND Owner
);
```



## <a name="parameters"></a><span data-ttu-id="df4e5-106">參數</span><span class="sxs-lookup"><span data-stu-id="df4e5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df4e5-107">*擁有者*</span><span class="sxs-lookup"><span data-stu-id="df4e5-107">*Owner*</span></span> 
</dt> <dd>

<span data-ttu-id="df4e5-108">父視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="df4e5-108">Handle to the parent window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df4e5-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="df4e5-109">Return value</span></span>

<span data-ttu-id="df4e5-110">傳回 >AAD-USERREADUSINGALTERNATIVESECURITYID-NOERROR。</span><span class="sxs-lookup"><span data-stu-id="df4e5-110">Returns NOERROR.</span></span>

## <a name="remarks"></a><span data-ttu-id="df4e5-111">備註</span><span class="sxs-lookup"><span data-stu-id="df4e5-111">Remarks</span></span>

<span data-ttu-id="df4e5-112">就內部而言，這個方法會呼叫 Microsoft Win32 **SetParent** 函式來設定新的擁有者，並將父視窗的樣式設定為 WS \_ 子系。</span><span class="sxs-lookup"><span data-stu-id="df4e5-112">Internally, this method calls the Microsoft Win32 **SetParent** function to set the new owner and sets the parent window's style to WS\_CHILD.</span></span> <span data-ttu-id="df4e5-113">父視窗接著會將特定的一組訊息轉寄 (特別是滑鼠和鍵盤訊息) 至影片視窗。</span><span class="sxs-lookup"><span data-stu-id="df4e5-113">The parent window will then forward certain sets of messages (in particular, mouse and keyboard messages) to the video window.</span></span>

<span data-ttu-id="df4e5-114">設定影片視窗的擁有者之後，您必須先將擁有者設為 **Null** ，並將擁有者的視窗樣式設定為 ws 重迭 \_ 和 ws CLIPCHILDREN，然後 \_ 再釋放篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="df4e5-114">After you set the video window's owner, you must set the owner to **NULL** and the owner's window style to WS\_OVERLAPPED and WS\_CLIPCHILDREN before releasing the filter graph.</span></span> <span data-ttu-id="df4e5-115">當您將擁有者設為 **Null** 時，這個方法會關閉父視窗的 WS \_ 子位。</span><span class="sxs-lookup"><span data-stu-id="df4e5-115">When you set the owner to **NULL**, this method turns off the parent window's WS\_CHILD bit.</span></span> <span data-ttu-id="df4e5-116">如果您未將擁有者設為 **Null**，父視窗會繼續將訊息傳遞至影片視窗，而且在應用程式關閉時可能會發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="df4e5-116">If you don't set the owner to **NULL**, the parent window will continue to pass messages to the video window and errors will likely occur when the application closes.</span></span>

## <a name="requirements"></a><span data-ttu-id="df4e5-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="df4e5-117">Requirements</span></span>



| <span data-ttu-id="df4e5-118">需求</span><span class="sxs-lookup"><span data-stu-id="df4e5-118">Requirement</span></span> | <span data-ttu-id="df4e5-119">值</span><span class="sxs-lookup"><span data-stu-id="df4e5-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df4e5-120">標頭</span><span class="sxs-lookup"><span data-stu-id="df4e5-120">Header</span></span><br/>  | <dl> <span data-ttu-id="df4e5-121"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="df4e5-121"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="df4e5-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="df4e5-122">Library</span></span><br/> | <dl> <span data-ttu-id="df4e5-123"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="df4e5-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df4e5-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="df4e5-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df4e5-125">**CBaseControlWindow 類別**</span><span class="sxs-lookup"><span data-stu-id="df4e5-125">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




