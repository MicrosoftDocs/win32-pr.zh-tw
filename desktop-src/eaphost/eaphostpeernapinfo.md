---
title: 'EapHostPeerNapInfo 結構 (Eaphostpeerapis .h) '
description: 包含 EAP 要求者 (NAP) 資訊的網路存取保護。
ms.assetid: 703eda56-5932-44d5-ae7f-0a6328d82237
keywords:
- EapHostPeerNapInfo 結構 EAPHost
topic_type:
- apiref
api_name:
- EapHostPeerNapInfo
api_location:
- eaphostpeerapis.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3221f40dea9e84e410a1a643bbbcdc94e9039b21
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025412"
---
# <a name="eaphostpeernapinfo-structure"></a><span data-ttu-id="bb0eb-104">EapHostPeerNapInfo 結構</span><span class="sxs-lookup"><span data-stu-id="bb0eb-104">EapHostPeerNapInfo structure</span></span>

<span data-ttu-id="bb0eb-105">**EapHostPeerNapInfo** 結構包含 EAP 要求者 (NAP) 資訊的網路存取保護。</span><span class="sxs-lookup"><span data-stu-id="bb0eb-105">The **EapHostPeerNapInfo** structure contains the Network Access Protection (NAP) information on an EAP supplicant.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb0eb-106">語法</span><span class="sxs-lookup"><span data-stu-id="bb0eb-106">Syntax</span></span>


```C++
typedef struct _tagEapHostPeerNapInfo {
  ISOLATION_STATE isolationState;
  ProbationTime   probationTime;
  UINT32          stringCorrelationIdLength;
} EapHostPeerNapInfo;
```



## <a name="members"></a><span data-ttu-id="bb0eb-107">成員</span><span class="sxs-lookup"><span data-stu-id="bb0eb-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="bb0eb-108">**isolationState**</span><span class="sxs-lookup"><span data-stu-id="bb0eb-108">**isolationState**</span></span>
</dt> <dd>

<span data-ttu-id="bb0eb-109">指定電腦之 NAP 隔離狀態的 [**隔離 \_ 狀態**](/windows/desktop/api/eaphostpeertypes/ne-eaphostpeertypes-isolation_state) 結構。</span><span class="sxs-lookup"><span data-stu-id="bb0eb-109">An [**ISOLATION\_STATE**](/windows/desktop/api/eaphostpeertypes/ne-eaphostpeertypes-isolation_state) structure that specifies the NAP isolation state of a computer.</span></span> <span data-ttu-id="bb0eb-110">隔離狀態決定授與的網路存取層級。</span><span class="sxs-lookup"><span data-stu-id="bb0eb-110">The isolation state determines the level of network access granted.</span></span>

</dd> <dt>

<span data-ttu-id="bb0eb-111">**probationTime**</span><span class="sxs-lookup"><span data-stu-id="bb0eb-111">**probationTime**</span></span>
</dt> <dd>

<span data-ttu-id="bb0eb-112">**ProbationTime** 結構，指定連接將在中斷之後離開隔離所需的時間。</span><span class="sxs-lookup"><span data-stu-id="bb0eb-112">A **ProbationTime** structure that specifies the time required for the connection to come out of quarantine after which the connection will be dropped.</span></span> <span data-ttu-id="bb0eb-113">**ProbationTime** 結構與 [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime)結構相同。</span><span class="sxs-lookup"><span data-stu-id="bb0eb-113">A **ProbationTime** structure is identical to a [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure.</span></span>

</dd> <dt>

<span data-ttu-id="bb0eb-114">**stringCorrelationIdLength**</span><span class="sxs-lookup"><span data-stu-id="bb0eb-114">**stringCorrelationIdLength**</span></span>
</dt> <dd>

<span data-ttu-id="bb0eb-115">遵循此結構之 NAP [stringCorrelationId](/windows/desktop/NAP/nap-datatypes) 的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="bb0eb-115">The length, in bytes, of the NAP [stringCorrelationId](/windows/desktop/NAP/nap-datatypes) that follows this structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bb0eb-116">備註</span><span class="sxs-lookup"><span data-stu-id="bb0eb-116">Remarks</span></span>

<span data-ttu-id="bb0eb-117">**EapHostPeerNapInfo** 結構會在 RPC 位元組資料流程中 **WCHAR** 資料類型的 NAP [stringCorrelationId](/windows/desktop/NAP/nap-datatypes)之前。</span><span class="sxs-lookup"><span data-stu-id="bb0eb-117">The **EapHostPeerNapInfo** structure precedes the NAP [stringCorrelationId](/windows/desktop/NAP/nap-datatypes) of data type **WCHAR** in the RPC byte stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb0eb-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="bb0eb-118">Requirements</span></span>



| <span data-ttu-id="bb0eb-119">需求</span><span class="sxs-lookup"><span data-stu-id="bb0eb-119">Requirement</span></span> | <span data-ttu-id="bb0eb-120">值</span><span class="sxs-lookup"><span data-stu-id="bb0eb-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb0eb-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bb0eb-121">Minimum supported client</span></span><br/> | <span data-ttu-id="bb0eb-122">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bb0eb-122">Windows 7 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="bb0eb-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bb0eb-123">Minimum supported server</span></span><br/> | <span data-ttu-id="bb0eb-124">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bb0eb-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="bb0eb-125">標頭</span><span class="sxs-lookup"><span data-stu-id="bb0eb-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb0eb-126"><dt>Eaphostpeerapis。h</dt></span><span class="sxs-lookup"><span data-stu-id="bb0eb-126"><dt>Eaphostpeerapis.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb0eb-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bb0eb-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb0eb-128">EAPHost 要求者結構</span><span class="sxs-lookup"><span data-stu-id="bb0eb-128">EAPHost Supplicant Structures</span></span>](eap-host-supplicant-structures.md)
</dt> <dt>

[<span data-ttu-id="bb0eb-129">**EapHostPeerGetAuthStatus**</span><span class="sxs-lookup"><span data-stu-id="bb0eb-129">**EapHostPeerGetAuthStatus**</span></span>](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetauthstatus)
</dt> <dt>

[<span data-ttu-id="bb0eb-130">**EapHostPeerMethodAuthParams**</span><span class="sxs-lookup"><span data-stu-id="bb0eb-130">**EapHostPeerMethodAuthParams**</span></span>](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerauthparams)
</dt> </dl>

 

