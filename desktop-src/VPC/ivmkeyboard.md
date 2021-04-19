---
title: 'IVMKeyboard 介面 (VPCCOMInterfaces .h) '
description: 控制虛擬機器內的鍵盤裝置。 您可以使用 IVMVirtualMachine 鍵盤屬性來抓取虛擬機器的 IVMKeyboard。
ms.assetid: a64a23b6-3937-40c6-af9d-fb341c04fbf7
keywords:
- IVMKeyboard 介面 Virtual PC
- IVMKeyboard 介面 Virtual PC，說明
topic_type:
- apiref
api_name:
- IVMKeyboard
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fce2ddddd00de509278760a22fe3ab464f27c1c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106973302"
---
# <a name="ivmkeyboard-interface"></a><span data-ttu-id="842ed-106">IVMKeyboard 介面</span><span class="sxs-lookup"><span data-stu-id="842ed-106">IVMKeyboard interface</span></span>

<span data-ttu-id="842ed-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="842ed-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="842ed-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="842ed-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="842ed-109">控制虛擬機器內的鍵盤裝置。</span><span class="sxs-lookup"><span data-stu-id="842ed-109">Controls the keyboard device within a virtual machine.</span></span> <span data-ttu-id="842ed-110">您可以使用 [**IVMVirtualMachine：：鍵盤**](ivmvirtualmachine-keyboard.md)屬性來抓取虛擬機器的 **IVMKeyboard** 。</span><span class="sxs-lookup"><span data-stu-id="842ed-110">The **IVMKeyboard** for a virtual machine can be retrieved using the [**IVMVirtualMachine::Keyboard**](ivmvirtualmachine-keyboard.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="842ed-111">成員</span><span class="sxs-lookup"><span data-stu-id="842ed-111">Members</span></span>

<span data-ttu-id="842ed-112">**IVMKeyboard** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。</span><span class="sxs-lookup"><span data-stu-id="842ed-112">The **IVMKeyboard** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="842ed-113">**IVMKeyboard** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="842ed-113">**IVMKeyboard** also has these types of members:</span></span>

-   [<span data-ttu-id="842ed-114">方法</span><span class="sxs-lookup"><span data-stu-id="842ed-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="842ed-115">屬性</span><span class="sxs-lookup"><span data-stu-id="842ed-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="842ed-116">方法</span><span class="sxs-lookup"><span data-stu-id="842ed-116">Methods</span></span>

<span data-ttu-id="842ed-117">**IVMKeyboard** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="842ed-117">The **IVMKeyboard** interface has these methods.</span></span>



| <span data-ttu-id="842ed-118">方法</span><span class="sxs-lookup"><span data-stu-id="842ed-118">Method</span></span>                                                       | <span data-ttu-id="842ed-119">描述</span><span class="sxs-lookup"><span data-stu-id="842ed-119">Description</span></span>                                                                   |
|:-------------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="842ed-120">**IsPressed**</span><span class="sxs-lookup"><span data-stu-id="842ed-120">**IsPressed**</span></span>](ivmkeyboard-ispressed.md)                   | <span data-ttu-id="842ed-121">判斷指定的索引鍵是否已關閉。</span><span class="sxs-lookup"><span data-stu-id="842ed-121">Determines whether the specified key is down.</span></span><br/>                      |
| [<span data-ttu-id="842ed-122">**PressAndReleaseKey**</span><span class="sxs-lookup"><span data-stu-id="842ed-122">**PressAndReleaseKey**</span></span>](ivmkeyboard-pressandreleasekey.md) | <span data-ttu-id="842ed-123">模擬按下的按鍵，然後釋放。</span><span class="sxs-lookup"><span data-stu-id="842ed-123">Simulates a key being pressed down and then released.</span></span><br/>              |
| [<span data-ttu-id="842ed-124">**PressKey**</span><span class="sxs-lookup"><span data-stu-id="842ed-124">**PressKey**</span></span>](ivmkeyboard-presskey.md)                     | <span data-ttu-id="842ed-125">模擬按下的按鍵。</span><span class="sxs-lookup"><span data-stu-id="842ed-125">Simulates a key being pressed down.</span></span><br/>                                |
| [<span data-ttu-id="842ed-126">**ReleaseKey**</span><span class="sxs-lookup"><span data-stu-id="842ed-126">**ReleaseKey**</span></span>](ivmkeyboard-releasekey.md)                 | <span data-ttu-id="842ed-127">模擬要釋放的金鑰。</span><span class="sxs-lookup"><span data-stu-id="842ed-127">Simulates a key being released.</span></span><br/>                                    |
| [<span data-ttu-id="842ed-128">**TypeAsciiText**</span><span class="sxs-lookup"><span data-stu-id="842ed-128">**TypeAsciiText**</span></span>](ivmkeyboard-typeasciitext.md)           | <span data-ttu-id="842ed-129">模擬輸入至來賓的一連串 ASCII 按鍵。</span><span class="sxs-lookup"><span data-stu-id="842ed-129">Simulates a series of ASCII keys being typed into the guest.</span></span><br/>       |
| [<span data-ttu-id="842ed-130">**TypeKeySequence**</span><span class="sxs-lookup"><span data-stu-id="842ed-130">**TypeKeySequence**</span></span>](ivmkeyboard-typekeysequence.md)       | <span data-ttu-id="842ed-131">模擬在來賓中輸入的索引鍵清單（以逗號分隔）。</span><span class="sxs-lookup"><span data-stu-id="842ed-131">Simulates a comma-delimited list of keys being typed in the guest.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="842ed-132">屬性</span><span class="sxs-lookup"><span data-stu-id="842ed-132">Properties</span></span>

<span data-ttu-id="842ed-133">**IVMKeyboard** 介面具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="842ed-133">The **IVMKeyboard** interface has these properties.</span></span>



| <span data-ttu-id="842ed-134">屬性</span><span class="sxs-lookup"><span data-stu-id="842ed-134">Property</span></span>                                                                | <span data-ttu-id="842ed-135">存取類型</span><span class="sxs-lookup"><span data-stu-id="842ed-135">Access type</span></span>           | <span data-ttu-id="842ed-136">Description</span><span class="sxs-lookup"><span data-stu-id="842ed-136">Description</span></span>                                                                                                |
|:------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="842ed-137">**HasExclusiveAccess**</span><span class="sxs-lookup"><span data-stu-id="842ed-137">**HasExclusiveAccess**</span></span>](ivmkeyboard-hasexclusiveaccess.md)<br/> | <span data-ttu-id="842ed-138">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="842ed-138">Read/write</span></span><br/> | <span data-ttu-id="842ed-139">指出此物件是否對虛擬機器的鍵盤裝置具有獨佔控制。</span><span class="sxs-lookup"><span data-stu-id="842ed-139">Indicates whether this object has exclusive control over the virtual machine's keyboard device.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="842ed-140">備註</span><span class="sxs-lookup"><span data-stu-id="842ed-140">Remarks</span></span>

