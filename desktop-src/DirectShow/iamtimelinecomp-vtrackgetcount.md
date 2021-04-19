---
description: VTrackGetCount 方法會抓取組合中包含的虛擬追蹤數目。
ms.assetid: a8117b06-4f42-45da-9b93-f547cb70aa5d
title: 'IAMTimelineComp：： VTrackGetCount 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.VTrackGetCount
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 36800381ce50ea60d5252841d9731b2657fc22cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001165"
---
# <a name="iamtimelinecompvtrackgetcount-method"></a><span data-ttu-id="4a516-103">IAMTimelineComp：： VTrackGetCount 方法</span><span class="sxs-lookup"><span data-stu-id="4a516-103">IAMTimelineComp::VTrackGetCount method</span></span>

> [!Note]  
> <span data-ttu-id="4a516-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="4a516-104">\[Deprecated.</span></span> <span data-ttu-id="4a516-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="4a516-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="4a516-106">方法會抓取 `VTrackGetCount` 組合中包含的虛擬追蹤數目。</span><span class="sxs-lookup"><span data-stu-id="4a516-106">The `VTrackGetCount` method retrieves the number of virtual tracks contained in the composition.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a516-107">語法</span><span class="sxs-lookup"><span data-stu-id="4a516-107">Syntax</span></span>


```C++
HRESULT VTrackGetCount(
   long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="4a516-108">參數</span><span class="sxs-lookup"><span data-stu-id="4a516-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a516-109">*pVal*</span><span class="sxs-lookup"><span data-stu-id="4a516-109">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="4a516-110">接收虛擬追蹤的數目。</span><span class="sxs-lookup"><span data-stu-id="4a516-110">Receives the number of virtual tracks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a516-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="4a516-111">Return value</span></span>

<span data-ttu-id="4a516-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="4a516-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4a516-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="4a516-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a516-114">備註</span><span class="sxs-lookup"><span data-stu-id="4a516-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4a516-115">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="4a516-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="4a516-116">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="4a516-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="4a516-117">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="4a516-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4a516-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="4a516-118">Requirements</span></span>



| <span data-ttu-id="4a516-119">需求</span><span class="sxs-lookup"><span data-stu-id="4a516-119">Requirement</span></span> | <span data-ttu-id="4a516-120">值</span><span class="sxs-lookup"><span data-stu-id="4a516-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4a516-121">標頭</span><span class="sxs-lookup"><span data-stu-id="4a516-121">Header</span></span><br/>  | <dl> <span data-ttu-id="4a516-122"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="4a516-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="4a516-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="4a516-123">Library</span></span><br/> | <dl> <span data-ttu-id="4a516-124"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="4a516-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a516-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4a516-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a516-126">**IAMTimelineComp 介面**</span><span class="sxs-lookup"><span data-stu-id="4a516-126">**IAMTimelineComp Interface**</span></span>](iamtimelinecomp.md)
</dt> <dt>

[<span data-ttu-id="4a516-127">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="4a516-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




