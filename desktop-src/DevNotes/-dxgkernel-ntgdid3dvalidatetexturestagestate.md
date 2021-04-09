---
description: 傳回可執行目前狀態中所指定之混合作業的行程數目。
ms.assetid: 355dae78-cd65-4fc9-8f08-8e5ae123064b
title: 'NtGdiD3DValidateTextureStageState 函式 (Ntgdi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiD3DValidateTextureStageState
api_type:
- HeaderDef
api_location:
- Ntgdi.h
ms.openlocfilehash: 37c852343c70c5d3325926c9108dcab2948fdc95
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847139"
---
# <a name="ntgdid3dvalidatetexturestagestate-function"></a><span data-ttu-id="3799d-103">NtGdiD3DValidateTextureStageState 函式</span><span class="sxs-lookup"><span data-stu-id="3799d-103">NtGdiD3DValidateTextureStageState function</span></span>

<span data-ttu-id="3799d-104">\[這項功能可能會隨著每個作業系統修訂而變更。</span><span class="sxs-lookup"><span data-stu-id="3799d-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="3799d-105">請改用 Microsoft DirectDraw 和 Microsoft Direct3DAPIs;這些 Api 會防止應用程式進行這類作業系統變更，並隱藏與顯示驅動程式直接互動的許多其他難題。\]</span><span class="sxs-lookup"><span data-stu-id="3799d-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="3799d-106">傳回可執行目前狀態中所指定之混合作業的行程數目。</span><span class="sxs-lookup"><span data-stu-id="3799d-106">Returns the number of passes where the hardware can perform the blending operations specified in the current state.</span></span>

## <a name="syntax"></a><span data-ttu-id="3799d-107">語法</span><span class="sxs-lookup"><span data-stu-id="3799d-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiD3DValidateTextureStageState(
  _Inout_ LPD3DNTHAL_VALIDATETEXTURESTAGESTATEDATA pData
);
```



## <a name="parameters"></a><span data-ttu-id="3799d-108">參數</span><span class="sxs-lookup"><span data-stu-id="3799d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3799d-109">*.pdata* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="3799d-109">*pData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3799d-110">[**D3DNTHAL \_ VALIDATETEXTURESTAGESTATEDATA**](/windows-hardware/drivers/ddi/)結構的指標，其中包含驅動程式所需的資訊，以決定和傳回執行混色作業所需的行程數目。</span><span class="sxs-lookup"><span data-stu-id="3799d-110">Pointer to a [**D3DNTHAL\_VALIDATETEXTURESTAGESTATEDATA**](/windows-hardware/drivers/ddi/) structure that contains the information required for the driver to determine and return the number of passes required to perform the blending operations.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3799d-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="3799d-111">Return value</span></span>

<span data-ttu-id="3799d-112">**NtGdiD3DValidateTextureStageState** 會傳回下列其中一個回呼碼。</span><span class="sxs-lookup"><span data-stu-id="3799d-112">**NtGdiD3DValidateTextureStageState** returns one of the following callback codes.</span></span>



| <span data-ttu-id="3799d-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="3799d-113">Return code</span></span>                                                                                              | <span data-ttu-id="3799d-114">Description</span><span class="sxs-lookup"><span data-stu-id="3799d-114">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3799d-115"><dt>**DDHAL \_ 驅動程式已 \_ 處理**</dt></span><span class="sxs-lookup"><span data-stu-id="3799d-115"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="3799d-116">驅動程式已執行作業，並傳回該操作的有效傳回碼。</span><span class="sxs-lookup"><span data-stu-id="3799d-116">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="3799d-117">如果這個程式碼是 DD \_ OK，DirectDraw 或 Direct3D 會繼續執行函數。</span><span class="sxs-lookup"><span data-stu-id="3799d-117">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="3799d-118">否則，DirectDraw 或 Direct3D 會傳回驅動程式所提供的錯誤碼，並中止函數。</span><span class="sxs-lookup"><span data-stu-id="3799d-118">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="3799d-119"><dt>**DDHAL \_ 驅動程式 \_ NOTHANDLED**</dt></span><span class="sxs-lookup"><span data-stu-id="3799d-119"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="3799d-120">驅動程式對要求的作業沒有任何批註。</span><span class="sxs-lookup"><span data-stu-id="3799d-120">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="3799d-121">如果驅動程式必須執行特定的回呼，DirectDraw 或 Direct3D 會報告錯誤狀況。</span><span class="sxs-lookup"><span data-stu-id="3799d-121">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="3799d-122">否則，DirectDraw 或 Direct3D 會處理此作業，就像尚未執行 DirectDraw 或 Direct3D 裝置獨立的執行所定義的驅動程式回呼一樣。</span><span class="sxs-lookup"><span data-stu-id="3799d-122">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3799d-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="3799d-123">Requirements</span></span>



| <span data-ttu-id="3799d-124">需求</span><span class="sxs-lookup"><span data-stu-id="3799d-124">Requirement</span></span> | <span data-ttu-id="3799d-125">值</span><span class="sxs-lookup"><span data-stu-id="3799d-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3799d-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3799d-126">Minimum supported client</span></span><br/> | <span data-ttu-id="3799d-127">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3799d-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="3799d-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3799d-128">Minimum supported server</span></span><br/> | <span data-ttu-id="3799d-129">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3799d-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3799d-130">標頭</span><span class="sxs-lookup"><span data-stu-id="3799d-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="3799d-131"><dt>Ntgdi。h</dt></span><span class="sxs-lookup"><span data-stu-id="3799d-131"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3799d-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3799d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3799d-133">圖形低層級用戶端支援</span><span class="sxs-lookup"><span data-stu-id="3799d-133">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
