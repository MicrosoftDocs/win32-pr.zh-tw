---
title: 'INapClientManagement RegisterSystemHealthAgent 方法 (NapManagement .h) '
description: 向 NAP 系統註冊 SHA。
ms.assetid: 37acfd11-8282-42ba-ae02-9a45c4509b8b
keywords:
- RegisterSystemHealthAgent 方法 NAP
- RegisterSystemHealthAgent 方法 NAP，INapClientManagement 介面
- INapClientManagement 介面 NAP，RegisterSystemHealthAgent 方法
topic_type:
- apiref
api_name:
- INapClientManagement.RegisterSystemHealthAgent
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 581c49a117a2b8aaa2c4dda2c6573e4a6327b688
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466041"
---
# <a name="inapclientmanagementregistersystemhealthagent-method"></a><span data-ttu-id="442f7-106">INapClientManagement：： RegisterSystemHealthAgent 方法</span><span class="sxs-lookup"><span data-stu-id="442f7-106">INapClientManagement::RegisterSystemHealthAgent method</span></span>

> [!Note]  
> <span data-ttu-id="442f7-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="442f7-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="442f7-108">**RegisterSystemHealthAgent** 方法會向 NAP 系統註冊 SHA。</span><span class="sxs-lookup"><span data-stu-id="442f7-108">The **RegisterSystemHealthAgent** method registers an SHA with the NAP system.</span></span>

## <a name="syntax"></a><span data-ttu-id="442f7-109">語法</span><span class="sxs-lookup"><span data-stu-id="442f7-109">Syntax</span></span>


```C++
HRESULT RegisterSystemHealthAgent(
  [in] const NapComponentRegistrationInfo *agent
);
```



## <a name="parameters"></a><span data-ttu-id="442f7-110">參數</span><span class="sxs-lookup"><span data-stu-id="442f7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="442f7-111">*代理程式* \[在\]</span><span class="sxs-lookup"><span data-stu-id="442f7-111">*agent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="442f7-112">[**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo)結構的指標，其中包含 SHA 的註冊資訊。</span><span class="sxs-lookup"><span data-stu-id="442f7-112">A pointer to a [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) structure that contains the registration information for the SHA.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="442f7-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="442f7-113">Return value</span></span>

<span data-ttu-id="442f7-114">方法會傳回 HRESULT 狀態碼，包括但不限於下列其中一項。</span><span class="sxs-lookup"><span data-stu-id="442f7-114">The method returns an HRESULT status code including but not limited to one of the following.</span></span>



| <span data-ttu-id="442f7-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="442f7-115">Return code</span></span>                                                                                            | <span data-ttu-id="442f7-116">Description</span><span class="sxs-lookup"><span data-stu-id="442f7-116">Description</span></span>                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="442f7-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="442f7-117"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="442f7-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="442f7-118">Operation successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="442f7-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="442f7-119"><dt>**E\_ACCESSDENIED**</dt></span></span> </dl>         | <span data-ttu-id="442f7-120">許可權錯誤，拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="442f7-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="442f7-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="442f7-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>          | <span data-ttu-id="442f7-122">系統資源限制，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="442f7-122">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="442f7-123"><dt>**NAP \_ E \_ 衝突 \_ 識別碼**</dt></span><span class="sxs-lookup"><span data-stu-id="442f7-123"><dt>**NAP\_E\_CONFLICTING\_ID**</dt></span></span> </dl> | <span data-ttu-id="442f7-124">使用此識別碼的 SHA 已經註冊。</span><span class="sxs-lookup"><span data-stu-id="442f7-124">An SHA that uses this ID is already registered.</span></span><br/>         |



 

## <a name="requirements"></a><span data-ttu-id="442f7-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="442f7-125">Requirements</span></span>



| <span data-ttu-id="442f7-126">需求</span><span class="sxs-lookup"><span data-stu-id="442f7-126">Requirement</span></span> | <span data-ttu-id="442f7-127">值</span><span class="sxs-lookup"><span data-stu-id="442f7-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="442f7-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="442f7-128">Minimum supported client</span></span><br/> | <span data-ttu-id="442f7-129">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="442f7-129">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="442f7-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="442f7-130">Minimum supported server</span></span><br/> | <span data-ttu-id="442f7-131">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="442f7-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="442f7-132">標頭</span><span class="sxs-lookup"><span data-stu-id="442f7-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="442f7-133"><dt>NapManagement。h</dt></span><span class="sxs-lookup"><span data-stu-id="442f7-133"><dt>NapManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="442f7-134">Idl</span><span class="sxs-lookup"><span data-stu-id="442f7-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="442f7-135"><dt>NapManagement .idl</dt></span><span class="sxs-lookup"><span data-stu-id="442f7-135"><dt>NapManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="442f7-136">DLL</span><span class="sxs-lookup"><span data-stu-id="442f7-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="442f7-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="442f7-137"><dt>Qagent.dll</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="442f7-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="442f7-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="442f7-139">**INapClientManagement**</span><span class="sxs-lookup"><span data-stu-id="442f7-139">**INapClientManagement**</span></span>](inapclientmanagement.md)
</dt> </dl>

 

 





