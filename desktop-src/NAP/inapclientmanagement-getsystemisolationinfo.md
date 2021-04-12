---
title: 'INapClientManagement GetSystemIsolationInfo 方法 (NapManagement .h) '
description: 抓取 NapClient 隔離狀態的相關資訊。
ms.assetid: e1f69e66-71ca-402e-9c94-8af159d00b21
keywords:
- GetSystemIsolationInfo 方法 NAP
- GetSystemIsolationInfo 方法 NAP，INapClientManagement 介面
- INapClientManagement 介面 NAP，GetSystemIsolationInfo 方法
topic_type:
- apiref
api_name:
- INapClientManagement.GetSystemIsolationInfo
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73b3d446e0a8068353be6656c16f0e6796df8922
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385017"
---
# <a name="inapclientmanagementgetsystemisolationinfo-method"></a><span data-ttu-id="ac866-106">INapClientManagement：： GetSystemIsolationInfo 方法</span><span class="sxs-lookup"><span data-stu-id="ac866-106">INapClientManagement::GetSystemIsolationInfo method</span></span>

> [!Note]  
> <span data-ttu-id="ac866-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="ac866-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="ac866-108">**GetSystemIsolationInfo** 方法會抓取 NapClient 的隔離狀態相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ac866-108">The **GetSystemIsolationInfo** method retrieves information about the isolation state of the NapClient.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac866-109">語法</span><span class="sxs-lookup"><span data-stu-id="ac866-109">Syntax</span></span>


```C++
HRESULT GetSystemIsolationInfo(
  [out] IsolationInfo **isolationInfo,
  [out] BOOL          *unknownConnections
) const;
```



## <a name="parameters"></a><span data-ttu-id="ac866-110">參數</span><span class="sxs-lookup"><span data-stu-id="ac866-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac866-111">*isolationInfo* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ac866-111">*isolationInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ac866-112">[**IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo)結構指標的指標，其中包含隔離狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="ac866-112">A pointer to a pointer to an [**IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) structure that contains isolation state information.</span></span>

</dd> <dt>

<span data-ttu-id="ac866-113">*unknownConnections* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ac866-113">*unknownConnections* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ac866-114">旗標的指標，指出是否有任何連接處於未知的狀態。</span><span class="sxs-lookup"><span data-stu-id="ac866-114">A pointer to a flag that indicates whether any of the connections are in an unknown state.</span></span> <span data-ttu-id="ac866-115">如果有的話，旗標會設為 **TRUE**;否則旗標會設為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="ac866-115">If any of them are, the flag is set to **TRUE**; otherwise the flag is set to **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac866-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="ac866-116">Return value</span></span>

<span data-ttu-id="ac866-117">方法會傳回 HRESULT 狀態碼，包括但不限於下列其中一項。</span><span class="sxs-lookup"><span data-stu-id="ac866-117">The method returns an HRESULT status code including but not limited to one of the following.</span></span>



| <span data-ttu-id="ac866-118">傳回碼</span><span class="sxs-lookup"><span data-stu-id="ac866-118">Return code</span></span>                                                                                         | <span data-ttu-id="ac866-119">Description</span><span class="sxs-lookup"><span data-stu-id="ac866-119">Description</span></span>                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="ac866-120"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="ac866-120"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="ac866-121">作業成功。</span><span class="sxs-lookup"><span data-stu-id="ac866-121">Operation successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="ac866-122"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="ac866-122"><dt>**E\_ACCESSDENIED**</dt></span></span> </dl>      | <span data-ttu-id="ac866-123">許可權錯誤，拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="ac866-123">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="ac866-124"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="ac866-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>       | <span data-ttu-id="ac866-125">系統資源限制，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="ac866-125">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="ac866-126"><dt>**RPC \_ E \_ 中斷連接**</dt></span><span class="sxs-lookup"><span data-stu-id="ac866-126"><dt>**RPC\_E\_DISCONNECTED**</dt></span></span> </dl> | <span data-ttu-id="ac866-127">NapAgent 未執行。</span><span class="sxs-lookup"><span data-stu-id="ac866-127">The NapAgent is not running.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="ac866-128">備註</span><span class="sxs-lookup"><span data-stu-id="ac866-128">Remarks</span></span>

<span data-ttu-id="ac866-129">抓取的隔離資訊不會反映不明的狀態。</span><span class="sxs-lookup"><span data-stu-id="ac866-129">The isolation information that is retrieved does not reflect unknown states.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac866-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="ac866-130">Requirements</span></span>



| <span data-ttu-id="ac866-131">需求</span><span class="sxs-lookup"><span data-stu-id="ac866-131">Requirement</span></span> | <span data-ttu-id="ac866-132">值</span><span class="sxs-lookup"><span data-stu-id="ac866-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac866-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ac866-133">Minimum supported client</span></span><br/> | <span data-ttu-id="ac866-134">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ac866-134">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="ac866-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ac866-135">Minimum supported server</span></span><br/> | <span data-ttu-id="ac866-136">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ac866-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="ac866-137">標頭</span><span class="sxs-lookup"><span data-stu-id="ac866-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac866-138"><dt>NapManagement。h</dt></span><span class="sxs-lookup"><span data-stu-id="ac866-138"><dt>NapManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="ac866-139">Idl</span><span class="sxs-lookup"><span data-stu-id="ac866-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ac866-140"><dt>NapManagement .idl</dt></span><span class="sxs-lookup"><span data-stu-id="ac866-140"><dt>NapManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="ac866-141">DLL</span><span class="sxs-lookup"><span data-stu-id="ac866-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ac866-142"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ac866-142"><dt>Qagent.dll</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="ac866-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ac866-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac866-144">**INapClientManagement**</span><span class="sxs-lookup"><span data-stu-id="ac866-144">**INapClientManagement**</span></span>](inapclientmanagement.md)
</dt> </dl>

 

 





