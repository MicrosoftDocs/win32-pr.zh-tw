---
description: CMediaControl。 CMediaControl 函式-函數方法。
ms.assetid: 00549dfe-5dd4-445e-bad3-eb6bcfea8f5f
title: 'CMediaControl. CMediaControl (Ctlutil. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaControl.CMediaControl
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 96775678a8d182a3dc88f25fc19b194367c57d92
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099206"
---
# <a name="cmediacontrolcmediacontrol-constructor"></a><span data-ttu-id="381a4-103">CMediaControl. CMediaControl 函數</span><span class="sxs-lookup"><span data-stu-id="381a4-103">CMediaControl.CMediaControl constructor</span></span>

<span data-ttu-id="381a4-104">函式方法。</span><span class="sxs-lookup"><span data-stu-id="381a4-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="381a4-105">語法</span><span class="sxs-lookup"><span data-stu-id="381a4-105">Syntax</span></span>


```C++
CMediaControl(
   const TCHAR     *pName,
         LPUNKNOWN pUnk
);
```



## <a name="parameters"></a><span data-ttu-id="381a4-106">參數</span><span class="sxs-lookup"><span data-stu-id="381a4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="381a4-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="381a4-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="381a4-108">用於偵測之物件名稱的指標。</span><span class="sxs-lookup"><span data-stu-id="381a4-108">Pointer to the name of the object for debugging purposes.</span></span>

</dd> <dt>

<span data-ttu-id="381a4-109">*朋 克*</span><span class="sxs-lookup"><span data-stu-id="381a4-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="381a4-110">這個物件之擁有者的指標。</span><span class="sxs-lookup"><span data-stu-id="381a4-110">Pointer to the owner of this object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="381a4-111">備註</span><span class="sxs-lookup"><span data-stu-id="381a4-111">Remarks</span></span>

<span data-ttu-id="381a4-112">在靜態記憶體中配置 *pName* 參數。</span><span class="sxs-lookup"><span data-stu-id="381a4-112">Allocate the *pName* parameter in static memory.</span></span> <span data-ttu-id="381a4-113">這個名稱會在物件的建立和刪除時，出現在偵錯工具的終端機上。</span><span class="sxs-lookup"><span data-stu-id="381a4-113">This name appears on the debugging terminal upon creation and deletion of the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="381a4-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="381a4-114">Requirements</span></span>



| <span data-ttu-id="381a4-115">需求</span><span class="sxs-lookup"><span data-stu-id="381a4-115">Requirement</span></span> | <span data-ttu-id="381a4-116">值</span><span class="sxs-lookup"><span data-stu-id="381a4-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="381a4-117">標頭</span><span class="sxs-lookup"><span data-stu-id="381a4-117">Header</span></span><br/>  | <dl> <span data-ttu-id="381a4-118"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="381a4-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="381a4-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="381a4-119">Library</span></span><br/> | <dl> <span data-ttu-id="381a4-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="381a4-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="381a4-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="381a4-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="381a4-122">**CMediaControl 類別**</span><span class="sxs-lookup"><span data-stu-id="381a4-122">**CMediaControl Class**</span></span>](cmediacontrol.md)
</dt> </dl>

 

 




