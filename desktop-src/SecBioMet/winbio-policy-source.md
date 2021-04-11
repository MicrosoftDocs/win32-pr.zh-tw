---
title: 'WINBIO_POLICY_SOURCE 列舉 (Winbio \_ 類型 .h) '
description: 列出針對生物特徵辨識因素偵測詐騙的可能來源原則資訊。
ms.assetid: 3DC3BB0B-1FD7-473C-8E0B-B7E0A4A44E9E
keywords:
- WINBIO_POLICY_SOURCE 列舉 Windows 生物特徵辨識架構 API
- PWINBIO_POLICY_SOURCE 列舉指標 Windows 生物特徵辨識架構 API
topic_type:
- apiref
api_name:
- WINBIO_POLICY_SOURCE
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 866d1d82d939f143c4385caa5d94c68ffe3758f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317483"
---
# <a name="winbio_policy_source-enumeration"></a><span data-ttu-id="73745-105">WINBIO \_ 原則 \_ 來源列舉</span><span class="sxs-lookup"><span data-stu-id="73745-105">WINBIO\_POLICY\_SOURCE enumeration</span></span>

<span data-ttu-id="73745-106">列出針對生物特徵辨識因素偵測詐騙的可能來源原則資訊。</span><span class="sxs-lookup"><span data-stu-id="73745-106">Lists the possible sources of policy information for the detection of spoofing for biometric factors.</span></span>

## <a name="syntax"></a><span data-ttu-id="73745-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="73745-107">Syntax</span></span>


```C++
typedef enum _WINBIO_POLICY_SOURCE { 
  WINBIO_POLICY_UNKNOWN  = 0x00000000,
  WINBIO_POLICY_DEFAULT  = 0x00000001,
  WINBIO_POLICY_LOCAL    = 0x00000002,
  WINBIO_POLICY_ADMIN    = 0x00000003
} WINBIO_POLICY_SOURCE, *PWINBIO_POLICY_SOURCE;
```



## <a name="constants"></a><span data-ttu-id="73745-108">常數</span><span class="sxs-lookup"><span data-stu-id="73745-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="73745-109"><span id="WINBIO_POLICY_UNKNOWN"></span><span id="winbio_policy_unknown"></span>**WINBIO \_ 原則 \_ 不明**</span><span class="sxs-lookup"><span data-stu-id="73745-109"><span id="WINBIO_POLICY_UNKNOWN"></span><span id="winbio_policy_unknown"></span>**WINBIO\_POLICY\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="73745-110">原則的來源不明。</span><span class="sxs-lookup"><span data-stu-id="73745-110">The source of the policy is unknown.</span></span>

</dd> <dt>

<span data-ttu-id="73745-111"><span id="WINBIO_POLICY_DEFAULT"></span><span id="winbio_policy_default"></span>**WINBIO \_ 原則 \_ 預設值**</span><span class="sxs-lookup"><span data-stu-id="73745-111"><span id="WINBIO_POLICY_DEFAULT"></span><span id="winbio_policy_default"></span>**WINBIO\_POLICY\_DEFAULT**</span></span>
</dt> <dd>

<span data-ttu-id="73745-112">原則是 Windows 生物特徵辨識架構提供的預設原則。</span><span class="sxs-lookup"><span data-stu-id="73745-112">The policy is the default policy that the Windows Biometric Framework provides.</span></span>

</dd> <dt>

<span data-ttu-id="73745-113"><span id="WINBIO_POLICY_LOCAL"></span><span id="winbio_policy_local"></span>**WINBIO \_ 原則 \_ 本機**</span><span class="sxs-lookup"><span data-stu-id="73745-113"><span id="WINBIO_POLICY_LOCAL"></span><span id="winbio_policy_local"></span>**WINBIO\_POLICY\_LOCAL**</span></span>
</dt> <dd>

<span data-ttu-id="73745-114">個別使用者使用 [ **設定** ] 應用程式為其帳戶設定的原則。</span><span class="sxs-lookup"><span data-stu-id="73745-114">The policy that the individual user set for their account by using the **Settings** app.</span></span> <span data-ttu-id="73745-115">此原則會覆寫預設原則。</span><span class="sxs-lookup"><span data-stu-id="73745-115">This policy overrides the default policy.</span></span>

</dd> <dt>

<span data-ttu-id="73745-116"><span id="WINBIO_POLICY_ADMIN"></span><span id="winbio_policy_admin"></span>**WINBIO \_ 原則 \_ 管理員**</span><span class="sxs-lookup"><span data-stu-id="73745-116"><span id="WINBIO_POLICY_ADMIN"></span><span id="winbio_policy_admin"></span>**WINBIO\_POLICY\_ADMIN**</span></span>
</dt> <dd>

<span data-ttu-id="73745-117">IT 系統管理員為企業設定的群組原則。</span><span class="sxs-lookup"><span data-stu-id="73745-117">A group policy that the IT administrator set for the enterprise.</span></span> <span data-ttu-id="73745-118">個別使用者無法覆寫此原則。</span><span class="sxs-lookup"><span data-stu-id="73745-118">Individual users cannot override this policy.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="73745-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="73745-119">Requirements</span></span>



| <span data-ttu-id="73745-120">需求</span><span class="sxs-lookup"><span data-stu-id="73745-120">Requirement</span></span> | <span data-ttu-id="73745-121">值</span><span class="sxs-lookup"><span data-stu-id="73745-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73745-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="73745-122">Minimum supported client</span></span><br/> | <span data-ttu-id="73745-123">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="73745-123">Windows 10 \[desktop apps only\]</span></span><br/>                                                                                                                              |
| <span data-ttu-id="73745-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="73745-124">Minimum supported server</span></span><br/> | <span data-ttu-id="73745-125">僅限 Windows Server 2016 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="73745-125">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="73745-126">標頭</span><span class="sxs-lookup"><span data-stu-id="73745-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="73745-127"><dt>Winbio \_ 類型 .h (包含適用于 Winbio 的用戶端應用程式或 Winbio 的 .h \_) </dt></span><span class="sxs-lookup"><span data-stu-id="73745-127"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73745-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="73745-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73745-129">**WINBIO \_ 反 \_ 詐騙 \_ 原則 \_ 動作**</span><span class="sxs-lookup"><span data-stu-id="73745-129">**WINBIO\_ANTI\_SPOOF\_POLICY\_ACTION**</span></span>](winbio-anti-spoof-policy-action.md)
</dt> </dl>

 

 





