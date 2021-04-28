---
description: IDelaydC：： Start 方法-Start 方法會啟動 capture。
ms.assetid: 92b25afc-d5d8-47e4-a155-4ed2a3571038
title: 'IDelaydC：： Start 方法 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Start
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 25bf778d9cccce20c736c5f8b83e6af9754ac933
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118436"
---
# <a name="idelaydcstart-method"></a><span data-ttu-id="322f1-103">IDelaydC：： Start 方法</span><span class="sxs-lookup"><span data-stu-id="322f1-103">IDelaydC::Start method</span></span>

<span data-ttu-id="322f1-104">**Start** 方法會啟動 capture。</span><span class="sxs-lookup"><span data-stu-id="322f1-104">The **Start** method starts a capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="322f1-105">語法</span><span class="sxs-lookup"><span data-stu-id="322f1-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Start(
  [out] char *pFileName
);
```



## <a name="parameters"></a><span data-ttu-id="322f1-106">參數</span><span class="sxs-lookup"><span data-stu-id="322f1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="322f1-107">*pFileName* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="322f1-107">*pFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="322f1-108">用來儲存網路資料之 [*捕獲*](c.md) 檔案的名稱指標。</span><span class="sxs-lookup"><span data-stu-id="322f1-108">Pointer to the name of the [*capture file*](c.md) used to store the network data.</span></span> <span data-ttu-id="322f1-109">如果需要日後參考，請務必快取此檔案名。</span><span class="sxs-lookup"><span data-stu-id="322f1-109">Be sure to cache this file name if it is needed for future reference.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="322f1-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="322f1-110">Return value</span></span>

<span data-ttu-id="322f1-111">如果方法成功，則傳回值為 NMERR \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="322f1-111">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="322f1-112">如果此方法不成功，則傳回值是下列其中一個錯誤碼：</span><span class="sxs-lookup"><span data-stu-id="322f1-112">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="322f1-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="322f1-113">Return code</span></span>                                                                                           | <span data-ttu-id="322f1-114">Description</span><span class="sxs-lookup"><span data-stu-id="322f1-114">Description</span></span>                                                                                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="322f1-115"><dt>**NMERR \_ CAPTURE 已 \_ 暫停**</dt></span><span class="sxs-lookup"><span data-stu-id="322f1-115"><dt>**NMERR\_CAPTURE\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="322f1-116">捕捉處於暫停狀態，必須先停止，才能重新開機。</span><span class="sxs-lookup"><span data-stu-id="322f1-116">The capture is in a paused state and must be stopped before it can be restarted.</span></span> <span data-ttu-id="322f1-117">呼叫 [**IDelaydC：： stop**](idelaydc-stop.md) 以停止捕捉。</span><span class="sxs-lookup"><span data-stu-id="322f1-117">Call [**IDelaydC::Stop**](idelaydc-stop.md) to stop the capture.</span></span> <span data-ttu-id="322f1-118">如需詳細資訊，請參閱本主題中的「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="322f1-118">For more information, see the Remarks section in this topic.</span></span><br/> |
| <dl> <span data-ttu-id="322f1-119"><dt>**NMERR \_ 捕獲**</dt></span><span class="sxs-lookup"><span data-stu-id="322f1-119"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>       | <span data-ttu-id="322f1-120">已啟動 capture。</span><span class="sxs-lookup"><span data-stu-id="322f1-120">The capture is already started.</span></span><br/>                                                                                                                                                                                 |
| <dl> <span data-ttu-id="322f1-121"><dt>**NMERR \_ 未 \_ 連接**</dt></span><span class="sxs-lookup"><span data-stu-id="322f1-121"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>  | <span data-ttu-id="322f1-122">NPP 未連接到網路。</span><span class="sxs-lookup"><span data-stu-id="322f1-122">The NPP is not connected to the network.</span></span> <span data-ttu-id="322f1-123">呼叫 [**IDelaydC：： connect**](idelaydc-connect.md) 以連接到網路。</span><span class="sxs-lookup"><span data-stu-id="322f1-123">Call [**IDelaydC::Connect**](idelaydc-connect.md) to connect to the network.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="322f1-124"><dt>**NMERR \_ 未 \_ 延遲**</dt></span><span class="sxs-lookup"><span data-stu-id="322f1-124"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>    | <span data-ttu-id="322f1-125">NPP 已連接到網路，但不是使用 [**IDelaydC：： Connect**](idelaydc-connect.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="322f1-125">The NPP is connected to the network but not with the [**IDelaydC::Connect**](idelaydc-connect.md) method.</span></span><br/>                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="322f1-126">備註</span><span class="sxs-lookup"><span data-stu-id="322f1-126">Remarks</span></span>

<span data-ttu-id="322f1-127">您可以在 Windows 登錄中指定 [*capture*](c.md) 檔案的位置，但您可以使用網路監視器來變更檔案的位置。</span><span class="sxs-lookup"><span data-stu-id="322f1-127">The location of the [*capture file*](c.md) is specified in your Windows registry, but you can use Network Monitor to change the file's location.</span></span>

<span data-ttu-id="322f1-128">若要使用 **IDelaydC：： start** 和 [**IDelaydC：： Stop**](idelaydc-stop.md)重新開機 capture，您必須呼叫 [**IDelaydC：： Configure**](idelaydc-configure.md) 方法，以在每次呼叫 **IDelaydC：： start** 方法重新開機捕獲資料時重新設定連接。</span><span class="sxs-lookup"><span data-stu-id="322f1-128">To restart the capture by using **IDelaydC::Start** and [**IDelaydC::Stop**](idelaydc-stop.md), you must call the [**IDelaydC::Configure**](idelaydc-configure.md) method to reconfigure the connection each time you call the **IDelaydC::Start** method to restart capturing data.</span></span> <span data-ttu-id="322f1-129">當您使用這三種方法來啟動和停止捕捉時，每次啟動捕獲時都會建立新的捕獲檔案。</span><span class="sxs-lookup"><span data-stu-id="322f1-129">When you start and stop the capture with these three methods, a new capture file is created each time the capture is started.</span></span>

> [!Note]  
> <span data-ttu-id="322f1-130">您也可以使用 [**IDelaydC：:P ause**](idelaydc-pause.md) 和 [**IDelaydC：： Resume**](idelaydc-resume.md) 方法來啟動和停止捕捉。</span><span class="sxs-lookup"><span data-stu-id="322f1-130">You can also start and stop the capture by using the [**IDelaydC::Pause**](idelaydc-pause.md) and [**IDelaydC::Resume**](idelaydc-resume.md) methods.</span></span> <span data-ttu-id="322f1-131">當您使用這兩種方法時，所捕獲的資料會儲存在相同的捕獲檔案中。</span><span class="sxs-lookup"><span data-stu-id="322f1-131">When you use these two methods, the captured data is stored in the same capture file.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="322f1-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="322f1-132">Requirements</span></span>



| <span data-ttu-id="322f1-133">需求</span><span class="sxs-lookup"><span data-stu-id="322f1-133">Requirement</span></span> | <span data-ttu-id="322f1-134">值</span><span class="sxs-lookup"><span data-stu-id="322f1-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="322f1-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="322f1-135">Minimum supported client</span></span><br/> | <span data-ttu-id="322f1-136">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="322f1-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="322f1-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="322f1-137">Minimum supported server</span></span><br/> | <span data-ttu-id="322f1-138">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="322f1-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="322f1-139">標頭</span><span class="sxs-lookup"><span data-stu-id="322f1-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="322f1-140"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="322f1-140"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="322f1-141">DLL</span><span class="sxs-lookup"><span data-stu-id="322f1-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="322f1-142"><dt>Ndisnpp.dll;</dt><dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="322f1-142"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="322f1-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="322f1-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="322f1-144">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="322f1-144">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="322f1-145">**IDelaydC：： Configure**</span><span class="sxs-lookup"><span data-stu-id="322f1-145">**IDelaydC::Configure**</span></span>](idelaydc-configure.md)
</dt> <dt>

[<span data-ttu-id="322f1-146">**IDelaydC：： Connect**</span><span class="sxs-lookup"><span data-stu-id="322f1-146">**IDelaydC::Connect**</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="322f1-147">**IDelaydC：:P ause**</span><span class="sxs-lookup"><span data-stu-id="322f1-147">**IDelaydC::Pause**</span></span>](idelaydc-pause.md)
</dt> <dt>

[<span data-ttu-id="322f1-148">**IDelaydC：： Resume**</span><span class="sxs-lookup"><span data-stu-id="322f1-148">**IDelaydC::Resume**</span></span>](idelaydc-resume.md)
</dt> <dt>

[<span data-ttu-id="322f1-149">**IDelaydC：： Stop**</span><span class="sxs-lookup"><span data-stu-id="322f1-149">**IDelaydC::Stop**</span></span>](idelaydc-stop.md)
</dt> </dl>

 

 




