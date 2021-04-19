---
description: Get \_ Visible 方法會抓取目前的視窗可見度。
ms.assetid: 7e643569-1116-4562-be33-babd12a7e899
title: 'CBaseControlWindow.get_Visible 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_Visible
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3bc38a0b35f46de223ed84174c3b10f5300cc94d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999694"
---
# <a name="cbasecontrolwindowget_visible-method"></a><span data-ttu-id="3b3b6-103">CBaseControlWindow。取得 \_ Visible 方法</span><span class="sxs-lookup"><span data-stu-id="3b3b6-103">CBaseControlWindow.get\_Visible method</span></span>

<span data-ttu-id="3b3b6-104">方法會抓取 `get_Visible` 目前的視窗可見度。</span><span class="sxs-lookup"><span data-stu-id="3b3b6-104">The `get_Visible` method retrieves the current window visibility.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b3b6-105">語法</span><span class="sxs-lookup"><span data-stu-id="3b3b6-105">Syntax</span></span>


```C++
HRESULT get_Visible(
   long *pVisible
);
```



## <a name="parameters"></a><span data-ttu-id="3b3b6-106">參數</span><span class="sxs-lookup"><span data-stu-id="3b3b6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b3b6-107">*pVisible*</span><span class="sxs-lookup"><span data-stu-id="3b3b6-107">*pVisible*</span></span> 
</dt> <dd>

<span data-ttu-id="3b3b6-108">自動化布林值旗標的指標 (0 是 off，1是) 。</span><span class="sxs-lookup"><span data-stu-id="3b3b6-108">Pointer to an Automation Boolean flag (0 is off,  1 is on).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b3b6-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="3b3b6-109">Return value</span></span>

<span data-ttu-id="3b3b6-110">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="3b3b6-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b3b6-111">備註</span><span class="sxs-lookup"><span data-stu-id="3b3b6-111">Remarks</span></span>

<span data-ttu-id="3b3b6-112">如果視窗具有 WS 可見樣式，則這個成員函式會傳回 1 \_ ; 否則會傳回0。</span><span class="sxs-lookup"><span data-stu-id="3b3b6-112">This member function returns  1 if the window has the WS\_VISIBLE style; 0 otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b3b6-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="3b3b6-113">Requirements</span></span>



| <span data-ttu-id="3b3b6-114">需求</span><span class="sxs-lookup"><span data-stu-id="3b3b6-114">Requirement</span></span> | <span data-ttu-id="3b3b6-115">值</span><span class="sxs-lookup"><span data-stu-id="3b3b6-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b3b6-116">標頭</span><span class="sxs-lookup"><span data-stu-id="3b3b6-116">Header</span></span><br/>  | <dl> <span data-ttu-id="3b3b6-117"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="3b3b6-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3b3b6-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="3b3b6-118">Library</span></span><br/> | <dl> <span data-ttu-id="3b3b6-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="3b3b6-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b3b6-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3b3b6-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b3b6-121">**CBaseControlWindow 類別**</span><span class="sxs-lookup"><span data-stu-id="3b3b6-121">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




