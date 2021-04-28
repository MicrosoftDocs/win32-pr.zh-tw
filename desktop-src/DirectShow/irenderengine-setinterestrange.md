---
description: IRenderEngine：： SetInterestRange 方法-不支援。
ms.assetid: 1e4c3bd4-2540-428f-9ca6-dd4c65c53434
title: IRenderEngine：： SetInterestRange 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetInterestRange
api_type:
- COM
api_location: ''
ms.openlocfilehash: ec9790e65efa30b83cf324da4153f20c541733b9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084456"
---
# <a name="irenderenginesetinterestrange-method"></a><span data-ttu-id="6ae5c-103">IRenderEngine：： SetInterestRange 方法</span><span class="sxs-lookup"><span data-stu-id="6ae5c-103">IRenderEngine::SetInterestRange method</span></span>

> [!Note]  
> <span data-ttu-id="6ae5c-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="6ae5c-104">\[Deprecated.</span></span> <span data-ttu-id="6ae5c-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="6ae5c-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="6ae5c-106">不支援。</span><span class="sxs-lookup"><span data-stu-id="6ae5c-106">Not supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ae5c-107">語法</span><span class="sxs-lookup"><span data-stu-id="6ae5c-107">Syntax</span></span>


```C++
HRESULT SetInterestRange(
   REFERENCE_TIME Start,
   REFERENCE_TIME Stop
);
```



## <a name="parameters"></a><span data-ttu-id="6ae5c-108">參數</span><span class="sxs-lookup"><span data-stu-id="6ae5c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ae5c-109">*開始*</span><span class="sxs-lookup"><span data-stu-id="6ae5c-109">*Start*</span></span> 
</dt> <dd>

<span data-ttu-id="6ae5c-110">保留的。</span><span class="sxs-lookup"><span data-stu-id="6ae5c-110">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="6ae5c-111">*停止*</span><span class="sxs-lookup"><span data-stu-id="6ae5c-111">*Stop*</span></span> 
</dt> <dd>

<span data-ttu-id="6ae5c-112">保留的。</span><span class="sxs-lookup"><span data-stu-id="6ae5c-112">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ae5c-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="6ae5c-113">Return value</span></span>

<span data-ttu-id="6ae5c-114">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="6ae5c-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6ae5c-115">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="6ae5c-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ae5c-116">備註</span><span class="sxs-lookup"><span data-stu-id="6ae5c-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6ae5c-117">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="6ae5c-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="6ae5c-118">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="6ae5c-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="6ae5c-119">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="6ae5c-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="6ae5c-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6ae5c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ae5c-121">**IRenderEngine 介面**</span><span class="sxs-lookup"><span data-stu-id="6ae5c-121">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> </dl>

 

 



