---
title: 'INapSoHProcessor Initialize 方法 (NapProtocol .h) '
description: 初始化通訊協定封包和 SoH 處理器系統。 這個方法必須剛好呼叫一次。
ms.assetid: 4fccc847-3c4d-4fc5-935d-28fb2964a9be
keywords:
- Initialize 方法 NAP
- Initialize 方法 NAP，INapSoHProcessor 介面
- INapSoHProcessor 介面 NAP，Initialize 方法
topic_type:
- apiref
api_name:
- INapSoHProcessor.Initialize
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01ff3a32bb213caf19964ccea8175a43e5016f08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934376"
---
# <a name="inapsohprocessorinitialize-method"></a><span data-ttu-id="30072-107">INapSoHProcessor：： Initialize 方法</span><span class="sxs-lookup"><span data-stu-id="30072-107">INapSoHProcessor::Initialize method</span></span>

> [!Note]  
> <span data-ttu-id="30072-108">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="30072-108">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="30072-109">**INapSoHProcessor：： Initialize** 方法會初始化通訊協定封包和 SoH 處理器系統。</span><span class="sxs-lookup"><span data-stu-id="30072-109">The **INapSoHProcessor::Initialize** method initializes the protocol packet and SoH processor system.</span></span> <span data-ttu-id="30072-110">這個方法必須剛好呼叫一次。</span><span class="sxs-lookup"><span data-stu-id="30072-110">This method must be called exactly once.</span></span>

## <a name="syntax"></a><span data-ttu-id="30072-111">語法</span><span class="sxs-lookup"><span data-stu-id="30072-111">Syntax</span></span>


```C++
HRESULT Initialize(
  [in]  const SoH                  *soh,
  [in]        BOOL                 isRequest,
  [out]       SystemHealthEntityId *id
);
```



## <a name="parameters"></a><span data-ttu-id="30072-112">參數</span><span class="sxs-lookup"><span data-stu-id="30072-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30072-113">*soh* \[在\]</span><span class="sxs-lookup"><span data-stu-id="30072-113">*soh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30072-114">要處理的 [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) 封包指標。</span><span class="sxs-lookup"><span data-stu-id="30072-114">A pointer to the [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) packet to be processed.</span></span>

</dd> <dt>

<span data-ttu-id="30072-115">*isRequest* \[在\]</span><span class="sxs-lookup"><span data-stu-id="30072-115">*isRequest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30072-116">如果封包是 [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) ，則 **布林\*\*\*\*值為 TRUE** ，如果是 **SoHResponse**，則為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="30072-116">A **BOOL** that is **TRUE** if the packet is an [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) and **FALSE** if it is an **SoHResponse**.</span></span>

</dd> <dt>

<span data-ttu-id="30072-117">*識別碼* \[ 輸出\]</span><span class="sxs-lookup"><span data-stu-id="30072-117">*id* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="30072-118">唯一的 [SystemHealthEntityId](nap-datatypes.md) ，其中包含用來建立封包之 SHA 或 SHV 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="30072-118">A unique [SystemHealthEntityId](nap-datatypes.md) that contains the ID of the SHA or SHV that constructed the packet.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30072-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="30072-119">Return value</span></span>

<span data-ttu-id="30072-120">也可能傳回其他 COM 特定的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="30072-120">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="30072-121">傳回碼</span><span class="sxs-lookup"><span data-stu-id="30072-121">Return code</span></span>                                                                                            | <span data-ttu-id="30072-122">Description</span><span class="sxs-lookup"><span data-stu-id="30072-122">Description</span></span>                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="30072-123"><dt>**S \_確定**</dt></span><span class="sxs-lookup"><span data-stu-id="30072-123"><dt>**S\_OK** </dt></span></span> </dl>                  | <span data-ttu-id="30072-124">作業成功。</span><span class="sxs-lookup"><span data-stu-id="30072-124">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="30072-125"><dt>**E \_ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="30072-125"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>        | <span data-ttu-id="30072-126">許可權錯誤，拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="30072-126">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="30072-127"><dt>**E \_OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="30072-127"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>         | <span data-ttu-id="30072-128">系統資源限制，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="30072-128">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="30072-129"><dt>**NAP \_ E \_ 不正確封 \_ 包**</dt></span><span class="sxs-lookup"><span data-stu-id="30072-129"><dt>**NAP\_E\_INVALID\_PACKET**</dt></span></span> </dl> | <span data-ttu-id="30072-130">SoH 封包無效。</span><span class="sxs-lookup"><span data-stu-id="30072-130">The SoH packet is invalid.</span></span><br/>                              |



 

## <a name="requirements"></a><span data-ttu-id="30072-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="30072-131">Requirements</span></span>



| <span data-ttu-id="30072-132">需求</span><span class="sxs-lookup"><span data-stu-id="30072-132">Requirement</span></span> | <span data-ttu-id="30072-133">值</span><span class="sxs-lookup"><span data-stu-id="30072-133">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="30072-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="30072-134">Minimum supported client</span></span><br/> | <span data-ttu-id="30072-135">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="30072-135">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="30072-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="30072-136">Minimum supported server</span></span><br/> | <span data-ttu-id="30072-137">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="30072-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="30072-138">標頭</span><span class="sxs-lookup"><span data-stu-id="30072-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="30072-139"><dt>NapProtocol。h</dt></span><span class="sxs-lookup"><span data-stu-id="30072-139"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="30072-140">Idl</span><span class="sxs-lookup"><span data-stu-id="30072-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="30072-141"><dt>NapProtocol .idl</dt></span><span class="sxs-lookup"><span data-stu-id="30072-141"><dt>NapProtocol.idl</dt></span></span> </dl> |
| <span data-ttu-id="30072-142">DLL</span><span class="sxs-lookup"><span data-stu-id="30072-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30072-143"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30072-143"><dt>Qutil.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="30072-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="30072-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30072-145">**INapSoHProcessor**</span><span class="sxs-lookup"><span data-stu-id="30072-145">**INapSoHProcessor**</span></span>](inapsohprocessor.md)
</dt> </dl>

 

 





