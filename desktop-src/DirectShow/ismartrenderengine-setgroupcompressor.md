---
description: 指定轉譯指定群組時要使用的壓縮篩選。
ms.assetid: ba717cac-c5a8-4821-a5f0-dd9d5fe4834e
title: 'ISmartRenderEngine：： SetGroupCompressor 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISmartRenderEngine.SetGroupCompressor
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9cb02a9d8daf7e6ba74a45299daa9d45ab63d5db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987851"
---
# <a name="ismartrenderenginesetgroupcompressor-method"></a><span data-ttu-id="d76cd-103">ISmartRenderEngine：： SetGroupCompressor 方法</span><span class="sxs-lookup"><span data-stu-id="d76cd-103">ISmartRenderEngine::SetGroupCompressor method</span></span>

> [!Note]  
> <span data-ttu-id="d76cd-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="d76cd-104">\[Deprecated.</span></span> <span data-ttu-id="d76cd-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="d76cd-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d76cd-106">指定轉譯指定群組時要使用的壓縮篩選。</span><span class="sxs-lookup"><span data-stu-id="d76cd-106">Specifies a compression filter to use when rendering the specified group.</span></span>

## <a name="syntax"></a><span data-ttu-id="d76cd-107">語法</span><span class="sxs-lookup"><span data-stu-id="d76cd-107">Syntax</span></span>


```C++
HRESULT SetGroupCompressor(
   long        Group,
   IBaseFilter *pCompressor
);
```



## <a name="parameters"></a><span data-ttu-id="d76cd-108">參數</span><span class="sxs-lookup"><span data-stu-id="d76cd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d76cd-109">*群組*</span><span class="sxs-lookup"><span data-stu-id="d76cd-109">*Group*</span></span> 
</dt> <dd>

<span data-ttu-id="d76cd-110">群組以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="d76cd-110">Zero-based index of the group.</span></span>

</dd> <dt>

<span data-ttu-id="d76cd-111">*pCompressor*</span><span class="sxs-lookup"><span data-stu-id="d76cd-111">*pCompressor*</span></span> 
</dt> <dd>

<span data-ttu-id="d76cd-112">壓縮篩選之 [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="d76cd-112">Pointer to the [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface of the compression filter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d76cd-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="d76cd-113">Return value</span></span>

<span data-ttu-id="d76cd-114">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="d76cd-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d76cd-115">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="d76cd-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d76cd-116">備註</span><span class="sxs-lookup"><span data-stu-id="d76cd-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d76cd-117">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="d76cd-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="d76cd-118">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="d76cd-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="d76cd-119">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="d76cd-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d76cd-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="d76cd-120">Requirements</span></span>



| <span data-ttu-id="d76cd-121">需求</span><span class="sxs-lookup"><span data-stu-id="d76cd-121">Requirement</span></span> | <span data-ttu-id="d76cd-122">值</span><span class="sxs-lookup"><span data-stu-id="d76cd-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d76cd-123">標頭</span><span class="sxs-lookup"><span data-stu-id="d76cd-123">Header</span></span><br/>  | <dl> <span data-ttu-id="d76cd-124"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="d76cd-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="d76cd-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="d76cd-125">Library</span></span><br/> | <dl> <span data-ttu-id="d76cd-126"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d76cd-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d76cd-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d76cd-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d76cd-128">**ISmartRenderEngine 介面**</span><span class="sxs-lookup"><span data-stu-id="d76cd-128">**ISmartRenderEngine Interface**</span></span>](ismartrenderengine.md)
</dt> <dt>

[<span data-ttu-id="d76cd-129">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="d76cd-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




