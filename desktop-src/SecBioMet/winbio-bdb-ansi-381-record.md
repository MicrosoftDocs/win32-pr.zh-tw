---
title: 'WINBIO_BDB_ANSI_381_RECORD 結構 (Winbio \_ 類型 .h) '
description: 包含來自終端使用者的單一指紋或棕櫚範例的相關資訊。
ms.assetid: e0b32d05-3e96-4b42-9e18-57d10513f224
keywords:
- WINBIO_BDB_ANSI_381_RECORD 結構 Windows 生物特徵辨識架構 API
topic_type:
- apiref
api_name:
- WINBIO_BDB_ANSI_381_RECORD
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f30af31d88349dbe02066f231cdff21293aebe90
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383974"
---
# <a name="winbio_bdb_ansi_381_record-structure"></a><span data-ttu-id="6f2b3-104">WINBIO \_ BDB \_ ANSI \_ 381 \_ 記錄結構</span><span class="sxs-lookup"><span data-stu-id="6f2b3-104">WINBIO\_BDB\_ANSI\_381\_RECORD structure</span></span>

<span data-ttu-id="6f2b3-105">**WINBIO \_ BDB \_ ANSI \_ 381 \_ 記錄** 結構包含來自終端使用者的單一指紋或棕櫚範例的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="6f2b3-105">The **WINBIO\_BDB\_ANSI\_381\_RECORD** structure contains information about a single fingerprint or palm sample from an end user.</span></span> <span data-ttu-id="6f2b3-106">這些結構的集合會包含在每個 [**WINBIO \_ BDB \_ ANSI \_ 381 \_ 標頭**](winbio-bdb-ansi-381-header.md) 結構中。</span><span class="sxs-lookup"><span data-stu-id="6f2b3-106">A collection of these structures is included in each [**WINBIO\_BDB\_ANSI\_381\_HEADER**](winbio-bdb-ansi-381-header.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f2b3-107">語法</span><span class="sxs-lookup"><span data-stu-id="6f2b3-107">Syntax</span></span>


```C++
typedef struct _WINBIO_BDB_ANSI_381_RECORD {
  ULONG                    BlockLength;
  USHORT                   HorizontalLineLength;
  USHORT                   VerticalLineLength;
  WINBIO_BIOMETRIC_SUBTYPE Position;
  UCHAR                    CountOfViews;
  UCHAR                    ViewNumber;
  UCHAR                    ImageQuality;
  UCHAR                    ImpressionType;
  UCHAR                    Reserved;
} WINBIO_BDB_ANSI_381_RECORD;
```



## <a name="members"></a><span data-ttu-id="6f2b3-108">成員</span><span class="sxs-lookup"><span data-stu-id="6f2b3-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="6f2b3-109">**BlockLength**</span><span class="sxs-lookup"><span data-stu-id="6f2b3-109">**BlockLength**</span></span>
</dt> <dd>

<span data-ttu-id="6f2b3-110">包含此結構的位元組數目以及範例影像資料的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="6f2b3-110">Contains the number of bytes in this structure plus the number of bytes of sample image data.</span></span>

</dd> <dt>

<span data-ttu-id="6f2b3-111">**HorizontalLineLength**</span><span class="sxs-lookup"><span data-stu-id="6f2b3-111">**HorizontalLineLength**</span></span>
</dt> <dd>

<span data-ttu-id="6f2b3-112">指定取樣水準行中的圖元數。</span><span class="sxs-lookup"><span data-stu-id="6f2b3-112">Specifies the number of pixels in a horizontal line of the sample.</span></span>

</dd> <dt>

<span data-ttu-id="6f2b3-113">**VerticalLineLength**</span><span class="sxs-lookup"><span data-stu-id="6f2b3-113">**VerticalLineLength**</span></span>
</dt> <dd>

<span data-ttu-id="6f2b3-114">指定取樣垂直線的圖元數。</span><span class="sxs-lookup"><span data-stu-id="6f2b3-114">Specifies the number of pixels in a vertical line of the sample.</span></span>

</dd> <dt>

<span data-ttu-id="6f2b3-115">**位置**</span><span class="sxs-lookup"><span data-stu-id="6f2b3-115">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="6f2b3-116">**WINBIO \_ 生物特徵辨識 \_ 子類型** 值，指定用來產生生物特徵辨識範例的手指或掌。</span><span class="sxs-lookup"><span data-stu-id="6f2b3-116">A **WINBIO\_BIOMETRIC\_SUBTYPE** value that specifies the finger or palm used to generate the biometric sample.</span></span> <span data-ttu-id="6f2b3-117">如需詳細資訊，請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="6f2b3-117">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="6f2b3-118">**CountOfViews**</span><span class="sxs-lookup"><span data-stu-id="6f2b3-118">**CountOfViews**</span></span>
</dt> <dd>

<span data-ttu-id="6f2b3-119">這必須設定為一個 (1) ;</span><span class="sxs-lookup"><span data-stu-id="6f2b3-119">This must be set to one (1);</span></span>

</dd> <dt>

<span data-ttu-id="6f2b3-120">**ViewNumber**</span><span class="sxs-lookup"><span data-stu-id="6f2b3-120">**ViewNumber**</span></span>
</dt> <dd>

<span data-ttu-id="6f2b3-121">這必須設定為一個 (1) ;</span><span class="sxs-lookup"><span data-stu-id="6f2b3-121">This must be set to one (1);</span></span>

</dd> <dt>

<span data-ttu-id="6f2b3-122">**ImageQuality**</span><span class="sxs-lookup"><span data-stu-id="6f2b3-122">**ImageQuality**</span></span>
</dt> <dd>

<span data-ttu-id="6f2b3-123">保留的。</span><span class="sxs-lookup"><span data-stu-id="6f2b3-123">Reserved.</span></span> <span data-ttu-id="6f2b3-124">這必須是 254 (0xFE) 。</span><span class="sxs-lookup"><span data-stu-id="6f2b3-124">This must be 254 (0xFE).</span></span>

</dd> <dt>

<span data-ttu-id="6f2b3-125">**ImpressionType**</span><span class="sxs-lookup"><span data-stu-id="6f2b3-125">**ImpressionType**</span></span>
</dt> <dd>

<span data-ttu-id="6f2b3-126">保留的。</span><span class="sxs-lookup"><span data-stu-id="6f2b3-126">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="6f2b3-127">**已保留**</span><span class="sxs-lookup"><span data-stu-id="6f2b3-127">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="6f2b3-128">保留的。</span><span class="sxs-lookup"><span data-stu-id="6f2b3-128">Reserved.</span></span> <span data-ttu-id="6f2b3-129">必須設定為零 (0) 。</span><span class="sxs-lookup"><span data-stu-id="6f2b3-129">Must be set to zero (0).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6f2b3-130">備註</span><span class="sxs-lookup"><span data-stu-id="6f2b3-130">Remarks</span></span>

<span data-ttu-id="6f2b3-131">*Position* 成員會指定用來建立生物特徵辨識範例的手邊區域或掌上區域。</span><span class="sxs-lookup"><span data-stu-id="6f2b3-131">The *Position* member specifies the area of the hand or palm used to make the biometric sample.</span></span> <span data-ttu-id="6f2b3-132">Windows 生物特徵辨識架構 (WBF) 目前僅支援指紋捕捉，並使用下列常數來表示位置資訊。</span><span class="sxs-lookup"><span data-stu-id="6f2b3-132">The Windows Biometric Framework (WBF) currently supports only fingerprint capture and uses the following constants to represent position information.</span></span>

-   <span data-ttu-id="6f2b3-133">WINBIO \_ ANSI \_ 381 \_ POS \_ 不明</span><span class="sxs-lookup"><span data-stu-id="6f2b3-133">WINBIO\_ANSI\_381\_POS\_UNKNOWN</span></span>
-   <span data-ttu-id="6f2b3-134">WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ THUMB</span><span class="sxs-lookup"><span data-stu-id="6f2b3-134">WINBIO\_ANSI\_381\_POS\_RH\_THUMB</span></span>
-   <span data-ttu-id="6f2b3-135">WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ 食指 \_</span><span class="sxs-lookup"><span data-stu-id="6f2b3-135">WINBIO\_ANSI\_381\_POS\_RH\_INDEX\_FINGER</span></span>
-   <span data-ttu-id="6f2b3-136">WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ 中間 \_ 手指</span><span class="sxs-lookup"><span data-stu-id="6f2b3-136">WINBIO\_ANSI\_381\_POS\_RH\_MIDDLE\_FINGER</span></span>
-   <span data-ttu-id="6f2b3-137">WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ 環形 \_ 手指</span><span class="sxs-lookup"><span data-stu-id="6f2b3-137">WINBIO\_ANSI\_381\_POS\_RH\_RING\_FINGER</span></span>
-   <span data-ttu-id="6f2b3-138">WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ 小 \_ 手指</span><span class="sxs-lookup"><span data-stu-id="6f2b3-138">WINBIO\_ANSI\_381\_POS\_RH\_LITTLE\_FINGER</span></span>
-   <span data-ttu-id="6f2b3-139">WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ 經驗</span><span class="sxs-lookup"><span data-stu-id="6f2b3-139">WINBIO\_ANSI\_381\_POS\_LH\_THUMB</span></span>
-   <span data-ttu-id="6f2b3-140">WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ 索引 \_ 手指</span><span class="sxs-lookup"><span data-stu-id="6f2b3-140">WINBIO\_ANSI\_381\_POS\_LH\_INDEX\_FINGER</span></span>
-   <span data-ttu-id="6f2b3-141">WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ 中間 \_ 手指</span><span class="sxs-lookup"><span data-stu-id="6f2b3-141">WINBIO\_ANSI\_381\_POS\_LH\_MIDDLE\_FINGER</span></span>
-   <span data-ttu-id="6f2b3-142">WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ 環形 \_ 手指</span><span class="sxs-lookup"><span data-stu-id="6f2b3-142">WINBIO\_ANSI\_381\_POS\_LH\_RING\_FINGER</span></span>
-   <span data-ttu-id="6f2b3-143">WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ 小 \_ 手指</span><span class="sxs-lookup"><span data-stu-id="6f2b3-143">WINBIO\_ANSI\_381\_POS\_LH\_LITTLE\_FINGER</span></span>
-   <span data-ttu-id="6f2b3-144">WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ 四 \_ 手指</span><span class="sxs-lookup"><span data-stu-id="6f2b3-144">WINBIO\_ANSI\_381\_POS\_RH\_FOUR\_FINGERS</span></span>
-   <span data-ttu-id="6f2b3-145">WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ 四 \_ 手指</span><span class="sxs-lookup"><span data-stu-id="6f2b3-145">WINBIO\_ANSI\_381\_POS\_LH\_FOUR\_FINGERS</span></span>
-   <span data-ttu-id="6f2b3-146">WINBIO \_ ANSI \_ 381 \_ POS \_ 雙 \_ 拇指</span><span class="sxs-lookup"><span data-stu-id="6f2b3-146">WINBIO\_ANSI\_381\_POS\_TWO\_THUMBS</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="6f2b3-147">請勿嘗試驗證為 *位置* 值提供的值。</span><span class="sxs-lookup"><span data-stu-id="6f2b3-147">Do not attempt to validate the value supplied for the *Position* value.</span></span> <span data-ttu-id="6f2b3-148">Windows 生物識別服務會先驗證提供的值，再將其傳遞至您的實作為。</span><span class="sxs-lookup"><span data-stu-id="6f2b3-148">The Windows Biometrics Service will validate the supplied value before passing it through to your implementation.</span></span> <span data-ttu-id="6f2b3-149">如果值為 **WINBIO \_ 子類型 \_ NO \_ INFORMATION** 或 **WINBIO \_ 子類型 \_ ANY**，則在適當的位置驗證。</span><span class="sxs-lookup"><span data-stu-id="6f2b3-149">If the value is **WINBIO\_SUBTYPE\_NO\_INFORMATION** or **WINBIO\_SUBTYPE\_ANY**, then validate where appropriate.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6f2b3-150">規格需求</span><span class="sxs-lookup"><span data-stu-id="6f2b3-150">Requirements</span></span>



| <span data-ttu-id="6f2b3-151">需求</span><span class="sxs-lookup"><span data-stu-id="6f2b3-151">Requirement</span></span> | <span data-ttu-id="6f2b3-152">值</span><span class="sxs-lookup"><span data-stu-id="6f2b3-152">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f2b3-153">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6f2b3-153">Minimum supported client</span></span><br/> | <span data-ttu-id="6f2b3-154">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6f2b3-154">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="6f2b3-155">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6f2b3-155">Minimum supported server</span></span><br/> | <span data-ttu-id="6f2b3-156">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6f2b3-156">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="6f2b3-157">標頭</span><span class="sxs-lookup"><span data-stu-id="6f2b3-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f2b3-158"><dt>Winbio \_ 類型 .h (包含 Winbio .h) </dt></span><span class="sxs-lookup"><span data-stu-id="6f2b3-158"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f2b3-159">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6f2b3-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f2b3-160">用戶端應用程式結構</span><span class="sxs-lookup"><span data-stu-id="6f2b3-160">Client Application Structures</span></span>](client-application-structures.md)
</dt> </dl>

 

 





