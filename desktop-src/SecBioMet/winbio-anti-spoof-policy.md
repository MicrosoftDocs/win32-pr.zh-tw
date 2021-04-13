---
title: 'WINBIO_ANTI_SPOOF_POLICY 結構 (Winbio \_ 類型 .h) '
description: 表示使用者的 lnk-antispoofing 原則。
ms.assetid: 2B433AE8-21A0-4AF1-853C-9074527DB2E4
keywords:
- WINBIO_ANTI_SPOOF_POLICY 結構 Windows 生物特徵辨識架構 API
- PWINBIO_ANTI_SPOOF_POLICY 結構指標 Windows 生物特徵辨識架構 API
topic_type:
- apiref
api_name:
- WINBIO_ANTI_SPOOF_POLICY
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3da8b7811afb1de1ad464675125f125ef0ceab73
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465829"
---
# <a name="winbio_anti_spoof_policy-structure"></a><span data-ttu-id="4506e-105">WINBIO \_ 反 \_ 詐騙 \_ 原則結構</span><span class="sxs-lookup"><span data-stu-id="4506e-105">WINBIO\_ANTI\_SPOOF\_POLICY structure</span></span>

<span data-ttu-id="4506e-106">表示使用者的 lnk-antispoofing 原則。</span><span class="sxs-lookup"><span data-stu-id="4506e-106">Represents the antispoofing policy for a user.</span></span>

## <a name="syntax"></a><span data-ttu-id="4506e-107">語法</span><span class="sxs-lookup"><span data-stu-id="4506e-107">Syntax</span></span>


```C++
typedef struct _WINBIO_ANTI_SPOOF_POLICY {
  WINBIO_ANTI_SPOOF_POLICY_ACTION Action;
  WINBIO_POLICY_SOURCE            Source;
} WINBIO_ANTI_SPOOF_POLICY, *PWINBIO_ANTI_SPOOF_POLICY;
```



## <a name="members"></a><span data-ttu-id="4506e-108">成員</span><span class="sxs-lookup"><span data-stu-id="4506e-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="4506e-109">**動作**</span><span class="sxs-lookup"><span data-stu-id="4506e-109">**Action**</span></span>
</dt> <dd>

<span data-ttu-id="4506e-110">要針對 lnk-antispoofing 原則採取的動作類型。</span><span class="sxs-lookup"><span data-stu-id="4506e-110">The type of action to take for the antispoofing policy.</span></span>

</dd> <dt>

<span data-ttu-id="4506e-111">**來源**</span><span class="sxs-lookup"><span data-stu-id="4506e-111">**Source**</span></span>
</dt> <dd>

<span data-ttu-id="4506e-112">Lnk-antispoofing 原則的來源。</span><span class="sxs-lookup"><span data-stu-id="4506e-112">The source for the antispoofing policy.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4506e-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="4506e-113">Requirements</span></span>



| <span data-ttu-id="4506e-114">需求</span><span class="sxs-lookup"><span data-stu-id="4506e-114">Requirement</span></span> | <span data-ttu-id="4506e-115">值</span><span class="sxs-lookup"><span data-stu-id="4506e-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4506e-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4506e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="4506e-117">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4506e-117">Windows 10 \[desktop apps only\]</span></span><br/>                                                                                                                              |
| <span data-ttu-id="4506e-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4506e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="4506e-119">僅限 Windows Server 2016 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4506e-119">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="4506e-120">標頭</span><span class="sxs-lookup"><span data-stu-id="4506e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="4506e-121"><dt>Winbio \_ 類型 .h (包含適用于 Winbio 的用戶端應用程式或 Winbio 的 .h \_) </dt></span><span class="sxs-lookup"><span data-stu-id="4506e-121"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4506e-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4506e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4506e-123">**WINBIO \_ 反 \_ 詐騙 \_ 原則 \_ 動作**</span><span class="sxs-lookup"><span data-stu-id="4506e-123">**WINBIO\_ANTI\_SPOOF\_POLICY\_ACTION**</span></span>](winbio-anti-spoof-policy-action.md)
</dt> <dt>

[<span data-ttu-id="4506e-124">**WINBIO \_ 原則 \_ 來源**</span><span class="sxs-lookup"><span data-stu-id="4506e-124">**WINBIO\_POLICY\_SOURCE**</span></span>](winbio-policy-source.md)
</dt> <dt>

[<span data-ttu-id="4506e-125">**WINBIO \_ 非同步 \_ 結果**</span><span class="sxs-lookup"><span data-stu-id="4506e-125">**WINBIO\_ASYNC\_RESULT**</span></span>](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result)
</dt> <dt>

[<span data-ttu-id="4506e-126">**WinBioGetProperty**</span><span class="sxs-lookup"><span data-stu-id="4506e-126">**WinBioGetProperty**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty)
</dt> <dt>

[<span data-ttu-id="4506e-127">**WinBioSetProperty**</span><span class="sxs-lookup"><span data-stu-id="4506e-127">**WinBioSetProperty**</span></span>](/windows/desktop/api/winbio/nf-winbio-winbiosetproperty)
</dt> </dl>

 

 





