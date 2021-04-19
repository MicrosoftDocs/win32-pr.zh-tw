---
description: GetGroup 方法會抓取指定的群組。
ms.assetid: 4ff651e5-a3aa-4da9-af23-a3a2bdbf7c5b
title: 'IAMTimeline：： GetGroup 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetGroup
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 1241a125698cf78c1138d9264ecd8c73ff78056c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000700"
---
# <a name="iamtimelinegetgroup-method"></a><span data-ttu-id="beefd-103">IAMTimeline：： GetGroup 方法</span><span class="sxs-lookup"><span data-stu-id="beefd-103">IAMTimeline::GetGroup method</span></span>

> [!Note]  
> <span data-ttu-id="beefd-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="beefd-104">\[Deprecated.</span></span> <span data-ttu-id="beefd-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="beefd-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="beefd-106">方法會抓取 `GetGroup` 指定的群組。</span><span class="sxs-lookup"><span data-stu-id="beefd-106">The `GetGroup` method retrieves a specified group.</span></span>

## <a name="syntax"></a><span data-ttu-id="beefd-107">語法</span><span class="sxs-lookup"><span data-stu-id="beefd-107">Syntax</span></span>


```C++
HRESULT GetGroup(
  [out] IAMTimelineObj **ppGroup,
        long           WhichGroup
);
```



## <a name="parameters"></a><span data-ttu-id="beefd-108">參數</span><span class="sxs-lookup"><span data-stu-id="beefd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="beefd-109">*ppGroup* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="beefd-109">*ppGroup* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="beefd-110">接收群組 [**IAMTimelineObj**](iamtimelineobj.md) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="beefd-110">Receives a pointer to the group's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="beefd-111">*WhichGroup*</span><span class="sxs-lookup"><span data-stu-id="beefd-111">*WhichGroup*</span></span> 
</dt> <dd>

<span data-ttu-id="beefd-112">要抓取的群組索引（依據群組新增至時間軸的順序）。</span><span class="sxs-lookup"><span data-stu-id="beefd-112">Index of the group to retrieve, based on the order in which the groups were added to the timeline.</span></span> <span data-ttu-id="beefd-113">新增至時間軸的第一個群組索引為0。</span><span class="sxs-lookup"><span data-stu-id="beefd-113">The first group added to the timeline has an index of 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="beefd-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="beefd-114">Return value</span></span>

<span data-ttu-id="beefd-115">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="beefd-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="beefd-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="beefd-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="beefd-117">備註</span><span class="sxs-lookup"><span data-stu-id="beefd-117">Remarks</span></span>

<span data-ttu-id="beefd-118">如果方法成功，則傳回的 **IAMTimelineObj** 介面具有未處理的參考計數。</span><span class="sxs-lookup"><span data-stu-id="beefd-118">If the method succeeds, the **IAMTimelineObj** interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="beefd-119">使用完畢後，請務必釋放介面。</span><span class="sxs-lookup"><span data-stu-id="beefd-119">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="beefd-120">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="beefd-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="beefd-121">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="beefd-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="beefd-122">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="beefd-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="beefd-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="beefd-123">Requirements</span></span>



| <span data-ttu-id="beefd-124">需求</span><span class="sxs-lookup"><span data-stu-id="beefd-124">Requirement</span></span> | <span data-ttu-id="beefd-125">值</span><span class="sxs-lookup"><span data-stu-id="beefd-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="beefd-126">標頭</span><span class="sxs-lookup"><span data-stu-id="beefd-126">Header</span></span><br/>  | <dl> <span data-ttu-id="beefd-127"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="beefd-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="beefd-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="beefd-128">Library</span></span><br/> | <dl> <span data-ttu-id="beefd-129"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="beefd-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="beefd-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="beefd-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="beefd-131">**IAMTimeline 介面**</span><span class="sxs-lookup"><span data-stu-id="beefd-131">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="beefd-132">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="beefd-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




