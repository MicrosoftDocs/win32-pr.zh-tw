---
description: 將材質轉譯至檔案，並將結果傳回至主機 asynchrnously。
MS-HAID: vspixengine.IPixEngine5\_RenderTextureAsync\_UINT\_PixEngineTextureSliceIndex\_int\_float\_arr4\_float\_arr4\_BSTR\_UINT\_BSTR\_arr\_float\_arr\_UINT\_BSTR\_arr\_BOOL\_arr\_BSTR\_IPixEngine5Callbacks\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPixEngine5：： RenderTextureAsync 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd16214887514fa348a672c45d5eb85c2df6bca5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510042"
---
# <a name="span-idvspixengineipixengine5_rendertextureasync_uint_pixenginetexturesliceindex_int_float_arr4_float_arr4_bstr_uint_bstr_arr_float_arr_uint_bstr_arr_bool_arr_bstr_ipixengine5callbacks_ptr_dword_dwordspanipixengine5rendertextureasync-method"></a><span data-ttu-id="52cca-103"><span id="vspixengine.ipixengine5_rendertextureasync_uint_pixenginetexturesliceindex_int_float_arr4_float_arr4_bstr_uint_bstr_arr_float_arr_uint_bstr_arr_bool_arr_bstr_ipixengine5callbacks_ptr_dword_dword"></span>IPixEngine5：： RenderTextureAsync 方法</span><span class="sxs-lookup"><span data-stu-id="52cca-103"><span id="vspixengine.ipixengine5_rendertextureasync_uint_pixenginetexturesliceindex_int_float_arr4_float_arr4_bstr_uint_bstr_arr_float_arr_uint_bstr_arr_bool_arr_bstr_ipixengine5callbacks_ptr_dword_dword"></span>IPixEngine5::RenderTextureAsync method</span></span>

<span data-ttu-id="52cca-104">將材質轉譯至檔案，並將結果傳回至主機 asynchrnously。</span><span class="sxs-lookup"><span data-stu-id="52cca-104">Renders a texture to a file and returns the result to the host asynchrnously.</span></span>

## <a name="syntax"></a><span data-ttu-id="52cca-105">語法</span><span class="sxs-lookup"><span data-stu-id="52cca-105">Syntax</span></span>


