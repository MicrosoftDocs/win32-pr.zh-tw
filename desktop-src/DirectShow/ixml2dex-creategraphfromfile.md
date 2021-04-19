---
description: 未實作。
ms.assetid: b476e0c9-1432-4644-8002-154797a2a594
title: IXml2Dex：： CreateGraphFromFile 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex.CreateGraphFromFile
api_type:
- COM
api_location: ''
ms.openlocfilehash: 10a2e52716de77f9c62a51c87cbda550b92a8f90
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106970882"
---
# <a name="ixml2dexcreategraphfromfile-method"></a><span data-ttu-id="bdb43-103">IXml2Dex：： CreateGraphFromFile 方法</span><span class="sxs-lookup"><span data-stu-id="bdb43-103">IXml2Dex::CreateGraphFromFile method</span></span>

> [!Note]  
> <span data-ttu-id="bdb43-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="bdb43-104">\[Deprecated.</span></span> <span data-ttu-id="bdb43-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="bdb43-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="bdb43-106">未實作。</span><span class="sxs-lookup"><span data-stu-id="bdb43-106">Not implemented.</span></span>

## <a name="syntax"></a><span data-ttu-id="bdb43-107">語法</span><span class="sxs-lookup"><span data-stu-id="bdb43-107">Syntax</span></span>


```C++
HRESULT CreateGraphFromFile(
   IUnknown **ppGraph,
   IUnknown *pTimeline,
   BSTR     FileName
);
```



## <a name="parameters"></a><span data-ttu-id="bdb43-108">參數</span><span class="sxs-lookup"><span data-stu-id="bdb43-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bdb43-109">*ppGraph*</span><span class="sxs-lookup"><span data-stu-id="bdb43-109">*ppGraph*</span></span> 
</dt> <dd>

<span data-ttu-id="bdb43-110">保留的。</span><span class="sxs-lookup"><span data-stu-id="bdb43-110">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="bdb43-111">*pTimeline*</span><span class="sxs-lookup"><span data-stu-id="bdb43-111">*pTimeline*</span></span> 
</dt> <dd>

<span data-ttu-id="bdb43-112">保留的。</span><span class="sxs-lookup"><span data-stu-id="bdb43-112">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="bdb43-113">*FileName*</span><span class="sxs-lookup"><span data-stu-id="bdb43-113">*FileName*</span></span> 
</dt> <dd>

<span data-ttu-id="bdb43-114">保留的。</span><span class="sxs-lookup"><span data-stu-id="bdb43-114">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bdb43-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="bdb43-115">Return value</span></span>

<span data-ttu-id="bdb43-116">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="bdb43-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="bdb43-117">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="bdb43-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="bdb43-118">備註</span><span class="sxs-lookup"><span data-stu-id="bdb43-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="bdb43-119">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="bdb43-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="bdb43-120">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="bdb43-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="bdb43-121">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="bdb43-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="bdb43-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bdb43-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdb43-123">**IXml2Dex 介面**</span><span class="sxs-lookup"><span data-stu-id="bdb43-123">**IXml2Dex Interface**</span></span>](ixml2dex.md)
</dt> </dl>

 

 



