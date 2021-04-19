---
description: 當材質載入已完成時，用來通知主機的回呼函式。
MS-HAID: vspixengine.IPixEngine5Callbacks\_LoadTextureFromFileComplete\_UINT\_PixEngineTextureDescriptor\_UINT\_PixEngineTextureSliceIndex\_arr\_PixEngineTextureSliceDescriptor\_arr\_UINT\_int\_arr\_PixEngineHistogram\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPixEngine5Callbacks：： LoadTextureFromFileComplete 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef7fb4c38b733a7e85a237260404b5b253e3eb88
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106988053"
---
# <a name="span-idvspixengineipixengine5callbacks_loadtexturefromfilecomplete_uint_pixenginetexturedescriptor_uint_pixenginetexturesliceindex_arr_pixenginetextureslicedescriptor_arr_uint_int_arr_pixenginehistogram_ptrspanipixengine5callbacksloadtexturefromfilecomplete-method"></a><span data-ttu-id="5569a-103"><span id="vspixengine.ipixengine5callbacks_loadtexturefromfilecomplete_uint_pixenginetexturedescriptor_uint_pixenginetexturesliceindex_arr_pixenginetextureslicedescriptor_arr_uint_int_arr_pixenginehistogram_ptr"></span>IPixEngine5Callbacks：： LoadTextureFromFileComplete 方法</span><span class="sxs-lookup"><span data-stu-id="5569a-103"><span id="vspixengine.ipixengine5callbacks_loadtexturefromfilecomplete_uint_pixenginetexturedescriptor_uint_pixenginetexturesliceindex_arr_pixenginetextureslicedescriptor_arr_uint_int_arr_pixenginehistogram_ptr"></span>IPixEngine5Callbacks::LoadTextureFromFileComplete method</span></span>

<span data-ttu-id="5569a-104">當材質載入已完成時，用來通知主機的回呼函式。</span><span class="sxs-lookup"><span data-stu-id="5569a-104">A callback function used to notify the host when a texture load has been completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="5569a-105">語法</span><span class="sxs-lookup"><span data-stu-id="5569a-105">Syntax</span></span>


```C++
HRESULT LoadTextureFromFileComplete(
   UINT                               textureId,
   PixEngineTextureDescriptor         textureDesc,
   UINT                               numSlices,
   PixEngineTextureSliceIndex []      count2_sliceIndicies,
   PixEngineTextureSliceDescriptor [] count2_sliceDescriptors,
   UINT                               numFormatOverrides,
   int []                             count5_formatOverrides,
   PixEngineHistogram*                histogram
);
```

## <a name="parameters"></a><span data-ttu-id="5569a-106">參數</span><span class="sxs-lookup"><span data-stu-id="5569a-106">Parameters</span></span>

<span data-ttu-id="5569a-107">*textureId* </span><span class="sxs-lookup"><span data-stu-id="5569a-107">*textureId* </span></span>  
<span data-ttu-id="5569a-108">載入之材質的識別碼。</span><span class="sxs-lookup"><span data-stu-id="5569a-108">The ID of the loaded texture.</span></span>

<span data-ttu-id="5569a-109">*textureDesc* </span><span class="sxs-lookup"><span data-stu-id="5569a-109">*textureDesc* </span></span>  
<span data-ttu-id="5569a-110">載入之材質的材質描述項。</span><span class="sxs-lookup"><span data-stu-id="5569a-110">The texture descriptor of the loaded texture.</span></span>

<span data-ttu-id="5569a-111">*numSlices* </span><span class="sxs-lookup"><span data-stu-id="5569a-111">*numSlices* </span></span>  
<span data-ttu-id="5569a-112">材質具有的配量數目。</span><span class="sxs-lookup"><span data-stu-id="5569a-112">The number of slices the texture has.</span></span>

<span data-ttu-id="5569a-113">*count2 \_ sliceIndicies* </span><span class="sxs-lookup"><span data-stu-id="5569a-113">*count2\_sliceIndicies* </span></span>  
<span data-ttu-id="5569a-114">與材質相關聯的配量 indicies。</span><span class="sxs-lookup"><span data-stu-id="5569a-114">Slice indicies associated with the texture.</span></span>

<span data-ttu-id="5569a-115">*count2 \_ sliceDescriptors* </span><span class="sxs-lookup"><span data-stu-id="5569a-115">*count2\_sliceDescriptors* </span></span>  
<span data-ttu-id="5569a-116">每個配量的描述項。</span><span class="sxs-lookup"><span data-stu-id="5569a-116">Descriptors for each slice.</span></span>

<span data-ttu-id="5569a-117">*numFormatOverrides* </span><span class="sxs-lookup"><span data-stu-id="5569a-117">*numFormatOverrides* </span></span>  
<span data-ttu-id="5569a-118">格式覆寫的數目。</span><span class="sxs-lookup"><span data-stu-id="5569a-118">The number of format overrides.</span></span>

<span data-ttu-id="5569a-119">*count5 \_ formatOverrides* </span><span class="sxs-lookup"><span data-stu-id="5569a-119">*count5\_formatOverrides* </span></span>  
<span data-ttu-id="5569a-120">格式會覆寫。</span><span class="sxs-lookup"><span data-stu-id="5569a-120">The format overrides.</span></span>

<span data-ttu-id="5569a-121">*長條圖* </span><span class="sxs-lookup"><span data-stu-id="5569a-121">*histogram* </span></span>  
<span data-ttu-id="5569a-122">所載入紋理的長條圖資料位址。</span><span class="sxs-lookup"><span data-stu-id="5569a-122">The address of histogram data for the loaded texture.</span></span>

## <a name="return-value"></a><span data-ttu-id="5569a-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="5569a-123">Return value</span></span>

<span data-ttu-id="5569a-124">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="5569a-124">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5569a-125">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="5569a-125">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="5569a-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="5569a-126">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="5569a-127">標頭</span><span class="sxs-lookup"><span data-stu-id="5569a-127">Header</span></span></p></td><td><span data-ttu-id="5569a-128">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="5569a-128">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="5569a-129"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="5569a-129"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="5569a-130">**IPixEngine5Callbacks**</span><span class="sxs-lookup"><span data-stu-id="5569a-130">**IPixEngine5Callbacks**</span></span>](/windows/desktop/direct3dtools/ipixengine5callbacks)

 

 
