---
title: 'WINBIO_CAPABILITY 常數 (Winbio \_ 類型 .h) '
description: 指紋感應器子類型。
ms.assetid: D447273E-2A02-484E-B0E4-69FEADD15797
topic_type:
- apiref
api_name:
- WINBIO_CAPABILITY_SENSOR
- WINBIO_CAPABILITY_MATCHING
- WINBIO_CAPABILITY_DATABASE
- WINBIO_CAPABILITY_PROCESSING
- WINBIO_CAPABILITY_ENCRYPTION
- WINBIO_CAPABILITY_NAVIGATION
- WINBIO_CAPABILITY_INDICATOR
- WINBIO_CAPABILITY_VIRTUAL_SENSOR
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f16de3f496e5c3723722bb7aae22c81eb27c968
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843620"
---
# <a name="winbio_capability-constants"></a><span data-ttu-id="f0d1a-103">WINBIO \_ 功能常數</span><span class="sxs-lookup"><span data-stu-id="f0d1a-103">WINBIO\_CAPABILITY Constants</span></span>

<span data-ttu-id="f0d1a-104">下列指紋感應器子類型為 **WINBIO 的 \_ 功能** 值，可用來做為 [**WINBIO \_ 單元 \_ 架構**](winbio-unit-schema.md)之 *功能* 參數的位元遮罩。</span><span class="sxs-lookup"><span data-stu-id="f0d1a-104">The following fingerprint sensor sub types are **WINBIO\_CAPABILITIES** values that can be used as a bitmask for the *Capabilities* parameter of the [**WINBIO\_UNIT\_SCHEMA**](winbio-unit-schema.md) structure.</span></span> <span data-ttu-id="f0d1a-105">這些是指上架的感應器功能。</span><span class="sxs-lookup"><span data-stu-id="f0d1a-105">These refer to the onboard sensor capabilities.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="f0d1a-106">常數/值</span><span class="sxs-lookup"><span data-stu-id="f0d1a-106">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="f0d1a-107">Description</span><span class="sxs-lookup"><span data-stu-id="f0d1a-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="WINBIO_CAPABILITY_SENSOR"></span><span id="winbio_capability_sensor"></span><dl> <span data-ttu-id="f0d1a-108"><dt><strong>WINBIO_CAPABILITY_SENSOR</strong></dt> <dt>0x00000001</dt> </span><span class="sxs-lookup"><span data-stu-id="f0d1a-108"><dt><strong>WINBIO_CAPABILITY_SENSOR</strong></dt> <dt>0x00000001</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f0d1a-109">感應器可以捕獲生物特徵辨識資料。</span><span class="sxs-lookup"><span data-stu-id="f0d1a-109">The sensor can capture biometric data.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WINBIO_CAPABILITY_MATCHING"></span><span id="winbio_capability_matching"></span><dl> <span data-ttu-id="f0d1a-110"><dt><strong>WINBIO_CAPABILITY_MATCHING</strong></dt> <dt>0x00000002</dt> </span><span class="sxs-lookup"><span data-stu-id="f0d1a-110"><dt><strong>WINBIO_CAPABILITY_MATCHING</strong></dt> <dt>0x00000002</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f0d1a-111">感應器可將生物特徵辨識資料與身分識別進行比對。</span><span class="sxs-lookup"><span data-stu-id="f0d1a-111">The sensor can match biometric data to an identity.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WINBIO_CAPABILITY_DATABASE"></span><span id="winbio_capability_database"></span><dl> <span data-ttu-id="f0d1a-112"><dt><strong>WINBIO_CAPABILITY_DATABASE</strong></dt> <dt>0x00000004</dt> </span><span class="sxs-lookup"><span data-stu-id="f0d1a-112"><dt><strong>WINBIO_CAPABILITY_DATABASE</strong></dt> <dt>0x00000004</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f0d1a-113">感應器包含上架資料庫。</span><span class="sxs-lookup"><span data-stu-id="f0d1a-113">The sensor contains an onboard database.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WINBIO_CAPABILITY_PROCESSING"></span><span id="winbio_capability_processing"></span><dl> <span data-ttu-id="f0d1a-114"><dt><strong>WINBIO_CAPABILITY_PROCESSING</strong></dt> <dt>0x00000008</dt> </span><span class="sxs-lookup"><span data-stu-id="f0d1a-114"><dt><strong>WINBIO_CAPABILITY_PROCESSING</strong></dt> <dt>0x00000008</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f0d1a-115">感應器可以執行生物特徵辨識處理。</span><span class="sxs-lookup"><span data-stu-id="f0d1a-115">The sensor can perform biometric processing.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WINBIO_CAPABILITY_ENCRYPTION"></span><span id="winbio_capability_encryption"></span><dl> <span data-ttu-id="f0d1a-116"><dt><strong>WINBIO_CAPABILITY_ENCRYPTION</strong></dt> <dt>0x00000010</dt> </span><span class="sxs-lookup"><span data-stu-id="f0d1a-116"><dt><strong>WINBIO_CAPABILITY_ENCRYPTION</strong></dt> <dt>0x00000010</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f0d1a-117">感應器可以加密生物特徵辨識資料。</span><span class="sxs-lookup"><span data-stu-id="f0d1a-117">The sensor can encrypt biometric data.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WINBIO_CAPABILITY_NAVIGATION"></span><span id="winbio_capability_navigation"></span><dl> <span data-ttu-id="f0d1a-118"><dt><strong>WINBIO_CAPABILITY_NAVIGATION</strong></dt> <dt>0x00000020</dt> </span><span class="sxs-lookup"><span data-stu-id="f0d1a-118"><dt><strong>WINBIO_CAPABILITY_NAVIGATION</strong></dt> <dt>0x00000020</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f0d1a-119">感應器可作為滑鼠墊。</span><span class="sxs-lookup"><span data-stu-id="f0d1a-119">The sensor can act as a mouse pad.</span></span> <span data-ttu-id="f0d1a-120">目前不支援。</span><span class="sxs-lookup"><span data-stu-id="f0d1a-120">This is currently not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WINBIO_CAPABILITY_INDICATOR"></span><span id="winbio_capability_indicator"></span><dl> <span data-ttu-id="f0d1a-121"><dt><strong>WINBIO_CAPABILITY_INDICATOR</strong></dt> <dt>0x00000040</dt> </span><span class="sxs-lookup"><span data-stu-id="f0d1a-121"><dt><strong>WINBIO_CAPABILITY_INDICATOR</strong></dt> <dt>0x00000040</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f0d1a-122">感應器包含指標燈。</span><span class="sxs-lookup"><span data-stu-id="f0d1a-122">The sensor contains an indicator light.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WINBIO_CAPABILITY_VIRTUAL_SENSOR"></span><span id="winbio_capability_virtual_sensor"></span><dl> <span data-ttu-id="f0d1a-123"><dt><strong>WINBIO_CAPABILITY_VIRTUAL_SENSOR</strong></dt> <dt>0x00000080</dt> </span><span class="sxs-lookup"><span data-stu-id="f0d1a-123"><dt><strong>WINBIO_CAPABILITY_VIRTUAL_SENSOR</strong></dt> <dt>0x00000080</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f0d1a-124">感應器介面卡會管理它自己的生物特徵辨識硬體連接。</span><span class="sxs-lookup"><span data-stu-id="f0d1a-124">The sensor adapter manages its own connection to the biometric hardware.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="f0d1a-125">這個常數只適用于 Windows 10 和更新版本。</span><span class="sxs-lookup"><span data-stu-id="f0d1a-125">This constant applies only for Windows 10 and later.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="f0d1a-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="f0d1a-126">Requirements</span></span>



