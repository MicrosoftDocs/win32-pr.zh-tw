---
title: 'IVMKeyboard PressAndReleaseKey 方法 (VPCCOMInterfaces .h) '
description: 模擬按下的按鍵，然後釋放。
ms.assetid: 2a7fc36f-f1bf-4f1d-b8f7-ea5b167c82a7
keywords:
- PressAndReleaseKey 方法 Virtual PC
- PressAndReleaseKey 方法 Virtual PC，IVMKeyboard 介面
- IVMKeyboard 介面 Virtual PC，PressAndReleaseKey 方法
topic_type:
- apiref
api_name:
- IVMKeyboard.PressAndReleaseKey
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4adbcac2c79c02ce69584bbfdf21a6b08b350a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968175"
---
# <a name="ivmkeyboardpressandreleasekey-method"></a><span data-ttu-id="c74d9-106">IVMKeyboard：:P ressAndReleaseKey 方法</span><span class="sxs-lookup"><span data-stu-id="c74d9-106">IVMKeyboard::PressAndReleaseKey method</span></span>

<span data-ttu-id="c74d9-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="c74d9-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="c74d9-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="c74d9-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="c74d9-109">模擬按下的按鍵，然後釋放。</span><span class="sxs-lookup"><span data-stu-id="c74d9-109">Simulates a key being pressed down and then released.</span></span>

## <a name="syntax"></a><span data-ttu-id="c74d9-110">語法</span><span class="sxs-lookup"><span data-stu-id="c74d9-110">Syntax</span></span>


```C++
HRESULT PressAndReleaseKey(
  [in] BSTR key
);
```



## <a name="parameters"></a><span data-ttu-id="c74d9-111">參數</span><span class="sxs-lookup"><span data-stu-id="c74d9-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c74d9-112">*金鑰* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c74d9-112">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c74d9-113">要按下和釋出之索引鍵的按鍵碼。</span><span class="sxs-lookup"><span data-stu-id="c74d9-113">The key code for the key to be pressed and released.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c74d9-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="c74d9-114">Return value</span></span>

<span data-ttu-id="c74d9-115">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="c74d9-115">This method can return one of these values.</span></span>



| <span data-ttu-id="c74d9-116">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="c74d9-116">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="c74d9-117">Description</span><span class="sxs-lookup"><span data-stu-id="c74d9-117">Description</span></span>                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c74d9-118"><dt>**S \_確定**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c74d9-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="c74d9-119">作業成功。</span><span class="sxs-lookup"><span data-stu-id="c74d9-119">The operation was successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="c74d9-120"><dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="c74d9-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="c74d9-121">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="c74d9-121">The parameter is **NULL**.</span></span><br/>                                      |
| <dl> <span data-ttu-id="c74d9-122"><dt>**E \_INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="c74d9-122"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>      | <span data-ttu-id="c74d9-123">指定的字串是空的，或包含不正確按鍵碼。</span><span class="sxs-lookup"><span data-stu-id="c74d9-123">The specified string is empty, or contains an invalid key code.</span></span><br/> |
| <dl> <span data-ttu-id="c74d9-124"><dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="c74d9-124"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="c74d9-125">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="c74d9-125">An unexpected error has occurred.</span></span><br/>                               |



 

## <a name="requirements"></a><span data-ttu-id="c74d9-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="c74d9-126">Requirements</span></span>



| <span data-ttu-id="c74d9-127">需求</span><span class="sxs-lookup"><span data-stu-id="c74d9-127">Requirement</span></span> | <span data-ttu-id="c74d9-128">值</span><span class="sxs-lookup"><span data-stu-id="c74d9-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c74d9-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c74d9-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c74d9-130">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c74d9-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c74d9-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c74d9-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c74d9-132">都不支援</span><span class="sxs-lookup"><span data-stu-id="c74d9-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="c74d9-133">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="c74d9-133">End of client support</span></span><br/>    | <span data-ttu-id="c74d9-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c74d9-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="c74d9-135">產品</span><span class="sxs-lookup"><span data-stu-id="c74d9-135">Product</span></span><br/>                  | <span data-ttu-id="c74d9-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="c74d9-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="c74d9-137">標頭</span><span class="sxs-lookup"><span data-stu-id="c74d9-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="c74d9-138"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="c74d9-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="c74d9-139">IID</span><span class="sxs-lookup"><span data-stu-id="c74d9-139">IID</span></span><br/>                      | <span data-ttu-id="c74d9-140">IID \_ IVMKeyboard 定義為00695f2e-c5ad-4d6e-b1ab-336ed121f8c4</span><span class="sxs-lookup"><span data-stu-id="c74d9-140">IID\_IVMKeyboard is defined as 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="c74d9-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c74d9-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c74d9-142">**IVMKeyboard**</span><span class="sxs-lookup"><span data-stu-id="c74d9-142">**IVMKeyboard**</span></span>](ivmkeyboard.md)
</dt> </dl>

 

