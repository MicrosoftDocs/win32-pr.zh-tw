---
title: 'IADsPrintQueueOperations 屬性方法 (Iads .h) '
description: IADsPrintQueueOperations 介面的屬性方法會讀取並寫入下列清單中列出的屬性。 如需屬性方法的詳細資訊，請參閱介面屬性方法。
ms.assetid: a4e6bac5-5d52-4492-b48e-f051fec6158c
ms.tgt_platform: multiple
keywords:
- IADsPrintQueueOperations 屬性方法 ADSI
topic_type:
- apiref
api_name:
- IADsPrintQueueOperations Property Methods
- IADsPrintQueueOperations.Status
- IADsPrintQueueOperations.get_Name
- IADsPrintQueueOperations.put_Name
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8af7aef94dd9453af690f0c5d83b1e978d3b058
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934812"
---
# <a name="iadsprintqueueoperations-property-methods"></a><span data-ttu-id="11903-105">IADsPrintQueueOperations 屬性方法</span><span class="sxs-lookup"><span data-stu-id="11903-105">IADsPrintQueueOperations Property Methods</span></span>

<span data-ttu-id="11903-106">[**IADsPrintQueueOperations**](/windows/desktop/api/Iads/nn-iads-iadsprintqueueoperations)介面的屬性方法會讀取並寫入下列清單中列出的屬性。</span><span class="sxs-lookup"><span data-stu-id="11903-106">The property methods of the [**IADsPrintQueueOperations**](/windows/desktop/api/Iads/nn-iads-iadsprintqueueoperations) interface read and write the properties listed in the following list.</span></span> <span data-ttu-id="11903-107">如需屬性方法的詳細資訊，請參閱 [介面屬性方法](interface-property-methods.md)。</span><span class="sxs-lookup"><span data-stu-id="11903-107">For more information about property methods, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="11903-108">屬性</span><span class="sxs-lookup"><span data-stu-id="11903-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="11903-109">**狀態**</span><span class="sxs-lookup"><span data-stu-id="11903-109">**Status**</span></span>
<span data-ttu-id="11903-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="11903-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="11903-111">列印佇列作業的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="11903-111">Current status of the print queue operations.</span></span> <span data-ttu-id="11903-112">有效的狀態碼值會列在下列清單中。</span><span class="sxs-lookup"><span data-stu-id="11903-112">The valid status code values are listed in the following list.</span></span>

<dt>

<span id="ADS_PRINTER_PAUSED"></span><span id="ads_printer_paused"></span>

<span data-ttu-id="11903-113">**廣告 \_已 \_ 暫停印表機** (0x00000001) </span><span class="sxs-lookup"><span data-stu-id="11903-113">**ADS\_PRINTER\_PAUSED** (0x00000001)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PENDING_DELETION"></span><span id="ads_printer_pending_deletion"></span>

<span data-ttu-id="11903-114">**廣告 \_印表機 \_ 暫止 \_ 刪除** (0x00000002) </span><span class="sxs-lookup"><span data-stu-id="11903-114">**ADS\_PRINTER\_PENDING\_DELETION** (0x00000002)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_ERROR"></span><span id="ads_printer_error"></span>

<span data-ttu-id="11903-115">**廣告 \_印表機 \_ 錯誤** (0x00000003) </span><span class="sxs-lookup"><span data-stu-id="11903-115">**ADS\_PRINTER\_ERROR** (0x00000003)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PAPER_JAM"></span><span id="ads_printer_paper_jam"></span>

<span data-ttu-id="11903-116">**廣告 \_印表機 \_ 紙 \_ 卡** (0x00000004) </span><span class="sxs-lookup"><span data-stu-id="11903-116">**ADS\_PRINTER\_PAPER\_JAM** (0x00000004)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PAPER_OUT"></span><span id="ads_printer_paper_out"></span>

<span data-ttu-id="11903-117">**廣告 \_印表機 \_ 紙 \_** (0x00000005) </span><span class="sxs-lookup"><span data-stu-id="11903-117">**ADS\_PRINTER\_PAPER\_OUT** (0x00000005)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_MANUAL_FEED"></span><span id="ads_printer_manual_feed"></span>

<span data-ttu-id="11903-118">**廣告 \_印表機 \_ 手動 \_ 饋送** (0x00000006) </span><span class="sxs-lookup"><span data-stu-id="11903-118">**ADS\_PRINTER\_MANUAL\_FEED** (0x00000006)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PAPER_PROBLEM"></span><span id="ads_printer_paper_problem"></span>

<span data-ttu-id="11903-119">**廣告 \_印表機 \_ 紙張 \_ 問題** (0x00000007) </span><span class="sxs-lookup"><span data-stu-id="11903-119">**ADS\_PRINTER\_PAPER\_PROBLEM** (0x00000007)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_OFFLINE"></span><span id="ads_printer_offline"></span>

