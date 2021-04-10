---
title: 'IADsPrintJobOperations 屬性方法 (Iads .h) '
description: IADsPrintJobOperations 介面的屬性方法會讀取並寫入下表所列的屬性。 如需屬性方法的詳細資訊，請參閱介面屬性方法。
ms.assetid: d1710bd4-e600-4d92-892a-16b4316851d4
ms.tgt_platform: multiple
keywords:
- IADsPrintJobOperations 屬性方法 ADSI
topic_type:
- apiref
api_name:
- IADsPrintJobOperations Property Methods
- IADsPrintJobOperations.Status
- IADsPrintJobOperations.get_Status
- IADsPrintJobOperations.TimeElapsed
- IADsPrintJobOperations.get_TimeElapsed
- IADsPrintJobOperations.PagesPrinted
- IADsPrintJobOperations.get_PagesPrinted
- IADsPrintJobOperations.Position
- IADsPrintJobOperations.get_Position
- IADsPrintJobOperations.put_Position
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2981fcdd8043c0eb0ee8b05cfd0331fe3abfabe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844012"
---
# <a name="iadsprintjoboperations-property-methods"></a><span data-ttu-id="5606a-105">IADsPrintJobOperations 屬性方法</span><span class="sxs-lookup"><span data-stu-id="5606a-105">IADsPrintJobOperations Property Methods</span></span>

<span data-ttu-id="5606a-106">[**IADsPrintJobOperations**](/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations)介面的屬性方法會讀取並寫入下表所列的屬性。</span><span class="sxs-lookup"><span data-stu-id="5606a-106">The property methods of the [**IADsPrintJobOperations**](/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations) interface read and write the properties listed in the following table.</span></span> <span data-ttu-id="5606a-107">如需屬性方法的詳細資訊，請參閱 [介面屬性方法](interface-property-methods.md)。</span><span class="sxs-lookup"><span data-stu-id="5606a-107">For more information about property methods, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="5606a-108">屬性</span><span class="sxs-lookup"><span data-stu-id="5606a-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="5606a-109">**PagesPrinted**</span><span class="sxs-lookup"><span data-stu-id="5606a-109">**PagesPrinted**</span></span>
<span data-ttu-id="5606a-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="5606a-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="5606a-111">包含列印的頁面數目。</span><span class="sxs-lookup"><span data-stu-id="5606a-111">Contains the number of pages printed.</span></span>

<dt>

<span data-ttu-id="5606a-112">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5606a-112">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5606a-113">編寫資料類型的腳本： **LONG**</span><span class="sxs-lookup"><span data-stu-id="5606a-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PagesPrinted(
  [out] LONG* plPagesPrinted
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="5606a-114">**位置**</span><span class="sxs-lookup"><span data-stu-id="5606a-114">**Position**</span></span>
<span data-ttu-id="5606a-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="5606a-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="5606a-116">包含列印佇列中此列印工作的位置。</span><span class="sxs-lookup"><span data-stu-id="5606a-116">Contains the position of this print job in the print queue.</span></span>

<dt>

