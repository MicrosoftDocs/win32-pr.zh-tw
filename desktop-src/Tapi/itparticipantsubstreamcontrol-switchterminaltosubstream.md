---
description: SwitchTerminalToSubStream 方法會將終端機設定為參與者子流。
ms.assetid: 39e1d4b9-2e39-4b36-9a6a-89e41cd59153
title: 'ITParticipantSubStreamControl：： SwitchTerminalToSubStream 方法 (Confpriv .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00f10401b2cf1598c76537ebd3a7049d67bf0657
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999541"
---
# <a name="itparticipantsubstreamcontrolswitchterminaltosubstream-method"></a><span data-ttu-id="2cb73-103">ITParticipantSubStreamControl：： SwitchTerminalToSubStream 方法</span><span class="sxs-lookup"><span data-stu-id="2cb73-103">ITParticipantSubStreamControl::SwitchTerminalToSubStream method</span></span>

<span data-ttu-id="2cb73-104">\[**SwitchTerminalToSubStream** 無法在 windows Vista、windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="2cb73-104">\[**SwitchTerminalToSubStream** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="2cb73-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="2cb73-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="2cb73-106">**SwitchTerminalToSubStream** 方法會將終端機設定為參與者子流。</span><span class="sxs-lookup"><span data-stu-id="2cb73-106">The **SwitchTerminalToSubStream** method sets a terminal to the participant substream.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cb73-107">語法</span><span class="sxs-lookup"><span data-stu-id="2cb73-107">Syntax</span></span>


```C++
HRESULT SwitchTerminalToSubStream(
  [in] ITTerminal  *pITTerminal,
  [in] ITSubStream *pITSubStream
);
```



## <a name="parameters"></a><span data-ttu-id="2cb73-108">參數</span><span class="sxs-lookup"><span data-stu-id="2cb73-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2cb73-109">*pITTerminal* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2cb73-109">*pITTerminal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2cb73-110">[**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="2cb73-110">Pointer to [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) interface.</span></span>

</dd> <dt>

<span data-ttu-id="2cb73-111">*pITSubStream* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2cb73-111">*pITSubStream* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2cb73-112">[**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="2cb73-112">Pointer to [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2cb73-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="2cb73-113">Return value</span></span>

<span data-ttu-id="2cb73-114">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="2cb73-114">This method can return one of these values.</span></span>



| <span data-ttu-id="2cb73-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="2cb73-115">Return code</span></span>                                                                                     | <span data-ttu-id="2cb73-116">Description</span><span class="sxs-lookup"><span data-stu-id="2cb73-116">Description</span></span>                                                                                        |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2cb73-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="2cb73-117"><dt>**S\_OK**</dt></span></span> </dl>            | <span data-ttu-id="2cb73-118">方法成功。</span><span class="sxs-lookup"><span data-stu-id="2cb73-118">Method succeeded.</span></span><br/>                                                                       |
| <dl> <span data-ttu-id="2cb73-119"><dt>**E 未 \_ 預期**</dt></span><span class="sxs-lookup"><span data-stu-id="2cb73-119"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>    | <span data-ttu-id="2cb73-120">無法存取資料流程的參與者資訊。</span><span class="sxs-lookup"><span data-stu-id="2cb73-120">Participant information for the stream could not be accessed.</span></span><br/>                           |
| <dl> <span data-ttu-id="2cb73-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="2cb73-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>    | <span data-ttu-id="2cb73-122">*PParticipant* 或 *pITSubStream* 參數未指向有效的介面。</span><span class="sxs-lookup"><span data-stu-id="2cb73-122">The *pParticipant* or the *pITSubStream* parameter does not point to a valid interface.</span></span><br/> |
| <dl> <span data-ttu-id="2cb73-123"><dt>**TAPI \_ E \_ NOITEMS**</dt></span><span class="sxs-lookup"><span data-stu-id="2cb73-123"><dt>**TAPI\_E\_NOITEMS**</dt></span></span> </dl> | <span data-ttu-id="2cb73-124">子流未就緒。</span><span class="sxs-lookup"><span data-stu-id="2cb73-124">The substream is not ready.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="2cb73-125"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="2cb73-125"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>   | <span data-ttu-id="2cb73-126">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="2cb73-126">Insufficient memory exists to perform the operation.</span></span><br/>                                    |



 

## <a name="requirements"></a><span data-ttu-id="2cb73-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="2cb73-127">Requirements</span></span>



| <span data-ttu-id="2cb73-128">需求</span><span class="sxs-lookup"><span data-stu-id="2cb73-128">Requirement</span></span> | <span data-ttu-id="2cb73-129">值</span><span class="sxs-lookup"><span data-stu-id="2cb73-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2cb73-130">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="2cb73-130">TAPI version</span></span><br/> | <span data-ttu-id="2cb73-131">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="2cb73-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="2cb73-132">標頭</span><span class="sxs-lookup"><span data-stu-id="2cb73-132">Header</span></span><br/>       | <dl> <span data-ttu-id="2cb73-133"><dt>Confpriv。h</dt></span><span class="sxs-lookup"><span data-stu-id="2cb73-133"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="2cb73-134">程式庫</span><span class="sxs-lookup"><span data-stu-id="2cb73-134">Library</span></span><br/>      | <dl> <span data-ttu-id="2cb73-135"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="2cb73-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="2cb73-136">DLL</span><span class="sxs-lookup"><span data-stu-id="2cb73-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="2cb73-137"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2cb73-137"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="2cb73-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2cb73-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cb73-139">**ITParticipantSubStreamControl**</span><span class="sxs-lookup"><span data-stu-id="2cb73-139">**ITParticipantSubStreamControl**</span></span>](itparticipantsubstreamcontrol.md)
</dt> <dt>

[<span data-ttu-id="2cb73-140">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="2cb73-140">**ITParticipant**</span></span>](itparticipant.md)
</dt> <dt>

[<span data-ttu-id="2cb73-141">**ITSubStream**</span><span class="sxs-lookup"><span data-stu-id="2cb73-141">**ITSubStream**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)
</dt> <dt>

[<span data-ttu-id="2cb73-142">**ITTerminal**</span><span class="sxs-lookup"><span data-stu-id="2cb73-142">**ITTerminal**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itterminal)
</dt> </dl>

 

