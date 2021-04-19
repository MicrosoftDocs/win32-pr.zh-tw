---
description: GetCountOfType 方法會以遞迴方式抓取此組合中所包含之指定型別的物件數目及其所有虛擬追蹤。
ms.assetid: 2d14ccf7-77bc-4095-bfb8-12a52b4b9595
title: 'IAMTimelineComp：： GetCountOfType 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.GetCountOfType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 69c4c582a3883feedec962bfb88b4a833be3750b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996256"
---
# <a name="iamtimelinecompgetcountoftype-method"></a><span data-ttu-id="66af7-103">IAMTimelineComp：： GetCountOfType 方法</span><span class="sxs-lookup"><span data-stu-id="66af7-103">IAMTimelineComp::GetCountOfType method</span></span>

> [!Note]  
> <span data-ttu-id="66af7-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="66af7-104">\[Deprecated.</span></span> <span data-ttu-id="66af7-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="66af7-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="66af7-106">`GetCountOfType`方法會以遞迴方式抓取此組合中所包含之指定型別的物件數目及其所有虛擬追蹤。</span><span class="sxs-lookup"><span data-stu-id="66af7-106">The `GetCountOfType` method retrieves the number of objects of a given type contained in this composition and all its virtual tracks, recursively.</span></span>

## <a name="syntax"></a><span data-ttu-id="66af7-107">語法</span><span class="sxs-lookup"><span data-stu-id="66af7-107">Syntax</span></span>


```C++
HRESULT GetCountOfType(
   long                *pVal,
   long                *pValWithComps,
   TIMELINE_MAJOR_TYPE MajorType
);
```



## <a name="parameters"></a><span data-ttu-id="66af7-108">參數</span><span class="sxs-lookup"><span data-stu-id="66af7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66af7-109">*pVal*</span><span class="sxs-lookup"><span data-stu-id="66af7-109">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="66af7-110">以遞迴方式接收此組合中所包含之指定類型的物件數目及其所有虛擬追蹤。</span><span class="sxs-lookup"><span data-stu-id="66af7-110">Receives the number of objects of the specified type contained in this composition and all its virtual tracks, recursively.</span></span>

</dd> <dt>

<span data-ttu-id="66af7-111">*pValWithComps*</span><span class="sxs-lookup"><span data-stu-id="66af7-111">*pValWithComps*</span></span> 
</dt> <dd>

<span data-ttu-id="66af7-112">接收在 *pVal* 中傳回的計數加上所搜尋的組合數目（包含此項）。</span><span class="sxs-lookup"><span data-stu-id="66af7-112">Receives the count returned in *pVal* plus the number of compositions searched, including this one.</span></span>

</dd> <dt>

<span data-ttu-id="66af7-113">*MajorType*</span><span class="sxs-lookup"><span data-stu-id="66af7-113">*MajorType*</span></span> 
</dt> <dd>

<span data-ttu-id="66af7-114">[**時間軸 \_ 主要 \_ 類型**](timeline-major-type.md)列舉類型的成員，指定要計算的物件類型。</span><span class="sxs-lookup"><span data-stu-id="66af7-114">Member of the [**TIMELINE\_MAJOR\_TYPE**](timeline-major-type.md) enumerated type, specifying the type of object to count.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66af7-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="66af7-115">Return value</span></span>

<span data-ttu-id="66af7-116">\_如果成功，則傳回 [確定]，否則傳回 E \_ 指標。</span><span class="sxs-lookup"><span data-stu-id="66af7-116">Returns S\_OK if successful, or E\_POINTER otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="66af7-117">備註</span><span class="sxs-lookup"><span data-stu-id="66af7-117">Remarks</span></span>

<span data-ttu-id="66af7-118">一般來說，應用程式不會呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="66af7-118">Typically, an application will not call this method.</span></span> <span data-ttu-id="66af7-119">它是由轉譯引擎所呼叫。</span><span class="sxs-lookup"><span data-stu-id="66af7-119">It is called by the render engine.</span></span>

<span data-ttu-id="66af7-120">如果您計算組合，在 *pVal* 中傳回的值為零，而在 *pValWithComps* 中傳回的值是組合的數目。</span><span class="sxs-lookup"><span data-stu-id="66af7-120">If you count compositions, the value returned in *pVal* is zero and the value returned in *pValWithComps* is the number of compositions.</span></span> <span data-ttu-id="66af7-121">*\* PValWithComps* 的值包含您用來呼叫方法的組合。</span><span class="sxs-lookup"><span data-stu-id="66af7-121">The value of *\*pValWithComps* includes the composition on which you call the method.</span></span> <span data-ttu-id="66af7-122">例如，如果您在空的組合上呼叫這個方法，則 *\* pValWithComps* 等於1。</span><span class="sxs-lookup"><span data-stu-id="66af7-122">For example, if you call this method on an empty composition, *\*pValWithComps* equals 1.</span></span>

<span data-ttu-id="66af7-123">群組不能位於組合內，因此您無法使用這個方法來計算群組。</span><span class="sxs-lookup"><span data-stu-id="66af7-123">Groups cannot reside inside compositions, so you cannot use this method to count groups.</span></span> <span data-ttu-id="66af7-124"> (傳回的計數一律為零。 ) 若要計算群組，請呼叫 [**IAMTimeline：： GetGroupCount**](iamtimeline-getgroupcount.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="66af7-124">(The returned count will always be zero.) To count groups, call the [**IAMTimeline::GetGroupCount**](iamtimeline-getgroupcount.md) method.</span></span>

> [!Note]  
> <span data-ttu-id="66af7-125">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="66af7-125">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="66af7-126">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="66af7-126">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="66af7-127">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="66af7-127">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="66af7-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="66af7-128">Requirements</span></span>



| <span data-ttu-id="66af7-129">需求</span><span class="sxs-lookup"><span data-stu-id="66af7-129">Requirement</span></span> | <span data-ttu-id="66af7-130">值</span><span class="sxs-lookup"><span data-stu-id="66af7-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="66af7-131">標頭</span><span class="sxs-lookup"><span data-stu-id="66af7-131">Header</span></span><br/>  | <dl> <span data-ttu-id="66af7-132"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="66af7-132"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="66af7-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="66af7-133">Library</span></span><br/> | <dl> <span data-ttu-id="66af7-134"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="66af7-134"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66af7-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="66af7-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66af7-136">**IAMTimelineComp 介面**</span><span class="sxs-lookup"><span data-stu-id="66af7-136">**IAMTimelineComp Interface**</span></span>](iamtimelinecomp.md)
</dt> <dt>

[<span data-ttu-id="66af7-137">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="66af7-137">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




