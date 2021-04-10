---
title: 'INapSystemHealthAgentCallback GetFixupInfo 方法 (NapSystemHealthAgent .h) '
description: 由 NapAgent 呼叫，以判斷系統健康狀態代理程式在處理 SoHResponse 時的狀態。
ms.assetid: cf919b56-3d40-4c49-9c91-25c20ae5ccda
keywords:
- GetFixupInfo 方法 NAP
- GetFixupInfo 方法 NAP，INapSystemHealthAgentCallback 介面
- INapSystemHealthAgentCallback 介面 NAP，GetFixupInfo 方法
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback.GetFixupInfo
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1227cbe870c722189c995bff0c967eb187548cd1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104141"
---
# <a name="inapsystemhealthagentcallbackgetfixupinfo-method"></a><span data-ttu-id="b2c82-106">INapSystemHealthAgentCallback：： GetFixupInfo 方法</span><span class="sxs-lookup"><span data-stu-id="b2c82-106">INapSystemHealthAgentCallback::GetFixupInfo method</span></span>

> [!Note]  
> <span data-ttu-id="b2c82-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="b2c82-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="b2c82-108">**INapSystemHealthAgentCallback：： GetFixupInfo** 方法是由 NapAgent 呼叫，以判斷系統健康狀態代理程式在處理 [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh)時的狀態。</span><span class="sxs-lookup"><span data-stu-id="b2c82-108">The **INapSystemHealthAgentCallback::GetFixupInfo** method is called by the NapAgent to determine the state of the system health agent, while it is processing a [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh).</span></span>

## <a name="syntax"></a><span data-ttu-id="b2c82-109">語法</span><span class="sxs-lookup"><span data-stu-id="b2c82-109">Syntax</span></span>


```C++
HRESULT GetFixupInfo(
  [out] FixupInfo **info
);
```



## <a name="parameters"></a><span data-ttu-id="b2c82-110">參數</span><span class="sxs-lookup"><span data-stu-id="b2c82-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2c82-111">*資訊* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b2c82-111">*info* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b2c82-112">[**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo)結構指標的指標，其中包含代理程式的修正狀態。</span><span class="sxs-lookup"><span data-stu-id="b2c82-112">A pointer to a pointer to a [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) structure that contains the fix-up status of the agent.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2c82-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="b2c82-113">Return value</span></span>

<span data-ttu-id="b2c82-114">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="b2c82-114">This method can return one of these values.</span></span>



| <span data-ttu-id="b2c82-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="b2c82-115">Return code</span></span>                                                                          | <span data-ttu-id="b2c82-116">Description</span><span class="sxs-lookup"><span data-stu-id="b2c82-116">Description</span></span>                   |
|--------------------------------------------------------------------------------------|-------------------------------|
| <dl> <span data-ttu-id="b2c82-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="b2c82-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="b2c82-118">表示成功。</span><span class="sxs-lookup"><span data-stu-id="b2c82-118">Indicates success.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b2c82-119">備註</span><span class="sxs-lookup"><span data-stu-id="b2c82-119">Remarks</span></span>

<span data-ttu-id="b2c82-120">此回呼方法是由 NAP 系統所宣告，而且是由 SHA 寫入器所執行。</span><span class="sxs-lookup"><span data-stu-id="b2c82-120">This callback method is declared by the NAP system and is to be implemented by the SHA writer.</span></span>

<span data-ttu-id="b2c82-121">系統健康狀態代理程式必須立即傳回 **\_ [確定]** ，而不會封鎖。</span><span class="sxs-lookup"><span data-stu-id="b2c82-121">The system health agent must return **S\_OK** immediately without blocking.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2c82-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="b2c82-122">Requirements</span></span>



| <span data-ttu-id="b2c82-123">需求</span><span class="sxs-lookup"><span data-stu-id="b2c82-123">Requirement</span></span> | <span data-ttu-id="b2c82-124">值</span><span class="sxs-lookup"><span data-stu-id="b2c82-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2c82-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b2c82-125">Minimum supported client</span></span><br/> | <span data-ttu-id="b2c82-126">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b2c82-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b2c82-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b2c82-127">Minimum supported server</span></span><br/> | <span data-ttu-id="b2c82-128">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b2c82-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b2c82-129">標頭</span><span class="sxs-lookup"><span data-stu-id="b2c82-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2c82-130"><dt>NapSystemHealthAgent。h</dt></span><span class="sxs-lookup"><span data-stu-id="b2c82-130"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="b2c82-131">Idl</span><span class="sxs-lookup"><span data-stu-id="b2c82-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b2c82-132"><dt>NapSystemHealthAgent .idl</dt></span><span class="sxs-lookup"><span data-stu-id="b2c82-132"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2c82-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b2c82-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2c82-134">**INapSystemHealthAgentCallback**</span><span class="sxs-lookup"><span data-stu-id="b2c82-134">**INapSystemHealthAgentCallback**</span></span>](inapsystemhealthagentcallback.md)
</dt> </dl>

 

 





