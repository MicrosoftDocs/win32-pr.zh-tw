---
title: 'WINBIO_BSP_SCHEMA 結構 (Winbio \_ 類型 .h) '
description: 描述生物特徵辨識服務提供者的功能。
ms.assetid: d690c735-55a1-4e2c-8b39-d52a1972bf93
keywords:
- WINBIO_BSP_SCHEMA 結構 Windows 生物特徵辨識架構 API
- PWINBIO_BSP_SCHEMA 結構指標 Windows 生物特徵辨識架構 API
topic_type:
- apiref
api_name:
- WINBIO_BSP_SCHEMA
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8ae63aefb64eb22f454559b76e9922242ca9530
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465413"
---
# <a name="winbio_bsp_schema-structure"></a><span data-ttu-id="6bb5e-105">WINBIO \_ BSP \_ 架構結構</span><span class="sxs-lookup"><span data-stu-id="6bb5e-105">WINBIO\_BSP\_SCHEMA structure</span></span>

<span data-ttu-id="6bb5e-106">**WINBIO \_ BSP \_ 架構** 結構描述生物特徵辨識服務提供者的功能。</span><span class="sxs-lookup"><span data-stu-id="6bb5e-106">The **WINBIO\_BSP\_SCHEMA** structure describes the capabilities of a biometric service provider.</span></span> <span data-ttu-id="6bb5e-107">[**WinBioEnumServiceProviders**](/windows/desktop/api/Winbio/nf-winbio-winbioenumserviceproviders)函數會使用這個結構。</span><span class="sxs-lookup"><span data-stu-id="6bb5e-107">This structure is used by the [**WinBioEnumServiceProviders**](/windows/desktop/api/Winbio/nf-winbio-winbioenumserviceproviders) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="6bb5e-108">語法</span><span class="sxs-lookup"><span data-stu-id="6bb5e-108">Syntax</span></span>


```C++
typedef struct _WINBIO_BSP_SCHEMA {
  WINBIO_BIOMETRIC_TYPE BiometricFactor;
  WINBIO_UUID           BspId;
  WINBIO_STRING         Description;
  WINBIO_STRING         Vendor;
  WINBIO_VERSION        Version;
} WINBIO_BSP_SCHEMA, *PWINBIO_BSP_SCHEMA;
```



## <a name="members"></a><span data-ttu-id="6bb5e-109">成員</span><span class="sxs-lookup"><span data-stu-id="6bb5e-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="6bb5e-110">**BiometricFactor**</span><span class="sxs-lookup"><span data-stu-id="6bb5e-110">**BiometricFactor**</span></span>
</dt> <dd>

<span data-ttu-id="6bb5e-111">此裝置使用的生物特徵辨識測量型別。</span><span class="sxs-lookup"><span data-stu-id="6bb5e-111">The type of biometric measurement used by this device.</span></span> <span data-ttu-id="6bb5e-112">目前，這必須是 **WINBIO \_ 類型 \_ 指紋**。</span><span class="sxs-lookup"><span data-stu-id="6bb5e-112">Currently this must be **WINBIO\_TYPE\_FINGERPRINT**.</span></span>

</dd> <dt>

<span data-ttu-id="6bb5e-113">**BspId**</span><span class="sxs-lookup"><span data-stu-id="6bb5e-113">**BspId**</span></span>
</dt> <dd>

<span data-ttu-id="6bb5e-114">可唯一識別此生物特徵辨識服務提供者元件的值。</span><span class="sxs-lookup"><span data-stu-id="6bb5e-114">A value that uniquely identifies this biometric service provider component.</span></span>

</dd> <dt>

<span data-ttu-id="6bb5e-115">**說明**</span><span class="sxs-lookup"><span data-stu-id="6bb5e-115">**Description**</span></span>
</dt> <dd>

<span data-ttu-id="6bb5e-116">以 **Null** 終止的 Unicode 字串，其中包含生物識別服務提供者的描述。</span><span class="sxs-lookup"><span data-stu-id="6bb5e-116">A **NULL**-terminated Unicode string that contains a description of the biometric service provider.</span></span>

</dd> <dt>

<span data-ttu-id="6bb5e-117">**廠商**</span><span class="sxs-lookup"><span data-stu-id="6bb5e-117">**Vendor**</span></span>
</dt> <dd>

<span data-ttu-id="6bb5e-118">以 **Null** 終止的 Unicode 字串，其中包含提供生物特徵辨識服務提供者的供應商名稱。</span><span class="sxs-lookup"><span data-stu-id="6bb5e-118">A **NULL**-terminated Unicode string that contains the name of the vendor supplying the biometric service provider.</span></span>

</dd> <dt>

<span data-ttu-id="6bb5e-119">**版本**</span><span class="sxs-lookup"><span data-stu-id="6bb5e-119">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="6bb5e-120">[**WINBIO \_ 版本**](winbio-version.md)結構包含生物特徵辨識服務提供者元件的軟體版本。</span><span class="sxs-lookup"><span data-stu-id="6bb5e-120">A [**WINBIO\_VERSION**](winbio-version.md) structure the contains the software version of the biometric service provider component.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6bb5e-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="6bb5e-121">Requirements</span></span>



| <span data-ttu-id="6bb5e-122">需求</span><span class="sxs-lookup"><span data-stu-id="6bb5e-122">Requirement</span></span> | <span data-ttu-id="6bb5e-123">值</span><span class="sxs-lookup"><span data-stu-id="6bb5e-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6bb5e-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6bb5e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6bb5e-125">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6bb5e-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="6bb5e-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6bb5e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6bb5e-127">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6bb5e-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="6bb5e-128">標頭</span><span class="sxs-lookup"><span data-stu-id="6bb5e-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="6bb5e-129"><dt>Winbio \_ 類型 .h (包含 Winbio .h) </dt></span><span class="sxs-lookup"><span data-stu-id="6bb5e-129"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6bb5e-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6bb5e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bb5e-131">用戶端應用程式結構</span><span class="sxs-lookup"><span data-stu-id="6bb5e-131">Client Application Structures</span></span>](client-application-structures.md)
</dt> <dt>

[<span data-ttu-id="6bb5e-132">**WinBioEnumServiceProviders**</span><span class="sxs-lookup"><span data-stu-id="6bb5e-132">**WinBioEnumServiceProviders**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbioenumserviceproviders)
</dt> </dl>

 

 





