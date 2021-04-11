---
description: 抓取智慧卡的目前狀態。
ms.assetid: 0e6e4a8f-ecad-4a82-8804-aaf58f13f7ca
title: 'ISCard：： get_Status 方法 (Scardmgr .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.get_Status
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: f0daa47653779b3aa4b5e7cb65c0c56410b19ab9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195256"
---
# <a name="iscardget_status-method"></a><span data-ttu-id="67639-103">ISCard：： get \_ Status 方法</span><span class="sxs-lookup"><span data-stu-id="67639-103">ISCard::get\_Status method</span></span>

<span data-ttu-id="67639-104">\[**取得 \_ 狀態** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="67639-104">\[The **get\_Status** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="67639-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="67639-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="67639-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="67639-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="67639-107">**取得 \_ 狀態** 方法會抓取 [*智慧卡*](../secgloss/s-gly.md)的目前 [*狀態*](../secgloss/s-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="67639-107">The **get\_Status** method retrieves the current [*state*](../secgloss/s-gly.md) of the [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="67639-108">語法</span><span class="sxs-lookup"><span data-stu-id="67639-108">Syntax</span></span>


```C++
HRESULT get_Status(
  [out] SCARD_STATES *pStatus
);
```



## <a name="parameters"></a><span data-ttu-id="67639-109">參數</span><span class="sxs-lookup"><span data-stu-id="67639-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67639-110">*pStatus* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="67639-110">*pStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="67639-111">狀態變數的指標。</span><span class="sxs-lookup"><span data-stu-id="67639-111">Pointer to the state variable.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67639-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="67639-112">Return value</span></span>

<span data-ttu-id="67639-113">方法會傳回下列其中一個可能的值。</span><span class="sxs-lookup"><span data-stu-id="67639-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="67639-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="67639-114">Return code</span></span>                                                                                  | <span data-ttu-id="67639-115">Description</span><span class="sxs-lookup"><span data-stu-id="67639-115">Description</span></span>                                       |
|----------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <span data-ttu-id="67639-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="67639-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="67639-117">作業順利完成。</span><span class="sxs-lookup"><span data-stu-id="67639-117">Operation completed successfully.</span></span><br/>      |
| <dl> <span data-ttu-id="67639-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="67639-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="67639-119">*PStatus* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="67639-119">The *pStatus* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="67639-120"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="67639-120"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="67639-121">在 *pStatus* 中傳遞了錯誤指標。</span><span class="sxs-lookup"><span data-stu-id="67639-121">A bad pointer was passed in *pStatus*.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="67639-122">備註</span><span class="sxs-lookup"><span data-stu-id="67639-122">Remarks</span></span>

<span data-ttu-id="67639-123">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回智慧卡的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="67639-123">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="67639-124">如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="67639-124">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="67639-125">範例</span><span class="sxs-lookup"><span data-stu-id="67639-125">Examples</span></span>

<span data-ttu-id="67639-126">下列範例顯示如何取出智慧卡的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="67639-126">The following example shows retrieving the current state of the smart card.</span></span>


```C++
SCARD_STATES    scState;
HRESULT         hr;

// Determine the current state of the smart card.
hr = pISCard->get_Status(&scState);
if (FAILED(hr))
{
   printf("Failed get_Status\n");
   exit(1);  // Or other error handling action.
}
// Use the retrieved value. (This example merely displays it.)
switch (scState)
{
    case ABSENT:
        printf("Absent state\n");
        break;
    case PRESENT:
        printf("Present state\n");
        break;
    case SWALLOWED:
        printf("Swallowed state\n");
        break;
    case POWERED:
        printf("Powered state\n");
        break;
    case NEGOTIABLEMODE:
        printf("Negotiable mode state\n");
        break;
    case SPECIFICMODE:
        printf("Specific mode state\n");
        break;
    default:
        printf("Unexpected state\n");
        break;
}
```



## <a name="requirements"></a><span data-ttu-id="67639-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="67639-127">Requirements</span></span>



| <span data-ttu-id="67639-128">需求</span><span class="sxs-lookup"><span data-stu-id="67639-128">Requirement</span></span> | <span data-ttu-id="67639-129">值</span><span class="sxs-lookup"><span data-stu-id="67639-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="67639-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="67639-130">Minimum supported client</span></span><br/> | <span data-ttu-id="67639-131">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="67639-131">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="67639-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="67639-132">Minimum supported server</span></span><br/> | <span data-ttu-id="67639-133">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="67639-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="67639-134">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="67639-134">End of client support</span></span><br/>    | <span data-ttu-id="67639-135">Windows XP</span><span class="sxs-lookup"><span data-stu-id="67639-135">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="67639-136">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="67639-136">End of server support</span></span><br/>    | <span data-ttu-id="67639-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="67639-137">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="67639-138">標頭</span><span class="sxs-lookup"><span data-stu-id="67639-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="67639-139"><dt>Scardmgr。h</dt></span><span class="sxs-lookup"><span data-stu-id="67639-139"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="67639-140">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="67639-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="67639-141"><dt>Scardmgr .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="67639-141"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="67639-142">DLL</span><span class="sxs-lookup"><span data-stu-id="67639-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="67639-143"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="67639-143"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="67639-144">IID</span><span class="sxs-lookup"><span data-stu-id="67639-144">IID</span></span><br/>                      | <span data-ttu-id="67639-145">IID \_ ISCard 定義為1461AAC3-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="67639-145">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="67639-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="67639-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67639-147">**取得 \_ Atr**</span><span class="sxs-lookup"><span data-stu-id="67639-147">**get\_Atr**</span></span>](iscard-get-atr.md)
</dt> <dt>

[<span data-ttu-id="67639-148">**取得 \_ CardHandle**</span><span class="sxs-lookup"><span data-stu-id="67639-148">**get\_CardHandle**</span></span>](iscard-get-cardhandle.md)
</dt> <dt>

[<span data-ttu-id="67639-149">**取得 \_ 內容**</span><span class="sxs-lookup"><span data-stu-id="67639-149">**get\_Context**</span></span>](iscard-get-context.md)
</dt> <dt>

[<span data-ttu-id="67639-150">**取得 \_ 通訊協定**</span><span class="sxs-lookup"><span data-stu-id="67639-150">**get\_Protocol**</span></span>](iscard-get-protocol.md)
</dt> <dt>

[<span data-ttu-id="67639-151">**ISCard**</span><span class="sxs-lookup"><span data-stu-id="67639-151">**ISCard**</span></span>](iscard.md)
</dt> </dl>

 

 
