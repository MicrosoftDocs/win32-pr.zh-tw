---
description: 抓取替代類別識別碼的值。
ms.assetid: 80c7cbba-e28d-4973-9f3f-7636ff331b64
title: 'ISCardCmd：： get_AlternateClassId 方法 (Scarddat .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_AlternateClassId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 8cfc47011881ae3e3f6df5ef51c910899a054f84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987339"
---
# <a name="iscardcmdget_alternateclassid-method"></a><span data-ttu-id="165d9-103">ISCardCmd：： get \_ AlternateClassId 方法</span><span class="sxs-lookup"><span data-stu-id="165d9-103">ISCardCmd::get\_AlternateClassId method</span></span>

<span data-ttu-id="165d9-104">\[**Get \_ AlternateClassId** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="165d9-104">\[The **get\_AlternateClassId** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="165d9-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="165d9-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="165d9-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="165d9-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="165d9-107">**Get \_ AlternateClassId** 方法會抓取替代類別識別碼的值。</span><span class="sxs-lookup"><span data-stu-id="165d9-107">The **get\_AlternateClassId** method retrieves the value of the alternate class ID.</span></span> <span data-ttu-id="165d9-108">除非先前呼叫 [**put \_ AlternateClassId**](iscardcmd-put-alternateclassid.md)來設定替代識別碼，否則這個方法將會失敗。</span><span class="sxs-lookup"><span data-stu-id="165d9-108">This method will fail unless the alternate ID has been set by a previous call to [**put\_AlternateClassId**](iscardcmd-put-alternateclassid.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="165d9-109">語法</span><span class="sxs-lookup"><span data-stu-id="165d9-109">Syntax</span></span>


```C++
HRESULT get_AlternateClassId(
  [out] BYTE *pbyClass
);
```



## <a name="parameters"></a><span data-ttu-id="165d9-110">參數</span><span class="sxs-lookup"><span data-stu-id="165d9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="165d9-111">*pbyClass* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="165d9-111">*pbyClass* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="165d9-112">傳回時，包含替代類別識別碼值之位元組的指標。</span><span class="sxs-lookup"><span data-stu-id="165d9-112">Pointer to the byte that contains the alternate class ID value on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="165d9-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="165d9-113">Return value</span></span>

<span data-ttu-id="165d9-114">方法會傳回下列可能的值。</span><span class="sxs-lookup"><span data-stu-id="165d9-114">The method returns the following possible values.</span></span>



| <span data-ttu-id="165d9-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="165d9-115">Return code</span></span>                                                                                    | <span data-ttu-id="165d9-116">Description</span><span class="sxs-lookup"><span data-stu-id="165d9-116">Description</span></span>                                                                                                                                 |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="165d9-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="165d9-117"><dt>**S\_OK**</dt></span></span> </dl>           | <span data-ttu-id="165d9-118">作業已順利完成。</span><span class="sxs-lookup"><span data-stu-id="165d9-118">Operation was completed successfully.</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="165d9-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="165d9-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>   | <span data-ttu-id="165d9-120">*PbyClass* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="165d9-120">The *pbyClass* parameter is not valid.</span></span><br/>                                                                                           |
| <dl> <span data-ttu-id="165d9-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="165d9-121"><dt>**E\_ACCESSDENIED**</dt></span></span> </dl> | <span data-ttu-id="165d9-122">替代類別識別碼先前尚未藉由 [**put \_ AlternateClassId**](iscardcmd-put-alternateclassid.md)的呼叫來設定。</span><span class="sxs-lookup"><span data-stu-id="165d9-122">The alternate class ID has not been previously set by a call to [**put\_AlternateClassId**](iscardcmd-put-alternateclassid.md).</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="165d9-123">備註</span><span class="sxs-lookup"><span data-stu-id="165d9-123">Remarks</span></span>

<span data-ttu-id="165d9-124">此方法適用于使用 [*T = 0 通訊協定*](../secgloss/t-gly.md)的通訊。</span><span class="sxs-lookup"><span data-stu-id="165d9-124">This method applies to communications using the [*T=0 protocol*](../secgloss/t-gly.md).</span></span> <span data-ttu-id="165d9-125">如需詳細資訊，請參閱 [**put \_ AlternateClassId**](iscardcmd-put-alternateclassid.md)。</span><span class="sxs-lookup"><span data-stu-id="165d9-125">For more information, see [**put\_AlternateClassId**](iscardcmd-put-alternateclassid.md).</span></span>

## <a name="examples"></a><span data-ttu-id="165d9-126">範例</span><span class="sxs-lookup"><span data-stu-id="165d9-126">Examples</span></span>

<span data-ttu-id="165d9-127">下列範例顯示如何取出替代類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="165d9-127">The following example shows how to retrieve the alternate class ID.</span></span> <span data-ttu-id="165d9-128">此範例假設 pISCardCmd 是 [**ISCardCmd**](iscardcmd.md) 介面實例的有效指標。</span><span class="sxs-lookup"><span data-stu-id="165d9-128">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
BYTE     byAltClassID;
HRESULT  hr;

// Retrieve the alternate class ID.
hr = pISCardCmd->get_AlternateClassId(&byAltClassID);
if (FAILED(hr))
{
  printf("Failed get_AltClassId\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="165d9-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="165d9-129">Requirements</span></span>



| <span data-ttu-id="165d9-130">需求</span><span class="sxs-lookup"><span data-stu-id="165d9-130">Requirement</span></span> | <span data-ttu-id="165d9-131">值</span><span class="sxs-lookup"><span data-stu-id="165d9-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="165d9-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="165d9-132">Minimum supported client</span></span><br/> | <span data-ttu-id="165d9-133">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="165d9-133">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="165d9-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="165d9-134">Minimum supported server</span></span><br/> | <span data-ttu-id="165d9-135">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="165d9-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="165d9-136">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="165d9-136">End of client support</span></span><br/>    | <span data-ttu-id="165d9-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="165d9-137">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="165d9-138">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="165d9-138">End of server support</span></span><br/>    | <span data-ttu-id="165d9-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="165d9-139">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="165d9-140">標頭</span><span class="sxs-lookup"><span data-stu-id="165d9-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="165d9-141"><dt>Scarddat。h</dt></span><span class="sxs-lookup"><span data-stu-id="165d9-141"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="165d9-142">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="165d9-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="165d9-143"><dt>Scarddat .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="165d9-143"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="165d9-144">DLL</span><span class="sxs-lookup"><span data-stu-id="165d9-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="165d9-145"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="165d9-145"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="165d9-146">IID</span><span class="sxs-lookup"><span data-stu-id="165d9-146">IID</span></span><br/>                      | <span data-ttu-id="165d9-147">IID \_ ISCardCmd 定義為 D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="165d9-147">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="165d9-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="165d9-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="165d9-149">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="165d9-149">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> <dt>

[<span data-ttu-id="165d9-150">**put \_ AlternateClassId**</span><span class="sxs-lookup"><span data-stu-id="165d9-150">**put\_AlternateClassId**</span></span>](iscardcmd-put-alternateclassid.md)
</dt> </dl>

 

 
