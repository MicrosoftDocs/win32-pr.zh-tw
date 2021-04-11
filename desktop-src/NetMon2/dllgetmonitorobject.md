---
description: DllGetMonitorObject 函式必須由監視器所執行。 MCSVC 會呼叫這個函式來建立監視的實例。
ms.assetid: 2c39f752-264c-4ab9-8710-a0d660c4772f
title: 'DllGetMonitorObject 回呼函數 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DllGetMonitorObject
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 723c085fe86e8c24ebc13d83c760e5bfdd08eab2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852107"
---
# <a name="dllgetmonitorobject-callback-function"></a><span data-ttu-id="5a6a2-104">DllGetMonitorObject 回呼函式</span><span class="sxs-lookup"><span data-stu-id="5a6a2-104">DllGetMonitorObject callback function</span></span>

<span data-ttu-id="5a6a2-105">**DllGetMonitorObject** 函式必須由監視器所執行。</span><span class="sxs-lookup"><span data-stu-id="5a6a2-105">The **DllGetMonitorObject** function must be implemented by the monitor.</span></span> <span data-ttu-id="5a6a2-106">MCSVC 會呼叫這個函式來建立監視的實例。</span><span class="sxs-lookup"><span data-stu-id="5a6a2-106">The MCSVC calls this function to create an instance of the monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a6a2-107">語法</span><span class="sxs-lookup"><span data-stu-id="5a6a2-107">Syntax</span></span>


```C++
HRESULT DllGetMonitorObject(
  _In_  REFIID riid,
  _Out_ LPVOID *ppObj
);
```



## <a name="parameters"></a><span data-ttu-id="5a6a2-108">參數</span><span class="sxs-lookup"><span data-stu-id="5a6a2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a6a2-109">*riid* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5a6a2-109">*riid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a6a2-110">監視器的 UUID （如下所示），如 IMonitor .h 標頭檔中所定義。</span><span class="sxs-lookup"><span data-stu-id="5a6a2-110">UUID of monitors, shown below, as defined in the IMonitor.h header file.</span></span> <span data-ttu-id="5a6a2-111">如果提供的 UUID 無效，則函式會失敗，而且監視器必須傳回 E \_ NOINTERFACE。</span><span class="sxs-lookup"><span data-stu-id="5a6a2-111">If an invalid UUID is provided, the function fails, and the monitor must return E\_NOINTERFACE.</span></span>

``` syntax
IID_IMonitor
```

</dd> <dt>

<span data-ttu-id="5a6a2-112">*ppObj* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="5a6a2-112">*ppObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5a6a2-113">指標，指向接收在 *riid* 中要求之介面的指標。</span><span class="sxs-lookup"><span data-stu-id="5a6a2-113">Pointer to a pointer that receives the interface requested in *riid*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a6a2-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="5a6a2-114">Return value</span></span>

<span data-ttu-id="5a6a2-115">如果函式成功，則傳回值為 S \_ OK (與 >aad-userreadusingalternativesecurityid-noerror) 相同。</span><span class="sxs-lookup"><span data-stu-id="5a6a2-115">If the function is successful, the return value is S\_OK (which is the same as NOERROR).</span></span>

<span data-ttu-id="5a6a2-116">如果函式不成功，則傳回值為失敗碼。</span><span class="sxs-lookup"><span data-stu-id="5a6a2-116">If the function is unsuccessful, the return value is a failure code.</span></span> <span data-ttu-id="5a6a2-117">傳回失敗碼時，MCSVC 不會建立監視物件，也不會在介面指標上呼叫 [IUnknown：： Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) 方法。</span><span class="sxs-lookup"><span data-stu-id="5a6a2-117">When a failure code is returned, the MCSVC does not create the monitor object, and the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method is not called on the interface pointer.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a6a2-118">備註</span><span class="sxs-lookup"><span data-stu-id="5a6a2-118">Remarks</span></span>

<span data-ttu-id="5a6a2-119">每次 MCSVC 嘗試建立監視的實例時，就會呼叫 **DllGetMonitorObject** 函數。</span><span class="sxs-lookup"><span data-stu-id="5a6a2-119">The **DllGetMonitorObject** function is called each time the MCSVC tries to create an instance of the monitor.</span></span> <span data-ttu-id="5a6a2-120">此函式刻意為較常見的 [**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject) 函式提供強式非常相似。</span><span class="sxs-lookup"><span data-stu-id="5a6a2-120">This function intentionally bears a strong resemblance to the more common [**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject) function.</span></span> <span data-ttu-id="5a6a2-121">主要差異在於 CLSID 未傳遞至 **DllGetMonitorObject**。</span><span class="sxs-lookup"><span data-stu-id="5a6a2-121">The main difference is that a CLSID is not passed in to **DllGetMonitorObject**.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a6a2-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="5a6a2-122">Requirements</span></span>



| <span data-ttu-id="5a6a2-123">需求</span><span class="sxs-lookup"><span data-stu-id="5a6a2-123">Requirement</span></span> | <span data-ttu-id="5a6a2-124">值</span><span class="sxs-lookup"><span data-stu-id="5a6a2-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5a6a2-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5a6a2-125">Minimum supported client</span></span><br/> | <span data-ttu-id="5a6a2-126">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5a6a2-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="5a6a2-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5a6a2-127">Minimum supported server</span></span><br/> | <span data-ttu-id="5a6a2-128">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5a6a2-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="5a6a2-129">標頭</span><span class="sxs-lookup"><span data-stu-id="5a6a2-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a6a2-130"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="5a6a2-130"><dt>Netmon.h</dt></span></span> </dl> |



 

