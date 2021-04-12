---
description: 取得未壓縮像素格式的清單，這些格式可使用指定的 DirectX Video 加速 (DXVA) 設定檔來呈現。
ms.assetid: 7c69ea5f-6054-4430-95b5-820db6854fc0
title: 'IDirect3DVideoDevice9：： GetUncompressedDXVAFormats 方法 (Dxva .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.GetUncompressedDXVAFormats
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 94784ac5fe164d571a8a02e4170990f8ce06a4a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319007"
---
# <a name="idirect3dvideodevice9getuncompresseddxvaformats-method"></a><span data-ttu-id="f6a65-103">IDirect3DVideoDevice9：： GetUncompressedDXVAFormats 方法</span><span class="sxs-lookup"><span data-stu-id="f6a65-103">IDirect3DVideoDevice9::GetUncompressedDXVAFormats method</span></span>

<span data-ttu-id="f6a65-104">取得未壓縮像素格式的清單，這些格式可使用指定的 DirectX Video 加速 (DXVA) 設定檔來呈現。</span><span class="sxs-lookup"><span data-stu-id="f6a65-104">Gets a list of uncompressed pixel formats that can be rendered using a specified DirectX Video Acceleration (DXVA) profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6a65-105">語法</span><span class="sxs-lookup"><span data-stu-id="f6a65-105">Syntax</span></span>


```C++
HRESULT GetUncompressedDXVAFormats(
   GUID      *pGuid,
   DWORD     *pNumFormats,
   D3DFORMAT *pFormats
);
```



## <a name="parameters"></a><span data-ttu-id="f6a65-106">參數</span><span class="sxs-lookup"><span data-stu-id="f6a65-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6a65-107">*pGuid*</span><span class="sxs-lookup"><span data-stu-id="f6a65-107">*pGuid*</span></span> 
</dt> <dd>

<span data-ttu-id="f6a65-108">指定 DXVA 設定檔之 GUID 的指標。</span><span class="sxs-lookup"><span data-stu-id="f6a65-108">Pointer to a GUID that specifies the DXVA profile.</span></span> <span data-ttu-id="f6a65-109">若要取得支援的配置檔案清單，請呼叫 [**IDirect3DVideoDevice9：： GetDXVAGuids**](idirect3dvideodevice9-getdxvaguids.md)。</span><span class="sxs-lookup"><span data-stu-id="f6a65-109">To get a list of supported profiles, call [**IDirect3DVideoDevice9::GetDXVAGuids**](idirect3dvideodevice9-getdxvaguids.md).</span></span>

</dd> <dt>

<span data-ttu-id="f6a65-110">*pNumFormats*</span><span class="sxs-lookup"><span data-stu-id="f6a65-110">*pNumFormats*</span></span> 
</dt> <dd>

<span data-ttu-id="f6a65-111">在 [輸入] 上，指定 *pFormats* 陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="f6a65-111">On input, specifies the number of elements in the *pFormats* array.</span></span> <span data-ttu-id="f6a65-112">如果 *pFormats* 為 **Null**，的值 `*pNumFormats` 必須是零。</span><span class="sxs-lookup"><span data-stu-id="f6a65-112">If *pFormats* is **NULL**, the value of `*pNumFormats` must be zero.</span></span>

<span data-ttu-id="f6a65-113">在輸出中，如果 *pFormats* 為 **Null**，則 *pNumFormats* 會接收支援的像素格式數目。</span><span class="sxs-lookup"><span data-stu-id="f6a65-113">On output, if *pFormats* is **NULL**, *pNumFormats* receives the number of supported pixel formats.</span></span> <span data-ttu-id="f6a65-114">否則， *pNumFormats* 會接收復制到 *pFormats* 陣列的實際像素格式數目。</span><span class="sxs-lookup"><span data-stu-id="f6a65-114">Otherwise, *pNumFormats* receives the actual number of pixel formats copied to the *pFormats* array.</span></span>

</dd> <dt>

<span data-ttu-id="f6a65-115">*pFormats*</span><span class="sxs-lookup"><span data-stu-id="f6a65-115">*pFormats*</span></span> 
</dt> <dd>

<span data-ttu-id="f6a65-116">**D3DFORMAT** 值陣列的位址，或 **Null**。</span><span class="sxs-lookup"><span data-stu-id="f6a65-116">Address of an array of **D3DFORMAT** values, or **NULL**.</span></span> <span data-ttu-id="f6a65-117">如果此值為非 **Null**，則陣列會接收像素格式的清單。</span><span class="sxs-lookup"><span data-stu-id="f6a65-117">If the value is non-**NULL**, the array receives a list of pixel formats.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6a65-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="f6a65-118">Return value</span></span>

<span data-ttu-id="f6a65-119">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="f6a65-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f6a65-120">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="f6a65-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6a65-121">備註</span><span class="sxs-lookup"><span data-stu-id="f6a65-121">Remarks</span></span>

<span data-ttu-id="f6a65-122">呼叫這個方法兩次。</span><span class="sxs-lookup"><span data-stu-id="f6a65-122">Call this method twice.</span></span> <span data-ttu-id="f6a65-123">在第一次呼叫時，將 *pFormats* 設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="f6a65-123">On the first call, set *pFormats* to **NULL**.</span></span> <span data-ttu-id="f6a65-124">*PNumFormats* 參數會接收格式的數目。</span><span class="sxs-lookup"><span data-stu-id="f6a65-124">The *pNumFormats* parameter receives the number of formats.</span></span> <span data-ttu-id="f6a65-125">使用所需的大小來配置 **D3DFORMAT** 陣列，然後再次呼叫方法。</span><span class="sxs-lookup"><span data-stu-id="f6a65-125">Allocate a **D3DFORMAT** array with the required size, and call the method again.</span></span> <span data-ttu-id="f6a65-126">這次，請將 *pFormats* 設定為數組的位址。</span><span class="sxs-lookup"><span data-stu-id="f6a65-126">This time, set *pFormats* to the address of the array.</span></span> <span data-ttu-id="f6a65-127">方法會以像素格式清單來填滿陣列。</span><span class="sxs-lookup"><span data-stu-id="f6a65-127">The method fills the array with the list of pixel formats.</span></span>

<span data-ttu-id="f6a65-128">驅動程式應依喜好設定的遞減順序傳回格式，最慣用的格式最先列出。</span><span class="sxs-lookup"><span data-stu-id="f6a65-128">The driver should return the formats in decreasing order of preference, with the most preferred format listed first.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6a65-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="f6a65-129">Requirements</span></span>



| <span data-ttu-id="f6a65-130">需求</span><span class="sxs-lookup"><span data-stu-id="f6a65-130">Requirement</span></span> | <span data-ttu-id="f6a65-131">值</span><span class="sxs-lookup"><span data-stu-id="f6a65-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="f6a65-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f6a65-132">Minimum supported client</span></span><br/> | <span data-ttu-id="f6a65-133">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f6a65-133">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f6a65-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f6a65-134">Minimum supported server</span></span><br/> | <span data-ttu-id="f6a65-135">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f6a65-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="f6a65-136">標頭</span><span class="sxs-lookup"><span data-stu-id="f6a65-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6a65-137"><dt>Dxva。h</dt></span><span class="sxs-lookup"><span data-stu-id="f6a65-137"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6a65-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f6a65-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6a65-139">**IDirect3DVideoDevice9**</span><span class="sxs-lookup"><span data-stu-id="f6a65-139">**IDirect3DVideoDevice9**</span></span>](idirect3dvideodevice9.md)
</dt> </dl>

 

 




