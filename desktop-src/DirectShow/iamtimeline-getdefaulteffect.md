---
description: GetDefaultEffect 方法會抓取預設效果。 如果轉譯引擎無法轉譯效果，則會替代預設效果。
ms.assetid: 27eec6e8-702f-4e56-8d81-aa0633b8ec68
title: 'IAMTimeline：： GetDefaultEffect 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetDefaultEffect
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a0b1cf356a9c067ccae246814d2e1f381d7f78e5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987885"
---
# <a name="iamtimelinegetdefaulteffect-method"></a><span data-ttu-id="64768-104">IAMTimeline：： GetDefaultEffect 方法</span><span class="sxs-lookup"><span data-stu-id="64768-104">IAMTimeline::GetDefaultEffect method</span></span>

> [!Note]  
> <span data-ttu-id="64768-105">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="64768-105">\[Deprecated.</span></span> <span data-ttu-id="64768-106">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="64768-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="64768-107">方法會抓取 `GetDefaultEffect` 預設效果。</span><span class="sxs-lookup"><span data-stu-id="64768-107">The `GetDefaultEffect` method retrieves the default effect.</span></span> <span data-ttu-id="64768-108">如果轉譯引擎無法轉譯效果，則會替代預設效果。</span><span class="sxs-lookup"><span data-stu-id="64768-108">If the render engine cannot render an effect, it substitutes the default effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="64768-109">語法</span><span class="sxs-lookup"><span data-stu-id="64768-109">Syntax</span></span>


```C++
HRESULT GetDefaultEffect(
   GUID *pGuid
);
```



## <a name="parameters"></a><span data-ttu-id="64768-110">參數</span><span class="sxs-lookup"><span data-stu-id="64768-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64768-111">*pGuid*</span><span class="sxs-lookup"><span data-stu-id="64768-111">*pGuid*</span></span> 
</dt> <dd>

<span data-ttu-id="64768-112">接收預設效果 (GUID) 的全域唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="64768-112">Receives the globally unique identifier (GUID) of the default effect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64768-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="64768-113">Return value</span></span>

<span data-ttu-id="64768-114">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="64768-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="64768-115">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="64768-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="64768-116">備註</span><span class="sxs-lookup"><span data-stu-id="64768-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="64768-117">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="64768-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="64768-118">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="64768-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="64768-119">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="64768-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="64768-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="64768-120">Requirements</span></span>



| <span data-ttu-id="64768-121">需求</span><span class="sxs-lookup"><span data-stu-id="64768-121">Requirement</span></span> | <span data-ttu-id="64768-122">值</span><span class="sxs-lookup"><span data-stu-id="64768-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="64768-123">標頭</span><span class="sxs-lookup"><span data-stu-id="64768-123">Header</span></span><br/>  | <dl> <span data-ttu-id="64768-124"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="64768-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="64768-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="64768-125">Library</span></span><br/> | <dl> <span data-ttu-id="64768-126"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="64768-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64768-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="64768-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64768-128">**IAMTimeline 介面**</span><span class="sxs-lookup"><span data-stu-id="64768-128">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="64768-129">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="64768-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




