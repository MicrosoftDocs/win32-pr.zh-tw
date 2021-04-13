---
UID: ''
title: LsaManageSidNameMapping 函式
description: 從向 LSA 查閱服務註冊的對應集中，加入或移除 SID/名稱對應。
old-location: ''
ms.assetid: na
ms.date: 04/10/2019
ms.keywords: ''
ms.topic: reference
req.header: Ntsecapi.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: Secur32.lib
req.dll:
- Advapi32.dll
- API-MS-Win-DownLevel-AdvAPI32-l4-1-0.dll
- API-MS-Win-security-lsalookup-l2-1-1.dll
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location: ''
api_name:
- LsaManageSidNameMapping
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: fc0065c3964718d690149693f3c71ec4e9f676ec
ms.sourcegitcommit: 382c7259008374408368c173e0027fb641c848fe
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/22/2020
ms.locfileid: "104314493"
---
# <a name="lsamanagesidnamemapping-function"></a><span data-ttu-id="dc3d8-103">LsaManageSidNameMapping 函式</span><span class="sxs-lookup"><span data-stu-id="dc3d8-103">LsaManageSidNameMapping function</span></span>

## <a name="description"></a><span data-ttu-id="dc3d8-104">Description</span><span class="sxs-lookup"><span data-stu-id="dc3d8-104">Description</span></span>

<span data-ttu-id="dc3d8-105">**LsaManageSidNameMapping** 函式會從向 LSA 查閱服務註冊的對應集中，新增或移除 SID/名稱對應。</span><span class="sxs-lookup"><span data-stu-id="dc3d8-105">The **LsaManageSidNameMapping** function adds or removes SID/name mappings from the mapping set registered with the LSA Lookup Service.</span></span>

```cpp
void WINAPI LsaManageSidNameMapping(
  _In_  LSA_SID_NAME_MAPPING_OPERATION_TYPE    OpType,
  _In_  PLSA_SID_NAME_MAPPING_OPERATION_INPUT  OpInput,
  _Out_ PLSA_SID_NAME_MAPPING_OPERATION_OUTPUT *OpOutput
);
```

## <a name="parameters"></a><span data-ttu-id="dc3d8-106">參數</span><span class="sxs-lookup"><span data-stu-id="dc3d8-106">Parameters</span></span>

### <a name="optype-in"></a><span data-ttu-id="dc3d8-107">OpType [in]</span><span class="sxs-lookup"><span data-stu-id="dc3d8-107">OpType [in]</span></span>

<span data-ttu-id="dc3d8-108">指出是否呼叫這個函式來新增或移除 SID/名稱對應。</span><span class="sxs-lookup"><span data-stu-id="dc3d8-108">Indicates if a this function is being called to add or remove an SID/name mapping.</span></span>

### <a name="opinput-in"></a><span data-ttu-id="dc3d8-109">OpInput [in]</span><span class="sxs-lookup"><span data-stu-id="dc3d8-109">OpInput [in]</span></span>

<span data-ttu-id="dc3d8-110">指出要在此作業期間使用的網域、帳戶和 SID 值。</span><span class="sxs-lookup"><span data-stu-id="dc3d8-110">Indicates the domain, account, and SID values to use during this operation.</span></span> <span data-ttu-id="dc3d8-111">您也可以在此結構內設定其他旗標。</span><span class="sxs-lookup"><span data-stu-id="dc3d8-111">Additional flags can also be set within this structure.</span></span>

### <a name="opoutput-out"></a><span data-ttu-id="dc3d8-112">OpOutput [out]</span><span class="sxs-lookup"><span data-stu-id="dc3d8-112">OpOutput [out]</span></span>

<span data-ttu-id="dc3d8-113">包含表示作業成功或失敗的 [LSA_SID_NAME_MAPPING_OPERATION_ERROR](/previous-versions/windows/desktop/legacy/dn280707(v=vs.85)) 值。</span><span class="sxs-lookup"><span data-stu-id="dc3d8-113">Contains a value of [LSA_SID_NAME_MAPPING_OPERATION_ERROR](/previous-versions/windows/desktop/legacy/dn280707(v=vs.85)) that indicates operation success or failure.</span></span>

