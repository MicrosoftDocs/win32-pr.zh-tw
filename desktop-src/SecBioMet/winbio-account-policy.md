---
title: 'WINBIO_ACCOUNT_POLICY 結構 (Winbio \_ adapter .h) '
description: 包含預設或帳戶特定的 lnk-antispoofing 原則。
ms.assetid: 7098FC53-E487-42B2-8B4B-EB7E2D296CB6
keywords:
- WINBIO_ACCOUNT_POLICY 結構 Windows 生物特徵辨識架構 API
- PWINBIO_ACCOUNT_POLICY 結構指標 Windows 生物特徵辨識架構 API
topic_type:
- apiref
api_name:
- WINBIO_ACCOUNT_POLICY
api_location:
- Winbio_adapter.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c734fa6d98615b7708a65ebad1dddc47cdc77cc2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934371"
---
# <a name="winbio_account_policy-structure"></a><span data-ttu-id="be312-105">WINBIO \_ 帳戶 \_ 原則結構</span><span class="sxs-lookup"><span data-stu-id="be312-105">WINBIO\_ACCOUNT\_POLICY structure</span></span>

<span data-ttu-id="be312-106">**WINBIO \_ 帳戶 \_ 原則** 結構包含預設或帳戶特定的 lnk-antispoofing 原則。</span><span class="sxs-lookup"><span data-stu-id="be312-106">The **WINBIO\_ACCOUNT\_POLICY** structure contains either a default or account-specific antispoofing policy.</span></span>

## <a name="syntax"></a><span data-ttu-id="be312-107">語法</span><span class="sxs-lookup"><span data-stu-id="be312-107">Syntax</span></span>


```C++
typedef struct _WINBIO_ACCOUNT_POLICY {
  WINBIO_IDENTITY                 Identity;
  WINBIO_ANTI_SPOOF_POLICY_ACTION AntiSpoofBehavior;
} WINBIO_ACCOUNT_POLICY, *PWINBIO_ACCOUNT_POLICY;
```



## <a name="members"></a><span data-ttu-id="be312-108">成員</span><span class="sxs-lookup"><span data-stu-id="be312-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="be312-109">**身分識別**</span><span class="sxs-lookup"><span data-stu-id="be312-109">**Identity**</span></span>
</dt> <dd>

<span data-ttu-id="be312-110">指定帳戶資訊的 [**WINBIO 身分 \_ 識別**](winbio-identity.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="be312-110">A [**WINBIO\_IDENTITY**](winbio-identity.md) structure that specifies the account information.</span></span>

</dd> <dt>

<span data-ttu-id="be312-111">**AntiSpoofBehavior**</span><span class="sxs-lookup"><span data-stu-id="be312-111">**AntiSpoofBehavior**</span></span>
</dt> <dd>

<span data-ttu-id="be312-112">其中一個 [**WINBIO \_ 反詐騙 \_ \_ 原則 \_ 動作**](winbio-anti-spoof-policy-action.md) 列舉值，指定要對帳戶使用哪個 lnk-antispoofing 原則動作。</span><span class="sxs-lookup"><span data-stu-id="be312-112">One of the [**WINBIO\_ANTI\_SPOOF\_POLICY\_ACTION**](winbio-anti-spoof-policy-action.md) enumeration values that specifies what antispoofing policy action to use for the account.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="be312-113">備註</span><span class="sxs-lookup"><span data-stu-id="be312-113">Remarks</span></span>

<span data-ttu-id="be312-114">如需如何使用此結構的說明，請參閱 [**EngineAdapterSetAccountPolicy**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_account_policy_fn) 方法的討論。</span><span class="sxs-lookup"><span data-stu-id="be312-114">See the discussion of the [**EngineAdapterSetAccountPolicy**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_account_policy_fn) method for a description of how this structure is used.</span></span>

## <a name="requirements"></a><span data-ttu-id="be312-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="be312-115">Requirements</span></span>



| <span data-ttu-id="be312-116">需求</span><span class="sxs-lookup"><span data-stu-id="be312-116">Requirement</span></span> | <span data-ttu-id="be312-117">值</span><span class="sxs-lookup"><span data-stu-id="be312-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be312-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="be312-118">Minimum supported client</span></span><br/> | <span data-ttu-id="be312-119">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="be312-119">Windows 10 \[desktop apps only\]</span></span><br/>                                                                              |
| <span data-ttu-id="be312-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="be312-120">Minimum supported server</span></span><br/> | <span data-ttu-id="be312-121">僅限 Windows Server 2016 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="be312-121">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                     |
| <span data-ttu-id="be312-122">標頭</span><span class="sxs-lookup"><span data-stu-id="be312-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="be312-123"><dt>Winbio \_ adapter .h (包括 Winbio \_ adapter .h) </dt></span><span class="sxs-lookup"><span data-stu-id="be312-123"><dt>Winbio\_adapter.h (include Winbio\_adapter.h)</dt></span></span> </dl> |



 

 





