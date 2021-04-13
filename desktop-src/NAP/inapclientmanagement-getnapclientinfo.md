---
title: 'INapClientManagement GetNapClientInfo 方法 (NapManagement .h) '
description: 抓取 NAP 用戶端的相關資訊。
ms.assetid: c0b57cab-729b-40b2-81d2-32a961e377a5
keywords:
- GetNapClientInfo 方法 NAP
- GetNapClientInfo 方法 NAP，INapClientManagement 介面
- INapClientManagement 介面 NAP，GetNapClientInfo 方法
topic_type:
- apiref
api_name:
- INapClientManagement.GetNapClientInfo
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a11fc496374f2a7f0b7842e22212013149f44f22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508887"
---
# <a name="inapclientmanagementgetnapclientinfo-method"></a><span data-ttu-id="eaea9-106">INapClientManagement：： GetNapClientInfo 方法</span><span class="sxs-lookup"><span data-stu-id="eaea9-106">INapClientManagement::GetNapClientInfo method</span></span>

> [!Note]  
> <span data-ttu-id="eaea9-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="eaea9-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="eaea9-108">**GetNapClientInfo** 方法會抓取 NAP 用戶端的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="eaea9-108">The **GetNapClientInfo** method retrieves information about the NAP client.</span></span>

## <a name="syntax"></a><span data-ttu-id="eaea9-109">語法</span><span class="sxs-lookup"><span data-stu-id="eaea9-109">Syntax</span></span>


```C++
HRESULT GetNapClientInfo(
  [out] BOOL          *isNapEnabled,
  [out] CountedString **clientName,
  [out] CountedString **clientDescription,
  [out] CountedString **protocolVersion
) const;
```



## <a name="parameters"></a><span data-ttu-id="eaea9-110">參數</span><span class="sxs-lookup"><span data-stu-id="eaea9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eaea9-111">*isNapEnabled* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="eaea9-111">*isNapEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eaea9-112">如果啟用 NAP，則為布林值的指標，設定為 **TRUE** 。否則會設為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="eaea9-112">A pointer to a BOOL that is set to **TRUE** if NAP is enabled; otherwise it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="eaea9-113">*clientName* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="eaea9-113">*clientName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eaea9-114">指向包含用戶端名稱之 [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) 結構指標的指標。</span><span class="sxs-lookup"><span data-stu-id="eaea9-114">A pointer to a pointer to a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure that contains the client name.</span></span>

</dd> <dt>

<span data-ttu-id="eaea9-115">*clientDescription* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="eaea9-115">*clientDescription* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eaea9-116">[**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring)結構指標的指標，其中包含用戶端描述。</span><span class="sxs-lookup"><span data-stu-id="eaea9-116">A pointer to a pointer to a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure that contains the client description.</span></span>

</dd> <dt>

<span data-ttu-id="eaea9-117">*protocolVersion* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="eaea9-117">*protocolVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eaea9-118">[**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring)結構指標的指標，其中包含通訊協定版本。</span><span class="sxs-lookup"><span data-stu-id="eaea9-118">A pointer to a pointer to a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure that contains the protocol version.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eaea9-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="eaea9-119">Return value</span></span>

<span data-ttu-id="eaea9-120">方法會傳回 HRESULT 狀態碼，包括但不限於下列其中一項。</span><span class="sxs-lookup"><span data-stu-id="eaea9-120">The method returns an HRESULT status code including but not limited to one of the following.</span></span>



| <span data-ttu-id="eaea9-121">傳回碼</span><span class="sxs-lookup"><span data-stu-id="eaea9-121">Return code</span></span>                                                                                         | <span data-ttu-id="eaea9-122">Description</span><span class="sxs-lookup"><span data-stu-id="eaea9-122">Description</span></span>                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="eaea9-123"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="eaea9-123"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="eaea9-124">作業成功。</span><span class="sxs-lookup"><span data-stu-id="eaea9-124">Operation successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="eaea9-125"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="eaea9-125"><dt>**E\_ACCESSDENIED**</dt></span></span> </dl>      | <span data-ttu-id="eaea9-126">許可權錯誤，拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="eaea9-126">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="eaea9-127"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="eaea9-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>       | <span data-ttu-id="eaea9-128">系統資源限制，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="eaea9-128">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="eaea9-129"><dt>**RPC \_ E \_ 中斷連接**</dt></span><span class="sxs-lookup"><span data-stu-id="eaea9-129"><dt>**RPC\_E\_DISCONNECTED**</dt></span></span> </dl> | <span data-ttu-id="eaea9-130">NapAgent 未執行。</span><span class="sxs-lookup"><span data-stu-id="eaea9-130">The NapAgent is not running.</span></span><br/>                            |



 

## <a name="requirements"></a><span data-ttu-id="eaea9-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="eaea9-131">Requirements</span></span>



| <span data-ttu-id="eaea9-132">需求</span><span class="sxs-lookup"><span data-stu-id="eaea9-132">Requirement</span></span> | <span data-ttu-id="eaea9-133">值</span><span class="sxs-lookup"><span data-stu-id="eaea9-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="eaea9-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="eaea9-134">Minimum supported client</span></span><br/> | <span data-ttu-id="eaea9-135">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eaea9-135">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="eaea9-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="eaea9-136">Minimum supported server</span></span><br/> | <span data-ttu-id="eaea9-137">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eaea9-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="eaea9-138">標頭</span><span class="sxs-lookup"><span data-stu-id="eaea9-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="eaea9-139"><dt>NapManagement。h</dt></span><span class="sxs-lookup"><span data-stu-id="eaea9-139"><dt>NapManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="eaea9-140">Idl</span><span class="sxs-lookup"><span data-stu-id="eaea9-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="eaea9-141"><dt>NapManagement .idl</dt></span><span class="sxs-lookup"><span data-stu-id="eaea9-141"><dt>NapManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="eaea9-142">DLL</span><span class="sxs-lookup"><span data-stu-id="eaea9-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eaea9-143"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eaea9-143"><dt>Qagent.dll</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="eaea9-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eaea9-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eaea9-145">**INapClientManagement**</span><span class="sxs-lookup"><span data-stu-id="eaea9-145">**INapClientManagement**</span></span>](inapclientmanagement.md)
</dt> </dl>

 

 





