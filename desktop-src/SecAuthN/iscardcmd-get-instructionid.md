---
description: 從應用程式協定資料單位中抓取指令識別碼位元組 (APDU) 。
ms.assetid: 294f51cd-0a13-4dfb-bf02-9edd11a7085e
title: 'ISCardCmd：： get_InstructionId 方法 (Scarddat .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_InstructionId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 4b0125237ef94a5d6173f517483b9ae8781d5607
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945317"
---
# <a name="iscardcmdget_instructionid-method"></a><span data-ttu-id="981a9-103">ISCardCmd：： get \_ InstructionId 方法</span><span class="sxs-lookup"><span data-stu-id="981a9-103">ISCardCmd::get\_InstructionId method</span></span>

<span data-ttu-id="981a9-104">\[**Get \_ InstructionId** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="981a9-104">\[The **get\_InstructionId** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="981a9-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="981a9-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="981a9-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="981a9-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="981a9-107">**Get \_ InstructionId** 方法會從 [*應用程式協定資料單位*](../secgloss/a-gly.md)中抓取指令識別碼位元組 (APDU) 。</span><span class="sxs-lookup"><span data-stu-id="981a9-107">The **get\_InstructionId** method retrieves the instruction identifier byte from the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="981a9-108">語法</span><span class="sxs-lookup"><span data-stu-id="981a9-108">Syntax</span></span>


```C++
HRESULT get_InstructionId(
  [out] BYTE *pbyIns
);
```



## <a name="parameters"></a><span data-ttu-id="981a9-109">參數</span><span class="sxs-lookup"><span data-stu-id="981a9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="981a9-110">*pbyIns* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="981a9-110">*pbyIns* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="981a9-111">從傳回的 APDU 傳回的指令識別碼之位元組的指標。</span><span class="sxs-lookup"><span data-stu-id="981a9-111">Pointer to the byte that is the instruction ID from the APDU on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="981a9-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="981a9-112">Return value</span></span>

<span data-ttu-id="981a9-113">方法會傳回下列其中一個可能的值。</span><span class="sxs-lookup"><span data-stu-id="981a9-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="981a9-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="981a9-114">Return code</span></span>                                                                                   | <span data-ttu-id="981a9-115">Description</span><span class="sxs-lookup"><span data-stu-id="981a9-115">Description</span></span>                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="981a9-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="981a9-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="981a9-117">作業順利完成。</span><span class="sxs-lookup"><span data-stu-id="981a9-117">Operation completed successfully.</span></span><br/>     |
| <dl> <span data-ttu-id="981a9-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="981a9-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="981a9-119">*PbyIns* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="981a9-119">The *pbyIns* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="981a9-120"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="981a9-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="981a9-121">在 *pbyIns* 中傳遞了錯誤指標。</span><span class="sxs-lookup"><span data-stu-id="981a9-121">A bad pointer was passed in *pbyIns*.</span></span><br/> |
| <dl> <span data-ttu-id="981a9-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="981a9-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="981a9-123">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="981a9-123">Out of memory.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="981a9-124">備註</span><span class="sxs-lookup"><span data-stu-id="981a9-124">Remarks</span></span>

<span data-ttu-id="981a9-125">若要將教學識別碼設定為新的值，請呼叫 [**put \_ InstructionId**](iscardcmd-put-instructionid.md)。</span><span class="sxs-lookup"><span data-stu-id="981a9-125">To set the instructional identifier to a new value, call [**put\_InstructionId**](iscardcmd-put-instructionid.md).</span></span>

<span data-ttu-id="981a9-126">如需此介面所提供的所有方法清單，請參閱 [**ISCardCmd**](iscardcmd.md)。</span><span class="sxs-lookup"><span data-stu-id="981a9-126">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="981a9-127">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回 [*智慧卡*](../secgloss/s-gly.md) 的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="981a9-127">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="981a9-128">如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="981a9-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="981a9-129">範例</span><span class="sxs-lookup"><span data-stu-id="981a9-129">Examples</span></span>

<span data-ttu-id="981a9-130">下列範例示範如何從 [*應用程式協定資料單位*](../secgloss/a-gly.md) 中取出指令識別碼位元組 (APDU) 。</span><span class="sxs-lookup"><span data-stu-id="981a9-130">The following example shows how to retrieve the instruction identifier byte from the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="981a9-131">此範例假設 pISCardCmd 是 [**ISCardCmd**](iscardcmd.md) 介面實例的有效指標。</span><span class="sxs-lookup"><span data-stu-id="981a9-131">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
BYTE  byInstructID;
HRESULT hr;

// Retrieve the instruction ID.
hr = pISCardCmd->get_InstructionId(&byInstructID);
if (FAILED(hr))
{
  printf("Failed get_InstructionId\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="981a9-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="981a9-132">Requirements</span></span>



| <span data-ttu-id="981a9-133">需求</span><span class="sxs-lookup"><span data-stu-id="981a9-133">Requirement</span></span> | <span data-ttu-id="981a9-134">值</span><span class="sxs-lookup"><span data-stu-id="981a9-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="981a9-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="981a9-135">Minimum supported client</span></span><br/> | <span data-ttu-id="981a9-136">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="981a9-136">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="981a9-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="981a9-137">Minimum supported server</span></span><br/> | <span data-ttu-id="981a9-138">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="981a9-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="981a9-139">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="981a9-139">End of client support</span></span><br/>    | <span data-ttu-id="981a9-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="981a9-140">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="981a9-141">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="981a9-141">End of server support</span></span><br/>    | <span data-ttu-id="981a9-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="981a9-142">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="981a9-143">標頭</span><span class="sxs-lookup"><span data-stu-id="981a9-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="981a9-144"><dt>Scarddat。h</dt></span><span class="sxs-lookup"><span data-stu-id="981a9-144"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="981a9-145">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="981a9-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="981a9-146"><dt>Scarddat .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="981a9-146"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="981a9-147">DLL</span><span class="sxs-lookup"><span data-stu-id="981a9-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="981a9-148"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="981a9-148"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="981a9-149">IID</span><span class="sxs-lookup"><span data-stu-id="981a9-149">IID</span></span><br/>                      | <span data-ttu-id="981a9-150">IID \_ ISCardCmd 定義為 D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="981a9-150">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="981a9-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="981a9-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="981a9-152">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="981a9-152">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> <dt>

[<span data-ttu-id="981a9-153">**put \_ InstructionId**</span><span class="sxs-lookup"><span data-stu-id="981a9-153">**put\_InstructionId**</span></span>](iscardcmd-put-instructionid.md)
</dt> </dl>

 

 
