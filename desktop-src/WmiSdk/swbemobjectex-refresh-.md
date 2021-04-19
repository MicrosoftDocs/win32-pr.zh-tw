---
description: 更新具有效能提供者所提供之資料的物件資料，例如效能計數器類別。 您可以更快速地取得更新的資料，而不需要呼叫 SWbemServices。 Get \_ 。
ms.assetid: 6aeaa336-fb98-4eda-b746-fc958198d8ae
ms.tgt_platform: multiple
title: 'SWbemObjectEx.Refresh_ 方法 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectEx.Refresh_
- ISWbemObjectEx.Refresh_
- ISWbemObjectEx.Refresh_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 904e2b7f9b256596555c8396a699220108d4f37b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974188"
---
# <a name="swbemobjectexrefresh_-method"></a><span data-ttu-id="5412c-104">SWbemObjectEx \_ 方法</span><span class="sxs-lookup"><span data-stu-id="5412c-104">SWbemObjectEx.Refresh\_ method</span></span>

<span data-ttu-id="5412c-105">[**SWbemObjectEx**](swbemobjectex.md)的 **Refresh \_** 方法會更新具有效能提供者所提供之資料的物件資料，例如 [效能計數器類別](/windows/desktop/CIMWin32Prov/performance-counter-classes)。</span><span class="sxs-lookup"><span data-stu-id="5412c-105">The **Refresh\_** method of [**SWbemObjectEx**](swbemobjectex.md) updates the data for objects that have data supplied by a performance provider, such as the [Performance Counter Classes](/windows/desktop/CIMWin32Prov/performance-counter-classes).</span></span> <span data-ttu-id="5412c-106">您可以更快速地取得更新的資料，而不需要呼叫 [**SWbemServices \_ 。 Get**](swbemservices-get.md)。</span><span class="sxs-lookup"><span data-stu-id="5412c-106">You can obtain updated data more quickly and without a call to [**SWbemServices.Get\_**](swbemservices-get.md).</span></span>

<span data-ttu-id="5412c-107">如需此語法的詳細資訊，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="5412c-107">For more information about this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5412c-108">語法</span><span class="sxs-lookup"><span data-stu-id="5412c-108">Syntax</span></span>


```VB
SWbemObjectEx.Refresh_( _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="5412c-109">參數</span><span class="sxs-lookup"><span data-stu-id="5412c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5412c-110">*iFlags* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="5412c-110">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5412c-111">保留的作業旗標（如果有指定）必須是 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="5412c-111">Reserved operation flags which, if specified, must be 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="5412c-112">*objWbemNamedValueSet* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="5412c-112">*objWbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5412c-113">[**SWbemNamedValueSet**](swbemnamedvalueset.md)物件，它會設定作業的內容。</span><span class="sxs-lookup"><span data-stu-id="5412c-113">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that sets context for the operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5412c-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="5412c-114">Return value</span></span>

<span data-ttu-id="5412c-115">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="5412c-115">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="5412c-116">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="5412c-116">Error codes</span></span>

<span data-ttu-id="5412c-117">完成 **Refresh \_** 方法之後， **Err** 物件可能會包含下列清單中的其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="5412c-117">After completion of the **Refresh\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="5412c-118">**wbemErrFailed** -2147749889 (0x80041001) </span><span class="sxs-lookup"><span data-stu-id="5412c-118">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="5412c-119">提供者在內部失敗，即使作業有效也一樣。</span><span class="sxs-lookup"><span data-stu-id="5412c-119">The provider failed internally, even though the operation was valid.</span></span>

</dd> <dt>

<span data-ttu-id="5412c-120">**wbemErrNotFound** -2147749890 (0x80041002) </span><span class="sxs-lookup"><span data-stu-id="5412c-120">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="5412c-121">找不到要求的格式。</span><span class="sxs-lookup"><span data-stu-id="5412c-121">The requested format was not found.</span></span>

</dd> <dt>

<span data-ttu-id="5412c-122">**wbemErrInvalidParameter** -2147749896 (0x80041008) </span><span class="sxs-lookup"><span data-stu-id="5412c-122">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="5412c-123">呼叫的其中一個參數不正確。</span><span class="sxs-lookup"><span data-stu-id="5412c-123">One of the parameters to the call is not correct.</span></span>

</dd> <dt>

<span data-ttu-id="5412c-124">**wbemErrRefresherBusy** -2147749975 (0x80041057) </span><span class="sxs-lookup"><span data-stu-id="5412c-124">**wbemErrRefresherBusy** - 2147749975 (0x80041057)</span></span>
</dt> <dd>

<span data-ttu-id="5412c-125">重新整理器專注於進行其他作業。</span><span class="sxs-lookup"><span data-stu-id="5412c-125">The refresher is busy with another operation.</span></span>

</dd> <dt>

<span data-ttu-id="5412c-126">**wbemPartialResults** -2147745808 (0x80040010) </span><span class="sxs-lookup"><span data-stu-id="5412c-126">**wbemPartialResults** - 2147745808 (0x80040010)</span></span>
</dt> <dd>

<span data-ttu-id="5412c-127">並非所有的物件、列舉值或嵌套的刷新器都已成功更新。</span><span class="sxs-lookup"><span data-stu-id="5412c-127">Not all of the objects, enumerators, or nested refreshers were successfully updated.</span></span> <span data-ttu-id="5412c-128">這項傳回不是錯誤，而是表示作業不完整。</span><span class="sxs-lookup"><span data-stu-id="5412c-128">This return is not an error but an indication that the operation was incomplete.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="5412c-129">範例</span><span class="sxs-lookup"><span data-stu-id="5412c-129">Examples</span></span>

<span data-ttu-id="5412c-130">下列腳本程式碼範例示範如何取得系統進程的原始和處理後效能計數器。</span><span class="sxs-lookup"><span data-stu-id="5412c-130">The following script code example shows how to obtain both raw and cooked performance counters for the system process.</span></span> <span data-ttu-id="5412c-131">物件會每兩秒重新整理一次，並顯示內容。</span><span class="sxs-lookup"><span data-stu-id="5412c-131">The objects are refreshed every two seconds and the properties displayed.</span></span>


```VB
' Get the performance counter instance for the System process
set PerfRaw = GetObject( _
    "winmgmts:win32_perfrawdata_perfproc_process.name='system'")
