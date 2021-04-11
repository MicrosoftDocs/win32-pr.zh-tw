---
description: 將有效的命令應用程式通訊協定資料單位 (APDU) 傳送至智慧卡。
ms.assetid: d1003cc3-c235-4635-ad5a-8cea7363bf30
title: 'ISCardCmd：： BuildCmd 方法 (Scarddat .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.BuildCmd
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: f44597ea087f7ccec191abc9dd03787780e88b2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193912"
---
# <a name="iscardcmdbuildcmd-method"></a><span data-ttu-id="70419-103">ISCardCmd：： BuildCmd 方法</span><span class="sxs-lookup"><span data-stu-id="70419-103">ISCardCmd::BuildCmd method</span></span>

<span data-ttu-id="70419-104">\[**BuildCmd** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="70419-104">\[The **BuildCmd** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="70419-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="70419-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="70419-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="70419-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="70419-107">**BuildCmd** 方法會將有效的命令 [*應用程式通訊協定資料單位*](../secgloss/a-gly.md) (APDU) ，以傳輸至 [*智慧卡*](../secgloss/s-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="70419-107">The **BuildCmd** method constructs a valid command [*application protocol data unit*](../secgloss/a-gly.md) (APDU) for transmission to a [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="70419-108">語法</span><span class="sxs-lookup"><span data-stu-id="70419-108">Syntax</span></span>


```C++
HRESULT BuildCmd(
  [in] BYTE         byClassId,
  [in] BYTE         byInsId,
  [in] BYTE         byP1,
  [in] BYTE         byP2,
  [in] LPBYTEBUFFER pbyData,
  [in] LONG         *p1Le
);
```



## <a name="parameters"></a><span data-ttu-id="70419-109">參數</span><span class="sxs-lookup"><span data-stu-id="70419-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70419-110">*byClassId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="70419-110">*byClassId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70419-111">命令類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="70419-111">Command class identifier.</span></span>

</dd> <dt>

<span data-ttu-id="70419-112">*byInsId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="70419-112">*byInsId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70419-113">命令指令識別碼。</span><span class="sxs-lookup"><span data-stu-id="70419-113">Command instruction identifier.</span></span>

</dd> <dt>

<span data-ttu-id="70419-114">*byP1* \[在\]</span><span class="sxs-lookup"><span data-stu-id="70419-114">*byP1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70419-115">命令的第一個參數。</span><span class="sxs-lookup"><span data-stu-id="70419-115">Command's first parameter.</span></span>

</dd> <dt>

<span data-ttu-id="70419-116">*byP2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="70419-116">*byP2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70419-117">命令的第二個參數。</span><span class="sxs-lookup"><span data-stu-id="70419-117">Command's second parameter.</span></span>

</dd> <dt>

<span data-ttu-id="70419-118">*pbyData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="70419-118">*pbyData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70419-119">命令之資料部分的指標。</span><span class="sxs-lookup"><span data-stu-id="70419-119">Pointer to the data portion of the command.</span></span>

</dd> <dt>

<span data-ttu-id="70419-120">*p1Le* \[在\]</span><span class="sxs-lookup"><span data-stu-id="70419-120">*p1Le* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70419-121">長整數的指標，其中包含所傳回資料的預期長度。</span><span class="sxs-lookup"><span data-stu-id="70419-121">Pointer to a LONG integer containing the expected length of the returned data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70419-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="70419-122">Return value</span></span>

<span data-ttu-id="70419-123">方法會傳回下列其中一個可能的值。</span><span class="sxs-lookup"><span data-stu-id="70419-123">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="70419-124">傳回碼</span><span class="sxs-lookup"><span data-stu-id="70419-124">Return code</span></span>                                                                                   | <span data-ttu-id="70419-125">Description</span><span class="sxs-lookup"><span data-stu-id="70419-125">Description</span></span>                                    |
|-----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="70419-126"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="70419-126"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="70419-127">作業順利完成。</span><span class="sxs-lookup"><span data-stu-id="70419-127">Operation completed successfully.</span></span><br/>   |
| <dl> <span data-ttu-id="70419-128"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="70419-128"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="70419-129">其中一個參數無效。</span><span class="sxs-lookup"><span data-stu-id="70419-129">One of the parameters is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="70419-130"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="70419-130"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="70419-131">傳入了錯誤指標。</span><span class="sxs-lookup"><span data-stu-id="70419-131">A bad pointer was passed in.</span></span><br/>        |
| <dl> <span data-ttu-id="70419-132"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="70419-132"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="70419-133">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="70419-133">Out of memory.</span></span><br/>                      |



 

## <a name="remarks"></a><span data-ttu-id="70419-134">備註</span><span class="sxs-lookup"><span data-stu-id="70419-134">Remarks</span></span>

<span data-ttu-id="70419-135">若要將命令封裝到另一個命令，請呼叫 [**封裝**](iscardcmd-encapsulate.md)。</span><span class="sxs-lookup"><span data-stu-id="70419-135">To encapsulate the command into another command, call [**Encapsulate**](iscardcmd-encapsulate.md).</span></span>

<span data-ttu-id="70419-136">如需此介面所提供的所有方法清單，請參閱 [**ISCardCmd**](iscardcmd.md)。</span><span class="sxs-lookup"><span data-stu-id="70419-136">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="70419-137">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回智慧卡的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="70419-137">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="70419-138">如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="70419-138">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="70419-139">範例</span><span class="sxs-lookup"><span data-stu-id="70419-139">Examples</span></span>

<span data-ttu-id="70419-140">下列範例顯示如何建立命令 APDU。</span><span class="sxs-lookup"><span data-stu-id="70419-140">The following example shows how to construct a command APDU.</span></span> <span data-ttu-id="70419-141">此範例假設 pISCardCmd 是 [**ISCardCmd**](iscardcmd.md) 介面實例的有效指標，而 PIByteRequest 是 [**IByteBuffer**](ibytebuffer.md) 介面實例的有效指標，該介面是由先前對 [**IByteBuffer：： Initialize**](ibytebuffer-initialize.md) 方法的呼叫所初始化。</span><span class="sxs-lookup"><span data-stu-id="70419-141">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface and that pIByteRequest is a valid pointer to an instance of the [**IByteBuffer**](ibytebuffer.md) interface initialized with a previous call to the [**IByteBuffer::Initialize**](ibytebuffer-initialize.md) method.</span></span>


```C++
LONG       lLe = 0;
HRESULT    hr;

hr = pISCardCmd->BuildCmd(0x00,   // Some cards prefer 0xC0
                          0xa4,   // 'Select File'
                          0x00,
                          0x00,
                          pIByteRequest,
                          &lLe);
if (FAILED(hr))
{
    printf("Failed ISCardCmd::BuildCmd\n");
    // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="70419-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="70419-142">Requirements</span></span>



| <span data-ttu-id="70419-143">需求</span><span class="sxs-lookup"><span data-stu-id="70419-143">Requirement</span></span> | <span data-ttu-id="70419-144">值</span><span class="sxs-lookup"><span data-stu-id="70419-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="70419-145">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="70419-145">Minimum supported client</span></span><br/> | <span data-ttu-id="70419-146">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="70419-146">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="70419-147">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="70419-147">Minimum supported server</span></span><br/> | <span data-ttu-id="70419-148">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="70419-148">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="70419-149">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="70419-149">End of client support</span></span><br/>    | <span data-ttu-id="70419-150">Windows XP</span><span class="sxs-lookup"><span data-stu-id="70419-150">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="70419-151">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="70419-151">End of server support</span></span><br/>    | <span data-ttu-id="70419-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="70419-152">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="70419-153">標頭</span><span class="sxs-lookup"><span data-stu-id="70419-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="70419-154"><dt>Scarddat。h</dt></span><span class="sxs-lookup"><span data-stu-id="70419-154"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="70419-155">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="70419-155">Type library</span></span><br/>             | <dl> <span data-ttu-id="70419-156"><dt>Scarddat .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="70419-156"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="70419-157">DLL</span><span class="sxs-lookup"><span data-stu-id="70419-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="70419-158"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="70419-158"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="70419-159">IID</span><span class="sxs-lookup"><span data-stu-id="70419-159">IID</span></span><br/>                      | <span data-ttu-id="70419-160">IID \_ ISCardCmd 定義為 D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="70419-160">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="70419-161">另請參閱</span><span class="sxs-lookup"><span data-stu-id="70419-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70419-162">**封裝**</span><span class="sxs-lookup"><span data-stu-id="70419-162">**Encapsulate**</span></span>](iscardcmd-encapsulate.md)
</dt> <dt>

[<span data-ttu-id="70419-163">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="70419-163">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
