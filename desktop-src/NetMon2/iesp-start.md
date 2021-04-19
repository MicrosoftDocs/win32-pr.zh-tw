---
description: Start 方法會啟動 capture。
ms.assetid: 8bf8c0c7-20be-4404-8ea5-b28b4c658523
title: 'IESP：： Start 方法 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Start
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 2d9fc3a75fc82964f6fc5a5660ef77414ae065d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983574"
---
# <a name="iespstart-method"></a><span data-ttu-id="872d0-103">IESP：： Start 方法</span><span class="sxs-lookup"><span data-stu-id="872d0-103">IESP::Start method</span></span>

<span data-ttu-id="872d0-104">**Start** 方法會啟動 capture。</span><span class="sxs-lookup"><span data-stu-id="872d0-104">The **Start** method starts a capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="872d0-105">語法</span><span class="sxs-lookup"><span data-stu-id="872d0-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Start(
  [out] char *pFileName
);
```



## <a name="parameters"></a><span data-ttu-id="872d0-106">參數</span><span class="sxs-lookup"><span data-stu-id="872d0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="872d0-107">*pFileName* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="872d0-107">*pFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="872d0-108">用來儲存網路資料之 [*捕獲*](c.md) 檔案的名稱指標。</span><span class="sxs-lookup"><span data-stu-id="872d0-108">Pointer to the name of the [*capture file*](c.md) used to store the network data.</span></span> <span data-ttu-id="872d0-109">如果需要日後參考，請務必快取此檔案名。</span><span class="sxs-lookup"><span data-stu-id="872d0-109">Be sure to cache this file name if it is needed for future reference.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="872d0-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="872d0-110">Return value</span></span>

<span data-ttu-id="872d0-111">如果方法成功，則傳回值為 NMERR \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="872d0-111">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="872d0-112">如果此方法不成功，則傳回值是下列其中一個錯誤碼：</span><span class="sxs-lookup"><span data-stu-id="872d0-112">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="872d0-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="872d0-113">Return code</span></span>                                                                                           | <span data-ttu-id="872d0-114">Description</span><span class="sxs-lookup"><span data-stu-id="872d0-114">Description</span></span>                                                                                                                            |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="872d0-115"><dt>**NMERR \_ CAPTURE 已 \_ 暫停**</dt></span><span class="sxs-lookup"><span data-stu-id="872d0-115"><dt>**NMERR\_CAPTURE\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="872d0-116">此捕獲已暫停，必須先停止，才能重新開機。</span><span class="sxs-lookup"><span data-stu-id="872d0-116">The capture is paused and must be stopped before it can be restarted.</span></span> <span data-ttu-id="872d0-117">呼叫 [IESP：： stop](iesp-stop.md) 以停止捕捉。</span><span class="sxs-lookup"><span data-stu-id="872d0-117">Call [IESP::Stop](iesp-stop.md) to stop the capture.</span></span><br/> |
| <dl> <span data-ttu-id="872d0-118"><dt>**NMERR \_ 捕獲**</dt></span><span class="sxs-lookup"><span data-stu-id="872d0-118"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>       | <span data-ttu-id="872d0-119">已啟動 capture。</span><span class="sxs-lookup"><span data-stu-id="872d0-119">The capture is already started.</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="872d0-120"><dt>**NMERR \_ 未 \_ 連接**</dt></span><span class="sxs-lookup"><span data-stu-id="872d0-120"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>  | <span data-ttu-id="872d0-121">NPP 未連接到網路。</span><span class="sxs-lookup"><span data-stu-id="872d0-121">The NPP is not connected to the network.</span></span> <span data-ttu-id="872d0-122">呼叫 [IESP：： connect](iesp-connect.md) 以將 NPP 連接到網路。</span><span class="sxs-lookup"><span data-stu-id="872d0-122">Call [IESP::Connect](iesp-connect.md) to connect the NPP to the network.</span></span><br/>          |
| <dl> <span data-ttu-id="872d0-123"><dt>**NMERR \_ 非 \_ ESP**</dt></span><span class="sxs-lookup"><span data-stu-id="872d0-123"><dt>**NMERR\_NOT\_ESP**</dt></span></span> </dl>        | <span data-ttu-id="872d0-124">NPP 已連接到網路，但不是使用 [IESP：： Connect](iesp-connect.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="872d0-124">The NPP is connected to the network but not with the [IESP::Connect](iesp-connect.md) method.</span></span><br/>                              |



 

## <a name="remarks"></a><span data-ttu-id="872d0-125">備註</span><span class="sxs-lookup"><span data-stu-id="872d0-125">Remarks</span></span>

<span data-ttu-id="872d0-126">在 Windows 登錄中指定了 [*capture*](c.md) 檔案的位置，但您可以使用網路監視器來變更目錄位置。</span><span class="sxs-lookup"><span data-stu-id="872d0-126">The location of the [*capture file*](c.md) is specified in the Windows registry, but you can use Network Monitor to change the directory location.</span></span>

<span data-ttu-id="872d0-127">當您使用 IESP：： Start 和 [IESP：： Stop](iesp-stop.md) 方法重新開機捕捉時，您必須呼叫 [IESP：： Configure](iesp-configure.md) 方法，以在每次呼叫 IESP：： start 重新開機捕獲資料時重新設定連接。</span><span class="sxs-lookup"><span data-stu-id="872d0-127">When you restart the capture by using the IESP::Start and [IESP::Stop](iesp-stop.md) methods, you must call the [IESP::Configure](iesp-configure.md) method to reconfigure the connection each time you call IESP::Start to restart capturing data.</span></span> <span data-ttu-id="872d0-128">當您使用這三種方法來啟動和停止捕捉時，每次啟動捕獲時都會建立新的捕獲檔案。</span><span class="sxs-lookup"><span data-stu-id="872d0-128">When you start and stop the capture with these three methods, a new capture file is created each time the capture is started.</span></span>

> [!Note]  
> <span data-ttu-id="872d0-129">您也可以使用 [IESP：:P ause](iesp-pause.md) 和 [IESP：： Resume](iesp-resume.md) 方法來啟動和停止捕捉。</span><span class="sxs-lookup"><span data-stu-id="872d0-129">You can also start and stop the capture by using the [IESP::Pause](iesp-pause.md) and [IESP::Resume](iesp-resume.md) methods.</span></span> <span data-ttu-id="872d0-130">使用這兩種方法時，所捕獲的資料會儲存在相同的捕獲檔案中。</span><span class="sxs-lookup"><span data-stu-id="872d0-130">When these two methods are used, the captured data is stored in the same capture file.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="872d0-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="872d0-131">Requirements</span></span>



| <span data-ttu-id="872d0-132">需求</span><span class="sxs-lookup"><span data-stu-id="872d0-132">Requirement</span></span> | <span data-ttu-id="872d0-133">值</span><span class="sxs-lookup"><span data-stu-id="872d0-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="872d0-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="872d0-134">Minimum supported client</span></span><br/> | <span data-ttu-id="872d0-135">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="872d0-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="872d0-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="872d0-136">Minimum supported server</span></span><br/> | <span data-ttu-id="872d0-137">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="872d0-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="872d0-138">標頭</span><span class="sxs-lookup"><span data-stu-id="872d0-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="872d0-139"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="872d0-139"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="872d0-140">DLL</span><span class="sxs-lookup"><span data-stu-id="872d0-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="872d0-141"><dt>Ndisnpp.dll;</dt><dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="872d0-141"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="872d0-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="872d0-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="872d0-143">IESP</span><span class="sxs-lookup"><span data-stu-id="872d0-143">IESP</span></span>](iesp.md)
</dt> <dt>

[<span data-ttu-id="872d0-144">IESP：： Configure</span><span class="sxs-lookup"><span data-stu-id="872d0-144">IESP::Configure</span></span>](iesp-configure.md)
</dt> <dt>

[<span data-ttu-id="872d0-145">IESP：： Connect</span><span class="sxs-lookup"><span data-stu-id="872d0-145">IESP::Connect</span></span>](iesp-connect.md)
</dt> <dt>

[<span data-ttu-id="872d0-146">IESP：:P ause</span><span class="sxs-lookup"><span data-stu-id="872d0-146">IESP::Pause</span></span>](iesp-pause.md)
</dt> <dt>

[<span data-ttu-id="872d0-147">IESP：： Resume</span><span class="sxs-lookup"><span data-stu-id="872d0-147">IESP::Resume</span></span>](iesp-resume.md)
</dt> <dt>

[<span data-ttu-id="872d0-148">IESP：： Stop</span><span class="sxs-lookup"><span data-stu-id="872d0-148">IESP::Stop</span></span>](iesp-stop.md)
</dt> </dl>

 

 