<span data-ttu-id="842ed-141">您可以透過數種方式將金鑰輸入至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="842ed-141">Keys can be typed into the virtual machine in several ways.</span></span> <span data-ttu-id="842ed-142">若要輸入標準的 ASCII 字元序列，請使用 [**TypeAsciiText**](ivmkeyboard-typeasciitext.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="842ed-142">To type a normal ASCII sequence of characters, use the [**TypeAsciiText**](ivmkeyboard-typeasciitext.md) method.</span></span> <span data-ttu-id="842ed-143">如果需要更大的彈性， **IVMKeyboard** 有數種設計用來與下列清單中的主要代碼搭配使用的方法。</span><span class="sxs-lookup"><span data-stu-id="842ed-143">If greater flexibility is required, **IVMKeyboard** has several methods that are designed to be used with the key codes in the following list.</span></span> <span data-ttu-id="842ed-144">[**TypeKeySequence**](ivmkeyboard-typekeysequence.md)方法可以接受以逗號分隔的按鍵碼字串，此字串將依序按下並依序在虛擬機器中放開。</span><span class="sxs-lookup"><span data-stu-id="842ed-144">The [**TypeKeySequence**](ivmkeyboard-typekeysequence.md) method can accept a comma-delimited string of key codes, which will be pressed and released, in order, within the virtual machine.</span></span> <span data-ttu-id="842ed-145">除了這些按鍵碼以外，關鍵字可以用來強制只按下或只釋放按鍵。</span><span class="sxs-lookup"><span data-stu-id="842ed-145">In addition to these key codes, the keywords UP and DOWN can be used to force a key to only be pressed, or only be released.</span></span> <span data-ttu-id="842ed-146">UP 和 DOWN 關鍵字只適用于緊接在關鍵字後面的按鍵程式碼。</span><span class="sxs-lookup"><span data-stu-id="842ed-146">The UP and DOWN keywords only apply to the key code directly following the keyword.</span></span>

<span data-ttu-id="842ed-147">若要避免多個腳本、應用程式或使用者同時嘗試存取相同的鍵盤裝置，請將 [**HasExclusiveAccess**](ivmkeyboard-hasexclusiveaccess.md) 屬性設定為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="842ed-147">To avoid multiple scripts, applications, or users from simultaneously attempting to access the same keyboard device, set the [**HasExclusiveAccess**](ivmkeyboard-hasexclusiveaccess.md) property to **TRUE**.</span></span> <span data-ttu-id="842ed-148">如果有一個進程取得獨佔存取權，則在釋出獨佔存取權之前，會忽略其他程式傳送輸入到鍵盤裝置的任何嘗試。</span><span class="sxs-lookup"><span data-stu-id="842ed-148">If exclusive access is acquired by one process, any attempts by other processes to send input to the keyboard device will be ignored until exclusive access has been released.</span></span>

## <a name="requirements"></a><span data-ttu-id="842ed-149">規格需求</span><span class="sxs-lookup"><span data-stu-id="842ed-149">Requirements</span></span>



| <span data-ttu-id="842ed-150">需求</span><span class="sxs-lookup"><span data-stu-id="842ed-150">Requirement</span></span> | <span data-ttu-id="842ed-151">值</span><span class="sxs-lookup"><span data-stu-id="842ed-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="842ed-152">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="842ed-152">Minimum supported client</span></span><br/> | <span data-ttu-id="842ed-153">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="842ed-153">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="842ed-154">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="842ed-154">Minimum supported server</span></span><br/> | <span data-ttu-id="842ed-155">都不支援</span><span class="sxs-lookup"><span data-stu-id="842ed-155">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="842ed-156">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="842ed-156">End of client support</span></span><br/>    | <span data-ttu-id="842ed-157">Windows 7</span><span class="sxs-lookup"><span data-stu-id="842ed-157">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="842ed-158">產品</span><span class="sxs-lookup"><span data-stu-id="842ed-158">Product</span></span><br/>                  | <span data-ttu-id="842ed-159">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="842ed-159">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="842ed-160">標頭</span><span class="sxs-lookup"><span data-stu-id="842ed-160">Header</span></span><br/>                   | <dl> <span data-ttu-id="842ed-161"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="842ed-161"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="842ed-162">IID</span><span class="sxs-lookup"><span data-stu-id="842ed-162">IID</span></span><br/>                      | <span data-ttu-id="842ed-163">IID \_ IVMKeyboard 定義為00695f2e-c5ad-4d6e-b1ab-336ed121f8c4</span><span class="sxs-lookup"><span data-stu-id="842ed-163">IID\_IVMKeyboard is defined as 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="842ed-164">另請參閱</span><span class="sxs-lookup"><span data-stu-id="842ed-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="842ed-165">Windows Virtual PC 介面</span><span class="sxs-lookup"><span data-stu-id="842ed-165">Windows Virtual PC Interfaces</span></span>](virtual-pc-interfaces.md)
</dt> <dt>

[<span data-ttu-id="842ed-166">主要序列</span><span class="sxs-lookup"><span data-stu-id="842ed-166">Key Sequences</span></span>](key-sequences.md)
</dt> </dl>

 

