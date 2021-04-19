---
description: 讀取材質值，並將結果傳回至主機 asynchrnously。
MS-HAID: vspixengine.IPixEngine5\_ReadTexelValueAsync\_UINT\_PixEngineTextureSliceIndex\_int\_int\_int\_IPixEngine5Callbacks\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPixEngine5：： ReadTexelValueAsync 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 28C44D12-383D-4E91-8BB1-12869782533C
api_name:
- IPixEngine5.ReadTexelValueAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: ca3510b01038df3b07b3033364902f76f2e05b4e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106972947"
---
# <a name="span-idvspixengineipixengine5_readtexelvalueasync_uint_pixenginetexturesliceindex_int_int_int_ipixengine5callbacks_ptr_dword_dwordspanipixengine5readtexelvalueasync-method"></a><span data-ttu-id="20b8a-103"><span id="vspixengine.ipixengine5_readtexelvalueasync_uint_pixenginetexturesliceindex_int_int_int_ipixengine5callbacks_ptr_dword_dword"></span>IPixEngine5：： ReadTexelValueAsync 方法</span><span class="sxs-lookup"><span data-stu-id="20b8a-103"><span id="vspixengine.ipixengine5_readtexelvalueasync_uint_pixenginetexturesliceindex_int_int_int_ipixengine5callbacks_ptr_dword_dword"></span>IPixEngine5::ReadTexelValueAsync method</span></span>

<span data-ttu-id="20b8a-104">讀取材質值，並將結果傳回至主機 asynchrnously。</span><span class="sxs-lookup"><span data-stu-id="20b8a-104">Reads a texel value and returns the result to the host asynchrnously.</span></span>

## <a name="syntax"></a><span data-ttu-id="20b8a-105">語法</span><span class="sxs-lookup"><span data-stu-id="20b8a-105">Syntax</span></span>


```C++
HRESULT ReadTexelValueAsync(
   UINT                       textureId,
   PixEngineTextureSliceIndex sliceIndex,
   int                        x,
   int                        y,
   int                        formatOverride,
   IPixEngine5Callbacks*      callbacks,
   DWORD                      requestCookie,
   DWORD                      progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="20b8a-106">參數</span><span class="sxs-lookup"><span data-stu-id="20b8a-106">Parameters</span></span>

<span data-ttu-id="20b8a-107">*textureId* </span><span class="sxs-lookup"><span data-stu-id="20b8a-107">*textureId* </span></span>  
<span data-ttu-id="20b8a-108">要從中讀取材質值的材質識別碼。</span><span class="sxs-lookup"><span data-stu-id="20b8a-108">The ID of the texture to read the texel value from.</span></span>

<span data-ttu-id="20b8a-109">*sliceIndex* </span><span class="sxs-lookup"><span data-stu-id="20b8a-109">*sliceIndex* </span></span>  
<span data-ttu-id="20b8a-110">要從中讀取材質值之材質內的配量索引。</span><span class="sxs-lookup"><span data-stu-id="20b8a-110">The index of the slice within the texture to read the texel value from.</span></span>

<span data-ttu-id="20b8a-111">*X* </span><span class="sxs-lookup"><span data-stu-id="20b8a-111">*x* </span></span>  
<span data-ttu-id="20b8a-112">要讀取的 x 材質座標。</span><span class="sxs-lookup"><span data-stu-id="20b8a-112">The x texel coordinate to read.</span></span>

<span data-ttu-id="20b8a-113">*Y* </span><span class="sxs-lookup"><span data-stu-id="20b8a-113">*y* </span></span>  
<span data-ttu-id="20b8a-114">要讀取的 y 材質座標。</span><span class="sxs-lookup"><span data-stu-id="20b8a-114">The y texel coordinate to read.</span></span>

<span data-ttu-id="20b8a-115">*formatOverride* </span><span class="sxs-lookup"><span data-stu-id="20b8a-115">*formatOverride* </span></span>  
<span data-ttu-id="20b8a-116">色彩格式覆寫。</span><span class="sxs-lookup"><span data-stu-id="20b8a-116">The color format override.</span></span>

<span data-ttu-id="20b8a-117">*回檔* </span><span class="sxs-lookup"><span data-stu-id="20b8a-117">*callbacks* </span></span>  
<span data-ttu-id="20b8a-118">提供 IPixEngine5 回呼介面之物件的位址。</span><span class="sxs-lookup"><span data-stu-id="20b8a-118">The address of an object that provides the IPixEngine5 callbacks interface.</span></span>

<span data-ttu-id="20b8a-119">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="20b8a-119">*requestCookie* </span></span>  
<span data-ttu-id="20b8a-120">可唯一識別要求的 cookie，而且可用來指示它被取消。</span><span class="sxs-lookup"><span data-stu-id="20b8a-120">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="20b8a-121">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="20b8a-121">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="20b8a-122">未使用。</span><span class="sxs-lookup"><span data-stu-id="20b8a-122">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="20b8a-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="20b8a-123">Return value</span></span>

<span data-ttu-id="20b8a-124">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="20b8a-124">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="20b8a-125">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="20b8a-125">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="20b8a-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="20b8a-126">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="20b8a-127">標頭</span><span class="sxs-lookup"><span data-stu-id="20b8a-127">Header</span></span></p></td><td><span data-ttu-id="20b8a-128">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="20b8a-128">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="20b8a-129"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="20b8a-129"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="20b8a-130">**IPixEngine5**</span><span class="sxs-lookup"><span data-stu-id="20b8a-130">**IPixEngine5**</span></span>](/windows/desktop/direct3dtools/ipixengine5)

 

 
