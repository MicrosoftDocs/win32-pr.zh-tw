---
title: 'WINBIO_BDB_ANSI_381_HEADER 結構 (Winbio \_ 類型 .h) '
description: 指定一系列指紋或棕櫚範例的相關資訊。
ms.assetid: 8b0caa50-9bba-45c4-b4bf-514540894793
keywords:
- WINBIO_BDB_ANSI_381_HEADER 結構 Windows 生物特徵辨識架構 API
topic_type:
- apiref
api_name:
- WINBIO_BDB_ANSI_381_HEADER
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9da04643bbdff273a2594394011ba46c16bfa29d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106996181"
---
# <a name="winbio_bdb_ansi_381_header-structure"></a><span data-ttu-id="a31c7-104">WINBIO \_ BDB \_ ANSI \_ 381 \_ 標頭結構</span><span class="sxs-lookup"><span data-stu-id="a31c7-104">WINBIO\_BDB\_ANSI\_381\_HEADER structure</span></span>

<span data-ttu-id="a31c7-105">**WINBIO \_ BDB \_ ANSI \_ 381 \_ 標頭** 結構會指定一系列指紋或棕櫚範例的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a31c7-105">The **WINBIO\_BDB\_ANSI\_381\_HEADER** structure specifies information about a series of fingerprint or palm samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="a31c7-106">語法</span><span class="sxs-lookup"><span data-stu-id="a31c7-106">Syntax</span></span>


```C++
typedef struct _WINBIO_BDB_ANSI_381_HEADER {
  ULONG64                  RecordLength;
  ULONG                    FormatIdentifier;
  ULONG                    VersionNumber;
  WINBIO_REGISTERED_FORMAT ProductId;
  USHORT                   CaptureDeviceId;
  USHORT                   ImageAcquisitionLevel;
  USHORT                   HorizontalScanResolution;
  USHORT                   VerticalScanResolution;
  USHORT                   HorizontalImageResolution;
  USHORT                   VerticalImageResolution;
  UCHAR                    ElementCount;
  UCHAR                    ScaleUnits;
  UCHAR                    PixelDepth;
  UCHAR                    ImageCompressionAlg;
  USHORT                   Reserved;
} WINBIO_BDB_ANSI_381_HEADER;
```



## <a name="members"></a><span data-ttu-id="a31c7-107">成員</span><span class="sxs-lookup"><span data-stu-id="a31c7-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="a31c7-108">**RecordLength**</span><span class="sxs-lookup"><span data-stu-id="a31c7-108">**RecordLength**</span></span>
</dt> <dd>

<span data-ttu-id="a31c7-109">此結構的大小（以位元組為單位），以及從終端使用者所捕獲之指紋或 palm 範例的所有 [**WINBIO \_ BDB \_ ANSI \_ 381 \_ 記錄**](winbio-bdb-ansi-381-record.md) 結構的大小。</span><span class="sxs-lookup"><span data-stu-id="a31c7-109">The size, in bytes, of this structure plus the size of all [**WINBIO\_BDB\_ANSI\_381\_RECORD**](winbio-bdb-ansi-381-record.md) structures for the fingerprint or palm samples captured from an end user.</span></span> <span data-ttu-id="a31c7-110">只有低6個位元組有效。</span><span class="sxs-lookup"><span data-stu-id="a31c7-110">Only the low six bytes are valid.</span></span>

</dd> <dt>

<span data-ttu-id="a31c7-111">**FormatIdentifier**</span><span class="sxs-lookup"><span data-stu-id="a31c7-111">**FormatIdentifier**</span></span>
</dt> <dd>

<span data-ttu-id="a31c7-112">指定格式。</span><span class="sxs-lookup"><span data-stu-id="a31c7-112">Specifies the format.</span></span> <span data-ttu-id="a31c7-113">目前，這必須是0x46495200。</span><span class="sxs-lookup"><span data-stu-id="a31c7-113">Currently, this must be 0x46495200.</span></span>

</dd> <dt>

<span data-ttu-id="a31c7-114">**VersionNumber**</span><span class="sxs-lookup"><span data-stu-id="a31c7-114">**VersionNumber**</span></span>
</dt> <dd>

<span data-ttu-id="a31c7-115">指定版本號碼。</span><span class="sxs-lookup"><span data-stu-id="a31c7-115">Specifies the version number.</span></span> <span data-ttu-id="a31c7-116">目前，這必須是0x30313000，它會在內部對應至0.1.0.0 版。</span><span class="sxs-lookup"><span data-stu-id="a31c7-116">Currently this must be 0x30313000 which corresponds internally to 0.1.0.0.</span></span>

</dd> <dt>

<span data-ttu-id="a31c7-117">**ProductId**</span><span class="sxs-lookup"><span data-stu-id="a31c7-117">**ProductId**</span></span>
</dt> <dd>

<span data-ttu-id="a31c7-118">[**WINBIO \_ 註冊的 \_ 格式**](winbio-registered-format.md)結構，其中包含已註冊的資料格式作為擁有者/型別配對。</span><span class="sxs-lookup"><span data-stu-id="a31c7-118">A [**WINBIO\_REGISTERED\_FORMAT**](winbio-registered-format.md) structure that contains the registered data format as an owner/type pair.</span></span>

</dd> <dt>

<span data-ttu-id="a31c7-119">**CaptureDeviceId**</span><span class="sxs-lookup"><span data-stu-id="a31c7-119">**CaptureDeviceId**</span></span>
</dt> <dd>

<span data-ttu-id="a31c7-120">包含用來捕捉範例之裝置的單位識別碼。</span><span class="sxs-lookup"><span data-stu-id="a31c7-120">Contains the unit ID of the device used to capture the sample.</span></span>

</dd> <dt>

