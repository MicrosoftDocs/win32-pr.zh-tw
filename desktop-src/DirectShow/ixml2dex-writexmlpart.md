---
description: IXml2Dex：： WriteXMLPart 方法-未執行。
ms.assetid: d0fc571f-79f5-448a-8082-6e5f7f48118f
title: IXml2Dex：： WriteXMLPart 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex.WriteXMLPart
api_type:
- COM
api_location: ''
ms.openlocfilehash: 957fa74f09a79f94e2e0feb35c418a711c91c1b0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084356"
---
# <a name="ixml2dexwritexmlpart-method"></a><span data-ttu-id="eeb7d-103">IXml2Dex：： WriteXMLPart 方法</span><span class="sxs-lookup"><span data-stu-id="eeb7d-103">IXml2Dex::WriteXMLPart method</span></span>

> [!Note]  
> <span data-ttu-id="eeb7d-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="eeb7d-104">\[Deprecated.</span></span> <span data-ttu-id="eeb7d-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="eeb7d-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="eeb7d-106">未實作。</span><span class="sxs-lookup"><span data-stu-id="eeb7d-106">Not implemented.</span></span>

## <a name="syntax"></a><span data-ttu-id="eeb7d-107">語法</span><span class="sxs-lookup"><span data-stu-id="eeb7d-107">Syntax</span></span>


```C++
HRESULT WriteXMLPart(
   IUnknown *pTimeline,
   double   dStart,
   double   dEnd,
   BSTR     FileName
);
```



## <a name="parameters"></a><span data-ttu-id="eeb7d-108">參數</span><span class="sxs-lookup"><span data-stu-id="eeb7d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eeb7d-109">*pTimeline*</span><span class="sxs-lookup"><span data-stu-id="eeb7d-109">*pTimeline*</span></span> 
</dt> <dd>

<span data-ttu-id="eeb7d-110">保留的。</span><span class="sxs-lookup"><span data-stu-id="eeb7d-110">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="eeb7d-111">*dStart*</span><span class="sxs-lookup"><span data-stu-id="eeb7d-111">*dStart*</span></span> 
</dt> <dd>

<span data-ttu-id="eeb7d-112">保留的。</span><span class="sxs-lookup"><span data-stu-id="eeb7d-112">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="eeb7d-113">*dEnd*</span><span class="sxs-lookup"><span data-stu-id="eeb7d-113">*dEnd*</span></span> 
</dt> <dd>

<span data-ttu-id="eeb7d-114">保留的。</span><span class="sxs-lookup"><span data-stu-id="eeb7d-114">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="eeb7d-115">*FileName*</span><span class="sxs-lookup"><span data-stu-id="eeb7d-115">*FileName*</span></span> 
</dt> <dd>

<span data-ttu-id="eeb7d-116">保留的。</span><span class="sxs-lookup"><span data-stu-id="eeb7d-116">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eeb7d-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="eeb7d-117">Return value</span></span>

<span data-ttu-id="eeb7d-118">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="eeb7d-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="eeb7d-119">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="eeb7d-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="eeb7d-120">備註</span><span class="sxs-lookup"><span data-stu-id="eeb7d-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="eeb7d-121">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="eeb7d-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="eeb7d-122">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="eeb7d-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="eeb7d-123">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="eeb7d-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="eeb7d-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eeb7d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eeb7d-125">**IXml2Dex 介面**</span><span class="sxs-lookup"><span data-stu-id="eeb7d-125">**IXml2Dex Interface**</span></span>](ixml2dex.md)
</dt> </dl>

 

 



