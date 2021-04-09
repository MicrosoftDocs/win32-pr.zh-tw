---
title: 'INapClientManagement2 GetSystemIsolationInfoEx 方法 (NapManagement .h) '
description: 抓取 NapClient 的隔離狀態和擴充隔離狀態的相關資訊。
ms.assetid: 614bcf19-873e-4043-98b2-dcb152bae3e2
keywords:
- GetSystemIsolationInfoEx 方法 NAP
- GetSystemIsolationInfoEx 方法 NAP，INapClientManagement2 介面
- INapClientManagement2 介面 NAP，GetSystemIsolationInfoEx 方法
topic_type:
- apiref
api_name:
- INapClientManagement2.GetSystemIsolationInfoEx
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e75a6554ea7e55c3bebe35b797f888494a55627
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024894"
---
# <a name="inapclientmanagement2getsystemisolationinfoex-method"></a><span data-ttu-id="53ba3-106">INapClientManagement2：： GetSystemIsolationInfoEx 方法</span><span class="sxs-lookup"><span data-stu-id="53ba3-106">INapClientManagement2::GetSystemIsolationInfoEx method</span></span>

> [!Note]  
> <span data-ttu-id="53ba3-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="53ba3-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="53ba3-108">**GetSystemIsolationInfoEx** 方法會抓取 NapClient 的隔離狀態和擴充隔離狀態的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="53ba3-108">The **GetSystemIsolationInfoEx** method retrieves information about the isolation state and extended isolation state of the NapClient.</span></span>

## <a name="syntax"></a><span data-ttu-id="53ba3-109">語法</span><span class="sxs-lookup"><span data-stu-id="53ba3-109">Syntax</span></span>


```C++
HRESULT GetSystemIsolationInfoEx(
  [out] IsolationInfoEx **isolationInfo,
  [out] BOOL            *unknownConnections
) const;
```



## <a name="parameters"></a><span data-ttu-id="53ba3-110">參數</span><span class="sxs-lookup"><span data-stu-id="53ba3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53ba3-111">*isolationInfo* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="53ba3-111">*isolationInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="53ba3-112">[**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex)結構指標的指標，其中包含隔離狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="53ba3-112">A pointer to a pointer to an [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) structure that contains isolation state information.</span></span>

</dd> <dt>

<span data-ttu-id="53ba3-113">*unknownConnections* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="53ba3-113">*unknownConnections* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="53ba3-114">布林值的指標，如果有任何連接處於未知狀態，則為 **TRUE** ，否則為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="53ba3-114">A pointer to a BOOL that is **TRUE** if any of the connections are in an unknown state and **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53ba3-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="53ba3-115">Return value</span></span>

<span data-ttu-id="53ba3-116">方法會傳回 HRESULT 狀態碼，包括但不限於下列其中一項。</span><span class="sxs-lookup"><span data-stu-id="53ba3-116">The method returns an HRESULT status code including but not limited to one of the following.</span></span>



| <span data-ttu-id="53ba3-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="53ba3-117">Return code</span></span>                                                                                         | <span data-ttu-id="53ba3-118">Description</span><span class="sxs-lookup"><span data-stu-id="53ba3-118">Description</span></span>                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="53ba3-119"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="53ba3-119"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="53ba3-120">作業成功。</span><span class="sxs-lookup"><span data-stu-id="53ba3-120">Operation successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="53ba3-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="53ba3-121"><dt>**E\_ACCESSDENIED**</dt></span></span> </dl>      | <span data-ttu-id="53ba3-122">許可權錯誤，拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="53ba3-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="53ba3-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="53ba3-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>       | <span data-ttu-id="53ba3-124">系統資源限制，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="53ba3-124">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="53ba3-125"><dt>**RPC \_ E \_ 中斷連接**</dt></span><span class="sxs-lookup"><span data-stu-id="53ba3-125"><dt>**RPC\_E\_DISCONNECTED**</dt></span></span> </dl> | <span data-ttu-id="53ba3-126">NapAgent 未執行。</span><span class="sxs-lookup"><span data-stu-id="53ba3-126">The NapAgent is not running.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="53ba3-127">備註</span><span class="sxs-lookup"><span data-stu-id="53ba3-127">Remarks</span></span>

<span data-ttu-id="53ba3-128">抓取的隔離資訊不會反映不明的狀態。</span><span class="sxs-lookup"><span data-stu-id="53ba3-128">The isolation information that is retrieved does not reflect unknown states.</span></span>

<span data-ttu-id="53ba3-129">SHA 必須藉由呼叫 [**FreeIsolationInfoEx**](freeisolationinfoex.md)來釋放 [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex)結構。</span><span class="sxs-lookup"><span data-stu-id="53ba3-129">The SHA must free the [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) structure by calling [**FreeIsolationInfoEx**](freeisolationinfoex.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="53ba3-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="53ba3-130">Requirements</span></span>



| <span data-ttu-id="53ba3-131">需求</span><span class="sxs-lookup"><span data-stu-id="53ba3-131">Requirement</span></span> | <span data-ttu-id="53ba3-132">值</span><span class="sxs-lookup"><span data-stu-id="53ba3-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="53ba3-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="53ba3-133">Minimum supported client</span></span><br/> | <span data-ttu-id="53ba3-134">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="53ba3-134">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="53ba3-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="53ba3-135">Minimum supported server</span></span><br/> | <span data-ttu-id="53ba3-136">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="53ba3-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="53ba3-137">標頭</span><span class="sxs-lookup"><span data-stu-id="53ba3-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="53ba3-138"><dt>NapManagement。h</dt></span><span class="sxs-lookup"><span data-stu-id="53ba3-138"><dt>NapManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="53ba3-139">Idl</span><span class="sxs-lookup"><span data-stu-id="53ba3-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="53ba3-140"><dt>NapManagement .idl</dt></span><span class="sxs-lookup"><span data-stu-id="53ba3-140"><dt>NapManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="53ba3-141">DLL</span><span class="sxs-lookup"><span data-stu-id="53ba3-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="53ba3-142"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53ba3-142"><dt>Qagent.dll</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="53ba3-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="53ba3-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53ba3-144">**INapClientManagement2**</span><span class="sxs-lookup"><span data-stu-id="53ba3-144">**INapClientManagement2**</span></span>](inapclientmanagement2.md)
</dt> </dl>

 

 





