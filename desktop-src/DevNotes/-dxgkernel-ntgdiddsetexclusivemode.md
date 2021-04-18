---
description: 當 Microsoft DirectDraw 應用程式切換至或從獨佔模式切換時，通知驅動程式。
ms.assetid: f2b63d90-7ede-479f-a2fd-ae9870c4d7b9
title: 'NtGdiDdSetExclusiveMode 函式 (Ntgdi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdSetExclusiveMode
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 1d2420f4ae093b4bfc3f68871daefd5c20da308e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971303"
---
# <a name="ntgdiddsetexclusivemode-function"></a><span data-ttu-id="f969d-103">NtGdiDdSetExclusiveMode 函式</span><span class="sxs-lookup"><span data-stu-id="f969d-103">NtGdiDdSetExclusiveMode function</span></span>

<span data-ttu-id="f969d-104">\[這項功能可能會隨著每個作業系統修訂而變更。</span><span class="sxs-lookup"><span data-stu-id="f969d-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="f969d-105">相反地，請使用 DirectDraw 和 Microsoft Direct3DAPIs;這些 Api 會防止應用程式進行這類作業系統變更，並隱藏與顯示驅動程式直接互動的許多其他難題。\]</span><span class="sxs-lookup"><span data-stu-id="f969d-105">Instead, use the DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="f969d-106">當 Microsoft DirectDraw 應用程式切換至或從獨佔模式切換時，通知驅動程式。</span><span class="sxs-lookup"><span data-stu-id="f969d-106">Notifies the driver when a Microsoft DirectDraw application is switching to or from exclusive mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="f969d-107">語法</span><span class="sxs-lookup"><span data-stu-id="f969d-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdSetExclusiveMode(
  _In_    HANDLE                   hDirectDraw,
  _Inout_ PDD_SETEXCLUSIVEMODEDATA puSetExclusiveModeData
);
```



## <a name="parameters"></a><span data-ttu-id="f969d-108">參數</span><span class="sxs-lookup"><span data-stu-id="f969d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f969d-109">*hDirectDraw* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f969d-109">*hDirectDraw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f969d-110">先前建立之核心模式 DirectDraw 物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="f969d-110">Handle to previously created kernel-mode DirectDraw object.</span></span>

</dd> <dt>

<span data-ttu-id="f969d-111">*puSetExclusiveModeData* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="f969d-111">*puSetExclusiveModeData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f969d-112">包含通知資訊之 [**DD \_ SETEXCLUSIVEMODEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_setexclusivemodedata) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="f969d-112">Pointer to a [**DD\_SETEXCLUSIVEMODEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_setexclusivemodedata) structure that contains the notification information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f969d-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="f969d-113">Return value</span></span>

<span data-ttu-id="f969d-114">**NtGdiDdSetExclusiveMode** 會傳回下列其中一個回呼碼。</span><span class="sxs-lookup"><span data-stu-id="f969d-114">**NtGdiDdSetExclusiveMode** returns one of the following callback codes.</span></span>



| <span data-ttu-id="f969d-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="f969d-115">Return code</span></span>                                                                                              | <span data-ttu-id="f969d-116">Description</span><span class="sxs-lookup"><span data-stu-id="f969d-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f969d-117"><dt>**DDHAL \_ 驅動程式已 \_ 處理**</dt></span><span class="sxs-lookup"><span data-stu-id="f969d-117"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="f969d-118">驅動程式已執行作業，並傳回該操作的有效傳回碼。</span><span class="sxs-lookup"><span data-stu-id="f969d-118">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="f969d-119">如果這個程式碼是 DD \_ OK，DirectDraw 或 Direct3D 會繼續執行函數。</span><span class="sxs-lookup"><span data-stu-id="f969d-119">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="f969d-120">否則，DirectDraw 或 Direct3D 會傳回驅動程式所提供的錯誤碼，並中止函數。</span><span class="sxs-lookup"><span data-stu-id="f969d-120">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="f969d-121"><dt>**DDHAL \_ 驅動程式 \_ NOTHANDLED**</dt></span><span class="sxs-lookup"><span data-stu-id="f969d-121"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="f969d-122">驅動程式對要求的作業沒有任何批註。</span><span class="sxs-lookup"><span data-stu-id="f969d-122">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="f969d-123">如果驅動程式必須執行特定的回呼，DirectDraw 或 Direct3D 會報告錯誤狀況。</span><span class="sxs-lookup"><span data-stu-id="f969d-123">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="f969d-124">否則，DirectDraw 或 Direct3D 會處理此作業，就像尚未執行 DirectDraw 或 Direct3D 裝置獨立的執行所定義的驅動程式回呼一樣。</span><span class="sxs-lookup"><span data-stu-id="f969d-124">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f969d-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="f969d-125">Requirements</span></span>



| <span data-ttu-id="f969d-126">需求</span><span class="sxs-lookup"><span data-stu-id="f969d-126">Requirement</span></span> | <span data-ttu-id="f969d-127">值</span><span class="sxs-lookup"><span data-stu-id="f969d-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f969d-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f969d-128">Minimum supported client</span></span><br/> | <span data-ttu-id="f969d-129">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f969d-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="f969d-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f969d-130">Minimum supported server</span></span><br/> | <span data-ttu-id="f969d-131">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f969d-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f969d-132">標頭</span><span class="sxs-lookup"><span data-stu-id="f969d-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="f969d-133"><dt>Ntgdi。h</dt></span><span class="sxs-lookup"><span data-stu-id="f969d-133"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f969d-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f969d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f969d-135">圖形低層級用戶端支援</span><span class="sxs-lookup"><span data-stu-id="f969d-135">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
