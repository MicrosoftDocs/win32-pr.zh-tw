---
description: 捕獲 NPP 狀態。
ms.assetid: 48682997-f641-4ae5-b5ad-64fd84f07ae3
title: 'IESP：： QueryStatus 方法 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.QueryStatus
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 3435ed832484042bfeb9229e4b46fa34441cb395
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192217"
---
# <a name="iespquerystatus-method"></a><span data-ttu-id="f1e7d-103">IESP：： QueryStatus 方法</span><span class="sxs-lookup"><span data-stu-id="f1e7d-103">IESP::QueryStatus method</span></span>

<span data-ttu-id="f1e7d-104">**QueryStatus** 方法會捕獲 NPP 狀態。</span><span class="sxs-lookup"><span data-stu-id="f1e7d-104">The **QueryStatus** method retrieves the NPP status.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1e7d-105">語法</span><span class="sxs-lookup"><span data-stu-id="f1e7d-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE QueryStatus(
  [out] NETWORKSTATUS *pNetworkStatus
);
```



## <a name="parameters"></a><span data-ttu-id="f1e7d-106">參數</span><span class="sxs-lookup"><span data-stu-id="f1e7d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1e7d-107">*pNetworkStatus* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f1e7d-107">*pNetworkStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f1e7d-108">傳回之 >networkstatus 結構的指標，指出目前狀態 (在 NPP 的) 上進行的[](networkstatus.md) 、暫停、停止等等。</span><span class="sxs-lookup"><span data-stu-id="f1e7d-108">A pointer to a returned [NETWORKSTATUS](networkstatus.md) structure that indicates the current state (capturing, paused, stopped, and so on) of the NPP.</span></span> <span data-ttu-id="f1e7d-109">使用者必須配置和釋放 >NETWORKSTATUS 結構的記憶體。</span><span class="sxs-lookup"><span data-stu-id="f1e7d-109">The user must allocate and free the memory for the NETWORKSTATUS structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1e7d-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="f1e7d-110">Return value</span></span>

<span data-ttu-id="f1e7d-111">如果方法成功，則傳回值為 NMERR \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="f1e7d-111">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="f1e7d-112">如果此方法不成功，則傳回值會是下列錯誤碼：</span><span class="sxs-lookup"><span data-stu-id="f1e7d-112">If the method is unsuccessful, the return value is the following error code:</span></span>



| <span data-ttu-id="f1e7d-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="f1e7d-113">Return code</span></span>                                                                                              | <span data-ttu-id="f1e7d-114">Description</span><span class="sxs-lookup"><span data-stu-id="f1e7d-114">Description</span></span>                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f1e7d-115"><dt>**NMERR \_ 不正確 \_ 參數**</dt></span><span class="sxs-lookup"><span data-stu-id="f1e7d-115"><dt>**NMERR\_INVALID\_PARAMETER**</dt></span></span> </dl> | <span data-ttu-id="f1e7d-116">*PNetworkStatus* 參數未指向有效的 [>networkstatus](networkstatus.md)結構。</span><span class="sxs-lookup"><span data-stu-id="f1e7d-116">The *pNetworkStatus* parameter is not pointing to a valid [NETWORKSTATUS](networkstatus.md) structure.</span></span> <span data-ttu-id="f1e7d-117">配置此結構的記憶體，並再次呼叫 **IESP：： QueryStatus** 。</span><span class="sxs-lookup"><span data-stu-id="f1e7d-117">Allocate memory for this structure and call **IESP::QueryStatus** again.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f1e7d-118">備註</span><span class="sxs-lookup"><span data-stu-id="f1e7d-118">Remarks</span></span>

<span data-ttu-id="f1e7d-119">呼叫 [CreateNPPInterface](createnppinterface.md) 之後，隨時都可以呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="f1e7d-119">This method can be called at any time after the [CreateNPPInterface](createnppinterface.md) is called.</span></span> <span data-ttu-id="f1e7d-120">您可以呼叫這個方法來查看 NPP 是否已連接到網路、找出目前的捕獲狀態，以及查看是否有任何觸發程式暫止。</span><span class="sxs-lookup"><span data-stu-id="f1e7d-120">You can call this method to see if the NPP is connected to the network, to find out the status of the current capture, and to see if any triggers are pending.</span></span>

<span data-ttu-id="f1e7d-121">在呼叫這個方法之前，請先配置 [>networkstatus](networkstatus.md) 結構所需的記憶體，並在不再需要該結構時釋放該記憶體。</span><span class="sxs-lookup"><span data-stu-id="f1e7d-121">Before calling this method, allocate the memory required for the [NETWORKSTATUS](networkstatus.md) structure and free that memory when the structure is no longer required.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1e7d-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="f1e7d-122">Requirements</span></span>



| <span data-ttu-id="f1e7d-123">需求</span><span class="sxs-lookup"><span data-stu-id="f1e7d-123">Requirement</span></span> | <span data-ttu-id="f1e7d-124">值</span><span class="sxs-lookup"><span data-stu-id="f1e7d-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1e7d-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f1e7d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f1e7d-126">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f1e7d-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="f1e7d-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f1e7d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f1e7d-128">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f1e7d-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="f1e7d-129">標頭</span><span class="sxs-lookup"><span data-stu-id="f1e7d-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1e7d-130"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="f1e7d-130"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="f1e7d-131">DLL</span><span class="sxs-lookup"><span data-stu-id="f1e7d-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f1e7d-132"><dt>Ndisnpp.dll;</dt><dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f1e7d-132"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1e7d-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f1e7d-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1e7d-134">IESP</span><span class="sxs-lookup"><span data-stu-id="f1e7d-134">IESP</span></span>](iesp.md)
</dt> <dt>

[<span data-ttu-id="f1e7d-135">CreateNPPInterface</span><span class="sxs-lookup"><span data-stu-id="f1e7d-135">CreateNPPInterface</span></span>](createnppinterface.md)
</dt> <dt>

[<span data-ttu-id="f1e7d-136">>NETWORKSTATUS</span><span class="sxs-lookup"><span data-stu-id="f1e7d-136">NETWORKSTATUS</span></span>](networkstatus.md)
</dt> </dl>

 

 




