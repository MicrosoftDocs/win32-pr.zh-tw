---
description: Clear 方法會清除應用程式協定資料單位 (APDU) 和回復 APDU 訊息緩衝區。
ms.assetid: 5fd3ebb9-b492-4668-9dd8-3ffbcfceb12c
title: 'ISCardCmd：： Clear 方法 (Scarddat .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.Clear
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 0701906c38764ed1b4817f40430dde9b48bfb12e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113237"
---
# <a name="iscardcmdclear-method"></a><span data-ttu-id="22447-103">ISCardCmd：： Clear 方法</span><span class="sxs-lookup"><span data-stu-id="22447-103">ISCardCmd::Clear method</span></span>

<span data-ttu-id="22447-104">\[**Clear** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="22447-104">\[The **Clear** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="22447-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="22447-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="22447-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="22447-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="22447-107">**Clear** 方法會清除 [*應用程式協定資料單位*](../secgloss/a-gly.md) (APDU) 和 [*回復 apdu*](../secgloss/r-gly.md)訊息緩衝區。</span><span class="sxs-lookup"><span data-stu-id="22447-107">The **Clear** method clears the [*application protocol data unit*](../secgloss/a-gly.md) (APDU) and [*reply APDU*](../secgloss/r-gly.md) message buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="22447-108">語法</span><span class="sxs-lookup"><span data-stu-id="22447-108">Syntax</span></span>


```C++
HRESULT Clear();
```



## <a name="parameters"></a><span data-ttu-id="22447-109">參數</span><span class="sxs-lookup"><span data-stu-id="22447-109">Parameters</span></span>

<span data-ttu-id="22447-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="22447-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="22447-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="22447-111">Return value</span></span>

<span data-ttu-id="22447-112">方法會傳回下列其中一個可能的值。</span><span class="sxs-lookup"><span data-stu-id="22447-112">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="22447-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="22447-113">Return code</span></span>                                                                             | <span data-ttu-id="22447-114">Description</span><span class="sxs-lookup"><span data-stu-id="22447-114">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="22447-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="22447-115"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="22447-116">作業順利完成。</span><span class="sxs-lookup"><span data-stu-id="22447-116">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="22447-117"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="22447-117"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="22447-118">未知的錯誤。</span><span class="sxs-lookup"><span data-stu-id="22447-118">Unknown error.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="22447-119">備註</span><span class="sxs-lookup"><span data-stu-id="22447-119">Remarks</span></span>

<span data-ttu-id="22447-120">若要建立命令 APDU，請呼叫 [**BuildCmd**](iscardcmd-buildcmd.md)。</span><span class="sxs-lookup"><span data-stu-id="22447-120">To build a command APDU, call [**BuildCmd**](iscardcmd-buildcmd.md).</span></span>

<span data-ttu-id="22447-121">如需此介面所提供的所有方法清單，請參閱 [**ISCardCmd**](iscardcmd.md)。</span><span class="sxs-lookup"><span data-stu-id="22447-121">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="22447-122">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回智慧卡的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="22447-122">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="22447-123">如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="22447-123">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="22447-124">範例</span><span class="sxs-lookup"><span data-stu-id="22447-124">Examples</span></span>

<span data-ttu-id="22447-125">下列範例顯示如何清除 APDU 和回復 APDU 訊息緩衝區。</span><span class="sxs-lookup"><span data-stu-id="22447-125">The following example shows how to clear the APDU and reply APDU message buffers.</span></span>


```C++
HRESULT  hr;

hr = pISCardCmd->Clear();
if (FAILED(hr))
{
    printf("Failed ISCardCmd::Clear\n");
    // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="22447-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="22447-126">Requirements</span></span>



| <span data-ttu-id="22447-127">需求</span><span class="sxs-lookup"><span data-stu-id="22447-127">Requirement</span></span> | <span data-ttu-id="22447-128">值</span><span class="sxs-lookup"><span data-stu-id="22447-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="22447-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="22447-129">Minimum supported client</span></span><br/> | <span data-ttu-id="22447-130">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="22447-130">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="22447-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="22447-131">Minimum supported server</span></span><br/> | <span data-ttu-id="22447-132">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="22447-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="22447-133">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="22447-133">End of client support</span></span><br/>    | <span data-ttu-id="22447-134">Windows XP</span><span class="sxs-lookup"><span data-stu-id="22447-134">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="22447-135">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="22447-135">End of server support</span></span><br/>    | <span data-ttu-id="22447-136">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="22447-136">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="22447-137">標頭</span><span class="sxs-lookup"><span data-stu-id="22447-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="22447-138"><dt>Scarddat。h</dt></span><span class="sxs-lookup"><span data-stu-id="22447-138"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="22447-139">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="22447-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="22447-140"><dt>Scarddat .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="22447-140"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="22447-141">DLL</span><span class="sxs-lookup"><span data-stu-id="22447-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="22447-142"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22447-142"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="22447-143">IID</span><span class="sxs-lookup"><span data-stu-id="22447-143">IID</span></span><br/>                      | <span data-ttu-id="22447-144">IID \_ ISCardCmd 定義為 D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="22447-144">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="22447-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="22447-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22447-146">**ISCardCmd::BuildCmd**</span><span class="sxs-lookup"><span data-stu-id="22447-146">**ISCardCmd::BuildCmd**</span></span>](iscardcmd-buildcmd.md)
</dt> <dt>

[<span data-ttu-id="22447-147">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="22447-147">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
