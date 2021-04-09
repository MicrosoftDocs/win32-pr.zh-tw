---
title: 'WINBIO_BIOMETRIC_SUBTYPE 常數 (Winbio \_ 類型 .h) '
description: 提供生物特徵辨識測量的相關資訊。
ms.assetid: 019569A9-6184-4E75-9B82-C98F4F45F61A
topic_type:
- apiref
api_name:
- WINBIO_SUBTYPE_NO_INFORMATION
- WINBIO_SUBTYPE_ANY
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba1bc25337bf49a48b54b6b2426673daf8a15bd9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934598"
---
# <a name="winbio_biometric_subtype-constants"></a><span data-ttu-id="f61b3-103">WINBIO \_ 生物特徵辨識 \_ 子類型常數</span><span class="sxs-lookup"><span data-stu-id="f61b3-103">WINBIO\_BIOMETRIC\_SUBTYPE Constants</span></span>

<span data-ttu-id="f61b3-104">**WINBIO \_所有 Windows 生物特徵辨識架構都會使用生物特徵 \_ 子類型** 常數，以提供生物特徵辨識測量的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f61b3-104">**WINBIO\_BIOMETRIC\_SUBTYPE** constants are used throughout the Windows Biometric Framework to provide additional information about a biometric measurement.</span></span> <span data-ttu-id="f61b3-105">當不需要任何子類型或需要任何子型別時，可以使用下列常數。</span><span class="sxs-lookup"><span data-stu-id="f61b3-105">The following constants can be used when no subtype is required or when any subtype is required.</span></span>



| <span data-ttu-id="f61b3-106">常數/值</span><span class="sxs-lookup"><span data-stu-id="f61b3-106">Constant/value</span></span>                                                                                                                                                                                                                                                            | <span data-ttu-id="f61b3-107">Description</span><span class="sxs-lookup"><span data-stu-id="f61b3-107">Description</span></span>                        |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------|
| <span id="WINBIO_SUBTYPE_NO_INFORMATION"></span><span id="winbio_subtype_no_information"></span><dl> <span data-ttu-id="f61b3-108"><dt>**WINBIO \_子類型 \_ 沒有 \_ 資訊**</dt> <dt>0x00</dt></span><span class="sxs-lookup"><span data-stu-id="f61b3-108"><dt>**WINBIO\_SUBTYPE\_NO\_INFORMATION**</dt> <dt>0x00</dt></span></span> </dl> | <span data-ttu-id="f61b3-109">沒有子類型資訊。</span><span class="sxs-lookup"><span data-stu-id="f61b3-109">No subtype information.</span></span><br/> |
| <span id="WINBIO_SUBTYPE_ANY"></span><span id="winbio_subtype_any"></span><dl> <span data-ttu-id="f61b3-110"><dt>**WINBIO \_子類型 \_ 任何**</dt> <dt>0xff</dt></span><span class="sxs-lookup"><span data-stu-id="f61b3-110"><dt>**WINBIO\_SUBTYPE\_ANY**</dt> <dt>0xFF</dt></span></span> </dl>                                   | <span data-ttu-id="f61b3-111">任何子型別。</span><span class="sxs-lookup"><span data-stu-id="f61b3-111">Any subtype.</span></span><br/>            |



## <a name="remarks"></a><span data-ttu-id="f61b3-112">備註</span><span class="sxs-lookup"><span data-stu-id="f61b3-112">Remarks</span></span>

