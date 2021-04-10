---
description: 在應用程式協定資料單位中設定新的類別識別碼 (APDU) 。
ms.assetid: 7e7d42f2-2858-4b37-a7d5-a919e3e005da
title: 'ISCardCmd：:p ut_ClassId 方法 (Scarddat .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_ClassId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: ed4b1f273ebe9ea0a5e105ec3d88fc8446f7a831
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943668"
---
# <a name="iscardcmdput_classid-method"></a><span data-ttu-id="be9f7-103">ISCardCmd：:p 的 ui \_ ClassId 方法</span><span class="sxs-lookup"><span data-stu-id="be9f7-103">ISCardCmd::put\_ClassId method</span></span>

<span data-ttu-id="be9f7-104">\[**Put \_ ClassId** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="be9f7-104">\[The **put\_ClassId** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="be9f7-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="be9f7-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="be9f7-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="be9f7-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="be9f7-107">**Put \_ ClassId** 方法會在 [*應用程式協定資料單位*](../secgloss/a-gly.md)中設定新的類別識別碼， (APDU) 。</span><span class="sxs-lookup"><span data-stu-id="be9f7-107">The **put\_ClassId** method sets a new class identifier in the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="be9f7-108">語法</span><span class="sxs-lookup"><span data-stu-id="be9f7-108">Syntax</span></span>


```C++
HRESULT put_ClassId(
  [in] BYTE byClass
);
```



## <a name="parameters"></a><span data-ttu-id="be9f7-109">參數</span><span class="sxs-lookup"><span data-stu-id="be9f7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be9f7-110">*byClass* \[在\]</span><span class="sxs-lookup"><span data-stu-id="be9f7-110">*byClass* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be9f7-111">表示類別識別碼的位元組。</span><span class="sxs-lookup"><span data-stu-id="be9f7-111">The byte that represents the class identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be9f7-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="be9f7-112">Return value</span></span>

<span data-ttu-id="be9f7-113">方法會傳回下列其中一個可能的值。</span><span class="sxs-lookup"><span data-stu-id="be9f7-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="be9f7-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="be9f7-114">Return code</span></span>                                                                                   | <span data-ttu-id="be9f7-115">Description</span><span class="sxs-lookup"><span data-stu-id="be9f7-115">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="be9f7-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="be9f7-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="be9f7-117">作業順利完成。</span><span class="sxs-lookup"><span data-stu-id="be9f7-117">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="be9f7-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="be9f7-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="be9f7-119">*ByClass* 無效。</span><span class="sxs-lookup"><span data-stu-id="be9f7-119">The *byClass* is not valid.</span></span><br/>       |
| <dl> <span data-ttu-id="be9f7-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="be9f7-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="be9f7-121">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="be9f7-121">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="be9f7-122">備註</span><span class="sxs-lookup"><span data-stu-id="be9f7-122">Remarks</span></span>

<span data-ttu-id="be9f7-123">若要取得目前的類別識別碼，請呼叫 [**get \_ ClassId**](iscardcmd-get-classid.md)。</span><span class="sxs-lookup"><span data-stu-id="be9f7-123">To retrieve the current class identifier, call [**get\_ClassId**](iscardcmd-get-classid.md).</span></span>

<span data-ttu-id="be9f7-124">如需此介面所提供的所有方法清單，請參閱 [**ISCardCmd**](iscardcmd.md)。</span><span class="sxs-lookup"><span data-stu-id="be9f7-124">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="be9f7-125">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回 [*智慧卡*](../secgloss/s-gly.md) 的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="be9f7-125">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="be9f7-126">如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="be9f7-126">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="be9f7-127">範例</span><span class="sxs-lookup"><span data-stu-id="be9f7-127">Examples</span></span>

<span data-ttu-id="be9f7-128">下列範例顯示如何在 [*應用程式協定資料單位*](../secgloss/a-gly.md) 中設定新的類別識別碼， (APDU) 。</span><span class="sxs-lookup"><span data-stu-id="be9f7-128">The following example shows how to set a new class identifier in the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="be9f7-129">此範例假設 pISCardCmd 是 [**ISCardCmd**](iscardcmd.md) 介面實例的有效指標。</span><span class="sxs-lookup"><span data-stu-id="be9f7-129">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
HRESULT  hr;

// Set the class ID.
hr = pISCardCmd->put_ClassId(0xC0);
if (FAILED(hr))
{
  printf("Failed put_ClassId\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="be9f7-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="be9f7-130">Requirements</span></span>



| <span data-ttu-id="be9f7-131">需求</span><span class="sxs-lookup"><span data-stu-id="be9f7-131">Requirement</span></span> | <span data-ttu-id="be9f7-132">值</span><span class="sxs-lookup"><span data-stu-id="be9f7-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="be9f7-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="be9f7-133">Minimum supported client</span></span><br/> | <span data-ttu-id="be9f7-134">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="be9f7-134">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="be9f7-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="be9f7-135">Minimum supported server</span></span><br/> | <span data-ttu-id="be9f7-136">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="be9f7-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="be9f7-137">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="be9f7-137">End of client support</span></span><br/>    | <span data-ttu-id="be9f7-138">Windows XP</span><span class="sxs-lookup"><span data-stu-id="be9f7-138">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="be9f7-139">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="be9f7-139">End of server support</span></span><br/>    | <span data-ttu-id="be9f7-140">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="be9f7-140">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="be9f7-141">標頭</span><span class="sxs-lookup"><span data-stu-id="be9f7-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="be9f7-142"><dt>Scarddat。h</dt></span><span class="sxs-lookup"><span data-stu-id="be9f7-142"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="be9f7-143">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="be9f7-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="be9f7-144"><dt>Scarddat .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="be9f7-144"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="be9f7-145">DLL</span><span class="sxs-lookup"><span data-stu-id="be9f7-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be9f7-146"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be9f7-146"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="be9f7-147">IID</span><span class="sxs-lookup"><span data-stu-id="be9f7-147">IID</span></span><br/>                      | <span data-ttu-id="be9f7-148">IID \_ ISCardCmd 定義為 D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="be9f7-148">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="be9f7-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="be9f7-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be9f7-150">**取得 \_ ClassId**</span><span class="sxs-lookup"><span data-stu-id="be9f7-150">**get\_ClassId**</span></span>](iscardcmd-get-classid.md)
</dt> <dt>

[<span data-ttu-id="be9f7-151">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="be9f7-151">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
