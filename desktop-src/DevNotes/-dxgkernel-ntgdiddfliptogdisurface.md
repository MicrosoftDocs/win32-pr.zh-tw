---
description: 當 Microsoft DirectDraw 在 Windows 圖形裝置介面 (GDI) 介面上來回翻轉時，通知驅動程式。
ms.assetid: e79be33a-24bc-477b-bc67-395fff74309c
title: 'NtGdiDdFlipToGDISurface 函式 (Ntgdi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdFlipToGDISurface
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 7e233bddf72c79507eab1fcefbf3de66460d228e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110672"
---
# <a name="ntgdiddfliptogdisurface-function"></a><span data-ttu-id="ad044-103">NtGdiDdFlipToGDISurface 函式</span><span class="sxs-lookup"><span data-stu-id="ad044-103">NtGdiDdFlipToGDISurface function</span></span>

<span data-ttu-id="ad044-104">\[這項功能可能會隨著每個作業系統修訂而變更。</span><span class="sxs-lookup"><span data-stu-id="ad044-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="ad044-105">相反地，請使用 DirectDraw 和 Microsoft Direct3DAPIs;這些 Api 會防止應用程式進行這類作業系統變更，並隱藏與顯示驅動程式直接互動的許多其他難題。\]</span><span class="sxs-lookup"><span data-stu-id="ad044-105">Instead, use the DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="ad044-106">當 Microsoft DirectDraw 在 Windows 圖形裝置介面 (GDI) 介面上來回翻轉時，通知驅動程式。</span><span class="sxs-lookup"><span data-stu-id="ad044-106">Notifies the driver when Microsoft DirectDraw is flipping to or from a Windows Graphics Device Interface (GDI) surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad044-107">語法</span><span class="sxs-lookup"><span data-stu-id="ad044-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdFlipToGDISurface(
  _In_    HANDLE                   hDirectDraw,
  _Inout_ PDD_FLIPTOGDISURFACEDATA puFlipToGDISurfaceData
);
```



## <a name="parameters"></a><span data-ttu-id="ad044-108">參數</span><span class="sxs-lookup"><span data-stu-id="ad044-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad044-109">*hDirectDraw* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ad044-109">*hDirectDraw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad044-110">先前建立之核心模式 DirectDraw 物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="ad044-110">Handle to previously created kernel-mode DirectDraw object.</span></span>

</dd> <dt>

<span data-ttu-id="ad044-111">*puFlipToGDISurfaceData* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="ad044-111">*puFlipToGDISurfaceData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ad044-112">包含通知資訊之 [DD \_ FLIPTOGDISURFACEDATA](https://msdn.microsoft.com/library/ms793922.aspx) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="ad044-112">Pointer to a [DD\_FLIPTOGDISURFACEDATA](https://msdn.microsoft.com/library/ms793922.aspx) structure that contains the notification information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad044-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="ad044-113">Return value</span></span>

<span data-ttu-id="ad044-114">**NtGdiDdFlipToGDISurface** 會傳回下列其中一個回呼碼。</span><span class="sxs-lookup"><span data-stu-id="ad044-114">**NtGdiDdFlipToGDISurface** returns one of the following callback codes.</span></span>



| <span data-ttu-id="ad044-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="ad044-115">Return code</span></span>                                                                                              | <span data-ttu-id="ad044-116">Description</span><span class="sxs-lookup"><span data-stu-id="ad044-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ad044-117"><dt>**DDHAL \_ 驅動程式已 \_ 處理**</dt></span><span class="sxs-lookup"><span data-stu-id="ad044-117"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="ad044-118">驅動程式已執行作業，並傳回該操作的有效傳回碼。</span><span class="sxs-lookup"><span data-stu-id="ad044-118">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="ad044-119">如果這個程式碼是 DD \_ OK，DirectDraw 或 Direct3D 會繼續執行函數。</span><span class="sxs-lookup"><span data-stu-id="ad044-119">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="ad044-120">否則，DirectDraw 或 Direct3D 會傳回驅動程式所提供的錯誤碼，並中止函數。</span><span class="sxs-lookup"><span data-stu-id="ad044-120">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="ad044-121"><dt>**DDHAL \_ 驅動程式 \_ NOTHANDLED**</dt></span><span class="sxs-lookup"><span data-stu-id="ad044-121"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="ad044-122">驅動程式對要求的作業沒有任何批註。</span><span class="sxs-lookup"><span data-stu-id="ad044-122">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="ad044-123">如果驅動程式必須執行特定的回呼，DirectDraw 或 Direct3D 會報告錯誤狀況。</span><span class="sxs-lookup"><span data-stu-id="ad044-123">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="ad044-124">否則，DirectDraw 或 Direct3D 會處理此作業，就像尚未執行 DirectDraw 或 Direct3D 裝置獨立的執行所定義的驅動程式回呼一樣。</span><span class="sxs-lookup"><span data-stu-id="ad044-124">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ad044-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="ad044-125">Requirements</span></span>



| <span data-ttu-id="ad044-126">需求</span><span class="sxs-lookup"><span data-stu-id="ad044-126">Requirement</span></span> | <span data-ttu-id="ad044-127">值</span><span class="sxs-lookup"><span data-stu-id="ad044-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ad044-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ad044-128">Minimum supported client</span></span><br/> | <span data-ttu-id="ad044-129">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ad044-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="ad044-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ad044-130">Minimum supported server</span></span><br/> | <span data-ttu-id="ad044-131">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ad044-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ad044-132">標頭</span><span class="sxs-lookup"><span data-stu-id="ad044-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad044-133"><dt>Ntgdi。h</dt></span><span class="sxs-lookup"><span data-stu-id="ad044-133"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad044-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ad044-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad044-135">圖形低層級用戶端支援</span><span class="sxs-lookup"><span data-stu-id="ad044-135">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 




