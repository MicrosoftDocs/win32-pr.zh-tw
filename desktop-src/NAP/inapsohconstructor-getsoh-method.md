---
title: 'INapSoHConstructor GetSoH 方法 (NapProtocol .h) '
description: 抓取已建立的 SoHRequest 或 SoHResponse 封包。
ms.assetid: 402c72fd-9e23-453a-8c95-57615295e056
keywords:
- GetSoH 方法 NAP
- GetSoH 方法 NAP，INapSoHConstructor 介面
- INapSoHConstructor 介面 NAP，GetSoH 方法
topic_type:
- apiref
api_name:
- INapSoHConstructor.GetSoH
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 066257aadf0ed14816efec06936d4b070087159f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094487"
---
# <a name="inapsohconstructorgetsoh-method"></a><span data-ttu-id="67dbb-106">INapSoHConstructor：： GetSoH 方法</span><span class="sxs-lookup"><span data-stu-id="67dbb-106">INapSoHConstructor::GetSoH method</span></span>

> [!Note]  
> <span data-ttu-id="67dbb-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="67dbb-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="67dbb-108">**INapSoHConstructor：： GetSoH** 方法會抓取已建立的 SoHRequest 或 SoHResponse 封包。</span><span class="sxs-lookup"><span data-stu-id="67dbb-108">The **INapSoHConstructor::GetSoH** method retrieves the constructed SoHRequest or SoHResponse packet.</span></span>

## <a name="syntax"></a><span data-ttu-id="67dbb-109">語法</span><span class="sxs-lookup"><span data-stu-id="67dbb-109">Syntax</span></span>


```C++
HRESULT GetSoH(
  [out] SoH **soh
);
```



## <a name="parameters"></a><span data-ttu-id="67dbb-110">參數</span><span class="sxs-lookup"><span data-stu-id="67dbb-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67dbb-111">*soh* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="67dbb-111">*soh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="67dbb-112">指向已建立之 [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) 或 **SoHResponse** 封包指標的指標。</span><span class="sxs-lookup"><span data-stu-id="67dbb-112">A pointer to a pointer to the constructed [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) or **SoHResponse** packet.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67dbb-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="67dbb-113">Return value</span></span>

<span data-ttu-id="67dbb-114">也可能傳回其他 COM 特定的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="67dbb-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="67dbb-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="67dbb-115">Return code</span></span>                                                                                     | <span data-ttu-id="67dbb-116">Description</span><span class="sxs-lookup"><span data-stu-id="67dbb-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="67dbb-117"><dt>**S \_確定**</dt></span><span class="sxs-lookup"><span data-stu-id="67dbb-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="67dbb-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="67dbb-118">Operation successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="67dbb-119"><dt>**E \_ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="67dbb-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="67dbb-120">許可權錯誤，拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="67dbb-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="67dbb-121"><dt>**E \_OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="67dbb-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="67dbb-122">系統資源限制，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="67dbb-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="67dbb-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="67dbb-123">Requirements</span></span>



| <span data-ttu-id="67dbb-124">需求</span><span class="sxs-lookup"><span data-stu-id="67dbb-124">Requirement</span></span> | <span data-ttu-id="67dbb-125">值</span><span class="sxs-lookup"><span data-stu-id="67dbb-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="67dbb-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="67dbb-126">Minimum supported client</span></span><br/> | <span data-ttu-id="67dbb-127">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="67dbb-127">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="67dbb-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="67dbb-128">Minimum supported server</span></span><br/> | <span data-ttu-id="67dbb-129">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="67dbb-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="67dbb-130">標頭</span><span class="sxs-lookup"><span data-stu-id="67dbb-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="67dbb-131"><dt>NapProtocol。h</dt></span><span class="sxs-lookup"><span data-stu-id="67dbb-131"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="67dbb-132">Idl</span><span class="sxs-lookup"><span data-stu-id="67dbb-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="67dbb-133"><dt>NapProtocol .idl</dt></span><span class="sxs-lookup"><span data-stu-id="67dbb-133"><dt>NapProtocol.idl</dt></span></span> </dl> |
| <span data-ttu-id="67dbb-134">DLL</span><span class="sxs-lookup"><span data-stu-id="67dbb-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="67dbb-135"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="67dbb-135"><dt>Qutil.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="67dbb-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="67dbb-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67dbb-137">**INapSoHConstructor**</span><span class="sxs-lookup"><span data-stu-id="67dbb-137">**INapSoHConstructor**</span></span>](inapsohconstructor.md)
</dt> </dl>

 

 





