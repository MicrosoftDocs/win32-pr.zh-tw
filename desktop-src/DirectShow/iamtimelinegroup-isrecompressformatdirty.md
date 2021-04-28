---
description: IAMTimelineGroup：： IsRecompressFormatDirty 方法-不支援。
ms.assetid: 4fd6b9d9-1749-44e6-884a-16faeced4ed6
title: 'IAMTimelineGroup：： IsRecompressFormatDirty 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.IsRecompressFormatDirty
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 842b4178f93505a2848fa01aa055541943fb3c22
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098616"
---
# <a name="iamtimelinegroupisrecompressformatdirty-method"></a><span data-ttu-id="e7b27-103">IAMTimelineGroup：： IsRecompressFormatDirty 方法</span><span class="sxs-lookup"><span data-stu-id="e7b27-103">IAMTimelineGroup::IsRecompressFormatDirty method</span></span>

> [!Note]  
> <span data-ttu-id="e7b27-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="e7b27-104">\[Deprecated.</span></span> <span data-ttu-id="e7b27-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="e7b27-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e7b27-106">不支援。</span><span class="sxs-lookup"><span data-stu-id="e7b27-106">Not supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7b27-107">語法</span><span class="sxs-lookup"><span data-stu-id="e7b27-107">Syntax</span></span>


```C++
HRESULT IsRecompressFormatDirty(
   BOOL *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="e7b27-108">參數</span><span class="sxs-lookup"><span data-stu-id="e7b27-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7b27-109">*pVal*</span><span class="sxs-lookup"><span data-stu-id="e7b27-109">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="e7b27-110">保留的。</span><span class="sxs-lookup"><span data-stu-id="e7b27-110">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7b27-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="e7b27-111">Return value</span></span>

<span data-ttu-id="e7b27-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="e7b27-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e7b27-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="e7b27-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7b27-114">備註</span><span class="sxs-lookup"><span data-stu-id="e7b27-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e7b27-115">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="e7b27-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e7b27-116">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="e7b27-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e7b27-117">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="e7b27-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e7b27-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="e7b27-118">Requirements</span></span>



| <span data-ttu-id="e7b27-119">需求</span><span class="sxs-lookup"><span data-stu-id="e7b27-119">Requirement</span></span> | <span data-ttu-id="e7b27-120">值</span><span class="sxs-lookup"><span data-stu-id="e7b27-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e7b27-121">標頭</span><span class="sxs-lookup"><span data-stu-id="e7b27-121">Header</span></span><br/>  | <dl> <span data-ttu-id="e7b27-122"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="e7b27-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e7b27-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="e7b27-123">Library</span></span><br/> | <dl> <span data-ttu-id="e7b27-124"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e7b27-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7b27-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e7b27-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7b27-126">**IAMTimelineGroup 介面**</span><span class="sxs-lookup"><span data-stu-id="e7b27-126">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> </dl>

 

 




