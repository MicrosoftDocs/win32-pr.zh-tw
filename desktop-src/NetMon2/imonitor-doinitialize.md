---
description: DoInitialize 方法必須由監視器所執行。 在呼叫 NPPs IRTCConnect 方法之前，MCSVC 會呼叫這個方法來立即取得 capture 篩選器。
ms.assetid: 5e43be75-21b3-4f37-ad53-3ffdd55f56a1
title: 'IMonitorDoInitialize 方法 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.DoInitialize
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: 93133ce8204e49d080f87635ad6952685f2ba82d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510967"
---
# <a name="imonitordoinitialize-method"></a><span data-ttu-id="6000f-104">IMonitor：:D oInitialize 方法</span><span class="sxs-lookup"><span data-stu-id="6000f-104">IMonitor::DoInitialize method</span></span>

<span data-ttu-id="6000f-105">**DoInitialize** 方法必須由監視器所執行。</span><span class="sxs-lookup"><span data-stu-id="6000f-105">The **DoInitialize** method must be implemented by the monitor.</span></span> <span data-ttu-id="6000f-106">在呼叫 NPP 的 [IRTC：： Connect](irtc-connect.md) 方法之前，MCSVC 會呼叫這個方法來立即取得 capture 篩選器。</span><span class="sxs-lookup"><span data-stu-id="6000f-106">The MCSVC calls this method to obtain a capture filter immediately before calling the NPP's [IRTC::Connect](irtc-connect.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6000f-107">語法</span><span class="sxs-lookup"><span data-stu-id="6000f-107">Syntax</span></span>


```C++
HRESULT DoInitialize(
  [in]      IUnknown *pUnkMonitorCtrl,
  [in, out] HBLOB    hNPPBlob
);
```



## <a name="parameters"></a><span data-ttu-id="6000f-108">參數</span><span class="sxs-lookup"><span data-stu-id="6000f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6000f-109">*pUnkMonitorCtrl* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6000f-109">*pUnkMonitorCtrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6000f-110">MCSVC 傳入的 [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) 指標。</span><span class="sxs-lookup"><span data-stu-id="6000f-110">An [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) pointer passed in by the MCSVC.</span></span> <span data-ttu-id="6000f-111">若要取得支援的監視器控制項介面，監視器必須在指標上呼叫 [IUnknown：： QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 。</span><span class="sxs-lookup"><span data-stu-id="6000f-111">To obtain a supported monitor control interface, the monitor must call [IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the pointer.</span></span>

</dd> <dt>

<span data-ttu-id="6000f-112">*hNPPBlob* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="6000f-112">*hNPPBlob* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6000f-113">在輸入上，NPP BLOB 的控制碼。</span><span class="sxs-lookup"><span data-stu-id="6000f-113">On input, a handle to an NPP BLOB.</span></span>

<span data-ttu-id="6000f-114">在輸出中，包含 capture 篩選的 NPP BLOB。</span><span class="sxs-lookup"><span data-stu-id="6000f-114">On output, an NPP BLOB that contains a capture filter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6000f-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="6000f-115">Return value</span></span>

<span data-ttu-id="6000f-116">如果方法成功，則傳回值為 S \_ OK (與 >aad-userreadusingalternativesecurityid-noerror) 相同。</span><span class="sxs-lookup"><span data-stu-id="6000f-116">If the method is successful, the return value is S\_OK (which is the same as NOERROR).</span></span>

<span data-ttu-id="6000f-117">如果此方法不成功，則傳回值會是錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="6000f-117">If the method is unsuccessful, the return value is an error code.</span></span> <span data-ttu-id="6000f-118">發生錯誤時，MCSVC 不會在介面指標上建立監視或呼叫 [IUnknown：： Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) 。</span><span class="sxs-lookup"><span data-stu-id="6000f-118">On error, the MCSVC will not create the monitor or call [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) on the interface pointer.</span></span>

## <a name="remarks"></a><span data-ttu-id="6000f-119">備註</span><span class="sxs-lookup"><span data-stu-id="6000f-119">Remarks</span></span>

<span data-ttu-id="6000f-120">MCSVC 會呼叫 **DoInitialize** 方法，以執行任何必要的監視器初始化。</span><span class="sxs-lookup"><span data-stu-id="6000f-120">The MCSVC calls the **DoInitialize** method to perform any required monitor initialization.</span></span>

## <a name="requirements"></a><span data-ttu-id="6000f-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="6000f-121">Requirements</span></span>



| <span data-ttu-id="6000f-122">需求</span><span class="sxs-lookup"><span data-stu-id="6000f-122">Requirement</span></span> | <span data-ttu-id="6000f-123">值</span><span class="sxs-lookup"><span data-stu-id="6000f-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6000f-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6000f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6000f-125">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6000f-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="6000f-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6000f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6000f-127">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6000f-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="6000f-128">標頭</span><span class="sxs-lookup"><span data-stu-id="6000f-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="6000f-129"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="6000f-129"><dt>Netmon.h</dt></span></span> </dl> |



 

