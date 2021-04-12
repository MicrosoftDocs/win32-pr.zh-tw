---
description: 傳回在動畫播放軌上指定的事件之後，排定要發生之下一個事件的事件控制碼。
ms.assetid: 616b2de1-6107-4d18-ad2e-de2ef4560aee
title: 'ID3DXAnimationController：： GetUpcomingTrackEvent 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetUpcomingTrackEvent
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f863ce918f25c6b0975010f71a63f067c01f7345
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946054"
---
# <a name="id3dxanimationcontrollergetupcomingtrackevent-method"></a><span data-ttu-id="f2b85-103">ID3DXAnimationController：： GetUpcomingTrackEvent 方法</span><span class="sxs-lookup"><span data-stu-id="f2b85-103">ID3DXAnimationController::GetUpcomingTrackEvent method</span></span>

<span data-ttu-id="f2b85-104">傳回在動畫播放軌上指定的事件之後，排定要發生之下一個事件的事件控制碼。</span><span class="sxs-lookup"><span data-stu-id="f2b85-104">Returns an event handle to the next event scheduled to occur after a specified event on an animation track.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2b85-105">語法</span><span class="sxs-lookup"><span data-stu-id="f2b85-105">Syntax</span></span>


```C++
D3DXEVENTHANDLE GetUpcomingTrackEvent(
  [in] UINT            Track,
  [in] D3DXEVENTHANDLE hEvent
);
```



## <a name="parameters"></a><span data-ttu-id="f2b85-106">參數</span><span class="sxs-lookup"><span data-stu-id="f2b85-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2b85-107">*追蹤* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f2b85-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2b85-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f2b85-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f2b85-109">追蹤識別碼。</span><span class="sxs-lookup"><span data-stu-id="f2b85-109">Track identifier.</span></span>

</dd> <dt>

<span data-ttu-id="f2b85-110">*hEvent* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f2b85-110">*hEvent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2b85-111">類型： **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="f2b85-111">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="f2b85-112">指定事件的事件控制碼，之後會在此搜尋下列事件。</span><span class="sxs-lookup"><span data-stu-id="f2b85-112">Event handle to a specified event after which to search for a following event.</span></span> <span data-ttu-id="f2b85-113">如果設定為 **Null**，則方法會傳回下一個排程的事件。</span><span class="sxs-lookup"><span data-stu-id="f2b85-113">If set to **NULL**, then the method will return the next scheduled event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2b85-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="f2b85-114">Return value</span></span>

<span data-ttu-id="f2b85-115">類型： **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="f2b85-115">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="f2b85-116">排定在指定的追蹤上執行的下一個事件的事件控制碼。如果未排定任何新的事件，則會傳回 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="f2b85-116">Event handle to the next event scheduled to run on the specified track. **NULL** is returned if no new event is scheduled.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2b85-117">備註</span><span class="sxs-lookup"><span data-stu-id="f2b85-117">Remarks</span></span>

<span data-ttu-id="f2b85-118">您可以重複將 **Null** 傳遞給 hEvent，以反復地使用這個方法來尋找所需的事件。</span><span class="sxs-lookup"><span data-stu-id="f2b85-118">This method can be used iteratively to locate a desired event by repeatedly passing in **NULL** for hEvent.</span></span>

> [!Note]  
> <span data-ttu-id="f2b85-119">當方法傳回 **Null** 之後，請勿再逐一查看。</span><span class="sxs-lookup"><span data-stu-id="f2b85-119">Do not iterate further after the method has returned **NULL**.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f2b85-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="f2b85-120">Requirements</span></span>



| <span data-ttu-id="f2b85-121">需求</span><span class="sxs-lookup"><span data-stu-id="f2b85-121">Requirement</span></span> | <span data-ttu-id="f2b85-122">值</span><span class="sxs-lookup"><span data-stu-id="f2b85-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f2b85-123">標頭</span><span class="sxs-lookup"><span data-stu-id="f2b85-123">Header</span></span><br/>  | <dl> <span data-ttu-id="f2b85-124"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="f2b85-124"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="f2b85-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="f2b85-125">Library</span></span><br/> | <dl> <span data-ttu-id="f2b85-126"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f2b85-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f2b85-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f2b85-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2b85-128">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="f2b85-128">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
