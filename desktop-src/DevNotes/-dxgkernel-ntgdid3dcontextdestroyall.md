---
description: 查詢驅動程式管理的記憶體堆積中的可用記憶體數量。
ms.assetid: d7f8792b-a515-4e70-9474-6a3474b6612b
title: 'NtGdiD3DCoNtextDestroyAll 函式 (Ntgdi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiD3DContextDestroyAll
api_type:
- HeaderDef
api_location:
- Ntgdi.h
ms.openlocfilehash: 8bb42c902555568ebe7a26656cd188e9c8e40213
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847190"
---
# <a name="ntgdid3dcontextdestroyall-function"></a><span data-ttu-id="5210d-103">NtGdiD3DCoNtextDestroyAll 函式</span><span class="sxs-lookup"><span data-stu-id="5210d-103">NtGdiD3DContextDestroyAll function</span></span>

<span data-ttu-id="5210d-104">\[這項功能可能會隨著每個作業系統修訂而變更。</span><span class="sxs-lookup"><span data-stu-id="5210d-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="5210d-105">請改用 Microsoft DirectDraw 和 Microsoft Direct3DAPIs;這些 Api 會防止應用程式進行這類作業系統變更，並隱藏與顯示驅動程式直接互動的許多其他難題。\]</span><span class="sxs-lookup"><span data-stu-id="5210d-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="5210d-106">查詢驅動程式管理的記憶體堆積中的可用記憶體數量。</span><span class="sxs-lookup"><span data-stu-id="5210d-106">Queries the amount of free memory in the driver-managed memory heap.</span></span>

## <a name="syntax"></a><span data-ttu-id="5210d-107">語法</span><span class="sxs-lookup"><span data-stu-id="5210d-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiD3DContextDestroyAll(void);
```



## <a name="parameters"></a><span data-ttu-id="5210d-108">參數</span><span class="sxs-lookup"><span data-stu-id="5210d-108">Parameters</span></span>

<span data-ttu-id="5210d-109">此函式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="5210d-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5210d-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="5210d-110">Return value</span></span>

<span data-ttu-id="5210d-111">**NtGdiD3DCoNtextDestroyAll** 會傳回下列其中一個回呼碼。</span><span class="sxs-lookup"><span data-stu-id="5210d-111">**NtGdiD3DContextDestroyAll** returns one of the following callback codes.</span></span>



| <span data-ttu-id="5210d-112">傳回碼</span><span class="sxs-lookup"><span data-stu-id="5210d-112">Return code</span></span>                                                                                              | <span data-ttu-id="5210d-113">Description</span><span class="sxs-lookup"><span data-stu-id="5210d-113">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5210d-114"><dt>**DDHAL \_ 驅動程式已 \_ 處理**</dt></span><span class="sxs-lookup"><span data-stu-id="5210d-114"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="5210d-115">驅動程式已執行作業，並傳回該操作的有效傳回碼。</span><span class="sxs-lookup"><span data-stu-id="5210d-115">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="5210d-116">如果這個程式碼是 DD \_ OK，DirectDraw 或 Direct3D 會繼續執行函數。</span><span class="sxs-lookup"><span data-stu-id="5210d-116">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="5210d-117">否則，DirectDraw 或 Direct3D 會傳回驅動程式所提供的錯誤碼，並中止函數。</span><span class="sxs-lookup"><span data-stu-id="5210d-117">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="5210d-118"><dt>**DDHAL \_ 驅動程式 \_ NOTHANDLED**</dt></span><span class="sxs-lookup"><span data-stu-id="5210d-118"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="5210d-119">驅動程式對要求的作業沒有任何批註。</span><span class="sxs-lookup"><span data-stu-id="5210d-119">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="5210d-120">如果驅動程式必須執行特定的回呼，DirectDraw 或 Direct3D 會報告錯誤狀況。</span><span class="sxs-lookup"><span data-stu-id="5210d-120">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="5210d-121">否則，DirectDraw 或 Direct3D 會處理此作業，就像尚未執行 DirectDraw 或 Direct3D 裝置獨立的執行所定義的驅動程式回呼一樣。</span><span class="sxs-lookup"><span data-stu-id="5210d-121">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="5210d-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="5210d-122">Requirements</span></span>



| <span data-ttu-id="5210d-123">需求</span><span class="sxs-lookup"><span data-stu-id="5210d-123">Requirement</span></span> | <span data-ttu-id="5210d-124">值</span><span class="sxs-lookup"><span data-stu-id="5210d-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5210d-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5210d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="5210d-126">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5210d-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="5210d-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5210d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="5210d-128">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5210d-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5210d-129">標頭</span><span class="sxs-lookup"><span data-stu-id="5210d-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="5210d-130"><dt>Ntgdi。h</dt></span><span class="sxs-lookup"><span data-stu-id="5210d-130"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5210d-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5210d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5210d-132">圖形低層級用戶端支援</span><span class="sxs-lookup"><span data-stu-id="5210d-132">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 




