---
title: 'HealthClassValue 列舉 (NapProtocol) '
description: 表示健全狀況類別 TLV 的值。
ms.assetid: af80c27a-a686-494b-8795-73eb366deaa0
keywords:
- HealthClassValue 列舉 NAP
topic_type:
- apiref
api_name:
- HealthClassValue
api_location:
- NapProtocol.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ade44b74d03a69d6ccf410a042adf3819b8cc782
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464209"
---
# <a name="healthclassvalue-enumeration"></a><span data-ttu-id="4156d-104">HealthClassValue 列舉</span><span class="sxs-lookup"><span data-stu-id="4156d-104">HealthClassValue enumeration</span></span>

> [!Note]  
> <span data-ttu-id="4156d-105">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="4156d-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="4156d-106">**HealthClassValue** 列舉型別會指出健全狀況類別 TLV 的值。</span><span class="sxs-lookup"><span data-stu-id="4156d-106">The **HealthClassValue** enumeration type indicates the value of the health class TLV.</span></span>

## <a name="syntax"></a><span data-ttu-id="4156d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="4156d-107">Syntax</span></span>


```C++
typedef enum tagHealthClassValue { 
  healthClassFirewall        = 0,
  healthClassPatchLevel      = 1,
  healthClassAntiVirus       = 2,
  healthClassCriticalUpdate  = 3,
  healthClassReserved        = 128
} HealthClassValue;
```



## <a name="constants"></a><span data-ttu-id="4156d-108">常數</span><span class="sxs-lookup"><span data-stu-id="4156d-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="4156d-109"><span id="healthClassFirewall"></span><span id="healthclassfirewall"></span><span id="HEALTHCLASSFIREWALL"></span>**healthClassFirewall**</span><span class="sxs-lookup"><span data-stu-id="4156d-109"><span id="healthClassFirewall"></span><span id="healthclassfirewall"></span><span id="HEALTHCLASSFIREWALL"></span>**healthClassFirewall**</span></span>
</dt> <dd>

<span data-ttu-id="4156d-110">健康情況類別的 TLV 是防火牆。</span><span class="sxs-lookup"><span data-stu-id="4156d-110">The health class TLV is firewall.</span></span>

</dd> <dt>

<span data-ttu-id="4156d-111"><span id="healthClassPatchLevel"></span><span id="healthclasspatchlevel"></span><span id="HEALTHCLASSPATCHLEVEL"></span>**healthClassPatchLevel**</span><span class="sxs-lookup"><span data-stu-id="4156d-111"><span id="healthClassPatchLevel"></span><span id="healthclasspatchlevel"></span><span id="HEALTHCLASSPATCHLEVEL"></span>**healthClassPatchLevel**</span></span>
</dt> <dd>

<span data-ttu-id="4156d-112">健全狀況類別的 TLV 是修補程式等級。</span><span class="sxs-lookup"><span data-stu-id="4156d-112">The health class TLV is patch level.</span></span>

</dd> <dt>

<span data-ttu-id="4156d-113"><span id="healthClassAntiVirus"></span><span id="healthclassantivirus"></span><span id="HEALTHCLASSANTIVIRUS"></span>**healthClassAntiVirus**</span><span class="sxs-lookup"><span data-stu-id="4156d-113"><span id="healthClassAntiVirus"></span><span id="healthclassantivirus"></span><span id="HEALTHCLASSANTIVIRUS"></span>**healthClassAntiVirus**</span></span>
</dt> <dd>

<span data-ttu-id="4156d-114">健康情況類別的 TLV 是防毒軟體。</span><span class="sxs-lookup"><span data-stu-id="4156d-114">The health class TLV is antivirus.</span></span>

</dd> <dt>

<span data-ttu-id="4156d-115"><span id="healthClassCriticalUpdate"></span><span id="healthclasscriticalupdate"></span><span id="HEALTHCLASSCRITICALUPDATE"></span>**healthClassCriticalUpdate**</span><span class="sxs-lookup"><span data-stu-id="4156d-115"><span id="healthClassCriticalUpdate"></span><span id="healthclasscriticalupdate"></span><span id="HEALTHCLASSCRITICALUPDATE"></span>**healthClassCriticalUpdate**</span></span>
</dt> <dd>

<span data-ttu-id="4156d-116">健全狀況類別的 TLV 是重大更新。</span><span class="sxs-lookup"><span data-stu-id="4156d-116">The health class TLV is critical update.</span></span>

</dd> <dt>

<span data-ttu-id="4156d-117"><span id="healthClassReserved"></span><span id="healthclassreserved"></span><span id="HEALTHCLASSRESERVED"></span>**healthClassReserved**</span><span class="sxs-lookup"><span data-stu-id="4156d-117"><span id="healthClassReserved"></span><span id="healthclassreserved"></span><span id="HEALTHCLASSRESERVED"></span>**healthClassReserved**</span></span>
</dt> <dd>

<span data-ttu-id="4156d-118">保留供系統使用。</span><span class="sxs-lookup"><span data-stu-id="4156d-118">Reserved for system use only.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4156d-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="4156d-119">Requirements</span></span>



| <span data-ttu-id="4156d-120">需求</span><span class="sxs-lookup"><span data-stu-id="4156d-120">Requirement</span></span> | <span data-ttu-id="4156d-121">值</span><span class="sxs-lookup"><span data-stu-id="4156d-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="4156d-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4156d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4156d-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4156d-123">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="4156d-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4156d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4156d-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4156d-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="4156d-126">標頭</span><span class="sxs-lookup"><span data-stu-id="4156d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="4156d-127"><dt>NapProtocol。h</dt></span><span class="sxs-lookup"><span data-stu-id="4156d-127"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="4156d-128">Idl</span><span class="sxs-lookup"><span data-stu-id="4156d-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4156d-129"><dt>NapProtocol .idl</dt></span><span class="sxs-lookup"><span data-stu-id="4156d-129"><dt>NapProtocol.idl</dt></span></span> </dl> |



 

 





