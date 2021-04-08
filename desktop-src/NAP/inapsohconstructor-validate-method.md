---
title: 'INapSoHConstructor Validate 方法 (NapProtocol .h) '
description: 檢查 SoH 封包的有效性。
ms.assetid: 66338213-43c0-461a-a794-5f18d56bd505
keywords:
- 驗證方法 NAP
- 驗證方法 NAP、INapSoHConstructor 介面
- INapSoHConstructor 介面 NAP，Validate 方法
topic_type:
- apiref
api_name:
- INapSoHConstructor.Validate
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7db8a52d7986348e85c724171b6d417996c7315
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686184"
---
# <a name="inapsohconstructorvalidate-method"></a><span data-ttu-id="3de1f-106">INapSoHConstructor：： Validate 方法</span><span class="sxs-lookup"><span data-stu-id="3de1f-106">INapSoHConstructor::Validate method</span></span>

> [!Note]  
> <span data-ttu-id="3de1f-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="3de1f-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="3de1f-108">**INapSoHConstructor：： Validate** 方法會檢查 SoH 封包的有效性。</span><span class="sxs-lookup"><span data-stu-id="3de1f-108">The **INapSoHConstructor::Validate** method checks the validity of the SoH packet.</span></span>

## <a name="syntax"></a><span data-ttu-id="3de1f-109">語法</span><span class="sxs-lookup"><span data-stu-id="3de1f-109">Syntax</span></span>


```C++
HRESULT Validate(
  [in] const SoH  *soh,
  [in]       BOOL isRequest
);
```



## <a name="parameters"></a><span data-ttu-id="3de1f-110">參數</span><span class="sxs-lookup"><span data-stu-id="3de1f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3de1f-111">*soh* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3de1f-111">*soh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3de1f-112">結構化 [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) 封包的指標。</span><span class="sxs-lookup"><span data-stu-id="3de1f-112">A pointer to the constructed [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) packet.</span></span>

</dd> <dt>

<span data-ttu-id="3de1f-113">*isRequest* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3de1f-113">*isRequest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3de1f-114">如果封包是 [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) ，則 **布林\*\*\*\*值為 TRUE** ，如果是 **SoHResponse**，則為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="3de1f-114">A **BOOL** that is **TRUE** if the packet is an [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) and **FALSE** if it is an **SoHResponse**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3de1f-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="3de1f-115">Return value</span></span>

<span data-ttu-id="3de1f-116">也可能傳回其他 COM 特定的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="3de1f-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="3de1f-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="3de1f-117">Return code</span></span>                                                                                            | <span data-ttu-id="3de1f-118">Description</span><span class="sxs-lookup"><span data-stu-id="3de1f-118">Description</span></span>                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="3de1f-119"><dt>**S \_確定**</dt></span><span class="sxs-lookup"><span data-stu-id="3de1f-119"><dt>**S\_OK** </dt></span></span> </dl>                  | <span data-ttu-id="3de1f-120">SoH 封包有效。</span><span class="sxs-lookup"><span data-stu-id="3de1f-120">The SoH packet is valid.</span></span><br/>                                |
| <dl> <span data-ttu-id="3de1f-121"><dt>**E \_ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="3de1f-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>        | <span data-ttu-id="3de1f-122">許可權錯誤，拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="3de1f-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="3de1f-123"><dt>**E \_OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="3de1f-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>         | <span data-ttu-id="3de1f-124">系統資源限制，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="3de1f-124">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="3de1f-125"><dt>**NAP \_ E \_ 不正確封 \_ 包**</dt></span><span class="sxs-lookup"><span data-stu-id="3de1f-125"><dt>**NAP\_E\_INVALID\_PACKET**</dt></span></span> </dl> | <span data-ttu-id="3de1f-126">SoH 封包無效。</span><span class="sxs-lookup"><span data-stu-id="3de1f-126">The SoH packet is invalid.</span></span><br/>                              |



 

## <a name="requirements"></a><span data-ttu-id="3de1f-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="3de1f-127">Requirements</span></span>



| <span data-ttu-id="3de1f-128">需求</span><span class="sxs-lookup"><span data-stu-id="3de1f-128">Requirement</span></span> | <span data-ttu-id="3de1f-129">值</span><span class="sxs-lookup"><span data-stu-id="3de1f-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="3de1f-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3de1f-130">Minimum supported client</span></span><br/> | <span data-ttu-id="3de1f-131">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3de1f-131">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="3de1f-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3de1f-132">Minimum supported server</span></span><br/> | <span data-ttu-id="3de1f-133">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3de1f-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="3de1f-134">標頭</span><span class="sxs-lookup"><span data-stu-id="3de1f-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="3de1f-135"><dt>NapProtocol。h</dt></span><span class="sxs-lookup"><span data-stu-id="3de1f-135"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="3de1f-136">Idl</span><span class="sxs-lookup"><span data-stu-id="3de1f-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3de1f-137"><dt>NapProtocol .idl</dt></span><span class="sxs-lookup"><span data-stu-id="3de1f-137"><dt>NapProtocol.idl</dt></span></span> </dl> |
| <span data-ttu-id="3de1f-138">DLL</span><span class="sxs-lookup"><span data-stu-id="3de1f-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3de1f-139"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3de1f-139"><dt>Qutil.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="3de1f-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3de1f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3de1f-141">**INapSoHConstructor**</span><span class="sxs-lookup"><span data-stu-id="3de1f-141">**INapSoHConstructor**</span></span>](inapsohconstructor.md)
</dt> </dl>

 

 





