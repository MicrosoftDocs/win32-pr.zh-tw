---
description: DoConfigure 方法必須由監視器所執行。 MCSVC 會呼叫這個方法來取得 capture 的設定資訊。
ms.assetid: bc2a3246-28dc-4452-a98e-a8a2447bb127
title: 'IMonitor： (Netmon 的:D oConfigure 方法) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.DoConfigure
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: e9a0ba2ade1095f291d5cb325a0902e6caeac3f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112800"
---
# <a name="imonitordoconfigure-method"></a><span data-ttu-id="830f7-104">IMonitor：:D oConfigure 方法</span><span class="sxs-lookup"><span data-stu-id="830f7-104">IMonitor::DoConfigure method</span></span>

<span data-ttu-id="830f7-105">**DoConfigure** 方法必須由監視器所執行。</span><span class="sxs-lookup"><span data-stu-id="830f7-105">The **DoConfigure** method must be implemented by the monitor.</span></span> <span data-ttu-id="830f7-106">MCSVC 會呼叫這個方法來取得 capture 的設定資訊。</span><span class="sxs-lookup"><span data-stu-id="830f7-106">The MCSVC calls this method to obtain configuration information for the capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="830f7-107">語法</span><span class="sxs-lookup"><span data-stu-id="830f7-107">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE DoConfigure(
  [in]  char *pName,
  [in]  char *pConfiguration,
  [out] char **ppScriptInstance
);
```



## <a name="parameters"></a><span data-ttu-id="830f7-108">參數</span><span class="sxs-lookup"><span data-stu-id="830f7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="830f7-109">*pName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="830f7-109">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="830f7-110">監視器實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="830f7-110">Name of an instance of the monitor.</span></span>

</dd> <dt>

<span data-ttu-id="830f7-111">*pConfiguration* \[在\]</span><span class="sxs-lookup"><span data-stu-id="830f7-111">*pConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="830f7-112">MCSVC 所提供的設定字串。</span><span class="sxs-lookup"><span data-stu-id="830f7-112">Configuration string provided by the MCSVC.</span></span> <span data-ttu-id="830f7-113">此監視器必須剖析此字串中的設定資料。</span><span class="sxs-lookup"><span data-stu-id="830f7-113">The monitor must parse this string for configuration data.</span></span>

</dd> <dt>

<span data-ttu-id="830f7-114">*ppScriptInstance* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="830f7-114">*ppScriptInstance* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="830f7-115">用來設定監視的 HTML 字串位址。</span><span class="sxs-lookup"><span data-stu-id="830f7-115">Address of the HTML string used to configure the monitor.</span></span> <span data-ttu-id="830f7-116">如果預設腳本用於設定，則此值應該設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="830f7-116">If a default script is used for configuration, this value should be set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="830f7-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="830f7-117">Return value</span></span>

<span data-ttu-id="830f7-118">如果方法成功，則傳回值為 S \_ OK (與 >aad-userreadusingalternativesecurityid-noerror) 相同，而且 MCSVC 將會執行監視器。</span><span class="sxs-lookup"><span data-stu-id="830f7-118">If the method is successful, the return value is S\_OK (which is the same as NOERROR), and the MCSVC will run the monitor.</span></span>

<span data-ttu-id="830f7-119">如果此方法不成功，則傳回值會是錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="830f7-119">If the method is unsuccessful, the return value is an error code.</span></span> <span data-ttu-id="830f7-120">NMERR 監視器設定的 \_ 傳回值 \_ \_ 是可接受的，但是當傳回此錯誤時，在未來的 **DoConfigure** 呼叫成功之前，無法啟動監視器。</span><span class="sxs-lookup"><span data-stu-id="830f7-120">A return value of NMERR\_MONITOR\_CONFIG\_FAILED is acceptable, but when this error is returned, the monitor cannot start until a future **DoConfigure** call succeeds.</span></span> <span data-ttu-id="830f7-121">任何其他錯誤都會導致無法啟用監視的實例。</span><span class="sxs-lookup"><span data-stu-id="830f7-121">Any other error prevents the instance of the monitor from being enabled.</span></span>

## <a name="remarks"></a><span data-ttu-id="830f7-122">備註</span><span class="sxs-lookup"><span data-stu-id="830f7-122">Remarks</span></span>

<span data-ttu-id="830f7-123">MCSVC 會在連接到網路之後，以及呼叫 [IRTC：： Configure](irtc-configure.md) 方法之前呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="830f7-123">The MCSVC calls this method after it has connected to the network and before the [IRTC::Configure](irtc-configure.md) method is called.</span></span>

<span data-ttu-id="830f7-124">此監視器可以儲存此呼叫所提供的資訊、更新 HTML 腳本或設定字串，以及在 NPP BLOB 中設定 [捕捉篩選](capture-filters.md) 。</span><span class="sxs-lookup"><span data-stu-id="830f7-124">The monitor can store information provided by this call, update the HTML script or configuration string, and set the [capture filter](capture-filters.md) in the NPP BLOB.</span></span>

<span data-ttu-id="830f7-125">MCSVC 可能會呼叫這個方法數次，但在監視器正在捕獲資料時無法呼叫。</span><span class="sxs-lookup"><span data-stu-id="830f7-125">The MCSVC may call this method several times, but it cannot be not called while the monitor is capturing data.</span></span> <span data-ttu-id="830f7-126">請注意，每次 [NPP](network-packet-providers.md) 啟動捕獲時，都必須設定網路的連接。</span><span class="sxs-lookup"><span data-stu-id="830f7-126">Note that every time an [NPP](network-packet-providers.md) starts a capture, the connection to the network must be configured.</span></span> <span data-ttu-id="830f7-127">這項限制包含 NPP 啟動和停止相同捕捉的情況。</span><span class="sxs-lookup"><span data-stu-id="830f7-127">This restriction includes situations in which the NPP starts and stops the same capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="830f7-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="830f7-128">Requirements</span></span>



| <span data-ttu-id="830f7-129">需求</span><span class="sxs-lookup"><span data-stu-id="830f7-129">Requirement</span></span> | <span data-ttu-id="830f7-130">值</span><span class="sxs-lookup"><span data-stu-id="830f7-130">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="830f7-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="830f7-131">Minimum supported client</span></span><br/> | <span data-ttu-id="830f7-132">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="830f7-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="830f7-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="830f7-133">Minimum supported server</span></span><br/> | <span data-ttu-id="830f7-134">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="830f7-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="830f7-135">標頭</span><span class="sxs-lookup"><span data-stu-id="830f7-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="830f7-136"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="830f7-136"><dt>Netmon.h</dt></span></span> </dl> |



 

 