| <span data-ttu-id="f0d1a-127">需求</span><span class="sxs-lookup"><span data-stu-id="f0d1a-127">Requirement</span></span> | <span data-ttu-id="f0d1a-128">值</span><span class="sxs-lookup"><span data-stu-id="f0d1a-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0d1a-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f0d1a-129">Minimum supported client</span></span><br/> | <span data-ttu-id="f0d1a-130">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f0d1a-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                                                                                               |
| <span data-ttu-id="f0d1a-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f0d1a-131">Minimum supported server</span></span><br/> | <span data-ttu-id="f0d1a-132">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f0d1a-132">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                                                                                  |
| <span data-ttu-id="f0d1a-133">標頭</span><span class="sxs-lookup"><span data-stu-id="f0d1a-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0d1a-134"><dt>Winbio \_ 類型 .h (包含適用于 Winbio 的用戶端應用程式或 Winbio 的 .h \_) </dt></span><span class="sxs-lookup"><span data-stu-id="f0d1a-134"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0d1a-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f0d1a-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0d1a-136">用戶端應用程式常數</span><span class="sxs-lookup"><span data-stu-id="f0d1a-136">Client Application Constants</span></span>](client-application-constants.md)
</dt> <dt>

[<span data-ttu-id="f0d1a-137">**WINBIO \_ 單元 \_ 架構**</span><span class="sxs-lookup"><span data-stu-id="f0d1a-137">**WINBIO\_UNIT\_SCHEMA**</span></span>](winbio-unit-schema.md)
</dt> </dl>

 

 