<span data-ttu-id="11903-120">**廣告 \_印表機 \_ 離線** (0x00000008) </span><span class="sxs-lookup"><span data-stu-id="11903-120">**ADS\_PRINTER\_OFFLINE** (0x00000008)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_IO_ACTIVE"></span><span id="ads_printer_io_active"></span>

<span data-ttu-id="11903-121">**廣告 \_印表機 \_ IO \_ 主動** (0x00000100) </span><span class="sxs-lookup"><span data-stu-id="11903-121">**ADS\_PRINTER\_IO\_ACTIVE** (0x00000100)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_BUSY"></span><span id="ads_printer_busy"></span>

<span data-ttu-id="11903-122">**廣告 \_印表機 \_ 忙碌** (0x00000200) </span><span class="sxs-lookup"><span data-stu-id="11903-122">**ADS\_PRINTER\_BUSY** (0x00000200)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PRINTING"></span><span id="ads_printer_printing"></span>

<span data-ttu-id="11903-123">**廣告 \_印表機 \_ 列印** (0x00000400) </span><span class="sxs-lookup"><span data-stu-id="11903-123">**ADS\_PRINTER\_PRINTING** (0x00000400)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_OUTPUT_BIN_FULL"></span><span id="ads_printer_output_bin_full"></span>

<span data-ttu-id="11903-124">**廣告 \_印表機 \_ 輸出 \_ BIN \_ FULL** (0x00000800) </span><span class="sxs-lookup"><span data-stu-id="11903-124">**ADS\_PRINTER\_OUTPUT\_BIN\_FULL** (0x00000800)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_NOT_AVAILABLE"></span><span id="ads_printer_not_available"></span>

