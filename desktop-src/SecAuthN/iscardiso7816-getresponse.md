---
description: GetResponse 方法會建立應用程式協定資料單位 (APDU) 命令，此命令會將 APDU 命令傳輸 (或部分的 APDU 命令) 否則無法由可用的通訊協定傳輸。
ms.assetid: 1aa83d38-d46d-4d3b-8f57-0256e5875e35
title: 'ISCardISO7816：： GetResponse 方法 (Scardssp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.GetResponse
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 0b74fe9620aefc390957b88f9cf286f7871c1d18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985002"
---
# <a name="iscardiso7816getresponse-method"></a><span data-ttu-id="00eab-103">ISCardISO7816：： GetResponse 方法</span><span class="sxs-lookup"><span data-stu-id="00eab-103">ISCardISO7816::GetResponse method</span></span>

<span data-ttu-id="00eab-104">\[**GetResponse** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="00eab-104">\[The **GetResponse** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="00eab-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="00eab-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="00eab-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="00eab-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="00eab-107">**GetResponse** 方法會建立 [*應用程式協定資料單位*](../secgloss/a-gly.md) (APDU) 命令，此命令會將 apdu 命令傳輸 (或部分的 apdu 命令) 否則無法由可用的通訊協定傳輸。</span><span class="sxs-lookup"><span data-stu-id="00eab-107">The **GetResponse** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that transmits APDU commands (or part of an APDU command) which otherwise could not be transmitted by the available protocols.</span></span>

## <a name="syntax"></a><span data-ttu-id="00eab-108">語法</span><span class="sxs-lookup"><span data-stu-id="00eab-108">Syntax</span></span>


```C++
HRESULT GetResponse(
  [in]      BYTE       byP1,
  [in]      BYTE       byP2,
  [in]      LONG       lDataLength,
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="00eab-109">參數</span><span class="sxs-lookup"><span data-stu-id="00eab-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00eab-110">*byP1* \[在\]</span><span class="sxs-lookup"><span data-stu-id="00eab-110">*byP1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00eab-111">根據 ISO 7816-4，P1 應該是零 (RFU) 。</span><span class="sxs-lookup"><span data-stu-id="00eab-111">Per the ISO 7816-4, P1 should be zero (RFU).</span></span>

</dd> <dt>

<span data-ttu-id="00eab-112">*byP2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="00eab-112">*byP2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00eab-113">根據 ISO 7816-4，P2 應該是零 (RFU) 。</span><span class="sxs-lookup"><span data-stu-id="00eab-113">Per the ISO 7816-4, P2 should be zero (RFU).</span></span>

</dd> <dt>

<span data-ttu-id="00eab-114">*lDataLength* \[在\]</span><span class="sxs-lookup"><span data-stu-id="00eab-114">*lDataLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00eab-115">傳送的資料長度。</span><span class="sxs-lookup"><span data-stu-id="00eab-115">Length of data transmitted.</span></span>

</dd> <dt>

<span data-ttu-id="00eab-116">*ppCmd* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="00eab-116">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="00eab-117">在輸入時， [**ISCardCmd**](iscardcmd.md) 介面物件的指標或 **Null**。</span><span class="sxs-lookup"><span data-stu-id="00eab-117">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="00eab-118">傳回時，它會填入由這項作業所建立的 APDU 命令。</span><span class="sxs-lookup"><span data-stu-id="00eab-118">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="00eab-119">如果 *ppCmd* 設定為 **Null**，就會在內部建立 [*智慧卡*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) 物件，並透過 *ppCmd* 指標傳回。</span><span class="sxs-lookup"><span data-stu-id="00eab-119">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned via the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00eab-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="00eab-120">Return value</span></span>

<span data-ttu-id="00eab-121">方法會傳回下列其中一個可能的值。</span><span class="sxs-lookup"><span data-stu-id="00eab-121">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="00eab-122">傳回碼</span><span class="sxs-lookup"><span data-stu-id="00eab-122">Return code</span></span>                                                                                   | <span data-ttu-id="00eab-123">Description</span><span class="sxs-lookup"><span data-stu-id="00eab-123">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="00eab-124"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="00eab-124"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="00eab-125">作業順利完成。</span><span class="sxs-lookup"><span data-stu-id="00eab-125">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="00eab-126"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="00eab-126"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="00eab-127">無效的參數。</span><span class="sxs-lookup"><span data-stu-id="00eab-127">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="00eab-128"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="00eab-128"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="00eab-129">傳入了錯誤指標。</span><span class="sxs-lookup"><span data-stu-id="00eab-129">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="00eab-130"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="00eab-130"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="00eab-131">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="00eab-131">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="00eab-132">備註</span><span class="sxs-lookup"><span data-stu-id="00eab-132">Remarks</span></span>

<span data-ttu-id="00eab-133">如需此介面所提供的所有方法清單，請參閱 [**ISCardISO7816**](iscardiso7816.md)。</span><span class="sxs-lookup"><span data-stu-id="00eab-133">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="00eab-134">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回智慧卡的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="00eab-134">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="00eab-135">如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="00eab-135">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="00eab-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="00eab-136">Requirements</span></span>



| <span data-ttu-id="00eab-137">需求</span><span class="sxs-lookup"><span data-stu-id="00eab-137">Requirement</span></span> | <span data-ttu-id="00eab-138">值</span><span class="sxs-lookup"><span data-stu-id="00eab-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="00eab-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="00eab-139">Minimum supported client</span></span><br/> | <span data-ttu-id="00eab-140">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="00eab-140">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="00eab-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="00eab-141">Minimum supported server</span></span><br/> | <span data-ttu-id="00eab-142">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="00eab-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="00eab-143">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="00eab-143">End of client support</span></span><br/>    | <span data-ttu-id="00eab-144">Windows XP</span><span class="sxs-lookup"><span data-stu-id="00eab-144">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="00eab-145">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="00eab-145">End of server support</span></span><br/>    | <span data-ttu-id="00eab-146">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="00eab-146">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="00eab-147">標頭</span><span class="sxs-lookup"><span data-stu-id="00eab-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="00eab-148"><dt>Scardssp。h</dt></span><span class="sxs-lookup"><span data-stu-id="00eab-148"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="00eab-149">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="00eab-149">Type library</span></span><br/>             | <dl> <span data-ttu-id="00eab-150"><dt>Scardsrv .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="00eab-150"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="00eab-151">DLL</span><span class="sxs-lookup"><span data-stu-id="00eab-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="00eab-152"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="00eab-152"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="00eab-153">IID</span><span class="sxs-lookup"><span data-stu-id="00eab-153">IID</span></span><br/>                      | <span data-ttu-id="00eab-154">IID \_ ISCardISO7816 定義為53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="00eab-154">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="00eab-155">另請參閱</span><span class="sxs-lookup"><span data-stu-id="00eab-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00eab-156">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="00eab-156">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> </dl>

 

 
