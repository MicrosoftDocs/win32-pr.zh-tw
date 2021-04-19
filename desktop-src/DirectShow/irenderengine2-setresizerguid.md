---
description: SetResizerGUID 方法會指定自訂影片調整大小篩選的 CLSID。
ms.assetid: 709a6e7f-64ae-406d-bb6d-29f6c65b63a8
title: 'IRenderEngine2：： SetResizerGUID 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine2.SetResizerGUID
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 864053c2c5def6ef1b23ca2c2ee712664e132079
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996058"
---
# <a name="irenderengine2setresizerguid-method"></a><span data-ttu-id="ad5fd-103">IRenderEngine2：： SetResizerGUID 方法</span><span class="sxs-lookup"><span data-stu-id="ad5fd-103">IRenderEngine2::SetResizerGUID method</span></span>

> [!Note]  
> <span data-ttu-id="ad5fd-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="ad5fd-104">\[Deprecated.</span></span> <span data-ttu-id="ad5fd-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="ad5fd-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="ad5fd-106">`SetResizerGUID`方法會指定自訂影片調整大小篩選的 CLSID。</span><span class="sxs-lookup"><span data-stu-id="ad5fd-106">The `SetResizerGUID` method specifies the CLSID of a custom video resizing filter.</span></span> <span data-ttu-id="ad5fd-107">呼叫這個方法來取代 DirectShow 編輯服務所使用的預設調整大小篩選。</span><span class="sxs-lookup"><span data-stu-id="ad5fd-107">Call this method to replace the default resizing filter used by DirectShow Editing Services.</span></span> <span data-ttu-id="ad5fd-108">您的篩選準則必須註冊為使用者系統上的 COM 物件，且必須支援 [**IResize**](iresize.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="ad5fd-108">Your filter must be registered as a COM object on the user's system, and it must support the [**IResize**](iresize.md) interface.</span></span>

<span data-ttu-id="ad5fd-109">呼叫 [**IRenderEngine：： ConnectFrontEnd**](irenderengine-connectfrontend.md)之前，請先呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="ad5fd-109">Call this method before calling [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ad5fd-110">語法</span><span class="sxs-lookup"><span data-stu-id="ad5fd-110">Syntax</span></span>


```C++
HRESULT SetResizerGUID(
  [in] GUID ResizerGuid
);
```



## <a name="parameters"></a><span data-ttu-id="ad5fd-111">參數</span><span class="sxs-lookup"><span data-stu-id="ad5fd-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad5fd-112">*ResizerGuid* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ad5fd-112">*ResizerGuid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad5fd-113">篩選的 CLSID。</span><span class="sxs-lookup"><span data-stu-id="ad5fd-113">The CLSID of the filter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad5fd-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="ad5fd-114">Return value</span></span>

<span data-ttu-id="ad5fd-115">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="ad5fd-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ad5fd-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="ad5fd-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad5fd-117">備註</span><span class="sxs-lookup"><span data-stu-id="ad5fd-117">Remarks</span></span>

<span data-ttu-id="ad5fd-118">若要還原為預設的 DES 調整調整，請使用下列 CLSID：</span><span class="sxs-lookup"><span data-stu-id="ad5fd-118">To revert to the default DES resizer, use the following CLSID:</span></span>


```C++
// {F97B8A60-31AD-11CF-B2DE-00DD01101B85}
DEFINE_GUID(CLSID_Resize, 
0xF97B8A60, 0x31AD, 0x11CF, 0xB2, 0xDE, 0x00, 0xDD, 0x01, 0x10, 0x1B, 0x85);
```



> [!Note]  
> <span data-ttu-id="ad5fd-119">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="ad5fd-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="ad5fd-120">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="ad5fd-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="ad5fd-121">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="ad5fd-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ad5fd-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="ad5fd-122">Requirements</span></span>



| <span data-ttu-id="ad5fd-123">需求</span><span class="sxs-lookup"><span data-stu-id="ad5fd-123">Requirement</span></span> | <span data-ttu-id="ad5fd-124">值</span><span class="sxs-lookup"><span data-stu-id="ad5fd-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ad5fd-125">版本</span><span class="sxs-lookup"><span data-stu-id="ad5fd-125">Version</span></span><br/> | <span data-ttu-id="ad5fd-126">DirectX 9.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="ad5fd-126">DirectX 9.0 or later</span></span><br/>                                                         |
| <span data-ttu-id="ad5fd-127">標頭</span><span class="sxs-lookup"><span data-stu-id="ad5fd-127">Header</span></span><br/>  | <dl> <span data-ttu-id="ad5fd-128"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="ad5fd-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="ad5fd-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="ad5fd-129">Library</span></span><br/> | <dl> <span data-ttu-id="ad5fd-130"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="ad5fd-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad5fd-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ad5fd-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad5fd-132">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="ad5fd-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="ad5fd-133">**IRenderEngine2 介面**</span><span class="sxs-lookup"><span data-stu-id="ad5fd-133">**IRenderEngine2 Interface**</span></span>](irenderengine2.md)
</dt> </dl>

 

 




