---
description: 從應用程式協定資料單位中抓取類別識別碼 (APDU) 。
ms.assetid: 03ea997d-7698-43c7-aa9a-dfc1bac6fcdd
title: 'ISCardCmd：： get_ClassId 方法 (Scarddat .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_ClassId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 6b78dfc9f3adf200a614b129ff1e86a16c88438f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113229"
---
# <a name="iscardcmdget_classid-method"></a><span data-ttu-id="f8526-103">ISCardCmd：： get \_ ClassId 方法</span><span class="sxs-lookup"><span data-stu-id="f8526-103">ISCardCmd::get\_ClassId method</span></span>

<span data-ttu-id="f8526-104">\[**Get \_ ClassId** 方法可在 [需求] 區段中指定的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="f8526-104">\[The **get\_ClassId** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="f8526-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="f8526-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="f8526-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="f8526-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="f8526-107">**Get \_ ClassId** 方法會從 [*應用程式協定資料單位*](../secgloss/a-gly.md)中，取得 (APDU) 的類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="f8526-107">The **get\_ClassId** method retrieves the class identifier from the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="f8526-108">語法</span><span class="sxs-lookup"><span data-stu-id="f8526-108">Syntax</span></span>


```C++
HRESULT get_ClassId(
  [out] BYTE *pbyClass
);
```



## <a name="parameters"></a><span data-ttu-id="f8526-109">參數</span><span class="sxs-lookup"><span data-stu-id="f8526-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8526-110">*pbyClass* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f8526-110">*pbyClass* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f8526-111">代表類別識別碼之位元組的指標。</span><span class="sxs-lookup"><span data-stu-id="f8526-111">Pointer to the byte that represents the class identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8526-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="f8526-112">Return value</span></span>

<span data-ttu-id="f8526-113">方法會傳回下列其中一個可能的值。</span><span class="sxs-lookup"><span data-stu-id="f8526-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="f8526-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="f8526-114">Return code</span></span>                                                                                   | <span data-ttu-id="f8526-115">Description</span><span class="sxs-lookup"><span data-stu-id="f8526-115">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="f8526-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="f8526-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="f8526-117">作業順利完成。</span><span class="sxs-lookup"><span data-stu-id="f8526-117">Operation completed successfully.</span></span><br/>       |
| <dl> <span data-ttu-id="f8526-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="f8526-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="f8526-119">*PbyClass* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="f8526-119">The *pbyClass* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="f8526-120"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="f8526-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="f8526-121">在 *pbyClass* 中傳遞了錯誤指標。</span><span class="sxs-lookup"><span data-stu-id="f8526-121">A bad pointer was passed in *pbyClass*.</span></span><br/> |
| <dl> <span data-ttu-id="f8526-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="f8526-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="f8526-123">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="f8526-123">Out of memory.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="f8526-124">備註</span><span class="sxs-lookup"><span data-stu-id="f8526-124">Remarks</span></span>

<span data-ttu-id="f8526-125">若要將類別識別碼設定為新的值，請呼叫 [**put \_ ClassId**](iscardcmd-put-classid.md)。</span><span class="sxs-lookup"><span data-stu-id="f8526-125">To set the class identifier to a new value, call [**put\_ClassId**](iscardcmd-put-classid.md).</span></span>

<span data-ttu-id="f8526-126">如需此介面所提供的所有方法清單，請參閱 [**ISCardCmd**](iscardcmd.md)。</span><span class="sxs-lookup"><span data-stu-id="f8526-126">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="f8526-127">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回智慧卡的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="f8526-127">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="f8526-128">如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="f8526-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="f8526-129">範例</span><span class="sxs-lookup"><span data-stu-id="f8526-129">Examples</span></span>

<span data-ttu-id="f8526-130">下列範例顯示如何取出類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="f8526-130">The following example shows how to retrieve the class ID.</span></span> <span data-ttu-id="f8526-131">此範例假設 pISCardCmd 是 [**ISCardCmd**](iscardcmd.md) 介面實例的有效指標。</span><span class="sxs-lookup"><span data-stu-id="f8526-131">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
BYTE     byClassID;
HRESULT  hr;

// Retrieve the class ID.
hr = pISCardCmd->get_ClassId(&byClassID);
if (FAILED(hr))
{
  printf("Failed get_ClassId\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="f8526-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="f8526-132">Requirements</span></span>



| <span data-ttu-id="f8526-133">需求</span><span class="sxs-lookup"><span data-stu-id="f8526-133">Requirement</span></span> | <span data-ttu-id="f8526-134">值</span><span class="sxs-lookup"><span data-stu-id="f8526-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f8526-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f8526-135">Minimum supported client</span></span><br/> | <span data-ttu-id="f8526-136">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f8526-136">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="f8526-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f8526-137">Minimum supported server</span></span><br/> | <span data-ttu-id="f8526-138">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f8526-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f8526-139">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="f8526-139">End of client support</span></span><br/>    | <span data-ttu-id="f8526-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f8526-140">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="f8526-141">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="f8526-141">End of server support</span></span><br/>    | <span data-ttu-id="f8526-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f8526-142">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="f8526-143">標頭</span><span class="sxs-lookup"><span data-stu-id="f8526-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8526-144"><dt>Scarddat。h</dt></span><span class="sxs-lookup"><span data-stu-id="f8526-144"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="f8526-145">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="f8526-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="f8526-146"><dt>Scarddat .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f8526-146"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f8526-147">DLL</span><span class="sxs-lookup"><span data-stu-id="f8526-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f8526-148"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f8526-148"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="f8526-149">IID</span><span class="sxs-lookup"><span data-stu-id="f8526-149">IID</span></span><br/>                      | <span data-ttu-id="f8526-150">IID \_ ISCardCmd 定義為 D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="f8526-150">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="f8526-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f8526-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8526-152">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="f8526-152">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> <dt>

[<span data-ttu-id="f8526-153">**put \_ ClassId**</span><span class="sxs-lookup"><span data-stu-id="f8526-153">**put\_ClassId**</span></span>](iscardcmd-put-classid.md)
</dt> </dl>

 

 
