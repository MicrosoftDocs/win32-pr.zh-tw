---
description: GetDefaultFPS 方法會捕獲來源物件的預設畫面播放速率。 如果轉譯引擎無法判斷原始來源的畫面播放速率，則會使用此值。
ms.assetid: c167cd85-e9bb-46ff-9b35-c88898a6c5a3
title: 'IAMTimelineSrc：： GetDefaultFPS 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.GetDefaultFPS
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e48ee38f385ba5ff06b2ede9b27b4558dac65270
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989248"
---
# <a name="iamtimelinesrcgetdefaultfps-method"></a><span data-ttu-id="70cf0-104">IAMTimelineSrc：： GetDefaultFPS 方法</span><span class="sxs-lookup"><span data-stu-id="70cf0-104">IAMTimelineSrc::GetDefaultFPS method</span></span>

> [!Note]  
> <span data-ttu-id="70cf0-105">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="70cf0-105">\[Deprecated.</span></span> <span data-ttu-id="70cf0-106">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="70cf0-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="70cf0-107">`GetDefaultFPS`方法會捕獲來源物件的預設畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="70cf0-107">The `GetDefaultFPS` method retrieves the source object's default frame rate.</span></span> <span data-ttu-id="70cf0-108">如果轉譯引擎無法判斷原始來源的畫面播放速率，則會使用此值。</span><span class="sxs-lookup"><span data-stu-id="70cf0-108">The render engine uses this value if it cannot determine the frame rate from the original source.</span></span>

## <a name="syntax"></a><span data-ttu-id="70cf0-109">語法</span><span class="sxs-lookup"><span data-stu-id="70cf0-109">Syntax</span></span>


```C++
HRESULT GetDefaultFPS(
   double *pFPS
);
```



## <a name="parameters"></a><span data-ttu-id="70cf0-110">參數</span><span class="sxs-lookup"><span data-stu-id="70cf0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70cf0-111">*pFPS*</span><span class="sxs-lookup"><span data-stu-id="70cf0-111">*pFPS*</span></span> 
</dt> <dd>

<span data-ttu-id="70cf0-112">接收預設畫面播放速率（以每秒畫面格數為單位）。</span><span class="sxs-lookup"><span data-stu-id="70cf0-112">Receives the default frame rate, in frames per second.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70cf0-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="70cf0-113">Return value</span></span>

<span data-ttu-id="70cf0-114">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="70cf0-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="70cf0-115">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="70cf0-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="70cf0-116">備註</span><span class="sxs-lookup"><span data-stu-id="70cf0-116">Remarks</span></span>

<span data-ttu-id="70cf0-117">如果檔案格式指定畫面播放速率，則不需要預設的畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="70cf0-117">The default frame rate is not required if the file format specifies the frame rate.</span></span> <span data-ttu-id="70cf0-118">這是音訊和影片格式的情況。</span><span class="sxs-lookup"><span data-stu-id="70cf0-118">This is the case for audio and video formats.</span></span>

<span data-ttu-id="70cf0-119">如果來源是點陣圖或 JPEG 影像，轉譯引擎會使用它做為與裝置無關的點陣圖中的第一個影像， (DIB) 序列，且畫面播放速率等於預設的畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="70cf0-119">If the source is a bitmap or JPEG image, the render engine uses it as the first image in a device-independent bitmap (DIB) sequence, with a frame rate equal to the default frame rate.</span></span> <span data-ttu-id="70cf0-120">若要呈現靜態影像，而不是 DIB 順序，請將預設畫面播放速率設定為0。</span><span class="sxs-lookup"><span data-stu-id="70cf0-120">To render a static image, rather than a DIB sequence, set the default frame rate to 0.</span></span>

<span data-ttu-id="70cf0-121">如果來源為 GIF，請勿設定畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="70cf0-121">If the source is a GIF, do not set the frame rate.</span></span> <span data-ttu-id="70cf0-122">若為動畫 Gif，GIF 檔案會指定每個影像之間的延遲。</span><span class="sxs-lookup"><span data-stu-id="70cf0-122">For animated GIFs, the GIF file specifies the delay between each image.</span></span>

> [!Note]  
> <span data-ttu-id="70cf0-123">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="70cf0-123">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="70cf0-124">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="70cf0-124">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="70cf0-125">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="70cf0-125">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="70cf0-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="70cf0-126">Requirements</span></span>



| <span data-ttu-id="70cf0-127">需求</span><span class="sxs-lookup"><span data-stu-id="70cf0-127">Requirement</span></span> | <span data-ttu-id="70cf0-128">值</span><span class="sxs-lookup"><span data-stu-id="70cf0-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="70cf0-129">標頭</span><span class="sxs-lookup"><span data-stu-id="70cf0-129">Header</span></span><br/>  | <dl> <span data-ttu-id="70cf0-130"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="70cf0-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="70cf0-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="70cf0-131">Library</span></span><br/> | <dl> <span data-ttu-id="70cf0-132"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="70cf0-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70cf0-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="70cf0-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70cf0-134">**IAMTimelineSrc 介面**</span><span class="sxs-lookup"><span data-stu-id="70cf0-134">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="70cf0-135">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="70cf0-135">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