```C++
HRESULT RenderTextureAsync(
   UINT                       textureId,
   PixEngineTextureSliceIndex sliceIndex,
   int                        formatOverride,
   float [4]                  lower,
   float [4]                  upper,
   BSTR                       shaderFileName,
   UINT                       numFloatShaderVars,
   BSTR []                    count6_shaderFloatVarName,
   float []                   count6_shaderFloatVarValue,
   UINT                       numBoolShaderVars,
   BSTR []                    count9_shaderBoolVarName,
   BOOL []                    count9_shaderBoolVarValue,
   BSTR                       renderContentFileName,
   IPixEngine5Callbacks*      callbacks,
   DWORD                      requestCookie,
   DWORD                      progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="52cca-106">參數</span><span class="sxs-lookup"><span data-stu-id="52cca-106">Parameters</span></span>

<span data-ttu-id="52cca-107">*textureId* </span><span class="sxs-lookup"><span data-stu-id="52cca-107">*textureId* </span></span>  
<span data-ttu-id="52cca-108">要呈現之材質的識別碼。</span><span class="sxs-lookup"><span data-stu-id="52cca-108">The ID of the texture to render.</span></span>

<span data-ttu-id="52cca-109">*sliceIndex* </span><span class="sxs-lookup"><span data-stu-id="52cca-109">*sliceIndex* </span></span>  
<span data-ttu-id="52cca-110">要呈現之材質內的配量索引。</span><span class="sxs-lookup"><span data-stu-id="52cca-110">The index of the slice within the texture to render.</span></span>

<span data-ttu-id="52cca-111">*formatOverride* </span><span class="sxs-lookup"><span data-stu-id="52cca-111">*formatOverride* </span></span>  
<span data-ttu-id="52cca-112">色彩格式覆寫。</span><span class="sxs-lookup"><span data-stu-id="52cca-112">The color format override.</span></span>

<span data-ttu-id="52cca-113">*降低*</span><span class="sxs-lookup"><span data-stu-id="52cca-113">*lower*</span></span>   

<span data-ttu-id="52cca-114">*上*</span><span class="sxs-lookup"><span data-stu-id="52cca-114">*upper*</span></span>   

<span data-ttu-id="52cca-115">*shaderFileName* </span><span class="sxs-lookup"><span data-stu-id="52cca-115">*shaderFileName* </span></span>  
<span data-ttu-id="52cca-116">COM 字串，其中包含著色器檔案的路徑名稱。</span><span class="sxs-lookup"><span data-stu-id="52cca-116">A COM string containing the pathname of the shader file.</span></span>

<span data-ttu-id="52cca-117">*numFloatShaderVars* </span><span class="sxs-lookup"><span data-stu-id="52cca-117">*numFloatShaderVars* </span></span>  
<span data-ttu-id="52cca-118">浮點數著色器變數的數目</span><span class="sxs-lookup"><span data-stu-id="52cca-118">The number of floating-point shader variables</span></span>

<span data-ttu-id="52cca-119">*count6 \_ shaderFloatVarName* </span><span class="sxs-lookup"><span data-stu-id="52cca-119">*count6\_shaderFloatVarName* </span></span>  
<span data-ttu-id="52cca-120">COM 字串會寫入浮點著色器變數的名稱。</span><span class="sxs-lookup"><span data-stu-id="52cca-120">COM strings contianing the names of the floating-point shader variables.</span></span>

<span data-ttu-id="52cca-121">*count6 \_ shaderFloatVarValue* </span><span class="sxs-lookup"><span data-stu-id="52cca-121">*count6\_shaderFloatVarValue* </span></span>  
<span data-ttu-id="52cca-122">浮點著色器變數。</span><span class="sxs-lookup"><span data-stu-id="52cca-122">The floating-point shader variables.</span></span>

<span data-ttu-id="52cca-123">*numBoolShaderVars* </span><span class="sxs-lookup"><span data-stu-id="52cca-123">*numBoolShaderVars* </span></span>  
<span data-ttu-id="52cca-124">布林著色器變數的數目。</span><span class="sxs-lookup"><span data-stu-id="52cca-124">The number of boolean shader variables.</span></span>

<span data-ttu-id="52cca-125">*count9 \_ shaderBoolVarName* </span><span class="sxs-lookup"><span data-stu-id="52cca-125">*count9\_shaderBoolVarName* </span></span>  
<span data-ttu-id="52cca-126">COM 字串會寫入布林著色器變數的名稱。</span><span class="sxs-lookup"><span data-stu-id="52cca-126">COM strings contianing the names of the boolean shader variables.</span></span>

<span data-ttu-id="52cca-127">*count9 \_ shaderBoolVarValue* </span><span class="sxs-lookup"><span data-stu-id="52cca-127">*count9\_shaderBoolVarValue* </span></span>  
<span data-ttu-id="52cca-128">布林著色器變數。</span><span class="sxs-lookup"><span data-stu-id="52cca-128">The boolean shader variables.</span></span>

<span data-ttu-id="52cca-129">*renderContentFileName* </span><span class="sxs-lookup"><span data-stu-id="52cca-129">*renderContentFileName* </span></span>  
<span data-ttu-id="52cca-130">COM 字串，其中包含轉譯的材質寫入之檔案的路徑名稱。</span><span class="sxs-lookup"><span data-stu-id="52cca-130">A COM string containing the pathname of the file where the rendered texture was written.</span></span>

<span data-ttu-id="52cca-131">*回檔* </span><span class="sxs-lookup"><span data-stu-id="52cca-131">*callbacks* </span></span>  
<span data-ttu-id="52cca-132">提供 IPixEngine5 回呼介面之物件的位址。</span><span class="sxs-lookup"><span data-stu-id="52cca-132">The address of an object that provides the IPixEngine5 callbacks interface.</span></span>

<span data-ttu-id="52cca-133">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="52cca-133">*requestCookie* </span></span>  
<span data-ttu-id="52cca-134">可唯一識別要求的 cookie，而且可用來指示它被取消。</span><span class="sxs-lookup"><span data-stu-id="52cca-134">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="52cca-135">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="52cca-135">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="52cca-136">未使用。</span><span class="sxs-lookup"><span data-stu-id="52cca-136">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="52cca-137">傳回值</span><span class="sxs-lookup"><span data-stu-id="52cca-137">Return value</span></span>

<span data-ttu-id="52cca-138">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="52cca-138">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="52cca-139">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="52cca-139">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="52cca-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="52cca-140">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="52cca-141">標頭</span><span class="sxs-lookup"><span data-stu-id="52cca-141">Header</span></span></p></td><td><span data-ttu-id="52cca-142">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="52cca-142">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="52cca-143"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="52cca-143"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="52cca-144">**IPixEngine5**</span><span class="sxs-lookup"><span data-stu-id="52cca-144">**IPixEngine5**</span></span>](/windows/desktop/direct3dtools/ipixengine5)

 

 