<span data-ttu-id="f61b3-113">若要尋找特定生物特徵辨識類型的可用生物特徵辨識子類型，請使用下表：</span><span class="sxs-lookup"><span data-stu-id="f61b3-113">To find the available biometric subtypes for a particular biometric type, use the following table:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f61b3-114"><strong>WINBIO_BIOMETRIC_TYPE</strong> 值</span><span class="sxs-lookup"><span data-stu-id="f61b3-114"><strong>WINBIO_BIOMETRIC_TYPE</strong> value</span></span></th>
<th><span data-ttu-id="f61b3-115">主題 (s) 尋找 <strong>WINBIO_BIOMETRIC_SUBTYPE</strong> 值</span><span class="sxs-lookup"><span data-stu-id="f61b3-115">Topic(s) to find <strong>WINBIO_BIOMETRIC_SUBTYPE</strong> values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f61b3-116"><strong>WINBIO_TYPE_FACIAL_FEATURES</strong></span><span class="sxs-lookup"><span data-stu-id="f61b3-116"><strong>WINBIO_TYPE_FACIAL_FEATURES</strong></span></span></td>
<td><span data-ttu-id="f61b3-117"><a href="winbio-ansi-385-face-constants.md"><strong>WINBIO_ANSI_385_FACE 常數</strong></a>
</span><span class="sxs-lookup"><span data-stu-id="f61b3-117"><a href="winbio-ansi-385-face-constants.md"><strong>WINBIO_ANSI_385_FACE Constants</strong></a>
</span></span><blockquote>
[!Note]<br />
<span data-ttu-id="f61b3-118">這些值僅適用于 Windows 10 和更新版本。</span><span class="sxs-lookup"><span data-stu-id="f61b3-118">These values apply only for Windows 10 and later.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f61b3-119"><strong>WINBIO_TYPE_FINGERPRINT</strong></span><span class="sxs-lookup"><span data-stu-id="f61b3-119"><strong>WINBIO_TYPE_FINGERPRINT</strong></span></span></td>
<td><span data-ttu-id="f61b3-120">下列其中一個主題：</span><span class="sxs-lookup"><span data-stu-id="f61b3-120">One of the following topics:</span></span>
<ul>
<li><span data-ttu-id="f61b3-121"><a href="winbio-ansi-381-format-constants.md"><strong>WINBIO_ANSI_381_FORMAT 常數</strong></a></span><span class="sxs-lookup"><span data-stu-id="f61b3-121"><a href="winbio-ansi-381-format-constants.md"><strong>WINBIO_ANSI_381_FORMAT Constants</strong></a></span></span></li>
<li><span data-ttu-id="f61b3-122"><a href="winbio-ansi-381-img-constants.md"><strong>WINBIO_ANSI_381_IMG 常數</strong></a></span><span class="sxs-lookup"><span data-stu-id="f61b3-122"><a href="winbio-ansi-381-img-constants.md"><strong>WINBIO_ANSI_381_IMG Constants</strong></a></span></span></li>
<li><span data-ttu-id="f61b3-123"><a href="winbio-ansi-381-img-acq-constants.md"><strong>WINBIO_ANSI_381_IMG_ACQ 常數</strong></a></span><span class="sxs-lookup"><span data-stu-id="f61b3-123"><a href="winbio-ansi-381-img-acq-constants.md"><strong>WINBIO_ANSI_381_IMG_ACQ Constants</strong></a></span></span></li>
<li><span data-ttu-id="f61b3-124"><a href="winbio-ansi-381-imp-type-constants.md"><strong>WINBIO_ANSI_381_IMP_TYPE 常數</strong></a></span><span class="sxs-lookup"><span data-stu-id="f61b3-124"><a href="winbio-ansi-381-imp-type-constants.md"><strong>WINBIO_ANSI_381_IMP_TYPE Constants</strong></a></span></span></li>
<li><span data-ttu-id="f61b3-125"><a href="winbio-ansi-381-pixels-constants.md"><strong>WINBIO_ANSI_381_PIXELS 常數</strong></a></span><span class="sxs-lookup"><span data-stu-id="f61b3-125"><a href="winbio-ansi-381-pixels-constants.md"><strong>WINBIO_ANSI_381_PIXELS Constants</strong></a></span></span></li>
<li><span data-ttu-id="f61b3-126"><a href="winbio-ansi-381-pos-fingerprint-constants.md"><strong>WINBIO_ANSI_381_POS 指紋常數</strong></a></span><span class="sxs-lookup"><span data-stu-id="f61b3-126"><a href="winbio-ansi-381-pos-fingerprint-constants.md"><strong>WINBIO_ANSI_381_POS Fingerprint Constants</strong></a></span></span></li>
<li><span data-ttu-id="f61b3-127"><a href="winbio-ansi-381-pos-palm-constants.md"><strong>WINBIO_ANSI_381_POS_Palm 常數</strong></a></span><span class="sxs-lookup"><span data-stu-id="f61b3-127"><a href="winbio-ansi-381-pos-palm-constants.md"><strong>WINBIO_ANSI_381_POS_Palm Constants</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f61b3-128"><strong>WINBIO_TYPE_IRIS</strong></span><span class="sxs-lookup"><span data-stu-id="f61b3-128"><strong>WINBIO_TYPE_IRIS</strong></span></span></td>
<td><span data-ttu-id="f61b3-129"><a href="winbio-iris-constants.md"><strong>WINBIO_IRIS 常數</strong></a>
</span><span class="sxs-lookup"><span data-stu-id="f61b3-129"><a href="winbio-iris-constants.md"><strong>WINBIO_IRIS Constants</strong></a>
</span></span><blockquote>
[!Note]<br />
<span data-ttu-id="f61b3-130">這些值僅適用于 Windows 10 和更新版本。</span><span class="sxs-lookup"><span data-stu-id="f61b3-130">These values apply only for Windows 10 and later.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f61b3-131"><strong>WINBIO_TYPE_VOICE</strong></span><span class="sxs-lookup"><span data-stu-id="f61b3-131"><strong>WINBIO_TYPE_VOICE</strong></span></span></td>
<td><span data-ttu-id="f61b3-132"><a href="https://www.bing.com/search?q=<strong>WINBIO_VOICE+Constants</strong>"><strong>WINBIO_VOICE 常數</strong></a>
</span><span class="sxs-lookup"><span data-stu-id="f61b3-132"><a href="https://www.bing.com/search?q=<strong>WINBIO_VOICE+Constants</strong>"><strong>WINBIO_VOICE Constants</strong></a>
</span></span><blockquote>
[!Note]<br />
<span data-ttu-id="f61b3-133">這些值僅適用于 Windows 10 和更新版本。</span><span class="sxs-lookup"><span data-stu-id="f61b3-133">These values apply only for Windows 10 and later.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="f61b3-134">如需詳細資訊，請參閱 [用戶端應用程式常數](client-application-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="f61b3-134">For more information, see [Client Application Constants](client-application-constants.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f61b3-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="f61b3-135">Requirements</span></span>



| <span data-ttu-id="f61b3-136">需求</span><span class="sxs-lookup"><span data-stu-id="f61b3-136">Requirement</span></span> | <span data-ttu-id="f61b3-137">值</span><span class="sxs-lookup"><span data-stu-id="f61b3-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f61b3-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f61b3-138">Minimum supported client</span></span><br/> | <span data-ttu-id="f61b3-139">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f61b3-139">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="f61b3-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f61b3-140">Minimum supported server</span></span><br/> | <span data-ttu-id="f61b3-141">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f61b3-141">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="f61b3-142">標頭</span><span class="sxs-lookup"><span data-stu-id="f61b3-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="f61b3-143"><dt>Winbio \_ 類型 .h (包含 Winbio .h) </dt></span><span class="sxs-lookup"><span data-stu-id="f61b3-143"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



 

 





