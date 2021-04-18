---
description: 從應用程式協定資料單位中，抓取第一個參數 (P1) 位元組 (APDU) 。
ms.assetid: a6648e70-96d8-4b7d-ae6d-8832e38d1c71
title: 'ISCardCmd：： get_P1 方法 (Scarddat .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_P1
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 047732fd8602828cc0501d623c57653bfdc9044f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511564"
---
# <a name="iscardcmdget_p1-method"></a><span data-ttu-id="b2593-103">ISCardCmd：： get \_ P1 方法</span><span class="sxs-lookup"><span data-stu-id="b2593-103">ISCardCmd::get\_P1 method</span></span>

<span data-ttu-id="b2593-104">\[**Get \_ P1** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="b2593-104">\[The **get\_P1** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b2593-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="b2593-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="b2593-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="b2593-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="b2593-107">**Get \_ P1** 方法會從 [*應用程式協定資料單位*](../secgloss/a-gly.md)（ (APDU) ）抓取第一個參數 (P1) 位元組。</span><span class="sxs-lookup"><span data-stu-id="b2593-107">The **get\_P1** method retrieves the first parameter (P1) byte from the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="b2593-108">語法</span><span class="sxs-lookup"><span data-stu-id="b2593-108">Syntax</span></span>


```C++
HRESULT get_P1(
  [out] BYTE *pbyP1
);
```



## <a name="parameters"></a><span data-ttu-id="b2593-109">參數</span><span class="sxs-lookup"><span data-stu-id="b2593-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2593-110">*pbyP1* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b2593-110">*pbyP1* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b2593-111">傳回之 APDU 中的 P1 位元組指標。</span><span class="sxs-lookup"><span data-stu-id="b2593-111">Pointer to the P1 byte in the APDU on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2593-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="b2593-112">Return value</span></span>

<span data-ttu-id="b2593-113">方法會傳回下列其中一個可能的值。</span><span class="sxs-lookup"><span data-stu-id="b2593-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="b2593-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="b2593-114">Return code</span></span>                                                                                   | <span data-ttu-id="b2593-115">Description</span><span class="sxs-lookup"><span data-stu-id="b2593-115">Description</span></span>                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="b2593-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="b2593-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="b2593-117">作業順利完成。</span><span class="sxs-lookup"><span data-stu-id="b2593-117">Operation completed successfully.</span></span><br/>    |
| <dl> <span data-ttu-id="b2593-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="b2593-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="b2593-119">*PbyP1* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="b2593-119">The *pbyP1* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="b2593-120"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="b2593-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="b2593-121">在 *pbyP1* 中傳遞了錯誤指標。</span><span class="sxs-lookup"><span data-stu-id="b2593-121">A bad pointer was passed in *pbyP1*.</span></span><br/> |
| <dl> <span data-ttu-id="b2593-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="b2593-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="b2593-123">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="b2593-123">Out of memory.</span></span><br/>                       |



 

## <a name="remarks"></a><span data-ttu-id="b2593-124">備註</span><span class="sxs-lookup"><span data-stu-id="b2593-124">Remarks</span></span>

<span data-ttu-id="b2593-125">若要將 P1 參數設定為新的值，請呼叫 [**put \_ P1**](iscardcmd-put-p1.md)。</span><span class="sxs-lookup"><span data-stu-id="b2593-125">To set the P1 parameter to a new value, call [**put\_P1**](iscardcmd-put-p1.md).</span></span>

<span data-ttu-id="b2593-126">若要取得 P2 或 P3 參數，請呼叫 [**get \_ P2**](iscardcmd-get-p2.md) 並分別 [**取得 \_ p3**](iscardcmd-get-p3.md) 。</span><span class="sxs-lookup"><span data-stu-id="b2593-126">To get the P2 or P3 parameters, call [**get\_P2**](iscardcmd-get-p2.md) and [**get\_P3**](iscardcmd-get-p3.md) respectively.</span></span>

<span data-ttu-id="b2593-127">如需此介面所提供的所有方法清單，請參閱 [**ISCardCmd**](iscardcmd.md)。</span><span class="sxs-lookup"><span data-stu-id="b2593-127">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="b2593-128">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回 [*智慧卡*](../secgloss/s-gly.md) 的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b2593-128">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="b2593-129">如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="b2593-129">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="b2593-130">範例</span><span class="sxs-lookup"><span data-stu-id="b2593-130">Examples</span></span>

<span data-ttu-id="b2593-131">下列範例示範如何從 [*應用程式協定資料單位*](../secgloss/a-gly.md) 取出第一個參數 (P1) 位元組 (APDU) 。</span><span class="sxs-lookup"><span data-stu-id="b2593-131">The following example shows how to retrieve the first parameter (P1) byte from the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="b2593-132">此範例假設 pISCardCmd 是 [**ISCardCmd**](iscardcmd.md) 介面實例的有效指標。</span><span class="sxs-lookup"><span data-stu-id="b2593-132">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
BYTE  byP1;
HRESULT  hr;

// Retrieve the P1 byte.
hr = pISCardCmd->get_P1(&byP1);
if (FAILED(hr))
{
  printf("Failed get_P1\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="b2593-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="b2593-133">Requirements</span></span>



| <span data-ttu-id="b2593-134">需求</span><span class="sxs-lookup"><span data-stu-id="b2593-134">Requirement</span></span> | <span data-ttu-id="b2593-135">值</span><span class="sxs-lookup"><span data-stu-id="b2593-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b2593-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b2593-136">Minimum supported client</span></span><br/> | <span data-ttu-id="b2593-137">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b2593-137">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="b2593-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b2593-138">Minimum supported server</span></span><br/> | <span data-ttu-id="b2593-139">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b2593-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b2593-140">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="b2593-140">End of client support</span></span><br/>    | <span data-ttu-id="b2593-141">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b2593-141">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="b2593-142">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="b2593-142">End of server support</span></span><br/>    | <span data-ttu-id="b2593-143">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b2593-143">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="b2593-144">標頭</span><span class="sxs-lookup"><span data-stu-id="b2593-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2593-145"><dt>Scarddat。h</dt></span><span class="sxs-lookup"><span data-stu-id="b2593-145"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="b2593-146">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="b2593-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="b2593-147"><dt>Scarddat .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b2593-147"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b2593-148">DLL</span><span class="sxs-lookup"><span data-stu-id="b2593-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b2593-149"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b2593-149"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="b2593-150">IID</span><span class="sxs-lookup"><span data-stu-id="b2593-150">IID</span></span><br/>                      | <span data-ttu-id="b2593-151">IID \_ ISCardCmd 定義為 D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="b2593-151">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="b2593-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b2593-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2593-153">**取得 \_ P2**</span><span class="sxs-lookup"><span data-stu-id="b2593-153">**get\_P2**</span></span>](iscardcmd-get-p2.md)
</dt> <dt>

[<span data-ttu-id="b2593-154">**取得 \_ P3**</span><span class="sxs-lookup"><span data-stu-id="b2593-154">**get\_P3**</span></span>](iscardcmd-get-p3.md)
</dt> <dt>

[<span data-ttu-id="b2593-155">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="b2593-155">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> <dt>

[<span data-ttu-id="b2593-156">**put \_ P1**</span><span class="sxs-lookup"><span data-stu-id="b2593-156">**put\_P1**</span></span>](iscardcmd-put-p1.md)
</dt> </dl>

 

 
