---
title: 'IVMKeyboard IsPressed 方法 (VPCCOMInterfaces .h) '
description: 判斷指定的索引鍵是否已關閉。
ms.assetid: 7541d678-762a-4c2e-80cd-686bb56c9cd7
keywords:
- IsPressed 方法 Virtual PC
- IsPressed 方法 Virtual PC，IVMKeyboard 介面
- IVMKeyboard 介面 Virtual PC，IsPressed 方法
topic_type:
- apiref
api_name:
- IVMKeyboard.IsPressed
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0a4185fa0310994bc1cffa917348dfca2fdedfe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686182"
---
# <a name="ivmkeyboardispressed-method"></a><span data-ttu-id="9e7e4-106">IVMKeyboard：： IsPressed 方法</span><span class="sxs-lookup"><span data-stu-id="9e7e4-106">IVMKeyboard::IsPressed method</span></span>

<span data-ttu-id="9e7e4-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="9e7e4-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="9e7e4-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="9e7e4-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="9e7e4-109">判斷指定的索引鍵是否已關閉。</span><span class="sxs-lookup"><span data-stu-id="9e7e4-109">Determines whether the specified key is down.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e7e4-110">語法</span><span class="sxs-lookup"><span data-stu-id="9e7e4-110">Syntax</span></span>


```C++
HRESULT IsPressed(
  [in]          BSTR         key,
  [out, retval] VARIANT_BOOL *pressed
);
```



## <a name="parameters"></a><span data-ttu-id="9e7e4-111">參數</span><span class="sxs-lookup"><span data-stu-id="9e7e4-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e7e4-112">*金鑰* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9e7e4-112">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e7e4-113">要查詢其狀態之索引鍵的按鍵碼。</span><span class="sxs-lookup"><span data-stu-id="9e7e4-113">The key code for the key whose state is to be queried.</span></span>

</dd> <dt>

<span data-ttu-id="9e7e4-114">已 *按下* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="9e7e4-114">*pressed* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="9e7e4-115">如果機碼目前已按下，**則為 TRUE** ，否則為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="9e7e4-115">**TRUE** if the key is currently pressed down, **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e7e4-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="9e7e4-116">Return value</span></span>

<span data-ttu-id="9e7e4-117">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="9e7e4-117">This method can return one of these values.</span></span>



| <span data-ttu-id="9e7e4-118">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="9e7e4-118">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="9e7e4-119">Description</span><span class="sxs-lookup"><span data-stu-id="9e7e4-119">Description</span></span>                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9e7e4-120"><dt>**S \_確定**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="9e7e4-120"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="9e7e4-121">作業成功。</span><span class="sxs-lookup"><span data-stu-id="9e7e4-121">The operation was successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="9e7e4-122"><dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="9e7e4-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="9e7e4-123">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="9e7e4-123">A parameter is **NULL**.</span></span><br/>                                        |
| <dl> <span data-ttu-id="9e7e4-124"><dt>**E \_INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="9e7e4-124"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>      | <span data-ttu-id="9e7e4-125">指定的字串是空的，或包含不正確按鍵碼。</span><span class="sxs-lookup"><span data-stu-id="9e7e4-125">The specified string is empty, or contains an invalid key code.</span></span><br/> |
| <dl> <span data-ttu-id="9e7e4-126"><dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="9e7e4-126"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="9e7e4-127">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="9e7e4-127">An unexpected error has occurred.</span></span><br/>                               |



 

## <a name="requirements"></a><span data-ttu-id="9e7e4-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="9e7e4-128">Requirements</span></span>



| <span data-ttu-id="9e7e4-129">需求</span><span class="sxs-lookup"><span data-stu-id="9e7e4-129">Requirement</span></span> | <span data-ttu-id="9e7e4-130">值</span><span class="sxs-lookup"><span data-stu-id="9e7e4-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e7e4-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9e7e4-131">Minimum supported client</span></span><br/> | <span data-ttu-id="9e7e4-132">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9e7e4-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9e7e4-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9e7e4-133">Minimum supported server</span></span><br/> | <span data-ttu-id="9e7e4-134">都不支援</span><span class="sxs-lookup"><span data-stu-id="9e7e4-134">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="9e7e4-135">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="9e7e4-135">End of client support</span></span><br/>    | <span data-ttu-id="9e7e4-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9e7e4-136">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="9e7e4-137">產品</span><span class="sxs-lookup"><span data-stu-id="9e7e4-137">Product</span></span><br/>                  | <span data-ttu-id="9e7e4-138">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="9e7e4-138">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="9e7e4-139">標頭</span><span class="sxs-lookup"><span data-stu-id="9e7e4-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e7e4-140"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="9e7e4-140"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="9e7e4-141">IID</span><span class="sxs-lookup"><span data-stu-id="9e7e4-141">IID</span></span><br/>                      | <span data-ttu-id="9e7e4-142">IID \_ IVMKeyboard 定義為00695f2e-c5ad-4d6e-b1ab-336ed121f8c4</span><span class="sxs-lookup"><span data-stu-id="9e7e4-142">IID\_IVMKeyboard is defined as 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="9e7e4-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9e7e4-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e7e4-144">**IVMKeyboard**</span><span class="sxs-lookup"><span data-stu-id="9e7e4-144">**IVMKeyboard**</span></span>](ivmkeyboard.md)
</dt> </dl>

 

