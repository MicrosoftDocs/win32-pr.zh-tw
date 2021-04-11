---
title: 'WINBIO_ANTI_SPOOF_POLICY_ACTION 列舉 (Winbio \_ 類型 .h) '
description: 指定您針對使用者的 lnk-antispoofing 原則所採取的動作類型。
ms.assetid: 846C0725-1796-49E4-883C-44AC7D618317
keywords:
- WINBIO_ANTI_SPOOF_POLICY_ACTION 列舉 Windows 生物特徵辨識架構 API
- PWINBIO_ANTI_SPOOF_POLICY 列舉指標 Windows 生物特徵辨識架構 API
topic_type:
- apiref
api_name:
- WINBIO_ANTI_SPOOF_POLICY_ACTION
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5905624bad252475cdde12c003f31a734e64dd2e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934599"
---
# <a name="winbio_anti_spoof_policy_action-enumeration"></a><span data-ttu-id="c7a97-105">WINBIO \_ 反 \_ 詐騙 \_ 原則 \_ 動作列舉</span><span class="sxs-lookup"><span data-stu-id="c7a97-105">WINBIO\_ANTI\_SPOOF\_POLICY\_ACTION enumeration</span></span>

<span data-ttu-id="c7a97-106">指定您針對使用者的 lnk-antispoofing 原則所採取的動作類型。</span><span class="sxs-lookup"><span data-stu-id="c7a97-106">Specifies the types of actions you take for the antispoofing policy of a user.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7a97-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c7a97-107">Syntax</span></span>


```C++
typedef enum _WINBIO_ANTI_SPOOF_POLICY_ACTION { 
  WINBIO_ANTI_SPOOF_DISABLE  = 0x00000000,
  WINBIO_ANTI_SPOOF_ENABLE   = 0x00000001,
  WINBIO_ANTI_SPOOF_REMOVE   = 0x00000002
} WINBIO_ANTI_SPOOF_POLICY_ACTION, *PWINBIO_ANTI_SPOOF_POLICY;
```



## <a name="constants"></a><span data-ttu-id="c7a97-108">常數</span><span class="sxs-lookup"><span data-stu-id="c7a97-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="c7a97-109"><span id="WINBIO_ANTI_SPOOF_DISABLE"></span><span id="winbio_anti_spoof_disable"></span>**WINBIO \_ 反 \_ 欺騙 \_ 停用**</span><span class="sxs-lookup"><span data-stu-id="c7a97-109"><span id="WINBIO_ANTI_SPOOF_DISABLE"></span><span id="winbio_anti_spoof_disable"></span>**WINBIO\_ANTI\_SPOOF\_DISABLE**</span></span>
</dt> <dd>

<span data-ttu-id="c7a97-110">關閉生物識別因素的詐騙偵測。</span><span class="sxs-lookup"><span data-stu-id="c7a97-110">Turns off the detection of spoofing for a biometric factor.</span></span>

</dd> <dt>

<span data-ttu-id="c7a97-111"><span id="WINBIO_ANTI_SPOOF_ENABLE"></span><span id="winbio_anti_spoof_enable"></span>**WINBIO \_ 反 \_ 詐騙 \_ 啟用**</span><span class="sxs-lookup"><span data-stu-id="c7a97-111"><span id="WINBIO_ANTI_SPOOF_ENABLE"></span><span id="winbio_anti_spoof_enable"></span>**WINBIO\_ANTI\_SPOOF\_ENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="c7a97-112">開啟生物識別因素的詐騙偵測。</span><span class="sxs-lookup"><span data-stu-id="c7a97-112">Turns on the detection of spoofing for a biometric factor.</span></span>

</dd> <dt>

<span data-ttu-id="c7a97-113"><span id="WINBIO_ANTI_SPOOF_REMOVE"></span><span id="winbio_anti_spoof_remove"></span>**WINBIO \_ 消除 \_ 詐騙 \_ 移除**</span><span class="sxs-lookup"><span data-stu-id="c7a97-113"><span id="WINBIO_ANTI_SPOOF_REMOVE"></span><span id="winbio_anti_spoof_remove"></span>**WINBIO\_ANTI\_SPOOF\_REMOVE**</span></span>
</dt> <dd>

<span data-ttu-id="c7a97-114">從帳戶中移除生物特徵辨識因素的整個 lnk-antispoofing 原則。</span><span class="sxs-lookup"><span data-stu-id="c7a97-114">Removes the entire antispoofing policy for the biometric factor from the account.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c7a97-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="c7a97-115">Requirements</span></span>



| <span data-ttu-id="c7a97-116">需求</span><span class="sxs-lookup"><span data-stu-id="c7a97-116">Requirement</span></span> | <span data-ttu-id="c7a97-117">值</span><span class="sxs-lookup"><span data-stu-id="c7a97-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7a97-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c7a97-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c7a97-119">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c7a97-119">Windows 10 \[desktop apps only\]</span></span><br/>                                                                                                                              |
| <span data-ttu-id="c7a97-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c7a97-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c7a97-121">僅限 Windows Server 2016 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c7a97-121">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="c7a97-122">標頭</span><span class="sxs-lookup"><span data-stu-id="c7a97-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7a97-123"><dt>Winbio \_ 類型 .h (包含適用于 Winbio 的用戶端應用程式或 Winbio 的 .h \_) </dt></span><span class="sxs-lookup"><span data-stu-id="c7a97-123"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7a97-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c7a97-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7a97-125">**WINBIO \_ 反 \_ 詐騙 \_ 原則 \_ 動作**</span><span class="sxs-lookup"><span data-stu-id="c7a97-125">**WINBIO\_ANTI\_SPOOF\_POLICY\_ACTION**</span></span>](winbio-anti-spoof-policy-action.md)
</dt> <dt>

[<span data-ttu-id="c7a97-126">**WINBIO \_ 原則 \_ 來源**</span><span class="sxs-lookup"><span data-stu-id="c7a97-126">**WINBIO\_POLICY\_SOURCE**</span></span>](winbio-policy-source.md)
</dt> </dl>

 

 





