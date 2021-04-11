---
description: 抓取回復訊息中智慧卡所使用 (Nad) 的節點位址。
ms.assetid: bf4f281c-d378-4abd-8f2e-e23c2f4e87a4
title: 'ISCardCmd：： get_ReplyNad 方法 (Scarddat .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_ReplyNad
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 2088aa208a97511fd53eecec5a8cdc473b612bc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113220"
---
# <a name="iscardcmdget_replynad-method"></a><span data-ttu-id="5d6d1-103">ISCardCmd：： get \_ ReplyNad 方法</span><span class="sxs-lookup"><span data-stu-id="5d6d1-103">ISCardCmd::get\_ReplyNad method</span></span>

<span data-ttu-id="5d6d1-104">\[**Get \_ ReplyNad** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="5d6d1-104">\[The **get\_ReplyNad** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="5d6d1-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="5d6d1-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="5d6d1-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="5d6d1-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="5d6d1-107">**Get \_ ReplyNad** 方法會抓取回復訊息中的 [*智慧卡*](../secgloss/s-gly.md)所使用的節點位址 (Nad) 。</span><span class="sxs-lookup"><span data-stu-id="5d6d1-107">The **get\_ReplyNad** method retrieves the node address (Nad) used by the [*smart card*](../secgloss/s-gly.md) in the reply message.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d6d1-108">語法</span><span class="sxs-lookup"><span data-stu-id="5d6d1-108">Syntax</span></span>


```C++
HRESULT get_ReplyNad(
  [out] BYTE *pbNad
);
```



## <a name="parameters"></a><span data-ttu-id="5d6d1-109">參數</span><span class="sxs-lookup"><span data-stu-id="5d6d1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d6d1-110">*pbNad* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="5d6d1-110">*pbNad* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5d6d1-111">傳回時，包含回復訊息所使用之 Nad 的位元組指標。</span><span class="sxs-lookup"><span data-stu-id="5d6d1-111">Pointer to the byte that contains the Nad used by the reply message, on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d6d1-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="5d6d1-112">Return value</span></span>

<span data-ttu-id="5d6d1-113">方法會傳回下列其中一個可能的值。</span><span class="sxs-lookup"><span data-stu-id="5d6d1-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="5d6d1-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="5d6d1-114">Return code</span></span>                                                                                    | <span data-ttu-id="5d6d1-115">Description</span><span class="sxs-lookup"><span data-stu-id="5d6d1-115">Description</span></span>                                                        |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="5d6d1-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="5d6d1-116"><dt>**S\_OK**</dt></span></span> </dl>           | <span data-ttu-id="5d6d1-117">作業已順利完成。</span><span class="sxs-lookup"><span data-stu-id="5d6d1-117">Operation was completed successfully.</span></span><br/>                   |
| <dl> <span data-ttu-id="5d6d1-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="5d6d1-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>   | <span data-ttu-id="5d6d1-119">*PbNad* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="5d6d1-119">The *pbNad* parameter is not valid.</span></span><br/>                     |
| <dl> <span data-ttu-id="5d6d1-120"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="5d6d1-120"><dt>**E\_ACCESSDENIED**</dt></span></span> </dl> | <span data-ttu-id="5d6d1-121">內部呼叫無法取出 Nad 資訊。</span><span class="sxs-lookup"><span data-stu-id="5d6d1-121">Internal calls were unable to retrieve Nad information.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5d6d1-122">備註</span><span class="sxs-lookup"><span data-stu-id="5d6d1-122">Remarks</span></span>

<span data-ttu-id="5d6d1-123">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此方法可能會傳回智慧卡的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="5d6d1-123">In addition to the COM error codes listed above, this method may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="5d6d1-124">如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="5d6d1-124">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="5d6d1-125">範例</span><span class="sxs-lookup"><span data-stu-id="5d6d1-125">Examples</span></span>

<span data-ttu-id="5d6d1-126">下列範例示範如何在回復訊息中，) [*智慧卡*](../secgloss/s-gly.md) 所使用 (Nad 的節點位址。</span><span class="sxs-lookup"><span data-stu-id="5d6d1-126">The following example shows how to retrieve the node address (Nad) used by the [*smart card*](../secgloss/s-gly.md) in the reply message.</span></span> <span data-ttu-id="5d6d1-127">此範例假設 pISCardCmd 是 [**ISCardCmd**](iscardcmd.md) 介面實例的有效指標。</span><span class="sxs-lookup"><span data-stu-id="5d6d1-127">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
BYTE    byNad;
HRESULT hr;

// Get reply Nad.
hr = pISCardCmd->get_ReplyNad(&byNad);
if (FAILED(hr))
{
  printf("Failed get_ReplyNad\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="5d6d1-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="5d6d1-128">Requirements</span></span>



| <span data-ttu-id="5d6d1-129">需求</span><span class="sxs-lookup"><span data-stu-id="5d6d1-129">Requirement</span></span> | <span data-ttu-id="5d6d1-130">值</span><span class="sxs-lookup"><span data-stu-id="5d6d1-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5d6d1-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5d6d1-131">Minimum supported client</span></span><br/> | <span data-ttu-id="5d6d1-132">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5d6d1-132">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="5d6d1-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5d6d1-133">Minimum supported server</span></span><br/> | <span data-ttu-id="5d6d1-134">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5d6d1-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5d6d1-135">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="5d6d1-135">End of client support</span></span><br/>    | <span data-ttu-id="5d6d1-136">Windows XP</span><span class="sxs-lookup"><span data-stu-id="5d6d1-136">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="5d6d1-137">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="5d6d1-137">End of server support</span></span><br/>    | <span data-ttu-id="5d6d1-138">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5d6d1-138">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="5d6d1-139">標頭</span><span class="sxs-lookup"><span data-stu-id="5d6d1-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d6d1-140"><dt>Scarddat。h</dt></span><span class="sxs-lookup"><span data-stu-id="5d6d1-140"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="5d6d1-141">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="5d6d1-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="5d6d1-142"><dt>Scarddat .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5d6d1-142"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5d6d1-143">DLL</span><span class="sxs-lookup"><span data-stu-id="5d6d1-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5d6d1-144"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5d6d1-144"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="5d6d1-145">IID</span><span class="sxs-lookup"><span data-stu-id="5d6d1-145">IID</span></span><br/>                      | <span data-ttu-id="5d6d1-146">IID \_ ISCardCmd 定義為 D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="5d6d1-146">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="5d6d1-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5d6d1-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d6d1-148">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="5d6d1-148">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
