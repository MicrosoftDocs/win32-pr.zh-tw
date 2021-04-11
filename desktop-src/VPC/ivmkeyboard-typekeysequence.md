---
title: 'IVMKeyboard TypeKeySequence 方法 (VPCCOMInterfaces .h) '
description: 模擬輸入的索引鍵清單（以逗號分隔）。
ms.assetid: ba4d4e43-cb2e-49ae-940d-2e81286d3473
keywords:
- TypeKeySequence 方法 Virtual PC
- TypeKeySequence 方法 Virtual PC，IVMKeyboard 介面
- IVMKeyboard 介面 Virtual PC，TypeKeySequence 方法
topic_type:
- apiref
api_name:
- IVMKeyboard.TypeKeySequence
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c34bd96077c1d28aad196ee0d6b11de122725d68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935030"
---
# <a name="ivmkeyboardtypekeysequence-method"></a><span data-ttu-id="2c2a5-106">IVMKeyboard：： TypeKeySequence 方法</span><span class="sxs-lookup"><span data-stu-id="2c2a5-106">IVMKeyboard::TypeKeySequence method</span></span>

<span data-ttu-id="2c2a5-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="2c2a5-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="2c2a5-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="2c2a5-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="2c2a5-109">模擬輸入的索引鍵清單（以逗號分隔）。</span><span class="sxs-lookup"><span data-stu-id="2c2a5-109">Simulates a comma-delimited list of keys being typed.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c2a5-110">語法</span><span class="sxs-lookup"><span data-stu-id="2c2a5-110">Syntax</span></span>


```C++
HRESULT TypeKeySequence(
  [in] BSTR keySequence
);
```



## <a name="parameters"></a><span data-ttu-id="2c2a5-111">參數</span><span class="sxs-lookup"><span data-stu-id="2c2a5-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c2a5-112">*keySequence* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2c2a5-112">*keySequence* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c2a5-113">要輸入的按鍵代碼（以逗號分隔）序列。</span><span class="sxs-lookup"><span data-stu-id="2c2a5-113">The comma-delimited sequence of key codes to be typed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c2a5-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="2c2a5-114">Return value</span></span>

<span data-ttu-id="2c2a5-115">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="2c2a5-115">This method can return one of these values.</span></span>



| <span data-ttu-id="2c2a5-116">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="2c2a5-116">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="2c2a5-117">Description</span><span class="sxs-lookup"><span data-stu-id="2c2a5-117">Description</span></span>                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2c2a5-118"><dt>**S \_確定**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2c2a5-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="2c2a5-119">作業成功。</span><span class="sxs-lookup"><span data-stu-id="2c2a5-119">The operation was successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="2c2a5-120"><dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="2c2a5-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="2c2a5-121">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="2c2a5-121">The parameter is **NULL**.</span></span><br/>                                      |
| <dl> <span data-ttu-id="2c2a5-122"><dt>**E \_INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="2c2a5-122"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>      | <span data-ttu-id="2c2a5-123">指定的字串是空的，或包含不正確按鍵碼。</span><span class="sxs-lookup"><span data-stu-id="2c2a5-123">The specified string is empty, or contains an invalid key code.</span></span><br/> |
| <dl> <span data-ttu-id="2c2a5-124"><dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="2c2a5-124"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="2c2a5-125">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="2c2a5-125">An unexpected error has occurred.</span></span><br/>                               |



 

## <a name="remarks"></a><span data-ttu-id="2c2a5-126">備註</span><span class="sxs-lookup"><span data-stu-id="2c2a5-126">Remarks</span></span>

<span data-ttu-id="2c2a5-127">金鑰序列字串是一組以逗號分隔的索引鍵識別碼，用來模擬標準美國101按鍵的按鍵和發行順序。</span><span class="sxs-lookup"><span data-stu-id="2c2a5-127">A key sequence string is a comma-delimited set of key identifiers which are used to simulate the key press and release sequence of a standard U.S. 101-key AT-style keyboard.</span></span>

