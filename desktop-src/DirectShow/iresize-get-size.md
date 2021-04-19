---
description: Get \_ Size 方法會傳回目前的輸出大小和延展模式。
ms.assetid: 61c0e439-26ce-45fc-986a-0ffc17056a55
title: 'IResize：： get_Size 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize.get_Size
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b9fe4971fd9ede0f695fe06a4102da8243e7c720
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996277"
---
# <a name="iresizeget_size-method"></a><span data-ttu-id="5abe8-103">IResize：： get \_ Size 方法</span><span class="sxs-lookup"><span data-stu-id="5abe8-103">IResize::get\_Size method</span></span>

> [!Note]  
> <span data-ttu-id="5abe8-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="5abe8-104">\[Deprecated.</span></span> <span data-ttu-id="5abe8-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="5abe8-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="5abe8-106">方法會傳回 `get_Size` 目前的輸出大小和延展模式。</span><span class="sxs-lookup"><span data-stu-id="5abe8-106">The `get_Size` method returns the current output size and stretch mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="5abe8-107">語法</span><span class="sxs-lookup"><span data-stu-id="5abe8-107">Syntax</span></span>


```C++
HRESULT get_Size(
  [out] int  *piHeight,
  [out] int  *piWidth,
  [out] long *pFlag
);
```



## <a name="parameters"></a><span data-ttu-id="5abe8-108">參數</span><span class="sxs-lookup"><span data-stu-id="5abe8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5abe8-109">*piHeight* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="5abe8-109">*piHeight* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5abe8-110">接收影片高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="5abe8-110">Receives the video height, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="5abe8-111">*piWidth* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="5abe8-111">*piWidth* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5abe8-112">接收影片寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="5abe8-112">Receives the video width, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="5abe8-113">*pFlag* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="5abe8-113">*pFlag* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5abe8-114">接收指定延展模式的旗標。</span><span class="sxs-lookup"><span data-stu-id="5abe8-114">Receives a flag specifying the stretch mode.</span></span> <span data-ttu-id="5abe8-115">請參閱重 [**設大小旗標**](resize-flags.md) 的可能值。</span><span class="sxs-lookup"><span data-stu-id="5abe8-115">See [**Resize Flags**](resize-flags.md) for possible values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5abe8-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="5abe8-116">Return value</span></span>

<span data-ttu-id="5abe8-117">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="5abe8-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5abe8-118">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="5abe8-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5abe8-119">備註</span><span class="sxs-lookup"><span data-stu-id="5abe8-119">Remarks</span></span>

<span data-ttu-id="5abe8-120">如果輸出類型尚未設定，則篩選準則應該會傳回預設值。</span><span class="sxs-lookup"><span data-stu-id="5abe8-120">If the output type has not been set, the filter should return default values.</span></span> <span data-ttu-id="5abe8-121">這些值可在設計階段任意選擇。</span><span class="sxs-lookup"><span data-stu-id="5abe8-121">These values can be arbitrarily chosen at design time.</span></span>

> [!Note]  
> <span data-ttu-id="5abe8-122">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="5abe8-122">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="5abe8-123">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="5abe8-123">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="5abe8-124">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="5abe8-124">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5abe8-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="5abe8-125">Requirements</span></span>



| <span data-ttu-id="5abe8-126">需求</span><span class="sxs-lookup"><span data-stu-id="5abe8-126">Requirement</span></span> | <span data-ttu-id="5abe8-127">值</span><span class="sxs-lookup"><span data-stu-id="5abe8-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5abe8-128">版本</span><span class="sxs-lookup"><span data-stu-id="5abe8-128">Version</span></span><br/> | <span data-ttu-id="5abe8-129">DirectX 9.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="5abe8-129">DirectX 9.0 or later</span></span><br/>                                                         |
| <span data-ttu-id="5abe8-130">標頭</span><span class="sxs-lookup"><span data-stu-id="5abe8-130">Header</span></span><br/>  | <dl> <span data-ttu-id="5abe8-131"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="5abe8-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="5abe8-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="5abe8-132">Library</span></span><br/> | <dl> <span data-ttu-id="5abe8-133"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="5abe8-133"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5abe8-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5abe8-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5abe8-135">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="5abe8-135">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="5abe8-136">**IResize 介面**</span><span class="sxs-lookup"><span data-stu-id="5abe8-136">**IResize Interface**</span></span>](iresize.md)
</dt> </dl>

 

 




