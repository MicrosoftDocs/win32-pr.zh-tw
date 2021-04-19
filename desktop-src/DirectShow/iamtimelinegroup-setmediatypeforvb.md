---
description: SetMediaTypeForVB 方法會指定 Automation 用戶端的群組媒體類型。
ms.assetid: 86f52088-a0dd-40be-98a0-8adc09b264dd
title: 'IAMTimelineGroup：： SetMediaTypeForVB 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetMediaTypeForVB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 1371b1d6c906666ca30e5df2d26dbe20eddf1745
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997787"
---
# <a name="iamtimelinegroupsetmediatypeforvb-method"></a><span data-ttu-id="03287-103">IAMTimelineGroup：： SetMediaTypeForVB 方法</span><span class="sxs-lookup"><span data-stu-id="03287-103">IAMTimelineGroup::SetMediaTypeForVB method</span></span>

> [!Note]  
> <span data-ttu-id="03287-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="03287-104">\[Deprecated.</span></span> <span data-ttu-id="03287-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="03287-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="03287-106">`SetMediaTypeForVB`方法會指定 Automation 用戶端的群組媒體類型。</span><span class="sxs-lookup"><span data-stu-id="03287-106">The `SetMediaTypeForVB` method specifies the group media type, for Automation clients.</span></span>

## <a name="syntax"></a><span data-ttu-id="03287-107">語法</span><span class="sxs-lookup"><span data-stu-id="03287-107">Syntax</span></span>


```C++
HRESULT SetMediaTypeForVB(
  [in] long Val
);
```



## <a name="parameters"></a><span data-ttu-id="03287-108">參數</span><span class="sxs-lookup"><span data-stu-id="03287-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03287-109">*Val* \[在\]</span><span class="sxs-lookup"><span data-stu-id="03287-109">*Val* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03287-110">指定媒體類型的值。</span><span class="sxs-lookup"><span data-stu-id="03287-110">Value that specifies the media type.</span></span> <span data-ttu-id="03287-111">將影片的值設定為0，或將音訊的值設定為1。</span><span class="sxs-lookup"><span data-stu-id="03287-111">Set the value to 0 for video, or 1 for audio.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03287-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="03287-112">Return value</span></span>

<span data-ttu-id="03287-113">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="03287-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="03287-114">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="03287-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="03287-115">備註</span><span class="sxs-lookup"><span data-stu-id="03287-115">Remarks</span></span>

<span data-ttu-id="03287-116">此方法適用于 Automation 用戶端。</span><span class="sxs-lookup"><span data-stu-id="03287-116">This method is intended for Automation clients.</span></span> <span data-ttu-id="03287-117">若是 c + + 應用程式，請使用 [**IAMTimelineGroup：： SetMediaType**](iamtimelinegroup-setmediatype.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="03287-117">For C++ applications, use the [**IAMTimelineGroup::SetMediaType**](iamtimelinegroup-setmediatype.md) method.</span></span>

> [!Note]  
> <span data-ttu-id="03287-118">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="03287-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="03287-119">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="03287-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="03287-120">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="03287-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="03287-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="03287-121">Requirements</span></span>



| <span data-ttu-id="03287-122">需求</span><span class="sxs-lookup"><span data-stu-id="03287-122">Requirement</span></span> | <span data-ttu-id="03287-123">值</span><span class="sxs-lookup"><span data-stu-id="03287-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="03287-124">標頭</span><span class="sxs-lookup"><span data-stu-id="03287-124">Header</span></span><br/>  | <dl> <span data-ttu-id="03287-125"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="03287-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="03287-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="03287-126">Library</span></span><br/> | <dl> <span data-ttu-id="03287-127"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="03287-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03287-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="03287-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03287-129">**IAMTimelineGroup 介面**</span><span class="sxs-lookup"><span data-stu-id="03287-129">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="03287-130">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="03287-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




