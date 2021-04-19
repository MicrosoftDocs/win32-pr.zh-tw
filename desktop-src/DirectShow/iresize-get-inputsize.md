---
description: Get \_ InputSize 方法會傳回檔整器篩選的目前輸入大小。
ms.assetid: 7066a044-52ea-4851-83f2-f1fb323c2251
title: 'IResize：： get_InputSize 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize.get_InputSize
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fab61edf6dc4469f06437483172161fbbe77e76d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991001"
---
# <a name="iresizeget_inputsize-method"></a><span data-ttu-id="7059c-103">IResize：： get \_ InputSize 方法</span><span class="sxs-lookup"><span data-stu-id="7059c-103">IResize::get\_InputSize method</span></span>

> [!Note]  
> <span data-ttu-id="7059c-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="7059c-104">\[Deprecated.</span></span> <span data-ttu-id="7059c-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="7059c-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="7059c-106">方法會傳回 `get_InputSize` 調整器篩選的目前輸入大小。</span><span class="sxs-lookup"><span data-stu-id="7059c-106">The `get_InputSize` method returns the resizer filter's current input size.</span></span>

## <a name="syntax"></a><span data-ttu-id="7059c-107">語法</span><span class="sxs-lookup"><span data-stu-id="7059c-107">Syntax</span></span>


```C++
HRESULT get_InputSize(
  [out] int *piHeight,
  [out] int *piWidth
);
```



## <a name="parameters"></a><span data-ttu-id="7059c-108">參數</span><span class="sxs-lookup"><span data-stu-id="7059c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7059c-109">*piHeight* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="7059c-109">*piHeight* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7059c-110">接收影片高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="7059c-110">Receives the video height, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="7059c-111">*piWidth* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="7059c-111">*piWidth* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7059c-112">接收影片寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="7059c-112">Receives the video width, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7059c-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="7059c-113">Return value</span></span>

<span data-ttu-id="7059c-114">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="7059c-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7059c-115">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="7059c-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7059c-116">備註</span><span class="sxs-lookup"><span data-stu-id="7059c-116">Remarks</span></span>

<span data-ttu-id="7059c-117">如果篩選的輸入 pin 未連接，則傳回錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="7059c-117">If the filter's input pin is not connected, return an error code.</span></span> <span data-ttu-id="7059c-118">否則，會傳回影片的寬度和高度，如輸入釘選的媒體類型所指定。</span><span class="sxs-lookup"><span data-stu-id="7059c-118">Otherwise, return the width and height of the video, as specified by the input pin's media type.</span></span>

> [!Note]  
> <span data-ttu-id="7059c-119">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="7059c-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="7059c-120">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="7059c-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="7059c-121">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="7059c-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7059c-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="7059c-122">Requirements</span></span>



| <span data-ttu-id="7059c-123">需求</span><span class="sxs-lookup"><span data-stu-id="7059c-123">Requirement</span></span> | <span data-ttu-id="7059c-124">值</span><span class="sxs-lookup"><span data-stu-id="7059c-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7059c-125">版本</span><span class="sxs-lookup"><span data-stu-id="7059c-125">Version</span></span><br/> | <span data-ttu-id="7059c-126">DirectX 9.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="7059c-126">DirectX 9.0 or later</span></span><br/>                                                         |
| <span data-ttu-id="7059c-127">標頭</span><span class="sxs-lookup"><span data-stu-id="7059c-127">Header</span></span><br/>  | <dl> <span data-ttu-id="7059c-128"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="7059c-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="7059c-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="7059c-129">Library</span></span><br/> | <dl> <span data-ttu-id="7059c-130"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="7059c-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7059c-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7059c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7059c-132">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="7059c-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="7059c-133">**IResize 介面**</span><span class="sxs-lookup"><span data-stu-id="7059c-133">**IResize Interface**</span></span>](iresize.md)
</dt> </dl>

 

 