set PerfCooked = GetObject( _
    "winmgmts:win32_perfformatteddata_perfproc_process.name='system'")

' Display some properties in a loop
for I = 1 to 5
    Wscript.Echo "HandleCount = "& PerfRaw.HandleCount & _
         " Raw ThreadCount = " & PerfRaw.ThreadCount & _
        " Cooked ThreadCount = " & PerfCooked.ThreadCount
    
    Wscript.Sleep 2000
    
' Refresh the objects
    PerfRaw.Refresh_
    PerfCooked.Refresh_
next
```



## <a name="requirements"></a><span data-ttu-id="5412c-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="5412c-132">Requirements</span></span>



| <span data-ttu-id="5412c-133">需求</span><span class="sxs-lookup"><span data-stu-id="5412c-133">Requirement</span></span> | <span data-ttu-id="5412c-134">值</span><span class="sxs-lookup"><span data-stu-id="5412c-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5412c-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5412c-135">Minimum supported client</span></span><br/> | <span data-ttu-id="5412c-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5412c-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5412c-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5412c-137">Minimum supported server</span></span><br/> | <span data-ttu-id="5412c-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5412c-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5412c-139">標頭</span><span class="sxs-lookup"><span data-stu-id="5412c-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="5412c-140"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="5412c-140"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="5412c-141">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="5412c-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="5412c-142"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5412c-142"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5412c-143">DLL</span><span class="sxs-lookup"><span data-stu-id="5412c-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5412c-144"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5412c-144"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="5412c-145">CLSID</span><span class="sxs-lookup"><span data-stu-id="5412c-145">CLSID</span></span><br/>                    | <span data-ttu-id="5412c-146">CLSID \_ SWbemObjectEx</span><span class="sxs-lookup"><span data-stu-id="5412c-146">CLSID\_SWbemObjectEx</span></span><br/>                                                         |
| <span data-ttu-id="5412c-147">IID</span><span class="sxs-lookup"><span data-stu-id="5412c-147">IID</span></span><br/>                      | <span data-ttu-id="5412c-148">IID \_ ISWbemObjectEx</span><span class="sxs-lookup"><span data-stu-id="5412c-148">IID\_ISWbemObjectEx</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="5412c-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5412c-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5412c-150">**SWbemObjectEx**</span><span class="sxs-lookup"><span data-stu-id="5412c-150">**SWbemObjectEx**</span></span>](swbemobjectex.md)
</dt> <dt>

[<span data-ttu-id="5412c-151">監視效能資料</span><span class="sxs-lookup"><span data-stu-id="5412c-151">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> </dl>

 

