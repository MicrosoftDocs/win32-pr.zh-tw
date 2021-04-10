---
description: 通知驅動程式，軟體解碼器將開始使用具有指定之 GUID 的動作補償。
ms.assetid: c9a55428-7fe6-45dd-987a-d9ab8ae8a1cb
title: 'NtGdiDdCreateMoComp 函式 (Ntgdi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCreateMoComp
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: f1705b5bf7ac5eddd1ac39e14f3b91b7fd3728cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110589"
---
# <a name="ntgdiddcreatemocomp-function"></a><span data-ttu-id="1dfe2-103">NtGdiDdCreateMoComp 函式</span><span class="sxs-lookup"><span data-stu-id="1dfe2-103">NtGdiDdCreateMoComp function</span></span>

<span data-ttu-id="1dfe2-104">\[這項功能可能會隨著每個作業系統修訂而變更。</span><span class="sxs-lookup"><span data-stu-id="1dfe2-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="1dfe2-105">請改用 Microsoft DirectDraw 和 Microsoft Direct3DAPIs;這些 Api 會防止應用程式進行這類作業系統變更，並隱藏與顯示驅動程式直接互動的許多其他難題。\]</span><span class="sxs-lookup"><span data-stu-id="1dfe2-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="1dfe2-106">通知驅動程式，軟體解碼器將開始使用具有指定之 GUID 的動作補償。</span><span class="sxs-lookup"><span data-stu-id="1dfe2-106">Notifies the driver that a software decoder will start using motion compensation with the specified GUID.</span></span>

## <a name="syntax"></a><span data-ttu-id="1dfe2-107">語法</span><span class="sxs-lookup"><span data-stu-id="1dfe2-107">Syntax</span></span>


```C++
HANDLE APIENTRY NtGdiDdCreateMoComp(
  _In_    HANDLE               hDirectDraw,
  _Inout_ PDD_CREATEMOCOMPDATA puCreateMoCompData
);
```



## <a name="parameters"></a><span data-ttu-id="1dfe2-108">參數</span><span class="sxs-lookup"><span data-stu-id="1dfe2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1dfe2-109">*hDirectDraw* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1dfe2-109">*hDirectDraw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1dfe2-110">針對要使用動作補償的裝置，處理先前建立的 DirectDraw 核心模式物件。</span><span class="sxs-lookup"><span data-stu-id="1dfe2-110">Handle to a previously created DirectDraw kernel-mode object for the device on which motion compensation is to be used.</span></span>

</dd> <dt>

<span data-ttu-id="1dfe2-111">*puCreateMoCompData* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="1dfe2-111">*puCreateMoCompData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1dfe2-112">[**DD \_ CREATEMOCOMPDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_createmocompdata)結構的指標，其中包含開始使用動作補償所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="1dfe2-112">Pointer to a [**DD\_CREATEMOCOMPDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_createmocompdata) structure that contains the information required to begin using motion compensation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1dfe2-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="1dfe2-113">Return value</span></span>

<span data-ttu-id="1dfe2-114">**NtGdiDdCreateMoComp** 會傳回下列其中一個回呼碼。</span><span class="sxs-lookup"><span data-stu-id="1dfe2-114">**NtGdiDdCreateMoComp** returns one of the following callback codes.</span></span>



| <span data-ttu-id="1dfe2-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="1dfe2-115">Return code</span></span>                                                                                              | <span data-ttu-id="1dfe2-116">Description</span><span class="sxs-lookup"><span data-stu-id="1dfe2-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1dfe2-117"><dt>**DDHAL \_ 驅動程式已 \_ 處理**</dt></span><span class="sxs-lookup"><span data-stu-id="1dfe2-117"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="1dfe2-118">驅動程式已執行作業，並傳回該操作的有效傳回碼。</span><span class="sxs-lookup"><span data-stu-id="1dfe2-118">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="1dfe2-119">如果這個程式碼是 DD \_ OK，DirectDraw 或 Direct3D 會繼續執行函數。</span><span class="sxs-lookup"><span data-stu-id="1dfe2-119">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="1dfe2-120">否則，DirectDraw 或 Direct3D 會傳回驅動程式所提供的錯誤碼，並中止函數。</span><span class="sxs-lookup"><span data-stu-id="1dfe2-120">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="1dfe2-121"><dt>**DDHAL \_ 驅動程式 \_ NOTHANDLED**</dt></span><span class="sxs-lookup"><span data-stu-id="1dfe2-121"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="1dfe2-122">驅動程式對要求的作業沒有任何批註。</span><span class="sxs-lookup"><span data-stu-id="1dfe2-122">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="1dfe2-123">如果驅動程式必須執行特定的回呼，DirectDraw 或 Direct3D 會報告錯誤狀況。</span><span class="sxs-lookup"><span data-stu-id="1dfe2-123">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="1dfe2-124">否則，DirectDraw 或 Direct3D 會處理此作業，就像尚未執行 DirectDraw 或 Direct3D 裝置獨立的執行所定義的驅動程式回呼一樣。</span><span class="sxs-lookup"><span data-stu-id="1dfe2-124">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1dfe2-125">備註</span><span class="sxs-lookup"><span data-stu-id="1dfe2-125">Remarks</span></span>

<span data-ttu-id="1dfe2-126">如需詳細資訊，請參閱 Microsoft (DDK) 的 Microsoft DirectX 影片加速驅動程式開發工具組。</span><span class="sxs-lookup"><span data-stu-id="1dfe2-126">For more information, see the Microsoft DirectX Video Acceleration Driver Development Kit (DDK).</span></span>

## <a name="requirements"></a><span data-ttu-id="1dfe2-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="1dfe2-127">Requirements</span></span>



| <span data-ttu-id="1dfe2-128">需求</span><span class="sxs-lookup"><span data-stu-id="1dfe2-128">Requirement</span></span> | <span data-ttu-id="1dfe2-129">值</span><span class="sxs-lookup"><span data-stu-id="1dfe2-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1dfe2-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1dfe2-130">Minimum supported client</span></span><br/> | <span data-ttu-id="1dfe2-131">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1dfe2-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="1dfe2-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1dfe2-132">Minimum supported server</span></span><br/> | <span data-ttu-id="1dfe2-133">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1dfe2-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1dfe2-134">標頭</span><span class="sxs-lookup"><span data-stu-id="1dfe2-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="1dfe2-135"><dt>Ntgdi。h</dt></span><span class="sxs-lookup"><span data-stu-id="1dfe2-135"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1dfe2-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1dfe2-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1dfe2-137">圖形低層級用戶端支援</span><span class="sxs-lookup"><span data-stu-id="1dfe2-137">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