<span data-ttu-id="a31c7-121">**ImageAcquisitionLevel**</span><span class="sxs-lookup"><span data-stu-id="a31c7-121">**ImageAcquisitionLevel**</span></span>
</dt> <dd>

<span data-ttu-id="a31c7-122">指定要在其中捕獲樣本的解析層級。</span><span class="sxs-lookup"><span data-stu-id="a31c7-122">Specifies the resolution level at which the sample is captured.</span></span>

</dd> <dt>

<span data-ttu-id="a31c7-123">**HorizontalScanResolution**</span><span class="sxs-lookup"><span data-stu-id="a31c7-123">**HorizontalScanResolution**</span></span>
</dt> <dd>

<span data-ttu-id="a31c7-124">指定掃描的水準解析度。</span><span class="sxs-lookup"><span data-stu-id="a31c7-124">Specifies the horizontal resolution of the scan.</span></span>

</dd> <dt>

<span data-ttu-id="a31c7-125">**VerticalScanResolution**</span><span class="sxs-lookup"><span data-stu-id="a31c7-125">**VerticalScanResolution**</span></span>
</dt> <dd>

<span data-ttu-id="a31c7-126">指定掃描的垂直解析度。</span><span class="sxs-lookup"><span data-stu-id="a31c7-126">Specifies the vertical resolution of the scan.</span></span>

</dd> <dt>

<span data-ttu-id="a31c7-127">**HorizontalImageResolution**</span><span class="sxs-lookup"><span data-stu-id="a31c7-127">**HorizontalImageResolution**</span></span>
</dt> <dd>

<span data-ttu-id="a31c7-128">指定所捕捉的指紋或掌上映射的水準解析度。</span><span class="sxs-lookup"><span data-stu-id="a31c7-128">Specifies the horizontal resolution of the captured fingerprint or palm image.</span></span>

</dd> <dt>

<span data-ttu-id="a31c7-129">**VerticalImageResolution**</span><span class="sxs-lookup"><span data-stu-id="a31c7-129">**VerticalImageResolution**</span></span>
</dt> <dd>

<span data-ttu-id="a31c7-130">指定所捕獲指紋或掌上映射的垂直解析度。</span><span class="sxs-lookup"><span data-stu-id="a31c7-130">Specifies the vertical resolution of the captured fingerprint or palm image.</span></span>

</dd> <dt>

<span data-ttu-id="a31c7-131">**ElementCount**</span><span class="sxs-lookup"><span data-stu-id="a31c7-131">**ElementCount**</span></span>
</dt> <dd>

<span data-ttu-id="a31c7-132">此結構中的手指或棕櫚記錄數目。</span><span class="sxs-lookup"><span data-stu-id="a31c7-132">Number of finger or palm records in this structure.</span></span>

</dd> <dt>

<span data-ttu-id="a31c7-133">**ScaleUnits**</span><span class="sxs-lookup"><span data-stu-id="a31c7-133">**ScaleUnits**</span></span>
</dt> <dd>

<span data-ttu-id="a31c7-134">包含測量單位，1表示英寸，1表示釐米，2。</span><span class="sxs-lookup"><span data-stu-id="a31c7-134">Contains the unit of measure, 1 for inches and 2 for centimeters.</span></span>

</dd> <dt>

<span data-ttu-id="a31c7-135">**PixelDepth**</span><span class="sxs-lookup"><span data-stu-id="a31c7-135">**PixelDepth**</span></span>
</dt> <dd>

<span data-ttu-id="a31c7-136">指定圖元中的位數。</span><span class="sxs-lookup"><span data-stu-id="a31c7-136">Specifies the number of bits in a pixel.</span></span> <span data-ttu-id="a31c7-137">色彩的每個圖元可以有1到16位。</span><span class="sxs-lookup"><span data-stu-id="a31c7-137">This can be 1 to 16 bits per pixel for color.</span></span>

</dd> <dt>

<span data-ttu-id="a31c7-138">**ImageCompressionAlg**</span><span class="sxs-lookup"><span data-stu-id="a31c7-138">**ImageCompressionAlg**</span></span>
</dt> <dd>

<span data-ttu-id="a31c7-139">指定用來壓縮手指或掌上影像的演算法。</span><span class="sxs-lookup"><span data-stu-id="a31c7-139">Specifies the algorithm used to compress the finger or palm image.</span></span>

</dd> <dt>

<span data-ttu-id="a31c7-140">**已保留**</span><span class="sxs-lookup"><span data-stu-id="a31c7-140">**Reserved**</span></span>
<span data-ttu-id="a31c7-141"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="a31c7-141"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="a31c7-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="a31c7-142">Requirements</span></span>



| <span data-ttu-id="a31c7-143">需求</span><span class="sxs-lookup"><span data-stu-id="a31c7-143">Requirement</span></span> | <span data-ttu-id="a31c7-144">值</span><span class="sxs-lookup"><span data-stu-id="a31c7-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a31c7-145">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a31c7-145">Minimum supported client</span></span><br/> | <span data-ttu-id="a31c7-146">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a31c7-146">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="a31c7-147">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a31c7-147">Minimum supported server</span></span><br/> | <span data-ttu-id="a31c7-148">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a31c7-148">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="a31c7-149">標頭</span><span class="sxs-lookup"><span data-stu-id="a31c7-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="a31c7-150"><dt>Winbio \_ 類型 .h (包含 Winbio .h) </dt></span><span class="sxs-lookup"><span data-stu-id="a31c7-150"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a31c7-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a31c7-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a31c7-152">用戶端應用程式結構</span><span class="sxs-lookup"><span data-stu-id="a31c7-152">Client Application Structures</span></span>](client-application-structures.md)
</dt> </dl>

 

 