<span data-ttu-id="11903-125">**廣告 \_印表機 \_ 無法 \_ 使用** (0x00001000) </span><span class="sxs-lookup"><span data-stu-id="11903-125">**ADS\_PRINTER\_NOT\_AVAILABLE** (0x00001000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_WAITING"></span><span id="ads_printer_waiting"></span>

<span data-ttu-id="11903-126">**廣告 \_印表機 \_ 正在等候** (0x00002000) </span><span class="sxs-lookup"><span data-stu-id="11903-126">**ADS\_PRINTER\_WAITING** (0x00002000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PROCESSING"></span><span id="ads_printer_processing"></span>

<span data-ttu-id="11903-127">**廣告 \_印表機 \_ 處理** (0x00004000) </span><span class="sxs-lookup"><span data-stu-id="11903-127">**ADS\_PRINTER\_PROCESSING** (0x00004000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_INITIALIZING"></span><span id="ads_printer_initializing"></span>

<span data-ttu-id="11903-128">**廣告 \_ (\_** 0x00008000) 的印表機初始化</span><span class="sxs-lookup"><span data-stu-id="11903-128">**ADS\_PRINTER\_INITIALIZING** (0x00008000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_WARMING_UP"></span><span id="ads_printer_warming_up"></span>

<span data-ttu-id="11903-129">**廣告 \_印表機 \_ 預熱 \_** (0x00010000) </span><span class="sxs-lookup"><span data-stu-id="11903-129">**ADS\_PRINTER\_WARMING\_UP** (0x00010000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_TONER_LOW"></span><span id="ads_printer_toner_low"></span>

<span data-ttu-id="11903-130">**廣告 \_印表機 \_ 墨粉 \_ 低** (0x00020000) </span><span class="sxs-lookup"><span data-stu-id="11903-130">**ADS\_PRINTER\_TONER\_LOW** (0x00020000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_NO_TONER"></span><span id="ads_printer_no_toner"></span>

<span data-ttu-id="11903-131">**廣告 \_印表機 \_ 沒有 \_ 碳粉** (0x00040000) </span><span class="sxs-lookup"><span data-stu-id="11903-131">**ADS\_PRINTER\_NO\_TONER** (0x00040000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PAGE_PUNT"></span><span id="ads_printer_page_punt"></span>

<span data-ttu-id="11903-132">**廣告 \_印表機 \_ 頁面 \_** (0x00080000) </span><span class="sxs-lookup"><span data-stu-id="11903-132">**ADS\_PRINTER\_PAGE\_PUNT** (0x00080000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_USER_INTERVENTION"></span><span id="ads_printer_user_intervention"></span>

<span data-ttu-id="11903-133">**廣告 \_ (0x00100000) 的印表機 \_ 使用者 \_ 介入**</span><span class="sxs-lookup"><span data-stu-id="11903-133">**ADS\_PRINTER\_USER\_INTERVENTION** (0x00100000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_OUT_OF_MEMORY"></span><span id="ads_printer_out_of_memory"></span>

<span data-ttu-id="11903-134">**廣告 \_印表機 \_ \_ \_ 記憶體** (0x00200000) </span><span class="sxs-lookup"><span data-stu-id="11903-134">**ADS\_PRINTER\_OUT\_OF\_MEMORY** (0x00200000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_DOOR_OPEN"></span><span id="ads_printer_door_open"></span>

<span data-ttu-id="11903-135">**廣告 \_印表機 \_ 門 \_ 開啟** (0x00400000) </span><span class="sxs-lookup"><span data-stu-id="11903-135">**ADS\_PRINTER\_DOOR\_OPEN** (0x00400000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_SERVER_UNKNOWN"></span><span id="ads_printer_server_unknown"></span>

<span data-ttu-id="11903-136">**廣告 \_印表機 \_ 伺服器 \_ 不明** (0x00800000) </span><span class="sxs-lookup"><span data-stu-id="11903-136">**ADS\_PRINTER\_SERVER\_UNKNOWN** (0x00800000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_POWER_SAVE"></span><span id="ads_printer_power_save"></span>

<span data-ttu-id="11903-137">**廣告 \_印表機 \_ 電源 \_ 節省** (0x01000000) </span><span class="sxs-lookup"><span data-stu-id="11903-137">**ADS\_PRINTER\_POWER\_SAVE** (0x01000000)</span></span>


</dt> <dd></dd> </dl> <dt>

<span data-ttu-id="11903-138">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="11903-138">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="11903-139">編寫資料類型的腳本： **LONG**</span><span class="sxs-lookup"><span data-stu-id="11903-139">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Name(
  [out] LONG* pbstrName
);
HRESULT put_Name(
  [in] LONG bstrName
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="11903-140">範例</span><span class="sxs-lookup"><span data-stu-id="11903-140">Examples</span></span>

<span data-ttu-id="11903-141">下列 Visual Basic 程式碼範例會驗證印表機是否已卡住。</span><span class="sxs-lookup"><span data-stu-id="11903-141">The following Visual Basic code example verifies that a printer is jammed.</span></span>


```VB
Dim pqo As IADsPrintQueueOperations
Set pqo = GetObject("WinNT://aMachine/aPrinter")
If pqo.Status = ADS_PRINTER_PAPER_JAM Then
MsgBox "Your printer is jammed."
End If
```



<span data-ttu-id="11903-142">下列 c + + 程式碼範例會驗證印表機是否已卡住。</span><span class="sxs-lookup"><span data-stu-id="11903-142">The following C++ code example verifies that a printer is jammed.</span></span>


```C++
IADsPrintQueueOperations *pqo;
HRESULT hr = ADsGetObject(L"WinNT://aMachine/aPrinter",
IID_IADsPrintQueueOperations,
(void**)&pqo)
long status;
hr = pqo->get_Status(&status);
if(status = ADS_PRINTER_PAPER_JAM) {
printf("Your printer is jammed.\n");
}
hr = pqo->Release();
```



## <a name="requirements"></a><span data-ttu-id="11903-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="11903-143">Requirements</span></span>



| <span data-ttu-id="11903-144">需求</span><span class="sxs-lookup"><span data-stu-id="11903-144">Requirement</span></span> | <span data-ttu-id="11903-145">值</span><span class="sxs-lookup"><span data-stu-id="11903-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="11903-146">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="11903-146">Minimum supported client</span></span><br/> | <span data-ttu-id="11903-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="11903-147">Windows Vista</span></span><br/>                                                                    |
| <span data-ttu-id="11903-148">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="11903-148">Minimum supported server</span></span><br/> | <span data-ttu-id="11903-149">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="11903-149">Windows Server 2008</span></span><br/>                                                              |
| <span data-ttu-id="11903-150">標頭</span><span class="sxs-lookup"><span data-stu-id="11903-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="11903-151"><dt>Iads。h</dt></span><span class="sxs-lookup"><span data-stu-id="11903-151"><dt>Iads.h</dt></span></span> </dl>           |
| <span data-ttu-id="11903-152">DLL</span><span class="sxs-lookup"><span data-stu-id="11903-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11903-153"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11903-153"><dt>Activeds.dll</dt></span></span> </dl>     |
| <span data-ttu-id="11903-154">IID</span><span class="sxs-lookup"><span data-stu-id="11903-154">IID</span></span><br/>                      | <span data-ttu-id="11903-155">IID \_ IADsPrintQueueOperations 定義為124BE5C0-156E-11CF-A986-00AA006BC149</span><span class="sxs-lookup"><span data-stu-id="11903-155">IID\_IADsPrintQueueOperations is defined as 124BE5C0-156E-11CF-A986-00AA006BC149</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="11903-156">另請參閱</span><span class="sxs-lookup"><span data-stu-id="11903-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11903-157">**IADsPrintQueue**</span><span class="sxs-lookup"><span data-stu-id="11903-157">**IADsPrintQueue**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)
</dt> <dt>

[<span data-ttu-id="11903-158">**IADsPrintQueueOperations**</span><span class="sxs-lookup"><span data-stu-id="11903-158">**IADsPrintQueueOperations**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsprintqueueoperations)
</dt> </dl>

 

 





