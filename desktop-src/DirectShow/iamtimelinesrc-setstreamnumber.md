---
description: SetStreamNumber 方法會指定要從與此來源物件相關聯的來源檔案中讀取的資料流程。
ms.assetid: d40d0889-3b28-4114-9dd2-529e380eaeb8
title: 'IAMTimelineSrc：： SetStreamNumber 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetStreamNumber
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 32deec91d4ae0fe55b4574344dd357932856db81
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994992"
---
# <a name="iamtimelinesrcsetstreamnumber-method"></a><span data-ttu-id="9a24f-103">IAMTimelineSrc：： SetStreamNumber 方法</span><span class="sxs-lookup"><span data-stu-id="9a24f-103">IAMTimelineSrc::SetStreamNumber method</span></span>

> [!Note]  
> <span data-ttu-id="9a24f-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="9a24f-104">\[Deprecated.</span></span> <span data-ttu-id="9a24f-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="9a24f-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="9a24f-106">`SetStreamNumber`方法會指定要從與此來源物件相關聯之來源檔案讀取的資料流程。</span><span class="sxs-lookup"><span data-stu-id="9a24f-106">The `SetStreamNumber` method specifies which stream to read from the source file associated with this source object.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a24f-107">語法</span><span class="sxs-lookup"><span data-stu-id="9a24f-107">Syntax</span></span>


```C++
HRESULT SetStreamNumber(
   long Val
);
```



## <a name="parameters"></a><span data-ttu-id="9a24f-108">參數</span><span class="sxs-lookup"><span data-stu-id="9a24f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a24f-109">*Val*</span><span class="sxs-lookup"><span data-stu-id="9a24f-109">*Val*</span></span> 
</dt> <dd>

<span data-ttu-id="9a24f-110">資料流程號碼，從與父群組之媒體類型相符的資料流程集合中。</span><span class="sxs-lookup"><span data-stu-id="9a24f-110">The stream number, from the set of streams matching the media type of the parent group.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a24f-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="9a24f-111">Return value</span></span>

<span data-ttu-id="9a24f-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="9a24f-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9a24f-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="9a24f-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a24f-114">備註</span><span class="sxs-lookup"><span data-stu-id="9a24f-114">Remarks</span></span>

<span data-ttu-id="9a24f-115">*Val* 參數會從一組符合父群組媒體類型的資料流程，而不是從原始程式檔中的整組資料流程指定資料流程號碼。</span><span class="sxs-lookup"><span data-stu-id="9a24f-115">The *Val* parameter specifies a stream number from the set of streams that matches the parent group's media type, not from the entire set of streams in the source file.</span></span> <span data-ttu-id="9a24f-116">例如，假設檔案包含兩個影片串流和兩個音訊串流。</span><span class="sxs-lookup"><span data-stu-id="9a24f-116">For example, For example, suppose that a file contains two video streams and two audio streams.</span></span> <span data-ttu-id="9a24f-117">如果來源物件是在影片群組內，將 *Val* 設定為0會選取第一個影片串流。</span><span class="sxs-lookup"><span data-stu-id="9a24f-117">If the source object is inside a video group, setting *Val* to 0 selects the first video stream.</span></span> <span data-ttu-id="9a24f-118">呼叫端負責指定有效的資料流程號碼。</span><span class="sxs-lookup"><span data-stu-id="9a24f-118">The caller is responsible for specifying a valid stream number.</span></span>

<span data-ttu-id="9a24f-119">資料流程編號的預設值為零。</span><span class="sxs-lookup"><span data-stu-id="9a24f-119">The stream number defaults to zero.</span></span>

> [!Note]  
> <span data-ttu-id="9a24f-120">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="9a24f-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="9a24f-121">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="9a24f-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="9a24f-122">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="9a24f-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9a24f-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="9a24f-123">Requirements</span></span>



| <span data-ttu-id="9a24f-124">需求</span><span class="sxs-lookup"><span data-stu-id="9a24f-124">Requirement</span></span> | <span data-ttu-id="9a24f-125">值</span><span class="sxs-lookup"><span data-stu-id="9a24f-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9a24f-126">標頭</span><span class="sxs-lookup"><span data-stu-id="9a24f-126">Header</span></span><br/>  | <dl> <span data-ttu-id="9a24f-127"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="9a24f-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="9a24f-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="9a24f-128">Library</span></span><br/> | <dl> <span data-ttu-id="9a24f-129"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="9a24f-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a24f-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9a24f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a24f-131">**IAMTimelineSrc 介面**</span><span class="sxs-lookup"><span data-stu-id="9a24f-131">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="9a24f-132">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="9a24f-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




