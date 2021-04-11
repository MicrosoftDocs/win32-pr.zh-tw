---
description: 中斷連線方法會中斷 NPP 與網路的連線。
ms.assetid: 476bbce4-2e3c-448f-b85e-6adac424fb0d
title: 'IDelaydC： (Netmon 的:D isconnect 方法) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Disconnect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: d192aa80f543706eea4bc197bc3dc8d57dd64aee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112220"
---
# <a name="idelaydcdisconnect-method"></a><span data-ttu-id="06663-103">IDelaydC：:D isconnect 方法</span><span class="sxs-lookup"><span data-stu-id="06663-103">IDelaydC::Disconnect method</span></span>

<span data-ttu-id="06663-104">**中斷** 連線方法會中斷 NPP 與網路的連線。</span><span class="sxs-lookup"><span data-stu-id="06663-104">The **Disconnect** method disconnects the NPP from the network.</span></span>

## <a name="syntax"></a><span data-ttu-id="06663-105">語法</span><span class="sxs-lookup"><span data-stu-id="06663-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Disconnect();
```



## <a name="parameters"></a><span data-ttu-id="06663-106">參數</span><span class="sxs-lookup"><span data-stu-id="06663-106">Parameters</span></span>

<span data-ttu-id="06663-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="06663-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="06663-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="06663-108">Return value</span></span>

<span data-ttu-id="06663-109">如果方法成功，則傳回值為 NMERR \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="06663-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="06663-110">如果此方法不成功，則傳回值是下列其中一個錯誤碼：</span><span class="sxs-lookup"><span data-stu-id="06663-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="06663-111">傳回碼</span><span class="sxs-lookup"><span data-stu-id="06663-111">Return code</span></span>                                                                                          | <span data-ttu-id="06663-112">Description</span><span class="sxs-lookup"><span data-stu-id="06663-112">Description</span></span>                                                                                                       |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="06663-113"><dt>**NMERR \_ 捕獲**</dt></span><span class="sxs-lookup"><span data-stu-id="06663-113"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>      | <span data-ttu-id="06663-114">NPP 正在捕獲資料。</span><span class="sxs-lookup"><span data-stu-id="06663-114">The NPP is capturing data.</span></span> <span data-ttu-id="06663-115">在捕捉期間，您無法中斷 NPP 與網路的連線。</span><span class="sxs-lookup"><span data-stu-id="06663-115">You cannot disconnect the NPP from the network during a capture.</span></span><br/>            |
| <dl> <span data-ttu-id="06663-116"><dt>**NMERR \_ 未 \_ 連接**</dt></span><span class="sxs-lookup"><span data-stu-id="06663-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="06663-117">NPP 未連接到網路。</span><span class="sxs-lookup"><span data-stu-id="06663-117">The NPP is not connected to the network.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="06663-118"><dt>**NMERR \_ 未 \_ 延遲**</dt></span><span class="sxs-lookup"><span data-stu-id="06663-118"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>   | <span data-ttu-id="06663-119">NPP 已連接到網路，但不是使用 [IDelaydC：： Connect](idelaydc-connect.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="06663-119">The NPP is connected to the network but not with the [IDelaydC::Connect](idelaydc-connect.md) method.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="06663-120">備註</span><span class="sxs-lookup"><span data-stu-id="06663-120">Remarks</span></span>

<span data-ttu-id="06663-121">當 NPP 正在捕捉資料時，無法呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="06663-121">This method cannot be called when the NPP is capturing data.</span></span> <span data-ttu-id="06663-122">呼叫 **中斷連接** 之前，您必須先呼叫 **IDelaydC：： Stop** 方法。</span><span class="sxs-lookup"><span data-stu-id="06663-122">You must call the **IDelaydC::Stop** method before calling **Disconnect**.</span></span>

## <a name="requirements"></a><span data-ttu-id="06663-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="06663-123">Requirements</span></span>



| <span data-ttu-id="06663-124">需求</span><span class="sxs-lookup"><span data-stu-id="06663-124">Requirement</span></span> | <span data-ttu-id="06663-125">值</span><span class="sxs-lookup"><span data-stu-id="06663-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06663-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="06663-126">Minimum supported client</span></span><br/> | <span data-ttu-id="06663-127">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="06663-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="06663-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="06663-128">Minimum supported server</span></span><br/> | <span data-ttu-id="06663-129">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="06663-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="06663-130">標頭</span><span class="sxs-lookup"><span data-stu-id="06663-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="06663-131"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="06663-131"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="06663-132">DLL</span><span class="sxs-lookup"><span data-stu-id="06663-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="06663-133"><dt>Ndisnpp.dll;</dt><dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="06663-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06663-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="06663-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06663-135">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="06663-135">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="06663-136">IDelaydC：： Connect</span><span class="sxs-lookup"><span data-stu-id="06663-136">IDelaydC::Connect</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="06663-137">IDelaydC：： Stop</span><span class="sxs-lookup"><span data-stu-id="06663-137">IDelaydC::Stop</span></span>](idelaydc-stop.md)
</dt> </dl>

 

 




