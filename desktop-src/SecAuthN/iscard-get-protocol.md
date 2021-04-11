---
description: 抓取智慧卡上目前正在使用的通訊協定識別碼。
ms.assetid: 68c75e98-da5c-4e3e-9836-369941751fb0
title: 'ISCard：： get_Protocol 方法 (Scardmgr .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.get_Protocol
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: fb58f890da85e3348ede6af70a006f98daac38a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320196"
---
# <a name="iscardget_protocol-method"></a><span data-ttu-id="aebb8-103">ISCard：： get \_ 通訊協定方法</span><span class="sxs-lookup"><span data-stu-id="aebb8-103">ISCard::get\_Protocol method</span></span>

<span data-ttu-id="aebb8-104">\[**取得 \_ 通訊協定** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="aebb8-104">\[The **get\_Protocol** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="aebb8-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="aebb8-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="aebb8-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="aebb8-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="aebb8-107">**Get \_ 通訊協定** 方法會抓取 [*智慧卡*](../secgloss/s-gly.md)上目前正在使用的通訊協定識別碼。</span><span class="sxs-lookup"><span data-stu-id="aebb8-107">The **get\_Protocol** method retrieves the identifier of the protocol currently in use on the [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="aebb8-108">語法</span><span class="sxs-lookup"><span data-stu-id="aebb8-108">Syntax</span></span>


```C++
HRESULT get_Protocol(
  [out] SCARD_PROTOCOLS *pProtocol
);
```



## <a name="parameters"></a><span data-ttu-id="aebb8-109">參數</span><span class="sxs-lookup"><span data-stu-id="aebb8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aebb8-110">*pProtocol* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="aebb8-110">*pProtocol* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aebb8-111">通訊協定識別碼的指標。</span><span class="sxs-lookup"><span data-stu-id="aebb8-111">Pointer to the protocol identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aebb8-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="aebb8-112">Return value</span></span>

<span data-ttu-id="aebb8-113">方法會傳回下列其中一個可能的值。</span><span class="sxs-lookup"><span data-stu-id="aebb8-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="aebb8-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="aebb8-114">Return code</span></span>                                                                                  | <span data-ttu-id="aebb8-115">Description</span><span class="sxs-lookup"><span data-stu-id="aebb8-115">Description</span></span>                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="aebb8-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="aebb8-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="aebb8-117">作業順利完成。</span><span class="sxs-lookup"><span data-stu-id="aebb8-117">Operation completed successfully.</span></span><br/>        |
| <dl> <span data-ttu-id="aebb8-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="aebb8-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="aebb8-119">*PProtocol* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="aebb8-119">The *pProtocol* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="aebb8-120"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="aebb8-120"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="aebb8-121">在 *pProtocol* 中傳遞了錯誤指標。</span><span class="sxs-lookup"><span data-stu-id="aebb8-121">A bad pointer was passed in *pProtocol*.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="aebb8-122">備註</span><span class="sxs-lookup"><span data-stu-id="aebb8-122">Remarks</span></span>

<span data-ttu-id="aebb8-123">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回智慧卡的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="aebb8-123">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="aebb8-124">如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="aebb8-124">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="aebb8-125">範例</span><span class="sxs-lookup"><span data-stu-id="aebb8-125">Examples</span></span>

<span data-ttu-id="aebb8-126">下列範例顯示如何抓取智慧卡上目前正在使用的通訊協定識別碼。</span><span class="sxs-lookup"><span data-stu-id="aebb8-126">The following example shows retrieving the identifier of the protocol currently in use on the smart card.</span></span>


```C++
SCARD_PROTOCOLS   scProtocol;
HRESULT           hr;

// Retrieve the protocol.
hr = pISCard->get_Protocol(&scProtocol);
if (FAILED(hr))
{
   printf("Failed get_Protocol\n");
   // Take other error handling action as needed.
}
// Use the retrieved protocol. (This example merely displays it.)
switch (scProtocol)
{
    case T0:
        printf("T0 protocol\n");
        break;
    case T1:
        printf("T1 protocol\n");
        break;
    default:
        printf("Other protocol\n");
        break;
}
```



## <a name="requirements"></a><span data-ttu-id="aebb8-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="aebb8-127">Requirements</span></span>



| <span data-ttu-id="aebb8-128">需求</span><span class="sxs-lookup"><span data-stu-id="aebb8-128">Requirement</span></span> | <span data-ttu-id="aebb8-129">值</span><span class="sxs-lookup"><span data-stu-id="aebb8-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aebb8-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="aebb8-130">Minimum supported client</span></span><br/> | <span data-ttu-id="aebb8-131">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aebb8-131">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="aebb8-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="aebb8-132">Minimum supported server</span></span><br/> | <span data-ttu-id="aebb8-133">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aebb8-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="aebb8-134">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="aebb8-134">End of client support</span></span><br/>    | <span data-ttu-id="aebb8-135">Windows XP</span><span class="sxs-lookup"><span data-stu-id="aebb8-135">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="aebb8-136">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="aebb8-136">End of server support</span></span><br/>    | <span data-ttu-id="aebb8-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="aebb8-137">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="aebb8-138">標頭</span><span class="sxs-lookup"><span data-stu-id="aebb8-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="aebb8-139"><dt>Scardmgr。h</dt></span><span class="sxs-lookup"><span data-stu-id="aebb8-139"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="aebb8-140">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="aebb8-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="aebb8-141"><dt>Scardmgr .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="aebb8-141"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="aebb8-142">DLL</span><span class="sxs-lookup"><span data-stu-id="aebb8-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aebb8-143"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aebb8-143"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="aebb8-144">IID</span><span class="sxs-lookup"><span data-stu-id="aebb8-144">IID</span></span><br/>                      | <span data-ttu-id="aebb8-145">IID \_ ISCard 定義為1461AAC3-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="aebb8-145">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="aebb8-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aebb8-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aebb8-147">**取得 \_ Atr**</span><span class="sxs-lookup"><span data-stu-id="aebb8-147">**get\_Atr**</span></span>](iscard-get-atr.md)
</dt> <dt>

[<span data-ttu-id="aebb8-148">**取得 \_ CardHandle**</span><span class="sxs-lookup"><span data-stu-id="aebb8-148">**get\_CardHandle**</span></span>](iscard-get-cardhandle.md)
</dt> <dt>

[<span data-ttu-id="aebb8-149">**取得 \_ 內容**</span><span class="sxs-lookup"><span data-stu-id="aebb8-149">**get\_Context**</span></span>](iscard-get-context.md)
</dt> <dt>

[<span data-ttu-id="aebb8-150">**取得 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="aebb8-150">**get\_Status**</span></span>](iscard-get-status.md)
</dt> <dt>

[<span data-ttu-id="aebb8-151">**ISCard**</span><span class="sxs-lookup"><span data-stu-id="aebb8-151">**ISCard**</span></span>](iscard.md)
</dt> </dl>

 

 
