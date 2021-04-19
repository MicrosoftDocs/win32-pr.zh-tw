---
description: 抓取進程可用之可用虛擬位址空間的目前大小（以位元組為單位）。
ms.assetid: 13b3b347-5db1-484f-bd1d-3a604eb6bc5b
ms.tgt_platform: multiple
title: Win32_Process 類別的 GetAvailableVirtualSize 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.GetAvailableVirtualSize
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: ee6e798b8df32822de481f3af1dc6b21a81d1024
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971952"
---
# <a name="getavailablevirtualsize-method-of-the-win32_process-class"></a><span data-ttu-id="711d6-103">Win32 進程類別的 GetAvailableVirtualSize 方法 \_</span><span class="sxs-lookup"><span data-stu-id="711d6-103">GetAvailableVirtualSize method of the Win32\_Process class</span></span>

<span data-ttu-id="711d6-104">抓取進程可用之可用虛擬位址空間的目前大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="711d6-104">Retrieves the current size, in bytes, of the free virtual address space available to the process.</span></span>

## <a name="syntax"></a><span data-ttu-id="711d6-105">語法</span><span class="sxs-lookup"><span data-stu-id="711d6-105">Syntax</span></span>


```mof
uint32 GetAvailableVirtualSize(
  [out] uint64 AvailableVirtualSize
);
```



## <a name="parameters"></a><span data-ttu-id="711d6-106">參數</span><span class="sxs-lookup"><span data-stu-id="711d6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="711d6-107">*AvailableVirtualSize* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="711d6-107">*AvailableVirtualSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="711d6-108">*AvailableVirtualSize* 參數會傳回此進程可用的可用虛擬位址空間。</span><span class="sxs-lookup"><span data-stu-id="711d6-108">The *AvailableVirtualSize* parameter returns the free virtual address space available to this process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="711d6-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="711d6-109">Return value</span></span>

<span data-ttu-id="711d6-110">傳回零 (0) 表示成功。</span><span class="sxs-lookup"><span data-stu-id="711d6-110">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="711d6-111">任何其他數字表示發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="711d6-111">Any other number indicates an error.</span></span> <span data-ttu-id="711d6-112">如需其他錯誤代碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="711d6-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="711d6-113">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="711d6-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="711d6-114">**成功完成**</span><span class="sxs-lookup"><span data-stu-id="711d6-114">**Successful completion**</span></span>
</dt> <dd>

<span data-ttu-id="711d6-115">0</span><span class="sxs-lookup"><span data-stu-id="711d6-115">0</span></span>

<span data-ttu-id="711d6-116">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="711d6-116">The operation completed successfully.</span></span>

</dd> <dt>

<span data-ttu-id="711d6-117">**拒絕存取**</span><span class="sxs-lookup"><span data-stu-id="711d6-117">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="711d6-118">2</span><span class="sxs-lookup"><span data-stu-id="711d6-118">2</span></span>

<span data-ttu-id="711d6-119">使用者無法存取所要求的資訊</span><span class="sxs-lookup"><span data-stu-id="711d6-119">The user does not have access to the requested information</span></span>

</dd> <dt>

<span data-ttu-id="711d6-120">**許可權不足**</span><span class="sxs-lookup"><span data-stu-id="711d6-120">**Insufficient privilege**</span></span>
</dt> <dd>

<span data-ttu-id="711d6-121">3</span><span class="sxs-lookup"><span data-stu-id="711d6-121">3</span></span>

<span data-ttu-id="711d6-122">使用者沒有足夠的許可權。</span><span class="sxs-lookup"><span data-stu-id="711d6-122">The user does not have sufficient privilege.</span></span>

</dd> <dt>

<span data-ttu-id="711d6-123">**未知的失敗**</span><span class="sxs-lookup"><span data-stu-id="711d6-123">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="711d6-124">8</span><span class="sxs-lookup"><span data-stu-id="711d6-124">8</span></span>

<span data-ttu-id="711d6-125">未知的失敗。</span><span class="sxs-lookup"><span data-stu-id="711d6-125">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="711d6-126">**找不到路徑**</span><span class="sxs-lookup"><span data-stu-id="711d6-126">**Path not found**</span></span>
</dt> <dd>

<span data-ttu-id="711d6-127">9</span><span class="sxs-lookup"><span data-stu-id="711d6-127">9</span></span>

<span data-ttu-id="711d6-128">指定的路徑不存在。</span><span class="sxs-lookup"><span data-stu-id="711d6-128">The path specified does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="711d6-129">**參數不正確**</span><span class="sxs-lookup"><span data-stu-id="711d6-129">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="711d6-130">21</span><span class="sxs-lookup"><span data-stu-id="711d6-130">21</span></span>

<span data-ttu-id="711d6-131">指定的參數無效。</span><span class="sxs-lookup"><span data-stu-id="711d6-131">The specified parameter is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="711d6-132">**其他**</span><span class="sxs-lookup"><span data-stu-id="711d6-132">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="711d6-133">22 4294967295</span><span class="sxs-lookup"><span data-stu-id="711d6-133">22 4294967295</span></span>

<span data-ttu-id="711d6-134">針對列出的值以外的值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes) 檔。</span><span class="sxs-lookup"><span data-stu-id="711d6-134">For values other than those listed, refer to the [System Error Codes](/windows/desktop/Debug/system-error-codes) documentation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="711d6-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="711d6-135">Requirements</span></span>



| <span data-ttu-id="711d6-136">需求</span><span class="sxs-lookup"><span data-stu-id="711d6-136">Requirement</span></span> | <span data-ttu-id="711d6-137">值</span><span class="sxs-lookup"><span data-stu-id="711d6-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="711d6-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="711d6-138">Minimum supported client</span></span><br/> | <span data-ttu-id="711d6-139">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="711d6-139">Windows 8.1</span></span><br/>                                                                  |
| <span data-ttu-id="711d6-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="711d6-140">Minimum supported server</span></span><br/> | <span data-ttu-id="711d6-141">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="711d6-141">Windows Server 2012 R2</span></span><br/>                                                       |
| <span data-ttu-id="711d6-142">命名空間</span><span class="sxs-lookup"><span data-stu-id="711d6-142">Namespace</span></span><br/>                | <span data-ttu-id="711d6-143">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="711d6-143">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="711d6-144">MOF</span><span class="sxs-lookup"><span data-stu-id="711d6-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="711d6-145"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="711d6-145"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="711d6-146">DLL</span><span class="sxs-lookup"><span data-stu-id="711d6-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="711d6-147"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="711d6-147"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="711d6-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="711d6-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="711d6-149">**Win32 \_ 進程**</span><span class="sxs-lookup"><span data-stu-id="711d6-149">**Win32\_Process**</span></span>](win32-process.md)
</dt> </dl>

 

