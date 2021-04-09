---
title: 'ISoftKbd UnadviseSoftKeyboardEventSink 方法 (Softkbdc .h) '
description: ISoftKbd UnadviseSoftKeyboardEventSink 方法會移除軟鍵盤事件接收器。
ms.assetid: 785340bd-c4f6-4c80-a492-6e60d1c1d552
keywords:
- UnadviseSoftKeyboardEventSink 方法文字服務架構
- UnadviseSoftKeyboardEventSink 方法文字服務架構，ISoftKbd 介面
- ISoftKbd 介面文字服務架構，UnadviseSoftKeyboardEventSink 方法
topic_type:
- apiref
api_name:
- ISoftKbd.UnadviseSoftKeyboardEventSink
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a77129d1b5df024964af4ab19318963708d4b3d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686229"
---
# <a name="isoftkbdunadvisesoftkeyboardeventsink-method"></a><span data-ttu-id="dc759-106">ISoftKbd：： UnadviseSoftKeyboardEventSink 方法</span><span class="sxs-lookup"><span data-stu-id="dc759-106">ISoftKbd::UnadviseSoftKeyboardEventSink method</span></span>

<span data-ttu-id="dc759-107">**ISoftKbd：： UnadviseSoftKeyboardEventSink** 方法會移除軟鍵盤事件接收器。</span><span class="sxs-lookup"><span data-stu-id="dc759-107">The **ISoftKbd::UnadviseSoftKeyboardEventSink** method removes a soft keyboard event sink.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc759-108">語法</span><span class="sxs-lookup"><span data-stu-id="dc759-108">Syntax</span></span>


```C++
HRESULT UnadviseSoftKeyboardEventSink(
  [in] TfClientId tid
);
```



## <a name="parameters"></a><span data-ttu-id="dc759-109">參數</span><span class="sxs-lookup"><span data-stu-id="dc759-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc759-110">*tid* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dc759-110">*tid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc759-111">擁有軟鍵盤事件接收器的用戶端識別碼。</span><span class="sxs-lookup"><span data-stu-id="dc759-111">Identifier of the client that owns the soft keyboard event sink.</span></span> <span data-ttu-id="dc759-112">此值是在使用 [ISoftKbd：： AdviseSoftKeyboardEventSink](isoftkbd-advisesoftkeyboardeventsink.md)安裝事件接收器時傳遞。</span><span class="sxs-lookup"><span data-stu-id="dc759-112">This value was passed when the event sink was installed using [ISoftKbd::AdviseSoftKeyboardEventSink](isoftkbd-advisesoftkeyboardeventsink.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc759-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="dc759-113">Return value</span></span>

<span data-ttu-id="dc759-114">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="dc759-114">This method can return one of these values.</span></span>



| <span data-ttu-id="dc759-115">值</span><span class="sxs-lookup"><span data-stu-id="dc759-115">Value</span></span>                                                                                                   | <span data-ttu-id="dc759-116">描述</span><span class="sxs-lookup"><span data-stu-id="dc759-116">Description</span></span>                                                   |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <span data-ttu-id="dc759-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="dc759-117"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="dc759-118">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="dc759-118">The method was successful.</span></span><br/>                         |
| <dl> <span data-ttu-id="dc759-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="dc759-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>            | <span data-ttu-id="dc759-120">*Tid* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="dc759-120">The *tid* parameter is invalid.</span></span><br/>                    |
| <dl> <span data-ttu-id="dc759-121"><dt>**CONNECT \_ E \_ NOCONNECTION**</dt></span><span class="sxs-lookup"><span data-stu-id="dc759-121"><dt>**CONNECT\_E\_NOCONNECTION**</dt></span></span> </dl> | <span data-ttu-id="dc759-122">找不到 *tid* 所識別的建議接收器。</span><span class="sxs-lookup"><span data-stu-id="dc759-122">The advise sink identified by *tid* was not found.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="dc759-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="dc759-123">Requirements</span></span>



| <span data-ttu-id="dc759-124">需求</span><span class="sxs-lookup"><span data-stu-id="dc759-124">Requirement</span></span> | <span data-ttu-id="dc759-125">值</span><span class="sxs-lookup"><span data-stu-id="dc759-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dc759-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dc759-126">Minimum supported client</span></span><br/> | <span data-ttu-id="dc759-127">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dc759-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="dc759-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dc759-128">Minimum supported server</span></span><br/> | <span data-ttu-id="dc759-129">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dc759-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="dc759-130">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="dc759-130">Redistributable</span></span><br/>          | <span data-ttu-id="dc759-131">Windows 2000 Professional 上的 TSF 1。0</span><span class="sxs-lookup"><span data-stu-id="dc759-131">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="dc759-132">標頭</span><span class="sxs-lookup"><span data-stu-id="dc759-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc759-133"><dt>Softkbdc。h</dt></span><span class="sxs-lookup"><span data-stu-id="dc759-133"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="dc759-134">Idl</span><span class="sxs-lookup"><span data-stu-id="dc759-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="dc759-135"><dt>Softkbd .idl</dt></span><span class="sxs-lookup"><span data-stu-id="dc759-135"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="dc759-136">DLL</span><span class="sxs-lookup"><span data-stu-id="dc759-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dc759-137"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dc759-137"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc759-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dc759-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc759-139">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="dc759-139">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="dc759-140">ISoftKbd::AdviseSoftKeyboardEventSink</span><span class="sxs-lookup"><span data-stu-id="dc759-140">ISoftKbd::AdviseSoftKeyboardEventSink</span></span>](isoftkbd-advisesoftkeyboardeventsink.md)
</dt> </dl>

 

 





