---
description: OnStart 方法是可由監視器執行的選擇性方法。 MCSVC 會呼叫這個方法來要求監視啟動捕獲。
ms.assetid: 992ee27e-aaba-4e65-989b-e3f0fbd542ea
title: 'IMonitor：： OnStart 方法 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.OnStart
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: ca9e5e17de1d6baf2c79cc0077c5e2036a2a6246
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112208"
---
# <a name="imonitoronstart-method"></a><span data-ttu-id="4d16c-104">IMonitor：： OnStart 方法</span><span class="sxs-lookup"><span data-stu-id="4d16c-104">IMonitor::OnStart method</span></span>

<span data-ttu-id="4d16c-105">**OnStart** 方法是可由監視器執行的選擇性方法。</span><span class="sxs-lookup"><span data-stu-id="4d16c-105">The **OnStart** method is an optional method that can be implemented by the monitor.</span></span> <span data-ttu-id="4d16c-106">MCSVC 會呼叫這個方法來要求監視啟動捕獲。</span><span class="sxs-lookup"><span data-stu-id="4d16c-106">The MCSVC calls this method to request that the monitor start the capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d16c-107">語法</span><span class="sxs-lookup"><span data-stu-id="4d16c-107">Syntax</span></span>


```C++
HRESULT OnStart(
  [in] IUnknown *pUnkNPP
);
```



## <a name="parameters"></a><span data-ttu-id="4d16c-108">參數</span><span class="sxs-lookup"><span data-stu-id="4d16c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d16c-109">*pUnkNPP* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4d16c-109">*pUnkNPP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d16c-110">[IRTC](irtc.md)介面的[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)指標。</span><span class="sxs-lookup"><span data-stu-id="4d16c-110">An [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) pointer to the [IRTC](irtc.md) interface.</span></span> <span data-ttu-id="4d16c-111">監視器可以使用這個介面來取得可用來判斷是否應該啟動 capture 的統計資料。</span><span class="sxs-lookup"><span data-stu-id="4d16c-111">The monitor can use this interface to obtain statistics that can be used to determine if the capture should be started.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d16c-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="4d16c-112">Return value</span></span>

<span data-ttu-id="4d16c-113">如果方法成功，則傳回值為 S \_ OK (與 >aad-userreadusingalternativesecurityid-noerror) 相同。</span><span class="sxs-lookup"><span data-stu-id="4d16c-113">If the method is successful, the return value is S\_OK (which is the same as NOERROR).</span></span> <span data-ttu-id="4d16c-114">傳回 S \_ OK 時，MCSVC 會呼叫 [IRTC：： Start](irtc-start.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="4d16c-114">When S\_OK is returned, the MCSVC calls the [IRTC::Start](irtc-start.md) method.</span></span>

<span data-ttu-id="4d16c-115">如果此方法不成功，則傳回值會是錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="4d16c-115">If the method is unsuccessful, the return value is an error code.</span></span> <span data-ttu-id="4d16c-116">如果傳回任何錯誤碼，MCSVC 將不會啟動 capture。</span><span class="sxs-lookup"><span data-stu-id="4d16c-116">The MCSVC will not start the capture if any error code is returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d16c-117">備註</span><span class="sxs-lookup"><span data-stu-id="4d16c-117">Remarks</span></span>

<span data-ttu-id="4d16c-118">MCSVC 會先呼叫這個方法，然後呼叫 NPP 的 [IRTC：： start](irtc-start.md) 方法來啟動 capture。</span><span class="sxs-lookup"><span data-stu-id="4d16c-118">The MCSVC calls this method before the NPP's [IRTC::Start](irtc-start.md) method is called to start the capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d16c-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="4d16c-119">Requirements</span></span>



| <span data-ttu-id="4d16c-120">需求</span><span class="sxs-lookup"><span data-stu-id="4d16c-120">Requirement</span></span> | <span data-ttu-id="4d16c-121">值</span><span class="sxs-lookup"><span data-stu-id="4d16c-121">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="4d16c-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4d16c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4d16c-123">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4d16c-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="4d16c-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4d16c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4d16c-125">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4d16c-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="4d16c-126">標頭</span><span class="sxs-lookup"><span data-stu-id="4d16c-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="4d16c-127"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="4d16c-127"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d16c-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4d16c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d16c-129">IMonitor</span><span class="sxs-lookup"><span data-stu-id="4d16c-129">IMonitor</span></span>](imonitor.md)
</dt> <dt>

[<span data-ttu-id="4d16c-130">網路封包提供者</span><span class="sxs-lookup"><span data-stu-id="4d16c-130">Network Packet Providers</span></span>](network-packet-providers.md)
</dt> </dl>

 

