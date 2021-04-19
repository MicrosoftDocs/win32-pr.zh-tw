---
description: Get FormatCodes 方法會取得媒體裝載格式的程式 \_ 代碼清單。 Variant 會傳回 Bstr 的 SAFEARRAY。 該陣列中的每個 BSTR 都是格式的程式碼字串。
ms.assetid: 8663d7e8-d46f-44d1-93db-9b5142bb28dd
title: 'ITMedia：： get_FormatCodes 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce9e28a0323ac001c948a3b19b8dae2cfe9daf5d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985580"
---
# <a name="itmediaget_formatcodes-method"></a><span data-ttu-id="c1a19-105">ITMedia：： get \_ FormatCodes 方法</span><span class="sxs-lookup"><span data-stu-id="c1a19-105">ITMedia::get\_FormatCodes method</span></span>

<span data-ttu-id="c1a19-106">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="c1a19-106">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="c1a19-107">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="c1a19-107">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="c1a19-108">**Get \_ FormatCodes** 方法會取得媒體裝載格式的程式代碼清單。</span><span class="sxs-lookup"><span data-stu-id="c1a19-108">The **get\_FormatCodes** method gets the list of media payload format codes.</span></span> <span data-ttu-id="c1a19-109">Variant 會傳回 **BSTR** 的 SAFEARRAY。</span><span class="sxs-lookup"><span data-stu-id="c1a19-109">The variant returns a SAFEARRAY of **BSTR** s.</span></span> <span data-ttu-id="c1a19-110">該陣列中的每個 **BSTR** 都是格式的程式碼字串。</span><span class="sxs-lookup"><span data-stu-id="c1a19-110">Each **BSTR** within that array is a format code string.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1a19-111">語法</span><span class="sxs-lookup"><span data-stu-id="c1a19-111">Syntax</span></span>


```C++
HRESULT get_FormatCodes(
  [out] VARIANT *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="c1a19-112">參數</span><span class="sxs-lookup"><span data-stu-id="c1a19-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1a19-113">*pVal* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c1a19-113">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c1a19-114">媒體承載格式代碼的陣列。</span><span class="sxs-lookup"><span data-stu-id="c1a19-114">Array of media payload format codes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1a19-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="c1a19-115">Return value</span></span>

<span data-ttu-id="c1a19-116">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="c1a19-116">This method can return one of these values.</span></span>



| <span data-ttu-id="c1a19-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="c1a19-117">Return code</span></span>                                                                                   | <span data-ttu-id="c1a19-118">Description</span><span class="sxs-lookup"><span data-stu-id="c1a19-118">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="c1a19-119"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="c1a19-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="c1a19-120">方法成功。</span><span class="sxs-lookup"><span data-stu-id="c1a19-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="c1a19-121"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="c1a19-121"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="c1a19-122">*PVal* 參數不是有效的指標。</span><span class="sxs-lookup"><span data-stu-id="c1a19-122">The *pVal* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="c1a19-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="c1a19-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="c1a19-124">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="c1a19-124">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="c1a19-125"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="c1a19-125"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="c1a19-126">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="c1a19-126">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="c1a19-127"><dt>**E \_ >NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="c1a19-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="c1a19-128">尚未實作這個方法。</span><span class="sxs-lookup"><span data-stu-id="c1a19-128">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="c1a19-129">備註</span><span class="sxs-lookup"><span data-stu-id="c1a19-129">Remarks</span></span>

<span data-ttu-id="c1a19-130">當提供承載格式的清單時，這表示這些格式可能會在會話中使用，但這些格式的第一種是會話的預設格式。</span><span class="sxs-lookup"><span data-stu-id="c1a19-130">When a list of payload formats is given, this implies that all of these formats may be used in the session, but the first of these formats is the default format for the session.</span></span> <span data-ttu-id="c1a19-131">當傳輸通訊協定為 RTP 時，格式代碼為 RTP 承載類型。</span><span class="sxs-lookup"><span data-stu-id="c1a19-131">When the transport protocol is RTP, the format codes are RTP payload types.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1a19-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="c1a19-132">Requirements</span></span>



| <span data-ttu-id="c1a19-133">需求</span><span class="sxs-lookup"><span data-stu-id="c1a19-133">Requirement</span></span> | <span data-ttu-id="c1a19-134">值</span><span class="sxs-lookup"><span data-stu-id="c1a19-134">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c1a19-135">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="c1a19-135">TAPI version</span></span><br/> | <span data-ttu-id="c1a19-136">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="c1a19-136">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="c1a19-137">標頭</span><span class="sxs-lookup"><span data-stu-id="c1a19-137">Header</span></span><br/>       | <dl> <span data-ttu-id="c1a19-138"><dt>Sdpblb。h</dt></span><span class="sxs-lookup"><span data-stu-id="c1a19-138"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="c1a19-139">程式庫</span><span class="sxs-lookup"><span data-stu-id="c1a19-139">Library</span></span><br/>      | <dl> <span data-ttu-id="c1a19-140"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="c1a19-140"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="c1a19-141">DLL</span><span class="sxs-lookup"><span data-stu-id="c1a19-141">DLL</span></span><br/>          | <dl> <span data-ttu-id="c1a19-142"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c1a19-142"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1a19-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c1a19-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1a19-144">**ITMedia**</span><span class="sxs-lookup"><span data-stu-id="c1a19-144">**ITMedia**</span></span>](itmedia.md)
</dt> <dt>

[<span data-ttu-id="c1a19-145">**ITMedia：:p 的 \_ FormatCodes**</span><span class="sxs-lookup"><span data-stu-id="c1a19-145">**ITMedia::put\_FormatCodes**</span></span>](itmedia-put-formatcodes.md)
</dt> </dl>

 

 




