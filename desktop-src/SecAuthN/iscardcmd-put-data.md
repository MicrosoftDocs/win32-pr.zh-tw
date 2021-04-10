---
description: 設定應用程式協定資料單位中的資料欄位 (APDU) 。
ms.assetid: 4508e00c-2b1d-4be5-b3a7-083b367a2158
title: 'ISCardCmd：:p ut_Data 方法 (Scarddat .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_Data
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 58c1fa7d709eff1ed0618f52a83825f5110c4457
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114144"
---
# <a name="iscardcmdput_data-method"></a><span data-ttu-id="f0aab-103">ISCardCmd：:p 的 ui \_ 資料方法</span><span class="sxs-lookup"><span data-stu-id="f0aab-103">ISCardCmd::put\_Data method</span></span>

<span data-ttu-id="f0aab-104">\[**Put \_ 資料** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="f0aab-104">\[The **put\_Data** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="f0aab-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="f0aab-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="f0aab-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="f0aab-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="f0aab-107">**Put \_ 資料** 方法會將 [*應用程式協定資料單位*](../secgloss/a-gly.md)中的資料欄位設定 (APDU) 。</span><span class="sxs-lookup"><span data-stu-id="f0aab-107">The **put\_Data** method sets the data field in the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="f0aab-108">語法</span><span class="sxs-lookup"><span data-stu-id="f0aab-108">Syntax</span></span>


```C++
HRESULT put_Data(
  [in] LPBYTEBUFFER pData
);
```



## <a name="parameters"></a><span data-ttu-id="f0aab-109">參數</span><span class="sxs-lookup"><span data-stu-id="f0aab-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0aab-110">*.pdata* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f0aab-110">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0aab-111">位元組緩衝區物件的指標， (**IStream**) 要複製到 [APDU 資料] 欄位中。</span><span class="sxs-lookup"><span data-stu-id="f0aab-111">Pointer to the byte buffer object (**IStream**) to be copied into the APDU data field.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0aab-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="f0aab-112">Return value</span></span>

<span data-ttu-id="f0aab-113">方法會傳回下列其中一個可能的值。</span><span class="sxs-lookup"><span data-stu-id="f0aab-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="f0aab-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="f0aab-114">Return code</span></span>                                                                                   | <span data-ttu-id="f0aab-115">Description</span><span class="sxs-lookup"><span data-stu-id="f0aab-115">Description</span></span>                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="f0aab-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="f0aab-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="f0aab-117">作業順利完成。</span><span class="sxs-lookup"><span data-stu-id="f0aab-117">Operation completed successfully.</span></span><br/>    |
| <dl> <span data-ttu-id="f0aab-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="f0aab-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="f0aab-119">*.Pdata* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="f0aab-119">The *pData* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="f0aab-120"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="f0aab-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="f0aab-121">在 *.pdata* 中傳遞了錯誤指標。</span><span class="sxs-lookup"><span data-stu-id="f0aab-121">A bad pointer was passed in *pData*.</span></span><br/> |
| <dl> <span data-ttu-id="f0aab-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="f0aab-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="f0aab-123">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="f0aab-123">Out of memory.</span></span><br/>                       |



 

## <a name="remarks"></a><span data-ttu-id="f0aab-124">備註</span><span class="sxs-lookup"><span data-stu-id="f0aab-124">Remarks</span></span>

<span data-ttu-id="f0aab-125">當您設定訊息的新資料部分時，資料欄位的長度會計算並儲存在 APDU 的 P3 參數中。</span><span class="sxs-lookup"><span data-stu-id="f0aab-125">When you set a new data portion of the message, the length of the data field is calculated and stored in the P3 parameter of the APDU.</span></span> <span data-ttu-id="f0aab-126">若要取出資料欄位的長度，請呼叫 [**get \_ P3**](iscardcmd-get-p3.md)。</span><span class="sxs-lookup"><span data-stu-id="f0aab-126">To retrieve the length of the data field, call [**get\_P3**](iscardcmd-get-p3.md).</span></span>

<span data-ttu-id="f0aab-127">若要從 APDU 取出資料欄位，請呼叫 [**取得 \_ 資料**](iscardcmd-get-data.md)。</span><span class="sxs-lookup"><span data-stu-id="f0aab-127">To retrieve the data field from the APDU, call [**get\_Data**](iscardcmd-get-data.md).</span></span>

## <a name="examples"></a><span data-ttu-id="f0aab-128">範例</span><span class="sxs-lookup"><span data-stu-id="f0aab-128">Examples</span></span>

<span data-ttu-id="f0aab-129">下列範例顯示如何在 [*應用程式協定資料單位*](../secgloss/a-gly.md) 中設定資料欄位， (APDU) 。</span><span class="sxs-lookup"><span data-stu-id="f0aab-129">The following example shows how to set the data field in the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="f0aab-130">此範例假設 pIByteData 是 [**IByteBuffer**](ibytebuffer.md) 介面實例的有效指標，而且該 PISCardCmd 是 [**ISCardCmd**](iscardcmd.md) 介面實例的有效指標。</span><span class="sxs-lookup"><span data-stu-id="f0aab-130">The example assumes that pIByteData is a valid pointer to an instance of the [**IByteBuffer**](ibytebuffer.md) interface, and that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
HRESULT    hr;

// pIByteData is a pointer to an instance of IByteBuffer.
// Set the data.
hr = pISCardCmd->put_Data(pIByteData);
if (FAILED(hr)) 
{
    printf("Failed put_Data.\n");
    // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="f0aab-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="f0aab-131">Requirements</span></span>



| <span data-ttu-id="f0aab-132">需求</span><span class="sxs-lookup"><span data-stu-id="f0aab-132">Requirement</span></span> | <span data-ttu-id="f0aab-133">值</span><span class="sxs-lookup"><span data-stu-id="f0aab-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f0aab-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f0aab-134">Minimum supported client</span></span><br/> | <span data-ttu-id="f0aab-135">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f0aab-135">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="f0aab-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f0aab-136">Minimum supported server</span></span><br/> | <span data-ttu-id="f0aab-137">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f0aab-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f0aab-138">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="f0aab-138">End of client support</span></span><br/>    | <span data-ttu-id="f0aab-139">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f0aab-139">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="f0aab-140">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="f0aab-140">End of server support</span></span><br/>    | <span data-ttu-id="f0aab-141">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f0aab-141">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="f0aab-142">標頭</span><span class="sxs-lookup"><span data-stu-id="f0aab-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0aab-143"><dt>Scarddat。h</dt></span><span class="sxs-lookup"><span data-stu-id="f0aab-143"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="f0aab-144">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="f0aab-144">Type library</span></span><br/>             | <dl> <span data-ttu-id="f0aab-145"><dt>Scarddat .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f0aab-145"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f0aab-146">DLL</span><span class="sxs-lookup"><span data-stu-id="f0aab-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f0aab-147"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f0aab-147"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="f0aab-148">IID</span><span class="sxs-lookup"><span data-stu-id="f0aab-148">IID</span></span><br/>                      | <span data-ttu-id="f0aab-149">IID \_ ISCardCmd 定義為 D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="f0aab-149">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="f0aab-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f0aab-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0aab-151">**取得 \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="f0aab-151">**get\_Data**</span></span>](iscardcmd-get-data.md)
</dt> <dt>

[<span data-ttu-id="f0aab-152">**取得 \_ P3**</span><span class="sxs-lookup"><span data-stu-id="f0aab-152">**get\_P3**</span></span>](iscardcmd-get-p3.md)
</dt> <dt>

[<span data-ttu-id="f0aab-153">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="f0aab-153">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
