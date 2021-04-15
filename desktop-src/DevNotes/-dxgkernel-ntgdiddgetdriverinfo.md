---
description: 查詢驅動程式是否有驅動程式支援的其他 Microsoft DirectDraw 和 Microsoft Direct3D 功能。
ms.assetid: 7169b672-5c61-4fca-860b-5ef426a7f925
title: 'NtGdiDdGetDriverInfo 函式 (Ntgdi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdGetDriverInfo
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 2e9f78ed832015979c6768ec8f09e53ca8d2d4a5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468217"
---
# <a name="ntgdiddgetdriverinfo-function"></a><span data-ttu-id="62fa8-103">NtGdiDdGetDriverInfo 函式</span><span class="sxs-lookup"><span data-stu-id="62fa8-103">NtGdiDdGetDriverInfo function</span></span>

<span data-ttu-id="62fa8-104">\[這項功能可能會隨著每個作業系統修訂而變更。</span><span class="sxs-lookup"><span data-stu-id="62fa8-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="62fa8-105">相反地，請使用 DirectDraw 和 Direct3DAPIs;這些 Api 會防止應用程式進行這類作業系統變更，並隱藏與顯示驅動程式直接互動的許多其他難題。\]</span><span class="sxs-lookup"><span data-stu-id="62fa8-105">Instead, use the DirectDraw and Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="62fa8-106">查詢驅動程式是否有驅動程式支援的其他 Microsoft DirectDraw 和 Microsoft Direct3D 功能。</span><span class="sxs-lookup"><span data-stu-id="62fa8-106">Queries the driver for additional Microsoft DirectDraw and Microsoft Direct3D functionality that the driver supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="62fa8-107">語法</span><span class="sxs-lookup"><span data-stu-id="62fa8-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdGetDriverInfo(
  _In_    HANDLE                hDirectDraw,
  _Inout_ PDD_GETDRIVERINFODATA puGetDriverInfoData
);
```



## <a name="parameters"></a><span data-ttu-id="62fa8-108">參數</span><span class="sxs-lookup"><span data-stu-id="62fa8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62fa8-109">*hDirectDraw* \[在\]</span><span class="sxs-lookup"><span data-stu-id="62fa8-109">*hDirectDraw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62fa8-110">先前建立之核心模式 DirectDraw 物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="62fa8-110">Handle to previously created kernel-mode DirectDraw object.</span></span>

</dd> <dt>

<span data-ttu-id="62fa8-111">*puGetDriverInfoData* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="62fa8-111">*puGetDriverInfoData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="62fa8-112">[DD \_ GETDRIVERINFODATA](https://msdn.microsoft.com/library/ms793868.aspx)結構的指標，其中包含執行查詢所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="62fa8-112">Pointer to a [DD\_GETDRIVERINFODATA](https://msdn.microsoft.com/library/ms793868.aspx) structure that contains the information required to perform the query.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62fa8-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="62fa8-113">Return value</span></span>

<span data-ttu-id="62fa8-114">**NtGdiDdGetDriverInfo** 會傳回下列其中一個回呼碼。</span><span class="sxs-lookup"><span data-stu-id="62fa8-114">**NtGdiDdGetDriverInfo** returns one of the following callback codes.</span></span>



| <span data-ttu-id="62fa8-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="62fa8-115">Return code</span></span>                                                                                              | <span data-ttu-id="62fa8-116">Description</span><span class="sxs-lookup"><span data-stu-id="62fa8-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="62fa8-117"><dt>**DDHAL \_ 驅動程式已 \_ 處理**</dt></span><span class="sxs-lookup"><span data-stu-id="62fa8-117"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="62fa8-118">驅動程式已執行作業，並傳回該操作的有效傳回碼。</span><span class="sxs-lookup"><span data-stu-id="62fa8-118">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="62fa8-119">如果這個程式碼是 DD \_ OK，DirectDraw 或 Direct3D 會繼續執行函數。</span><span class="sxs-lookup"><span data-stu-id="62fa8-119">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="62fa8-120">否則，DirectDraw 或 Direct3D 會傳回驅動程式所提供的錯誤碼，並中止函數。</span><span class="sxs-lookup"><span data-stu-id="62fa8-120">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="62fa8-121"><dt>**DDHAL \_ 驅動程式 \_ NOTHANDLED**</dt></span><span class="sxs-lookup"><span data-stu-id="62fa8-121"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="62fa8-122">驅動程式對要求的作業沒有任何批註。</span><span class="sxs-lookup"><span data-stu-id="62fa8-122">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="62fa8-123">如果驅動程式必須執行特定的回呼，DirectDraw 或 Direct3D 會報告錯誤狀況。</span><span class="sxs-lookup"><span data-stu-id="62fa8-123">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="62fa8-124">否則，DirectDraw 或 Direct3D 會處理此作業，就像尚未執行 DirectDraw 或 Direct3D 裝置獨立的執行所定義的驅動程式回呼一樣。</span><span class="sxs-lookup"><span data-stu-id="62fa8-124">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="62fa8-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="62fa8-125">Requirements</span></span>



| <span data-ttu-id="62fa8-126">需求</span><span class="sxs-lookup"><span data-stu-id="62fa8-126">Requirement</span></span> | <span data-ttu-id="62fa8-127">值</span><span class="sxs-lookup"><span data-stu-id="62fa8-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="62fa8-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="62fa8-128">Minimum supported client</span></span><br/> | <span data-ttu-id="62fa8-129">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="62fa8-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="62fa8-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="62fa8-130">Minimum supported server</span></span><br/> | <span data-ttu-id="62fa8-131">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="62fa8-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="62fa8-132">標頭</span><span class="sxs-lookup"><span data-stu-id="62fa8-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="62fa8-133"><dt>Ntgdi。h</dt></span><span class="sxs-lookup"><span data-stu-id="62fa8-133"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62fa8-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="62fa8-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62fa8-135">圖形低層級用戶端支援</span><span class="sxs-lookup"><span data-stu-id="62fa8-135">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 




