---
title: 'ISoftKbd AdviseSoftKeyboardEventSink 方法 (Softkbdc .h) '
description: ISoftKbd AdviseSoftKeyboardEventSink 方法會安裝一個軟鍵盤事件接收器，以處理來自軟鍵盤的 OnKeySelection 通知。
ms.assetid: f7a441dc-7bef-4fc0-bc62-c153a55a844c
keywords:
- AdviseSoftKeyboardEventSink 方法文字服務架構
- AdviseSoftKeyboardEventSink 方法文字服務架構，ISoftKbd 介面
- ISoftKbd 介面文字服務架構，AdviseSoftKeyboardEventSink 方法
topic_type:
- apiref
api_name:
- ISoftKbd.AdviseSoftKeyboardEventSink
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ab17de2104c6104b044f027152cfc45cca968b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385049"
---
# <a name="isoftkbdadvisesoftkeyboardeventsink-method"></a><span data-ttu-id="6e35b-106">ISoftKbd：： AdviseSoftKeyboardEventSink 方法</span><span class="sxs-lookup"><span data-stu-id="6e35b-106">ISoftKbd::AdviseSoftKeyboardEventSink method</span></span>

<span data-ttu-id="6e35b-107">**ISoftKbd：： AdviseSoftKeyboardEventSink** 方法會安裝軟鍵盤事件接收器，以處理來自螢幕小鍵盤的 OnKeySelection 通知。</span><span class="sxs-lookup"><span data-stu-id="6e35b-107">The **ISoftKbd::AdviseSoftKeyboardEventSink** method installs a soft keyboard event sink to handle OnKeySelection notifications from the soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e35b-108">語法</span><span class="sxs-lookup"><span data-stu-id="6e35b-108">Syntax</span></span>


```C++
HRESULT AdviseSoftKeyboardEventSink(
  [in]  DWORD    dwKeyboardId,
  [in]  REFIID   riid,
  [in]  IUnknown *punk,
  [out] DWORD    *pdwCookie
);
```



## <a name="parameters"></a><span data-ttu-id="6e35b-109">參數</span><span class="sxs-lookup"><span data-stu-id="6e35b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e35b-110">*dwKeyboardId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6e35b-110">*dwKeyboardId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e35b-111">軟鍵盤的識別碼。</span><span class="sxs-lookup"><span data-stu-id="6e35b-111">Identifier of the soft keyboard.</span></span>

</dd> <dt>

<span data-ttu-id="6e35b-112">*riid* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6e35b-112">*riid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e35b-113">接收介面的介面識別碼。</span><span class="sxs-lookup"><span data-stu-id="6e35b-113">Interface identifier for the sink interface.</span></span>

</dd> <dt>

<span data-ttu-id="6e35b-114">*punk* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6e35b-114">*punk* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e35b-115">由 *riid* 指定之接收器介面的 [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)指標。</span><span class="sxs-lookup"><span data-stu-id="6e35b-115">Pointer to [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) for the sink interface specified by *riid*.</span></span> <span data-ttu-id="6e35b-116">這個參數不能設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="6e35b-116">This parameter cannot be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="6e35b-117">*pdwCookie* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6e35b-117">*pdwCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6e35b-118">緩衝區的指標，此方法會在其中抓取用來連接至用戶端的軟鍵盤「cookie」。</span><span class="sxs-lookup"><span data-stu-id="6e35b-118">Pointer to the buffer in which this method retrieves the soft keyboard "cookie" used for connection to the client.</span></span> <span data-ttu-id="6e35b-119">每個連接的 cookie 都必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="6e35b-119">The cookie must be unique for each connection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e35b-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="6e35b-120">Return value</span></span>

<span data-ttu-id="6e35b-121">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="6e35b-121">This method can return one of these values.</span></span>



| <span data-ttu-id="6e35b-122">值</span><span class="sxs-lookup"><span data-stu-id="6e35b-122">Value</span></span>                                                                                        | <span data-ttu-id="6e35b-123">描述</span><span class="sxs-lookup"><span data-stu-id="6e35b-123">Description</span></span>                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="6e35b-124"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="6e35b-124"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="6e35b-125">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="6e35b-125">The method was successful.</span></span><br/>          |
| <dl> <span data-ttu-id="6e35b-126"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="6e35b-126"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="6e35b-127">一或多個參數無效。</span><span class="sxs-lookup"><span data-stu-id="6e35b-127">One or more parameters are invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="6e35b-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="6e35b-128">Requirements</span></span>



| <span data-ttu-id="6e35b-129">需求</span><span class="sxs-lookup"><span data-stu-id="6e35b-129">Requirement</span></span> | <span data-ttu-id="6e35b-130">值</span><span class="sxs-lookup"><span data-stu-id="6e35b-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6e35b-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6e35b-131">Minimum supported client</span></span><br/> | <span data-ttu-id="6e35b-132">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6e35b-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="6e35b-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6e35b-133">Minimum supported server</span></span><br/> | <span data-ttu-id="6e35b-134">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6e35b-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="6e35b-135">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="6e35b-135">Redistributable</span></span><br/>          | <span data-ttu-id="6e35b-136">Windows 2000 Professional 上的 TSF 1。0</span><span class="sxs-lookup"><span data-stu-id="6e35b-136">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="6e35b-137">標頭</span><span class="sxs-lookup"><span data-stu-id="6e35b-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e35b-138"><dt>Softkbdc。h</dt></span><span class="sxs-lookup"><span data-stu-id="6e35b-138"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="6e35b-139">Idl</span><span class="sxs-lookup"><span data-stu-id="6e35b-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6e35b-140"><dt>Softkbd .idl</dt></span><span class="sxs-lookup"><span data-stu-id="6e35b-140"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="6e35b-141">DLL</span><span class="sxs-lookup"><span data-stu-id="6e35b-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e35b-142"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e35b-142"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e35b-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6e35b-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e35b-144">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="6e35b-144">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="6e35b-145">**ISoftKbd::UnadviseSoftKeyboardEventSink**</span><span class="sxs-lookup"><span data-stu-id="6e35b-145">**ISoftKbd::UnadviseSoftKeyboardEventSink**</span></span>](isoftkbd-unadvisesoftkeyboardeventsink.md)
</dt> </dl>

 

