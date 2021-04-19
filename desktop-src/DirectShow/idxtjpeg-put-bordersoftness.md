---
description: Put \_ BorderSoftness 方法會指定抹除模式邊緣周圍模糊區域的寬度。
ms.assetid: 9fdbda7f-c89b-4ed8-8035-054bc28f3231
title: 'IDxtJpeg：:p ut_BorderSoftness 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_BorderSoftness
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4c72f59798ca84d01be79110cd4792da0a77f408
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001854"
---
# <a name="idxtjpegput_bordersoftness-method"></a><span data-ttu-id="26742-103">IDxtJpeg：:p 的 \_ BorderSoftness 方法</span><span class="sxs-lookup"><span data-stu-id="26742-103">IDxtJpeg::put\_BorderSoftness method</span></span>

> [!Note]  
> <span data-ttu-id="26742-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="26742-104">\[Deprecated.</span></span> <span data-ttu-id="26742-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="26742-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="26742-106">`put_BorderSoftness`方法會指定抹除模式邊緣周圍模糊區域的寬度。</span><span class="sxs-lookup"><span data-stu-id="26742-106">The `put_BorderSoftness` method specifies the width of the blurry region around the edges of the wipe pattern.</span></span>

## <a name="syntax"></a><span data-ttu-id="26742-107">語法</span><span class="sxs-lookup"><span data-stu-id="26742-107">Syntax</span></span>


```C++
HRESULT put_BorderSoftness(
  [in] long newVal
);
```



## <a name="parameters"></a><span data-ttu-id="26742-108">參數</span><span class="sxs-lookup"><span data-stu-id="26742-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26742-109">*newVal* \[在\]</span><span class="sxs-lookup"><span data-stu-id="26742-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26742-110">模糊區域的寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="26742-110">The width of the blurry region, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26742-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="26742-111">Return value</span></span>

<span data-ttu-id="26742-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="26742-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="26742-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="26742-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="26742-114">備註</span><span class="sxs-lookup"><span data-stu-id="26742-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="26742-115">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="26742-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="26742-116">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="26742-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="26742-117">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="26742-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="26742-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="26742-118">Requirements</span></span>



| <span data-ttu-id="26742-119">需求</span><span class="sxs-lookup"><span data-stu-id="26742-119">Requirement</span></span> | <span data-ttu-id="26742-120">值</span><span class="sxs-lookup"><span data-stu-id="26742-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="26742-121">標頭</span><span class="sxs-lookup"><span data-stu-id="26742-121">Header</span></span><br/>  | <dl> <span data-ttu-id="26742-122"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="26742-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="26742-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="26742-123">Library</span></span><br/> | <dl> <span data-ttu-id="26742-124"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="26742-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26742-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="26742-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26742-126">**IDxtJpeg 介面**</span><span class="sxs-lookup"><span data-stu-id="26742-126">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




