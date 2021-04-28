---
description: IXml2Dex：:P asteXMLFile 方法-未執行。
ms.assetid: 25300ba5-3578-4eb3-99e2-d547dbb2b9ee
title: IXml2Dex：:P asteXMLFile 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex.PasteXMLFile
api_type:
- COM
api_location: ''
ms.openlocfilehash: 415e71d87d8e8d9c7834df0a16fce754651d6a03
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088956"
---
# <a name="ixml2dexpastexmlfile-method"></a><span data-ttu-id="902d5-103">IXml2Dex：:P asteXMLFile 方法</span><span class="sxs-lookup"><span data-stu-id="902d5-103">IXml2Dex::PasteXMLFile method</span></span>

> [!Note]  
> <span data-ttu-id="902d5-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="902d5-104">\[Deprecated.</span></span> <span data-ttu-id="902d5-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="902d5-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="902d5-106">未實作。</span><span class="sxs-lookup"><span data-stu-id="902d5-106">Not implemented.</span></span>

## <a name="syntax"></a><span data-ttu-id="902d5-107">語法</span><span class="sxs-lookup"><span data-stu-id="902d5-107">Syntax</span></span>


```C++
HRESULT PasteXMLFile(
   IUnknown *pTimeline,
   double   dStart,
   BSTR     FileName
);
```



## <a name="parameters"></a><span data-ttu-id="902d5-108">參數</span><span class="sxs-lookup"><span data-stu-id="902d5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="902d5-109">*pTimeline*</span><span class="sxs-lookup"><span data-stu-id="902d5-109">*pTimeline*</span></span> 
</dt> <dd>

<span data-ttu-id="902d5-110">保留的。</span><span class="sxs-lookup"><span data-stu-id="902d5-110">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="902d5-111">*dStart*</span><span class="sxs-lookup"><span data-stu-id="902d5-111">*dStart*</span></span> 
</dt> <dd>

<span data-ttu-id="902d5-112">保留的。</span><span class="sxs-lookup"><span data-stu-id="902d5-112">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="902d5-113">*FileName*</span><span class="sxs-lookup"><span data-stu-id="902d5-113">*FileName*</span></span> 
</dt> <dd>

<span data-ttu-id="902d5-114">保留的。</span><span class="sxs-lookup"><span data-stu-id="902d5-114">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="902d5-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="902d5-115">Return value</span></span>

<span data-ttu-id="902d5-116">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="902d5-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="902d5-117">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="902d5-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="902d5-118">備註</span><span class="sxs-lookup"><span data-stu-id="902d5-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="902d5-119">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="902d5-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="902d5-120">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="902d5-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="902d5-121">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="902d5-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="902d5-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="902d5-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="902d5-123">**IXml2Dex 介面**</span><span class="sxs-lookup"><span data-stu-id="902d5-123">**IXml2Dex Interface**</span></span>](ixml2dex.md)
</dt> </dl>

 

 



