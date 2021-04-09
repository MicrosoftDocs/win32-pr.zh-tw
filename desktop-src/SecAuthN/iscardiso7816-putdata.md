---
description: PutData 方法會建立應用程式協定資料單位 (APDU) 命令，此命令會根據選取的檔案，儲存單一基本資料物件或包含在結構化資料物件中的資料物件集。
ms.assetid: 6bad45fb-b202-4eb0-b2f4-fe0a6af64330
title: 'ISCardISO7816：:P utData 方法 (Scardssp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.PutData
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 3c15239943a92067011011b6cedca191fa78c3a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850880"
---
# <a name="iscardiso7816putdata-method"></a><span data-ttu-id="af6ea-103">ISCardISO7816：:P utData 方法</span><span class="sxs-lookup"><span data-stu-id="af6ea-103">ISCardISO7816::PutData method</span></span>

<span data-ttu-id="af6ea-104">\[**PutData** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="af6ea-104">\[The **PutData** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="af6ea-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="af6ea-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="af6ea-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="af6ea-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="af6ea-107">**PutData** 方法會建立 [*應用程式協定資料單位*](../secgloss/a-gly.md) (APDU) 命令，此命令會根據選取的檔案，儲存單一基本資料物件或包含在結構化資料物件中的資料物件集。</span><span class="sxs-lookup"><span data-stu-id="af6ea-107">The **PutData** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that stores a single primitive data object or the set of data objects contained in a constructed data object, depending on the file selected.</span></span>

<span data-ttu-id="af6ea-108">物件的儲存方式 (寫入一次和（或）更新和/或附加) 取決於資料物件的定義或本質。</span><span class="sxs-lookup"><span data-stu-id="af6ea-108">How the objects are stored (writing once and/or updating and/or appending) depends on the definition or the nature of the data objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="af6ea-109">語法</span><span class="sxs-lookup"><span data-stu-id="af6ea-109">Syntax</span></span>


```C++
HRESULT PutData(
  [in]      BYTE         byP1,
  [in]      BYTE         byP2,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="af6ea-110">參數</span><span class="sxs-lookup"><span data-stu-id="af6ea-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af6ea-111">*byP1* \[在\]</span><span class="sxs-lookup"><span data-stu-id="af6ea-111">*byP1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af6ea-112">P1-P2 的編碼。</span><span class="sxs-lookup"><span data-stu-id="af6ea-112">Coding of P1-P2.</span></span>



| <span data-ttu-id="af6ea-113">值</span><span class="sxs-lookup"><span data-stu-id="af6ea-113">Value</span></span>                                                                                  | <span data-ttu-id="af6ea-114">意義</span><span class="sxs-lookup"><span data-stu-id="af6ea-114">Meaning</span></span>                                          |
|----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="af6ea-115"><dt>0000-003F</dt></span><span class="sxs-lookup"><span data-stu-id="af6ea-115"><dt>0000 - 003F</dt></span></span> </dl> | <span data-ttu-id="af6ea-116">RFU</span><span class="sxs-lookup"><span data-stu-id="af6ea-116">RFU</span></span><br/>                                   |
| <dl> <span data-ttu-id="af6ea-117"><dt>0040-00FF</dt></span><span class="sxs-lookup"><span data-stu-id="af6ea-117"><dt>0040 - 00FF</dt></span></span> </dl> | <span data-ttu-id="af6ea-118">BER-TLV 標記 (1 位元組) 在 P2 中</span><span class="sxs-lookup"><span data-stu-id="af6ea-118">BER-TLV tag (1 byte) in P2</span></span><br/>            |
| <dl> <span data-ttu-id="af6ea-119"><dt>0100-01FF</dt></span><span class="sxs-lookup"><span data-stu-id="af6ea-119"><dt>0100 - 01FF</dt></span></span> </dl> | <span data-ttu-id="af6ea-120">應用程式資料 (專屬編碼) </span><span class="sxs-lookup"><span data-stu-id="af6ea-120">Application data (proprietary coding)</span></span><br/> |
| <dl> <span data-ttu-id="af6ea-121"><dt>0200-02FF</dt></span><span class="sxs-lookup"><span data-stu-id="af6ea-121"><dt>0200 - 02FF</dt></span></span> </dl> | <span data-ttu-id="af6ea-122">P2 中的簡單 TLV 標記</span><span class="sxs-lookup"><span data-stu-id="af6ea-122">SIMPLE-TLV tag in P2</span></span><br/>                  |
| <dl> <span data-ttu-id="af6ea-123"><dt>0300-03FF</dt></span><span class="sxs-lookup"><span data-stu-id="af6ea-123"><dt>0300 - 03FF</dt></span></span> </dl> | <span data-ttu-id="af6ea-124">RFU</span><span class="sxs-lookup"><span data-stu-id="af6ea-124">RFU</span></span><br/>                                   |
| <dl> <span data-ttu-id="af6ea-125"><dt>0400 - 04FF</dt></span><span class="sxs-lookup"><span data-stu-id="af6ea-125"><dt>0400 - 04FF</dt></span></span> </dl> | <span data-ttu-id="af6ea-126">BER-TLV 標記 (2 個位元組) 在 P1-P2 中</span><span class="sxs-lookup"><span data-stu-id="af6ea-126">BER-TLV tag (2 bytes) in P1-P2</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="af6ea-127">*byP2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="af6ea-127">*byP2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af6ea-128">P1-P2 的編碼。</span><span class="sxs-lookup"><span data-stu-id="af6ea-128">Coding of P1-P2.</span></span>



| <span data-ttu-id="af6ea-129">值</span><span class="sxs-lookup"><span data-stu-id="af6ea-129">Value</span></span>                                                                                  | <span data-ttu-id="af6ea-130">意義</span><span class="sxs-lookup"><span data-stu-id="af6ea-130">Meaning</span></span>                                          |
|----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="af6ea-131"><dt>0000-003F</dt></span><span class="sxs-lookup"><span data-stu-id="af6ea-131"><dt>0000 - 003F</dt></span></span> </dl> | <span data-ttu-id="af6ea-132">RFU</span><span class="sxs-lookup"><span data-stu-id="af6ea-132">RFU</span></span><br/>                                   |
| <dl> <span data-ttu-id="af6ea-133"><dt>0040-00FF</dt></span><span class="sxs-lookup"><span data-stu-id="af6ea-133"><dt>0040 - 00FF</dt></span></span> </dl> | <span data-ttu-id="af6ea-134">BER-TLV 標記 (1 位元組) 在 P2 中</span><span class="sxs-lookup"><span data-stu-id="af6ea-134">BER-TLV tag (1 byte) in P2</span></span><br/>            |
| <dl> <span data-ttu-id="af6ea-135"><dt>0100-01FF</dt></span><span class="sxs-lookup"><span data-stu-id="af6ea-135"><dt>0100 - 01FF</dt></span></span> </dl> | <span data-ttu-id="af6ea-136">應用程式資料 (專屬編碼) </span><span class="sxs-lookup"><span data-stu-id="af6ea-136">Application data (proprietary coding)</span></span><br/> |
| <dl> <span data-ttu-id="af6ea-137"><dt>0200-02FF</dt></span><span class="sxs-lookup"><span data-stu-id="af6ea-137"><dt>0200 - 02FF</dt></span></span> </dl> | <span data-ttu-id="af6ea-138">P2 中的簡單 TLV 標記</span><span class="sxs-lookup"><span data-stu-id="af6ea-138">SIMPLE-TLV tag in P2</span></span><br/>                  |
| <dl> <span data-ttu-id="af6ea-139"><dt>0300-03FF</dt></span><span class="sxs-lookup"><span data-stu-id="af6ea-139"><dt>0300 - 03FF</dt></span></span> </dl> | <span data-ttu-id="af6ea-140">RFU</span><span class="sxs-lookup"><span data-stu-id="af6ea-140">RFU</span></span><br/>                                   |
| <dl> <span data-ttu-id="af6ea-141"><dt>0400 - 04FF</dt></span><span class="sxs-lookup"><span data-stu-id="af6ea-141"><dt>0400 - 04FF</dt></span></span> </dl> | <span data-ttu-id="af6ea-142">BER-TLV 標記 (2 個位元組) 在 P1-P2 中</span><span class="sxs-lookup"><span data-stu-id="af6ea-142">BER-TLV tag (2 bytes) in P1-P2</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="af6ea-143">*.pdata* \[在\]</span><span class="sxs-lookup"><span data-stu-id="af6ea-143">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af6ea-144">位元組緩衝區的指標，其中包含要寫入的參數和資料。</span><span class="sxs-lookup"><span data-stu-id="af6ea-144">Pointer to a byte buffer that contains the parameters and data to be written.</span></span>

</dd> <dt>

<span data-ttu-id="af6ea-145">*ppCmd* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="af6ea-145">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="af6ea-146">在輸入時， [**ISCardCmd**](iscardcmd.md) 介面物件的指標或 **Null**。</span><span class="sxs-lookup"><span data-stu-id="af6ea-146">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="af6ea-147">傳回時，它會填入由這項作業所建立的 APDU 命令。</span><span class="sxs-lookup"><span data-stu-id="af6ea-147">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="af6ea-148">如果 *ppCmd* 設定為 **Null**，就會在內部建立 [*智慧卡*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) 物件，並使用 *ppCmd* 指標來傳回。</span><span class="sxs-lookup"><span data-stu-id="af6ea-148">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned using the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af6ea-149">傳回值</span><span class="sxs-lookup"><span data-stu-id="af6ea-149">Return value</span></span>

<span data-ttu-id="af6ea-150">方法會傳回下列其中一個可能的值。</span><span class="sxs-lookup"><span data-stu-id="af6ea-150">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="af6ea-151">傳回碼</span><span class="sxs-lookup"><span data-stu-id="af6ea-151">Return code</span></span>                                                                                   | <span data-ttu-id="af6ea-152">Description</span><span class="sxs-lookup"><span data-stu-id="af6ea-152">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="af6ea-153"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="af6ea-153"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="af6ea-154">作業順利完成。</span><span class="sxs-lookup"><span data-stu-id="af6ea-154">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="af6ea-155"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="af6ea-155"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="af6ea-156">無效的參數。</span><span class="sxs-lookup"><span data-stu-id="af6ea-156">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="af6ea-157"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="af6ea-157"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="af6ea-158">傳入了錯誤指標。</span><span class="sxs-lookup"><span data-stu-id="af6ea-158">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="af6ea-159"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="af6ea-159"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="af6ea-160">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="af6ea-160">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="af6ea-161">備註</span><span class="sxs-lookup"><span data-stu-id="af6ea-161">Remarks</span></span>

<span data-ttu-id="af6ea-162">只有在安全性狀態符合函式 [*內容*](../secgloss/c-gly.md) 中的應用程式所定義的安全性條件時，才能執行此命令。</span><span class="sxs-lookup"><span data-stu-id="af6ea-162">The command can be performed only if the security status satisfies the security conditions defined by the application within the [*context*](../secgloss/c-gly.md) for the function.</span></span>

<dl> <dt>

<span data-ttu-id="af6ea-163"><span id="Store_Application_Data"></span><span id="store_application_data"></span><span id="STORE_APPLICATION_DATA"></span>儲存應用程式資料</span><span class="sxs-lookup"><span data-stu-id="af6ea-163"><span id="Store_Application_Data"></span><span id="store_application_data"></span><span id="STORE_APPLICATION_DATA"></span>Store Application Data</span></span>
</dt> <dd>

<span data-ttu-id="af6ea-164">當 P1-P2 的值位於0100至01FF 的範圍內時，P1-P2 的值應該是針對卡片內部測試所保留的識別碼，以及在指定的應用程式內容中有意義的專屬服務。</span><span class="sxs-lookup"><span data-stu-id="af6ea-164">When the value of P1-P2 lies in the range from 0100 to 01FF, the value of P1-P2 shall be an identifier reserved for card internal tests and for proprietary services meaningful within a given application context.</span></span>

</dd> <dt>

<span data-ttu-id="af6ea-165"><span id="Store_Data_Objects"></span><span id="store_data_objects"></span><span id="STORE_DATA_OBJECTS"></span>儲存資料物件</span><span class="sxs-lookup"><span data-stu-id="af6ea-165"><span id="Store_Data_Objects"></span><span id="store_data_objects"></span><span id="STORE_DATA_OBJECTS"></span>Store Data Objects</span></span>
</dt> <dd>

<span data-ttu-id="af6ea-166">當值 P1-P2 位於0040至00FF 的範圍內時，P2 的值應該是單一位元組上的 BER TLV 標記。</span><span class="sxs-lookup"><span data-stu-id="af6ea-166">When the value P1-P2 lies in the range from 0040 to 00FF, the value of P2 shall be a BER-TLV tag on a single byte.</span></span> <span data-ttu-id="af6ea-167">00FF 的值是保留的，表示資料欄位攜帶 BER 的 TLV 資料物件。</span><span class="sxs-lookup"><span data-stu-id="af6ea-167">The value of 00FF is reserved for indicating that the data field carries BER-TLV data objects.</span></span>

<span data-ttu-id="af6ea-168">當 P1-P2 的值位於0200至02FF 的範圍時，P2 的值應該是簡單的 TLV 標記。</span><span class="sxs-lookup"><span data-stu-id="af6ea-168">When the value of P1-P2 lies in the range 0200 to 02FF, the value of P2 shall be a SIMPLE-TLV tag.</span></span> <span data-ttu-id="af6ea-169">值0200為 RFU。</span><span class="sxs-lookup"><span data-stu-id="af6ea-169">The value 0200 is RFU.</span></span> <span data-ttu-id="af6ea-170">值02FF 會保留，表示資料欄位會攜帶簡單的 TLV 資料物件。</span><span class="sxs-lookup"><span data-stu-id="af6ea-170">The value 02FF is reserved for indicating that the data field carries SIMPLE-TLV data objects.</span></span>

<span data-ttu-id="af6ea-171">當 P1-P2 的值位於4000至 FFFF 的範圍內時，P1-P2 的值應該是兩個位元組上的 BER TLV 標記。</span><span class="sxs-lookup"><span data-stu-id="af6ea-171">When the value of P1-P2 lies in the range from 4000 to FFFF, the value of P1-P2 shall be a BER-TLV tag on two bytes.</span></span> <span data-ttu-id="af6ea-172">RFU 的值為4000至 FFFF。</span><span class="sxs-lookup"><span data-stu-id="af6ea-172">The values 4000 to FFFF are RFU.</span></span>

<span data-ttu-id="af6ea-173">當提供基本資料物件時，命令訊息的資料欄位應該會包含對應基本資料物件的值。</span><span class="sxs-lookup"><span data-stu-id="af6ea-173">When a primitive data object is provided, the data field of the command message shall contain the value of the corresponding primitive data object.</span></span>

<span data-ttu-id="af6ea-174">當提供了結構化資料物件時，命令訊息的資料欄位應該會包含已建立的資料物件值 (也就是資料物件，包括其標記、長度和值) 。</span><span class="sxs-lookup"><span data-stu-id="af6ea-174">When a constructed data object is provided, the data field of the command message shall contain the value of the constructed data object (that is, data objects including their tag, length, and value).</span></span>

</dd> </dl>

<span data-ttu-id="af6ea-175">如需此介面所提供的所有方法清單，請參閱 [**ISCardISO7816**](iscardiso7816.md)。</span><span class="sxs-lookup"><span data-stu-id="af6ea-175">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="af6ea-176">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回智慧卡的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="af6ea-176">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="af6ea-177">如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="af6ea-177">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="af6ea-178">規格需求</span><span class="sxs-lookup"><span data-stu-id="af6ea-178">Requirements</span></span>



| <span data-ttu-id="af6ea-179">需求</span><span class="sxs-lookup"><span data-stu-id="af6ea-179">Requirement</span></span> | <span data-ttu-id="af6ea-180">值</span><span class="sxs-lookup"><span data-stu-id="af6ea-180">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="af6ea-181">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="af6ea-181">Minimum supported client</span></span><br/> | <span data-ttu-id="af6ea-182">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="af6ea-182">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="af6ea-183">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="af6ea-183">Minimum supported server</span></span><br/> | <span data-ttu-id="af6ea-184">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="af6ea-184">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="af6ea-185">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="af6ea-185">End of client support</span></span><br/>    | <span data-ttu-id="af6ea-186">Windows XP</span><span class="sxs-lookup"><span data-stu-id="af6ea-186">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="af6ea-187">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="af6ea-187">End of server support</span></span><br/>    | <span data-ttu-id="af6ea-188">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="af6ea-188">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="af6ea-189">標頭</span><span class="sxs-lookup"><span data-stu-id="af6ea-189">Header</span></span><br/>                   | <dl> <span data-ttu-id="af6ea-190"><dt>Scardssp。h</dt></span><span class="sxs-lookup"><span data-stu-id="af6ea-190"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="af6ea-191">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="af6ea-191">Type library</span></span><br/>             | <dl> <span data-ttu-id="af6ea-192"><dt>Scardsrv .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="af6ea-192"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="af6ea-193">DLL</span><span class="sxs-lookup"><span data-stu-id="af6ea-193">DLL</span></span><br/>                      | <dl> <span data-ttu-id="af6ea-194"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="af6ea-194"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="af6ea-195">IID</span><span class="sxs-lookup"><span data-stu-id="af6ea-195">IID</span></span><br/>                      | <span data-ttu-id="af6ea-196">IID \_ ISCardISO7816 定義為53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="af6ea-196">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="af6ea-197">另請參閱</span><span class="sxs-lookup"><span data-stu-id="af6ea-197">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af6ea-198">**GetData**</span><span class="sxs-lookup"><span data-stu-id="af6ea-198">**GetData**</span></span>](iscardiso7816-getdata.md)
</dt> <dt>

[<span data-ttu-id="af6ea-199">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="af6ea-199">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> </dl>

 

 
