---
description: 載入紋理配量，並在完成時通知主機 asynchrnously。
MS-HAID: vspixengine.IPixEngine5\_LoadTextureSliceAsync\_UINT\_PixEngineTextureSliceIndex\_int\_BSTR\_IPixEngine5Callbacks\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPixEngine5：： LoadTextureSliceAsync 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 520DBB6D-D8F3-451F-942C-BE8428B9ADFF
api_name:
- IPixEngine5.LoadTextureSliceAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 505ccfd6668cbe08b4f62878b5f51e9c20185b41
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106972310"
---
# <a name="span-idvspixengineipixengine5_loadtexturesliceasync_uint_pixenginetexturesliceindex_int_bstr_ipixengine5callbacks_ptr_dword_dwordspanipixengine5loadtexturesliceasync-method"></a><span data-ttu-id="8ce42-103"><span id="vspixengine.ipixengine5_loadtexturesliceasync_uint_pixenginetexturesliceindex_int_bstr_ipixengine5callbacks_ptr_dword_dword"></span>IPixEngine5：： LoadTextureSliceAsync 方法</span><span class="sxs-lookup"><span data-stu-id="8ce42-103"><span id="vspixengine.ipixengine5_loadtexturesliceasync_uint_pixenginetexturesliceindex_int_bstr_ipixengine5callbacks_ptr_dword_dword"></span>IPixEngine5::LoadTextureSliceAsync method</span></span>

<span data-ttu-id="8ce42-104">載入紋理配量，並在完成時通知主機 asynchrnously。</span><span class="sxs-lookup"><span data-stu-id="8ce42-104">Loads a texture slice and notifies the host asynchrnously when it completes.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ce42-105">語法</span><span class="sxs-lookup"><span data-stu-id="8ce42-105">Syntax</span></span>


```C++
HRESULT LoadTextureSliceAsync(
   UINT                       textureId,
   PixEngineTextureSliceIndex sliceIndex,
   int                        formatOverride,
   BSTR                       histogramDataFileName,
   IPixEngine5Callbacks*      callbacks,
   DWORD                      requestCookie,
   DWORD                      progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="8ce42-106">參數</span><span class="sxs-lookup"><span data-stu-id="8ce42-106">Parameters</span></span>

<span data-ttu-id="8ce42-107">*textureId* </span><span class="sxs-lookup"><span data-stu-id="8ce42-107">*textureId* </span></span>  
<span data-ttu-id="8ce42-108">要載入配量的材質識別碼。</span><span class="sxs-lookup"><span data-stu-id="8ce42-108">The ID of the texture to load the slice for.</span></span>

<span data-ttu-id="8ce42-109">*sliceIndex* </span><span class="sxs-lookup"><span data-stu-id="8ce42-109">*sliceIndex* </span></span>  
<span data-ttu-id="8ce42-110">要載入之配量的索引。</span><span class="sxs-lookup"><span data-stu-id="8ce42-110">The index of the slice to load.</span></span>

<span data-ttu-id="8ce42-111">*formatOverride* </span><span class="sxs-lookup"><span data-stu-id="8ce42-111">*formatOverride* </span></span>  
<span data-ttu-id="8ce42-112">指定格式覆寫。</span><span class="sxs-lookup"><span data-stu-id="8ce42-112">Specifies the format override.</span></span>

<span data-ttu-id="8ce42-113">*histogramDataFileName* </span><span class="sxs-lookup"><span data-stu-id="8ce42-113">*histogramDataFileName* </span></span>  
<span data-ttu-id="8ce42-114">COM 字串，其中包含與材質配量相關聯的長條圖資料檔案名稱。</span><span class="sxs-lookup"><span data-stu-id="8ce42-114">A COM string containing the name of the histogram data file associated with the texture slice.</span></span>

<span data-ttu-id="8ce42-115">*回檔* </span><span class="sxs-lookup"><span data-stu-id="8ce42-115">*callbacks* </span></span>  
<span data-ttu-id="8ce42-116">提供 IPixEngine5 回呼介面之物件的位址。</span><span class="sxs-lookup"><span data-stu-id="8ce42-116">The address of an object that provides the IPixEngine5 callbacks interface.</span></span>

<span data-ttu-id="8ce42-117">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="8ce42-117">*requestCookie* </span></span>  
<span data-ttu-id="8ce42-118">可唯一識別要求的 cookie，而且可用來指示它被取消。</span><span class="sxs-lookup"><span data-stu-id="8ce42-118">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="8ce42-119">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="8ce42-119">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="8ce42-120">未使用。</span><span class="sxs-lookup"><span data-stu-id="8ce42-120">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="8ce42-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="8ce42-121">Return value</span></span>

<span data-ttu-id="8ce42-122">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="8ce42-122">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8ce42-123">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="8ce42-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ce42-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="8ce42-124">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="8ce42-125">標頭</span><span class="sxs-lookup"><span data-stu-id="8ce42-125">Header</span></span></p></td><td><span data-ttu-id="8ce42-126">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="8ce42-126">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="8ce42-127"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="8ce42-127"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="8ce42-128">**IPixEngine5**</span><span class="sxs-lookup"><span data-stu-id="8ce42-128">**IPixEngine5**</span></span>](/windows/desktop/direct3dtools/ipixengine5)

 

 