<span data-ttu-id="2c2a5-128">如果索引鍵識別碼出現在字串中，但沒有先前的修飾詞，則會將按鍵按鍵的程式碼傳送到虛擬機器會話，緊接著其對應的金鑰發行程式碼。</span><span class="sxs-lookup"><span data-stu-id="2c2a5-128">If a key identifier appears in the string without a preceding modifier, a key-pressed code is sent to the virtual machine session, followed immediately by its corresponding key-released code.</span></span> <span data-ttu-id="2c2a5-129">金鑰修飾詞可以用來變更此行為。</span><span class="sxs-lookup"><span data-stu-id="2c2a5-129">Key modifiers can be used to change this behavior.</span></span>

<span data-ttu-id="2c2a5-130">例如，向下修飾詞會傳送下列金鑰識別碼的按鍵按鍵程式碼，而不會傳送金鑰發行程式碼。</span><span class="sxs-lookup"><span data-stu-id="2c2a5-130">For example, the DOWN modifier will send the key-pressed code for the following key identifier without sending the key-released code.</span></span> <span data-ttu-id="2c2a5-131">當您在傳送其他索引鍵時，如果將 Ctrl、Alt 和 Shift 鍵保持在一起，則這非常有用。</span><span class="sxs-lookup"><span data-stu-id="2c2a5-131">This is useful for simulating Ctrl, Alt, and Shift keys when they are held down while other keys are being sent.</span></span> <span data-ttu-id="2c2a5-132">若要釋放金鑰，必須連同先前的 UP 修飾詞一起包含在金鑰字串中。</span><span class="sxs-lookup"><span data-stu-id="2c2a5-132">To release the key, it must be included in the key string again along with a preceding UP modifier.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c2a5-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="2c2a5-133">Requirements</span></span>



| <span data-ttu-id="2c2a5-134">需求</span><span class="sxs-lookup"><span data-stu-id="2c2a5-134">Requirement</span></span> | <span data-ttu-id="2c2a5-135">值</span><span class="sxs-lookup"><span data-stu-id="2c2a5-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c2a5-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2c2a5-136">Minimum supported client</span></span><br/> | <span data-ttu-id="2c2a5-137">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2c2a5-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2c2a5-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2c2a5-138">Minimum supported server</span></span><br/> | <span data-ttu-id="2c2a5-139">都不支援</span><span class="sxs-lookup"><span data-stu-id="2c2a5-139">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="2c2a5-140">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="2c2a5-140">End of client support</span></span><br/>    | <span data-ttu-id="2c2a5-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2c2a5-141">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="2c2a5-142">產品</span><span class="sxs-lookup"><span data-stu-id="2c2a5-142">Product</span></span><br/>                  | <span data-ttu-id="2c2a5-143">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="2c2a5-143">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="2c2a5-144">標頭</span><span class="sxs-lookup"><span data-stu-id="2c2a5-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c2a5-145"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="2c2a5-145"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="2c2a5-146">IID</span><span class="sxs-lookup"><span data-stu-id="2c2a5-146">IID</span></span><br/>                      | <span data-ttu-id="2c2a5-147">IID \_ IVMKeyboard 定義為00695f2e-c5ad-4d6e-b1ab-336ed121f8c4</span><span class="sxs-lookup"><span data-stu-id="2c2a5-147">IID\_IVMKeyboard is defined as 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="2c2a5-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2c2a5-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c2a5-149">**IVMKeyboard**</span><span class="sxs-lookup"><span data-stu-id="2c2a5-149">**IVMKeyboard**</span></span>](ivmkeyboard.md)
</dt> <dt>

[<span data-ttu-id="2c2a5-150">主要序列</span><span class="sxs-lookup"><span data-stu-id="2c2a5-150">Key Sequences</span></span>](key-sequences.md)
</dt> </dl>

 

