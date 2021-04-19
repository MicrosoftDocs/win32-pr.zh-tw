---
description: 取得顯示驅動程式支援 (DXVA) 設定檔的 DirectX 影片加速清單。
ms.assetid: 4adbbac2-a25d-4e17-b62e-a02a67dcdbed
title: 'IDirect3DVideoDevice9：： GetDXVAGuids 方法 (Dxva .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.GetDXVAGuids
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 3ea05af8f27399af38419e177d7bd40b029cd63b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983586"
---
# <a name="idirect3dvideodevice9getdxvaguids-method"></a><span data-ttu-id="a24d0-103">IDirect3DVideoDevice9：： GetDXVAGuids 方法</span><span class="sxs-lookup"><span data-stu-id="a24d0-103">IDirect3DVideoDevice9::GetDXVAGuids method</span></span>

<span data-ttu-id="a24d0-104">取得顯示驅動程式支援 (DXVA) 設定檔的 DirectX 影片加速清單。</span><span class="sxs-lookup"><span data-stu-id="a24d0-104">Gets a list of DirectX Video Acceleration (DXVA) profiles that are supported by the display driver.</span></span>

## <a name="syntax"></a><span data-ttu-id="a24d0-105">語法</span><span class="sxs-lookup"><span data-stu-id="a24d0-105">Syntax</span></span>


```C++
HRESULT GetDXVAGuids(
   DWORD *pNumGuids,
   GUID  *pGuids
);
```



## <a name="parameters"></a><span data-ttu-id="a24d0-106">參數</span><span class="sxs-lookup"><span data-stu-id="a24d0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a24d0-107">*pNumGuids*</span><span class="sxs-lookup"><span data-stu-id="a24d0-107">*pNumGuids*</span></span> 
</dt> <dd>

<span data-ttu-id="a24d0-108">在 [輸入] 上，指定 *pGuids* 陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="a24d0-108">On input, specifies the number of elements in the *pGuids* array.</span></span> <span data-ttu-id="a24d0-109">如果 *pGuids* 為 **Null**，的值 `*pNumGuids` 必須是零。</span><span class="sxs-lookup"><span data-stu-id="a24d0-109">If *pGuids* is **NULL**, the value of `*pNumGuids` must be zero.</span></span>

<span data-ttu-id="a24d0-110">在輸出時，如果 *pGuids* 為 **Null**， *PNUMGUIDS* 會收到限制模式 DXVA 設定檔的數目。</span><span class="sxs-lookup"><span data-stu-id="a24d0-110">On output, if *pGuids* is **NULL**, *pNumGuids* receives the number of restricted-mode DXVA profiles.</span></span> <span data-ttu-id="a24d0-111">否則， *pNumGuids* 會接收復制到 *pGuids* 陣列的實際 guid 數目。</span><span class="sxs-lookup"><span data-stu-id="a24d0-111">Otherwise, *pNumGuids* receives the actual number of GUIDs that are copied to the *pGuids* array.</span></span>

</dd> <dt>

<span data-ttu-id="a24d0-112">*pGuids*</span><span class="sxs-lookup"><span data-stu-id="a24d0-112">*pGuids*</span></span> 
</dt> <dd>

<span data-ttu-id="a24d0-113">Guid 陣列的位址或 **Null**。</span><span class="sxs-lookup"><span data-stu-id="a24d0-113">Address of an array of GUIDs or **NULL**.</span></span> <span data-ttu-id="a24d0-114">如果此值為非 **Null**，則陣列會接收指定受限制模式 DXVA 設定檔的 guid 清單。</span><span class="sxs-lookup"><span data-stu-id="a24d0-114">If the value is non-**NULL**, the array receives a list of GUIDs that specify restricted-mode DXVA profiles.</span></span> <span data-ttu-id="a24d0-115">這些 Guid 是在 dxva 中定義的，並記載于 [dxva 1.0 規格](/windows-hardware/drivers/display/directx-video-acceleration)中。</span><span class="sxs-lookup"><span data-stu-id="a24d0-115">These GUIDs are defined in dxva.h, and are documented in the [DXVA 1.0 specification](/windows-hardware/drivers/display/directx-video-acceleration).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a24d0-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="a24d0-116">Return value</span></span>

<span data-ttu-id="a24d0-117">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="a24d0-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a24d0-118">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="a24d0-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a24d0-119">備註</span><span class="sxs-lookup"><span data-stu-id="a24d0-119">Remarks</span></span>

<span data-ttu-id="a24d0-120">呼叫這個方法兩次。</span><span class="sxs-lookup"><span data-stu-id="a24d0-120">Call this method twice.</span></span> <span data-ttu-id="a24d0-121">在第一次呼叫時，將 *pGuids* 設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="a24d0-121">On the first call, set *pGuids* to **NULL**.</span></span> <span data-ttu-id="a24d0-122">*PNumGuids* 參數會接收 DXVA 設定檔 guid 的數目。</span><span class="sxs-lookup"><span data-stu-id="a24d0-122">The *pNumGuids* parameter receives the number of DXVA profile GUIDs.</span></span> <span data-ttu-id="a24d0-123">配置具有所需大小的 Guid 陣列，然後再次呼叫方法。</span><span class="sxs-lookup"><span data-stu-id="a24d0-123">Allocate an array of GUIDs with the required size and call the method again.</span></span> <span data-ttu-id="a24d0-124">這次，請將 *pGuids* 設定為數組的位址。</span><span class="sxs-lookup"><span data-stu-id="a24d0-124">This time, set *pGuids* to the address of the array.</span></span> <span data-ttu-id="a24d0-125">方法會使用 DXVA 設定檔 Guid 清單來填入陣列。</span><span class="sxs-lookup"><span data-stu-id="a24d0-125">The method fills the array with the list of DXVA profile GUIDs.</span></span>

## <a name="requirements"></a><span data-ttu-id="a24d0-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="a24d0-126">Requirements</span></span>



| <span data-ttu-id="a24d0-127">需求</span><span class="sxs-lookup"><span data-stu-id="a24d0-127">Requirement</span></span> | <span data-ttu-id="a24d0-128">值</span><span class="sxs-lookup"><span data-stu-id="a24d0-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="a24d0-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a24d0-129">Minimum supported client</span></span><br/> | <span data-ttu-id="a24d0-130">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a24d0-130">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a24d0-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a24d0-131">Minimum supported server</span></span><br/> | <span data-ttu-id="a24d0-132">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a24d0-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a24d0-133">標頭</span><span class="sxs-lookup"><span data-stu-id="a24d0-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="a24d0-134"><dt>Dxva。h</dt></span><span class="sxs-lookup"><span data-stu-id="a24d0-134"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a24d0-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a24d0-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a24d0-136">**IDirect3DVideoDevice9**</span><span class="sxs-lookup"><span data-stu-id="a24d0-136">**IDirect3DVideoDevice9**</span></span>](idirect3dvideodevice9.md)
</dt> </dl>

 

 
