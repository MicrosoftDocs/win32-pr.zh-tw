---
title: 'WINBIO_PROPERTY_TYPE 常數 (Winbio) '
description: 在 WinBioGetProperty 函數中指定屬性資訊的來源。
ms.assetid: 82C54092-032B-4F32-820E-A1D4BB81ECCE
topic_type:
- apiref
api_name:
- WINBIO_PROPERTY_TYPE_SESSION
- WINBIO_PROPERTY_TYPE_TEMPLATE
- WINBIO_PROPERTY_TYPE_UNIT
- WINBIO_PROPERTY_TYPE_ACCOUNT
api_location:
- Winbio.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f4a1420af18bfa4d2ba5d0457b22cd5f77e7b0c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466997"
---
# <a name="winbio_property_type-constants"></a><span data-ttu-id="3c9d5-103">WINBIO \_ 屬性 \_ 類型常數</span><span class="sxs-lookup"><span data-stu-id="3c9d5-103">WINBIO\_PROPERTY\_TYPE Constants</span></span>

<span data-ttu-id="3c9d5-104">下列 **WINBIO \_ 屬性 \_ 類型** 常數可以用來指定 [**WinBioGetProperty**](/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty) 函數中的屬性資訊來源。</span><span class="sxs-lookup"><span data-stu-id="3c9d5-104">The following **WINBIO\_PROPERTY\_TYPE** constants can be used to specify the source of the property information in the [**WinBioGetProperty**](/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty) function.</span></span>

<dl> <dt>

<span data-ttu-id="3c9d5-105"><span id="WINBIO_PROPERTY_TYPE_SESSION"></span><span id="winbio_property_type_session"></span>**WINBIO \_ 屬性 \_ 類型 \_ 會話**</span><span class="sxs-lookup"><span data-stu-id="3c9d5-105"><span id="WINBIO_PROPERTY_TYPE_SESSION"></span><span id="winbio_property_type_session"></span>**WINBIO\_PROPERTY\_TYPE\_SESSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3c9d5-106">屬性會套用至特定的生物識別會話。</span><span class="sxs-lookup"><span data-stu-id="3c9d5-106">The property applies to a specific biometric session.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3c9d5-107"><span id="WINBIO_PROPERTY_TYPE_TEMPLATE"></span><span id="winbio_property_type_template"></span>**WINBIO \_ 屬性 \_ 類型 \_ 範本**</span><span class="sxs-lookup"><span data-stu-id="3c9d5-107"><span id="WINBIO_PROPERTY_TYPE_TEMPLATE"></span><span id="winbio_property_type_template"></span>**WINBIO\_PROPERTY\_TYPE\_TEMPLATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3c9d5-108">屬性會套用至特定的生物識別範本。</span><span class="sxs-lookup"><span data-stu-id="3c9d5-108">The property applies to a specific biometric template.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3c9d5-109"><span id="WINBIO_PROPERTY_TYPE_UNIT"></span><span id="winbio_property_type_unit"></span>**WINBIO \_ 屬性 \_ 類型 \_ 單位**</span><span class="sxs-lookup"><span data-stu-id="3c9d5-109"><span id="WINBIO_PROPERTY_TYPE_UNIT"></span><span id="winbio_property_type_unit"></span>**WINBIO\_PROPERTY\_TYPE\_UNIT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3c9d5-110">屬性會套用至特定的生物特徵辨識單位。</span><span class="sxs-lookup"><span data-stu-id="3c9d5-110">The property applies to a specific biometric unit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3c9d5-111"><span id="WINBIO_PROPERTY_TYPE_ACCOUNT"></span><span id="winbio_property_type_account"></span>**WINBIO \_ 屬性 \_ 類型 \_ 帳戶**</span><span class="sxs-lookup"><span data-stu-id="3c9d5-111"><span id="WINBIO_PROPERTY_TYPE_ACCOUNT"></span><span id="winbio_property_type_account"></span>**WINBIO\_PROPERTY\_TYPE\_ACCOUNT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3c9d5-112">屬性會套用至具有生物特徵辨識註冊的特定使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="3c9d5-112">The property applies to a specific user account that has a biometric enrollment.</span></span> <span data-ttu-id="3c9d5-113">從 Windows 10 開始支援此值。</span><span class="sxs-lookup"><span data-stu-id="3c9d5-113">This value is supported starting in Windows 10.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3c9d5-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="3c9d5-114">Requirements</span></span>



| <span data-ttu-id="3c9d5-115">需求</span><span class="sxs-lookup"><span data-stu-id="3c9d5-115">Requirement</span></span> | <span data-ttu-id="3c9d5-116">值</span><span class="sxs-lookup"><span data-stu-id="3c9d5-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c9d5-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3c9d5-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3c9d5-118">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3c9d5-118">Windows 7 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="3c9d5-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3c9d5-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3c9d5-120">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3c9d5-120">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="3c9d5-121">標頭</span><span class="sxs-lookup"><span data-stu-id="3c9d5-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c9d5-122"><dt>Winbio (包含 Winbio) </dt></span><span class="sxs-lookup"><span data-stu-id="3c9d5-122"><dt>Winbio.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c9d5-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3c9d5-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c9d5-124">用戶端應用程式常數</span><span class="sxs-lookup"><span data-stu-id="3c9d5-124">Client Application Constants</span></span>](client-application-constants.md)
</dt> <dt>

[<span data-ttu-id="3c9d5-125">**WinBioGetProperty**</span><span class="sxs-lookup"><span data-stu-id="3c9d5-125">**WinBioGetProperty**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty)
</dt> </dl>

 

 





