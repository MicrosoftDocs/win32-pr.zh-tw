---
description: Stop 方法會停止目前的捕捉。
ms.assetid: 1b627137-e72d-4425-98d9-e296fb07e509
title: 'IDelaydC：： Stop 方法 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Stop
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 42c9cc1c4b6da7b5f934dd96f26aa9348c43ac0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468740"
---
# <a name="idelaydcstop-method"></a><span data-ttu-id="a7627-103">IDelaydC：： Stop 方法</span><span class="sxs-lookup"><span data-stu-id="a7627-103">IDelaydC::Stop method</span></span>

<span data-ttu-id="a7627-104">**Stop** 方法會停止目前的捕捉。</span><span class="sxs-lookup"><span data-stu-id="a7627-104">The **Stop** method stops the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7627-105">語法</span><span class="sxs-lookup"><span data-stu-id="a7627-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Stop(
  [out] LPSTATISTICS lpStats
);
```



## <a name="parameters"></a><span data-ttu-id="a7627-106">參數</span><span class="sxs-lookup"><span data-stu-id="a7627-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7627-107">*lpStats* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a7627-107">*lpStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a7627-108">[統計資料](statistics.md)結構的指標，其中包含網路統計資料，例如總畫面格總數和已捕獲的位元組總數。</span><span class="sxs-lookup"><span data-stu-id="a7627-108">Pointer to a [STATISTICS](statistics.md) structure that contains network statistics such as total frames and total bytes captured.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7627-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="a7627-109">Return value</span></span>

<span data-ttu-id="a7627-110">如果方法成功，則傳回值為 NMERR \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="a7627-110">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="a7627-111">如果此方法不成功，則傳回值是下列其中一個錯誤碼：</span><span class="sxs-lookup"><span data-stu-id="a7627-111">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="a7627-112">傳回碼</span><span class="sxs-lookup"><span data-stu-id="a7627-112">Return code</span></span>                                                                                          | <span data-ttu-id="a7627-113">Description</span><span class="sxs-lookup"><span data-stu-id="a7627-113">Description</span></span>                                                                                                                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a7627-114"><dt>**NMERR \_ 未 \_ 連接**</dt></span><span class="sxs-lookup"><span data-stu-id="a7627-114"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="a7627-115">NPP 未連接到網路。</span><span class="sxs-lookup"><span data-stu-id="a7627-115">The NPP is not connected to the network.</span></span> <span data-ttu-id="a7627-116">呼叫 [IDelaydC：： connect](idelaydc-connect.md) 以將 NPP 連接到網路。</span><span class="sxs-lookup"><span data-stu-id="a7627-116">Call [IDelaydC::Connect](idelaydc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="a7627-117"><dt>**NMERR \_ 未 \_ 捕獲**</dt></span><span class="sxs-lookup"><span data-stu-id="a7627-117"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl> | <span data-ttu-id="a7627-118">NPP 不會捕捉資料。</span><span class="sxs-lookup"><span data-stu-id="a7627-118">The NPP is not capturing data.</span></span> <span data-ttu-id="a7627-119">呼叫 [IDelaydC：： start](idelaydc-start.md) 以開始捕獲。</span><span class="sxs-lookup"><span data-stu-id="a7627-119">Call [IDelaydC::Start](idelaydc-start.md) to start the capture.</span></span><br/>                            |
| <dl> <span data-ttu-id="a7627-120"><dt>**NMERR \_ 未 \_ 延遲**</dt></span><span class="sxs-lookup"><span data-stu-id="a7627-120"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>   | <span data-ttu-id="a7627-121">NPP 已連接到網路，但不是使用 [IDelaydC：： Connect](idelaydc-connect.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="a7627-121">The NPP is connected to the network but not with the [IDelaydC::Connect](idelaydc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="a7627-122">備註</span><span class="sxs-lookup"><span data-stu-id="a7627-122">Remarks</span></span>

<span data-ttu-id="a7627-123">當呼叫 **IDelaydC：： Stop** 時，網路監視器會停止捕獲資料並關閉 [*capture*](c.md)檔案。</span><span class="sxs-lookup"><span data-stu-id="a7627-123">When **IDelaydC::Stop** is called, Network Monitor stops capturing data and closes the [*capture file*](c.md).</span></span> <span data-ttu-id="a7627-124"> (在呼叫 [IDelaydC：： Start](idelaydc-start.md) 時傳回的 capture 檔名稱) 。</span><span class="sxs-lookup"><span data-stu-id="a7627-124">(The name of the capture file was returned when [IDelaydC::Start](idelaydc-start.md) was called).</span></span> <span data-ttu-id="a7627-125">您現在可以查看 capture 檔案的內容。</span><span class="sxs-lookup"><span data-stu-id="a7627-125">You can now look at the contents of the capture file.</span></span>

<span data-ttu-id="a7627-126">當您停止並開始進行捕捉時，請務必在每次呼叫[IDelaydC：： start](idelaydc-start.md)以重新開機捕獲時呼叫[IDelaydC：： Configure](idelaydc-configure.md)方法。</span><span class="sxs-lookup"><span data-stu-id="a7627-126">When you stop and start the capture, make sure you call the [IDelaydC::Configure](idelaydc-configure.md) method each time you call [IDelaydC::Start](idelaydc-start.md) to restart the capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7627-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="a7627-127">Requirements</span></span>



| <span data-ttu-id="a7627-128">需求</span><span class="sxs-lookup"><span data-stu-id="a7627-128">Requirement</span></span> | <span data-ttu-id="a7627-129">值</span><span class="sxs-lookup"><span data-stu-id="a7627-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7627-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a7627-130">Minimum supported client</span></span><br/> | <span data-ttu-id="a7627-131">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a7627-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="a7627-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a7627-132">Minimum supported server</span></span><br/> | <span data-ttu-id="a7627-133">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a7627-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="a7627-134">標頭</span><span class="sxs-lookup"><span data-stu-id="a7627-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7627-135"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="a7627-135"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="a7627-136">DLL</span><span class="sxs-lookup"><span data-stu-id="a7627-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a7627-137"><dt>Ndisnpp.dll;</dt><dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a7627-137"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7627-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a7627-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7627-139">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="a7627-139">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="a7627-140">IDelaydC：： Connect</span><span class="sxs-lookup"><span data-stu-id="a7627-140">IDelaydC::Connect</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="a7627-141">IDelaydC：： Configure</span><span class="sxs-lookup"><span data-stu-id="a7627-141">IDelaydC::Configure</span></span>](idelaydc-configure.md)
</dt> <dt>

[<span data-ttu-id="a7627-142">IDelaydC：： Start</span><span class="sxs-lookup"><span data-stu-id="a7627-142">IDelaydC::Start</span></span>](idelaydc-start.md)
</dt> <dt>

[<span data-ttu-id="a7627-143">統計</span><span class="sxs-lookup"><span data-stu-id="a7627-143">STATISTICS</span></span>](statistics.md)
</dt> </dl>

 

 




