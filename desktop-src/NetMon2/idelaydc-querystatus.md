---
description: QueryStatus 方法會捕獲 NPP 的狀態。
ms.assetid: b035d495-a078-4436-9501-0a30fbfa7268
title: 'IDelaydC：： QueryStatus 方法 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.QueryStatus
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: cff92dfec95555076f9edba5a1b591f0ef905c1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106975034"
---
# <a name="idelaydcquerystatus-method"></a><span data-ttu-id="cfa9e-103">IDelaydC：： QueryStatus 方法</span><span class="sxs-lookup"><span data-stu-id="cfa9e-103">IDelaydC::QueryStatus method</span></span>

<span data-ttu-id="cfa9e-104">**QueryStatus** 方法會捕獲 NPP 的狀態。</span><span class="sxs-lookup"><span data-stu-id="cfa9e-104">The **QueryStatus** method retrieves the status of the NPP.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfa9e-105">語法</span><span class="sxs-lookup"><span data-stu-id="cfa9e-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE QueryStatus(
  [out] NETWORKSTATUS *pNetworkStatus
);
```



## <a name="parameters"></a><span data-ttu-id="cfa9e-106">參數</span><span class="sxs-lookup"><span data-stu-id="cfa9e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfa9e-107">*pNetworkStatus* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="cfa9e-107">*pNetworkStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cfa9e-108">傳回之 >networkstatus 結構的指標，指出目前狀態 (在 NPP 的) 上進行的[](networkstatus.md) 、暫停、停止等等。</span><span class="sxs-lookup"><span data-stu-id="cfa9e-108">Pointer to a returned [NETWORKSTATUS](networkstatus.md) structure that indicates the current state (capturing, paused, stopped, and so on) of the NPP.</span></span> <span data-ttu-id="cfa9e-109">您必須負責配置和釋放與 **>networkstatus** 結構相關聯的記憶體。</span><span class="sxs-lookup"><span data-stu-id="cfa9e-109">It is your responsibility to allocate and free the memory associated with the **NETWORKSTATUS** structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfa9e-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="cfa9e-110">Return value</span></span>

<span data-ttu-id="cfa9e-111">如果方法成功，則傳回值為 NMERR \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="cfa9e-111">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="cfa9e-112">如果此方法不成功，則傳回值會是下列錯誤碼：</span><span class="sxs-lookup"><span data-stu-id="cfa9e-112">If the method is unsuccessful, the return value is the following error code:</span></span>



| <span data-ttu-id="cfa9e-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="cfa9e-113">Return code</span></span>                                                                                              | <span data-ttu-id="cfa9e-114">Description</span><span class="sxs-lookup"><span data-stu-id="cfa9e-114">Description</span></span>                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cfa9e-115"><dt>**NMERR \_ 不正確 \_ 參數**</dt></span><span class="sxs-lookup"><span data-stu-id="cfa9e-115"><dt>**NMERR\_INVALID\_PARAMETER**</dt></span></span> </dl> | <span data-ttu-id="cfa9e-116">*PNetworkStatus* 參數未指向有效的 [>networkstatus](networkstatus.md)結構。</span><span class="sxs-lookup"><span data-stu-id="cfa9e-116">The *pNetworkStatus* parameter is not pointing to a valid [NETWORKSTATUS](networkstatus.md) structure.</span></span> <span data-ttu-id="cfa9e-117">配置此結構的記憶體，並再次呼叫 **IDelaydC：： QueryStatus** 方法。</span><span class="sxs-lookup"><span data-stu-id="cfa9e-117">Allocate memory for this structure and call the **IDelaydC::QueryStatus** method again.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="cfa9e-118">備註</span><span class="sxs-lookup"><span data-stu-id="cfa9e-118">Remarks</span></span>

<span data-ttu-id="cfa9e-119">呼叫 [CreateNPPInterface](createnppinterface.md) 之後，隨時都可以呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="cfa9e-119">This method can be called at any time after [CreateNPPInterface](createnppinterface.md) is called.</span></span> <span data-ttu-id="cfa9e-120">您可以呼叫它來查看 NPP 是否已連線到網路、找出目前的捕獲狀態，以及查看是否有任何觸發程式暫止。</span><span class="sxs-lookup"><span data-stu-id="cfa9e-120">It can be called to see if the NPP is connected to the network, to find out the status of the current capture, and to see if any triggers are pending.</span></span>

<span data-ttu-id="cfa9e-121">在呼叫這個方法之前，您必須先配置 [>networkstatus](networkstatus.md) 結構所需的記憶體，並在不再需要該結構時釋放該記憶體。</span><span class="sxs-lookup"><span data-stu-id="cfa9e-121">Before calling this method, you must allocate the memory needed for the [NETWORKSTATUS](networkstatus.md) structure and free that memory when the structure is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="cfa9e-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="cfa9e-122">Requirements</span></span>



| <span data-ttu-id="cfa9e-123">需求</span><span class="sxs-lookup"><span data-stu-id="cfa9e-123">Requirement</span></span> | <span data-ttu-id="cfa9e-124">值</span><span class="sxs-lookup"><span data-stu-id="cfa9e-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cfa9e-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cfa9e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="cfa9e-126">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cfa9e-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="cfa9e-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cfa9e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="cfa9e-128">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cfa9e-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="cfa9e-129">標頭</span><span class="sxs-lookup"><span data-stu-id="cfa9e-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="cfa9e-130"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="cfa9e-130"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="cfa9e-131">DLL</span><span class="sxs-lookup"><span data-stu-id="cfa9e-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cfa9e-132"><dt>Ndisnpp.dll;</dt><dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cfa9e-132"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfa9e-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cfa9e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfa9e-134">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="cfa9e-134">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="cfa9e-135">CreateNPPInterface</span><span class="sxs-lookup"><span data-stu-id="cfa9e-135">CreateNPPInterface</span></span>](createnppinterface.md)
</dt> <dt>

[<span data-ttu-id="cfa9e-136">>NETWORKSTATUS</span><span class="sxs-lookup"><span data-stu-id="cfa9e-136">NETWORKSTATUS</span></span>](networkstatus.md)
</dt> </dl>

 

 