<span data-ttu-id="5606a-117">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5606a-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5606a-118">編寫資料類型的腳本： **LONG**</span><span class="sxs-lookup"><span data-stu-id="5606a-118">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Position(
  [out] LONG* plPosition
);
HRESULT put_Position(
  [in] LONG lPosition
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="5606a-119">**狀態**</span><span class="sxs-lookup"><span data-stu-id="5606a-119">**Status**</span></span>
<span data-ttu-id="5606a-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="5606a-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="5606a-121">包含列印工作的目前狀態，如其中一個 [**ADSI 列印工作狀態常數**](adsi-print-job-status-constants.md) 值所表示。</span><span class="sxs-lookup"><span data-stu-id="5606a-121">Contains the current status of the print job as indicated by one of the [**ADSI Print Job Status Constants**](adsi-print-job-status-constants.md) values.</span></span>

<dt>

<span data-ttu-id="5606a-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5606a-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5606a-123">編寫資料類型的腳本： **LONG**</span><span class="sxs-lookup"><span data-stu-id="5606a-123">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Status(
  [out] LONG* plStatus
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="5606a-124">**>timeelapsed**</span><span class="sxs-lookup"><span data-stu-id="5606a-124">**TimeElapsed**</span></span>
<span data-ttu-id="5606a-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="5606a-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="5606a-126">包含自列印工作開始以來經過的毫秒數。</span><span class="sxs-lookup"><span data-stu-id="5606a-126">Contains the number of milliseconds elapsed since the print job started.</span></span>

<dt>

<span data-ttu-id="5606a-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5606a-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5606a-128">編寫資料類型的腳本： **LONG**</span><span class="sxs-lookup"><span data-stu-id="5606a-128">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_TimeElapsed(
  [out] LONG* plTimeElapsed
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="5606a-129">範例</span><span class="sxs-lookup"><span data-stu-id="5606a-129">Examples</span></span>

<span data-ttu-id="5606a-130">下列程式碼範例會示範如何使用 [**IADsPrintJobOperations**](/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations) 的屬性。</span><span class="sxs-lookup"><span data-stu-id="5606a-130">The following code example shows how the properties for [**IADsPrintJobOperations**](/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations) may be used.</span></span>


```VB
Dim pqo As IADsPrintQueueOperations
Dim pjo As IADsPrintJobOperations

On Error GoTo Cleanup

Set pqo = GetObject("WinNT://aMachine/aPrinter")
For Each pj In pqo.PrintJobs
    Set pjo = pj
    MsgBox pjo.PagesPrinted & " pages printed for job " & pj.Name
    If (pjo.position > 1) Then
        pjo.Position = pjo.status - 1
    End If
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set pqo = Nothing
    Set pjo = Nothing
```



## <a name="requirements"></a><span data-ttu-id="5606a-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="5606a-131">Requirements</span></span>



| <span data-ttu-id="5606a-132">需求</span><span class="sxs-lookup"><span data-stu-id="5606a-132">Requirement</span></span> | <span data-ttu-id="5606a-133">值</span><span class="sxs-lookup"><span data-stu-id="5606a-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="5606a-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5606a-134">Minimum supported client</span></span><br/> | <span data-ttu-id="5606a-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5606a-135">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="5606a-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5606a-136">Minimum supported server</span></span><br/> | <span data-ttu-id="5606a-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5606a-137">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="5606a-138">標頭</span><span class="sxs-lookup"><span data-stu-id="5606a-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="5606a-139"><dt>Iads。h</dt></span><span class="sxs-lookup"><span data-stu-id="5606a-139"><dt>Iads.h</dt></span></span> </dl>         |
| <span data-ttu-id="5606a-140">DLL</span><span class="sxs-lookup"><span data-stu-id="5606a-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5606a-141"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5606a-141"><dt>Activeds.dll</dt></span></span> </dl>   |
| <span data-ttu-id="5606a-142">IID</span><span class="sxs-lookup"><span data-stu-id="5606a-142">IID</span></span><br/>                      | <span data-ttu-id="5606a-143">IID \_ IADsPrintJobOperations 定義為32FB6780-1ED0-11CF-A988-00AA006BC149</span><span class="sxs-lookup"><span data-stu-id="5606a-143">IID\_IADsPrintJobOperations is defined as 32FB6780-1ED0-11CF-A988-00AA006BC149</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5606a-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5606a-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5606a-145">**IADsPrintJob**</span><span class="sxs-lookup"><span data-stu-id="5606a-145">**IADsPrintJob**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsprintjob)
</dt> <dt>

[<span data-ttu-id="5606a-146">**IADsPrintJobOperations**</span><span class="sxs-lookup"><span data-stu-id="5606a-146">**IADsPrintJobOperations**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations)
</dt> <dt>

[<span data-ttu-id="5606a-147">**IADsPrintQueue**</span><span class="sxs-lookup"><span data-stu-id="5606a-147">**IADsPrintQueue**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)
</dt> <dt>

[<span data-ttu-id="5606a-148">**ADSI 列印工作狀態常數**</span><span class="sxs-lookup"><span data-stu-id="5606a-148">**ADSI Print Job Status Constants**</span></span>](adsi-print-job-status-constants.md)
</dt> </dl>

 

 





