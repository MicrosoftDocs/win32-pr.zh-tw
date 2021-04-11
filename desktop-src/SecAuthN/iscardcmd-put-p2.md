---
description: 在應用程式協定資料單位中設定第二個參數 (P2) 位元組 (APDU) 。
ms.assetid: 8d11b967-33cd-4bfa-b294-cc0c422cf6cf
title: 'ISCardCmd：:p ut_P2 方法 (Scarddat .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_P2
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 362da530dece37a0a0ca600b1edb414d29e1bd48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191151"
---
# <a name="iscardcmdput_p2-method"></a><span data-ttu-id="d5dcc-103">ISCardCmd：:p ui \_ P2 方法</span><span class="sxs-lookup"><span data-stu-id="d5dcc-103">ISCardCmd::put\_P2 method</span></span>

<span data-ttu-id="d5dcc-104">\[**Put \_ P2** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="d5dcc-104">\[The **put\_P2** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d5dcc-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="d5dcc-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="d5dcc-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="d5dcc-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="d5dcc-107">**Put \_ P2** 方法會將 [*應用程式協定資料單位*](../secgloss/a-gly.md)中的第二個參數 (P2) byte， (APDU) 。</span><span class="sxs-lookup"><span data-stu-id="d5dcc-107">The **put\_P2** method sets the second parameter (P2) byte in the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="d5dcc-108">語法</span><span class="sxs-lookup"><span data-stu-id="d5dcc-108">Syntax</span></span>


```C++
HRESULT put_P2(
  [in] BYTE byP2
);
```



## <a name="parameters"></a><span data-ttu-id="d5dcc-109">參數</span><span class="sxs-lookup"><span data-stu-id="d5dcc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5dcc-110">*byP2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d5dcc-110">*byP2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5dcc-111">P2 欄位的位元組。</span><span class="sxs-lookup"><span data-stu-id="d5dcc-111">The byte that is the P2 field.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5dcc-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="d5dcc-112">Return value</span></span>

<span data-ttu-id="d5dcc-113">方法會傳回下列其中一個可能的值。</span><span class="sxs-lookup"><span data-stu-id="d5dcc-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="d5dcc-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="d5dcc-114">Return code</span></span>                                                                                   | <span data-ttu-id="d5dcc-115">Description</span><span class="sxs-lookup"><span data-stu-id="d5dcc-115">Description</span></span>                                   |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="d5dcc-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="d5dcc-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="d5dcc-117">作業順利完成。</span><span class="sxs-lookup"><span data-stu-id="d5dcc-117">Operation completed successfully.</span></span><br/>  |
| <dl> <span data-ttu-id="d5dcc-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="d5dcc-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="d5dcc-119">*ByP2* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="d5dcc-119">The *byP2* parameter is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="d5dcc-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="d5dcc-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="d5dcc-121">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="d5dcc-121">Out of memory.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="d5dcc-122">備註</span><span class="sxs-lookup"><span data-stu-id="d5dcc-122">Remarks</span></span>

<span data-ttu-id="d5dcc-123">若要設定 APDU 的 P1 值，請呼叫 [**put \_ P1**](iscardcmd-put-p1.md)。</span><span class="sxs-lookup"><span data-stu-id="d5dcc-123">To set the P1 value of the APDU, call [**put\_P1**](iscardcmd-put-p1.md).</span></span>

<span data-ttu-id="d5dcc-124">若要取出現有的 P1、P2 和 P3 值，請分別呼叫 [**get \_ p1**](iscardcmd-get-p1.md)、 [**取得 \_ P2**](iscardcmd-get-p2.md) 或 [**取得 \_ p3**](iscardcmd-get-p3.md) 。</span><span class="sxs-lookup"><span data-stu-id="d5dcc-124">To retrieve the existing P1, P2, and P3 values, call [**get\_P1**](iscardcmd-get-p1.md), [**get\_P2**](iscardcmd-get-p2.md) or [**get\_P3**](iscardcmd-get-p3.md) respectively.</span></span>

<span data-ttu-id="d5dcc-125">如需此介面所提供的所有方法清單，請參閱 [**ISCardCmd**](iscardcmd.md)。</span><span class="sxs-lookup"><span data-stu-id="d5dcc-125">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="d5dcc-126">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回 [*智慧卡*](../secgloss/s-gly.md) 的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="d5dcc-126">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="d5dcc-127">如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="d5dcc-127">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="d5dcc-128">範例</span><span class="sxs-lookup"><span data-stu-id="d5dcc-128">Examples</span></span>

<span data-ttu-id="d5dcc-129">下列範例示範如何設定 [*應用程式協定資料單位*](../secgloss/a-gly.md) (P2) 位元組的第二個參數， (APDU) 。</span><span class="sxs-lookup"><span data-stu-id="d5dcc-129">The following example shows how to set the second parameter (P2) byte of the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="d5dcc-130">此範例假設 pISCardCmd 是 [**ISCardCmd**](iscardcmd.md) 介面實例的有效指標。</span><span class="sxs-lookup"><span data-stu-id="d5dcc-130">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
HRESULT  hr;

// Set the P2 byte.
hr = pISCardCmd->put_P2(0x06);
if (FAILED(hr))
{
  printf("Failed put_P2\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="d5dcc-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="d5dcc-131">Requirements</span></span>



| <span data-ttu-id="d5dcc-132">需求</span><span class="sxs-lookup"><span data-stu-id="d5dcc-132">Requirement</span></span> | <span data-ttu-id="d5dcc-133">值</span><span class="sxs-lookup"><span data-stu-id="d5dcc-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d5dcc-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d5dcc-134">Minimum supported client</span></span><br/> | <span data-ttu-id="d5dcc-135">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d5dcc-135">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="d5dcc-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d5dcc-136">Minimum supported server</span></span><br/> | <span data-ttu-id="d5dcc-137">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d5dcc-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d5dcc-138">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="d5dcc-138">End of client support</span></span><br/>    | <span data-ttu-id="d5dcc-139">Windows XP</span><span class="sxs-lookup"><span data-stu-id="d5dcc-139">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="d5dcc-140">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="d5dcc-140">End of server support</span></span><br/>    | <span data-ttu-id="d5dcc-141">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d5dcc-141">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="d5dcc-142">標頭</span><span class="sxs-lookup"><span data-stu-id="d5dcc-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5dcc-143"><dt>Scarddat。h</dt></span><span class="sxs-lookup"><span data-stu-id="d5dcc-143"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="d5dcc-144">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="d5dcc-144">Type library</span></span><br/>             | <dl> <span data-ttu-id="d5dcc-145"><dt>Scarddat .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d5dcc-145"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d5dcc-146">DLL</span><span class="sxs-lookup"><span data-stu-id="d5dcc-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d5dcc-147"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d5dcc-147"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="d5dcc-148">IID</span><span class="sxs-lookup"><span data-stu-id="d5dcc-148">IID</span></span><br/>                      | <span data-ttu-id="d5dcc-149">IID \_ ISCardCmd 定義為 D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="d5dcc-149">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="d5dcc-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d5dcc-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5dcc-151">**取得 \_ P1**</span><span class="sxs-lookup"><span data-stu-id="d5dcc-151">**get\_P1**</span></span>](iscardcmd-get-p1.md)
</dt> <dt>

[<span data-ttu-id="d5dcc-152">**取得 \_ P2**</span><span class="sxs-lookup"><span data-stu-id="d5dcc-152">**get\_P2**</span></span>](iscardcmd-get-p2.md)
</dt> <dt>

[<span data-ttu-id="d5dcc-153">**取得 \_ P3**</span><span class="sxs-lookup"><span data-stu-id="d5dcc-153">**get\_P3**</span></span>](iscardcmd-get-p3.md)
</dt> <dt>

[<span data-ttu-id="d5dcc-154">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="d5dcc-154">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> <dt>

[<span data-ttu-id="d5dcc-155">**put \_ P1**</span><span class="sxs-lookup"><span data-stu-id="d5dcc-155">**put\_P1**</span></span>](iscardcmd-put-p1.md)
</dt> </dl>

 

 