| <span data-ttu-id="dc3d8-114">值</span><span class="sxs-lookup"><span data-stu-id="dc3d8-114">Value</span></span> | <span data-ttu-id="dc3d8-115">意義</span><span class="sxs-lookup"><span data-stu-id="dc3d8-115">Meaning</span></span> |
|-------|---------|
| <span data-ttu-id="dc3d8-116">「成功」</span><span class="sxs-lookup"><span data-stu-id="dc3d8-116">**Success**</span></span> | <span data-ttu-id="dc3d8-117">作業已完成，未發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="dc3d8-117">Operation is complete without error.</span></span> |
| <span data-ttu-id="dc3d8-118">**NonMappingError**</span><span class="sxs-lookup"><span data-stu-id="dc3d8-118">**NonMappingError**</span></span> | <span data-ttu-id="dc3d8-119">發生與 SID 名稱對應無關的錯誤。</span><span class="sxs-lookup"><span data-stu-id="dc3d8-119">An error unrelated to SID-name mapping has occurred.</span></span> |
| <span data-ttu-id="dc3d8-120">**NameCollision**</span><span class="sxs-lookup"><span data-stu-id="dc3d8-120">**NameCollision**</span></span> | <span data-ttu-id="dc3d8-121">因名稱衝突而導致作業失敗。</span><span class="sxs-lookup"><span data-stu-id="dc3d8-121">Operation failure due to name collision.</span></span> |
| <span data-ttu-id="dc3d8-122">**SidCollision**</span><span class="sxs-lookup"><span data-stu-id="dc3d8-122">**SidCollision**</span></span> | <span data-ttu-id="dc3d8-123">因 SID 衝突而導致作業失敗。</span><span class="sxs-lookup"><span data-stu-id="dc3d8-123">Operation failure due to SID collision.</span></span> |
| <span data-ttu-id="dc3d8-124">**DomainNotFound**</span><span class="sxs-lookup"><span data-stu-id="dc3d8-124">**DomainNotFound**</span></span> | <span data-ttu-id="dc3d8-125">找不到對應的網域。</span><span class="sxs-lookup"><span data-stu-id="dc3d8-125">Corresponding domain not found.</span></span> |
| <span data-ttu-id="dc3d8-126">**DomainSidPrefixMismatch**</span><span class="sxs-lookup"><span data-stu-id="dc3d8-126">**DomainSidPrefixMismatch**</span></span> | <span data-ttu-id="dc3d8-127">提供的 SID 沒有正確的網域前置詞。</span><span class="sxs-lookup"><span data-stu-id="dc3d8-127">Provided SID doesn't have the correct domain prefix.</span></span> |
| <span data-ttu-id="dc3d8-128">**MappingNotFound**</span><span class="sxs-lookup"><span data-stu-id="dc3d8-128">**MappingNotFound**</span></span> | <span data-ttu-id="dc3d8-129">在快取中找不到對應。</span><span class="sxs-lookup"><span data-stu-id="dc3d8-129">Mapping not found in the cache.</span></span> |

## <a name="returns"></a><span data-ttu-id="dc3d8-130">傳回</span><span class="sxs-lookup"><span data-stu-id="dc3d8-130">Returns</span></span>

<span data-ttu-id="dc3d8-131">如果成功插入對應，則傳回值為 STATUS_SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="dc3d8-131">If the mapping is inserted successfully, the return value is STATUS_SUCCESS.</span></span>
<span data-ttu-id="dc3d8-132">否則，如果函式因為 SID 或名稱衝突而失敗，則會傳回 STATUS_INVALID_PARAMETER 錯誤。</span><span class="sxs-lookup"><span data-stu-id="dc3d8-132">Otherwise, if the function fails due to SID or name conflicts, STATUS_INVALID_PARAMETER error will be returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc3d8-133">備註</span><span class="sxs-lookup"><span data-stu-id="dc3d8-133">Remarks</span></span>

## <a name="see-also"></a><span data-ttu-id="dc3d8-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dc3d8-134">See also</span></span>
