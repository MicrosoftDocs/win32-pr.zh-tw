---
title: 'WINBIO_BIR 結構 (Winbio \_ 類型 .h) '
description: 代表 (BIR) 的生物特徵辨識資訊記錄。
ms.assetid: 39cfab34-0416-4897-bf95-a1b3c3a6a7a1
keywords:
- WINBIO_BIR 結構 Windows 生物特徵辨識架構 API
topic_type:
- apiref
api_name:
- WINBIO_BIR
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e422bbe59414d75541127b41e5e2cc1829adaaa7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967568"
---
# <a name="winbio_bir-structure"></a><span data-ttu-id="034c5-104">WINBIO \_ BIR 結構</span><span class="sxs-lookup"><span data-stu-id="034c5-104">WINBIO\_BIR structure</span></span>

<span data-ttu-id="034c5-105">**WINBIO \_ BIR** 結構代表 (BIR) 的生物特徵辨識資訊記錄。</span><span class="sxs-lookup"><span data-stu-id="034c5-105">The **WINBIO\_BIR** structure represents a biometric information record (BIR).</span></span> <span data-ttu-id="034c5-106">資訊記錄包含標頭、資料和簽章區塊。</span><span class="sxs-lookup"><span data-stu-id="034c5-106">The information record contains header, data, and signature blocks.</span></span>

## <a name="syntax"></a><span data-ttu-id="034c5-107">語法</span><span class="sxs-lookup"><span data-stu-id="034c5-107">Syntax</span></span>


```C++
typedef struct _WINBIO_BIR {
  WINBIO_BIR_DATA HeaderBlock;
  WINBIO_BIR_DATA StandardDataBlock;
  WINBIO_BIR_DATA VendorDataBlock;
  WINBIO_BIR_DATA SignatureBlock;
} WINBIO_BIR;
```



## <a name="members"></a><span data-ttu-id="034c5-108">成員</span><span class="sxs-lookup"><span data-stu-id="034c5-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="034c5-109">**HeaderBlock**</span><span class="sxs-lookup"><span data-stu-id="034c5-109">**HeaderBlock**</span></span>
</dt> <dd>

<span data-ttu-id="034c5-110">[**WINBIO \_ BIR \_ 資料**](winbio-bir-data.md)結構，其中包含 BIR 標頭的大小（以位元組為單位）和位移。</span><span class="sxs-lookup"><span data-stu-id="034c5-110">A [**WINBIO\_BIR\_DATA**](winbio-bir-data.md) structure that contains the size, in bytes, and offset of the BIR header.</span></span> <span data-ttu-id="034c5-111">標頭包含描述資訊記錄內容的資訊。</span><span class="sxs-lookup"><span data-stu-id="034c5-111">The header contains information that describes the contents of the information record.</span></span>

</dd> <dt>

<span data-ttu-id="034c5-112">**StandardDataBlock**</span><span class="sxs-lookup"><span data-stu-id="034c5-112">**StandardDataBlock**</span></span>
</dt> <dd>

<span data-ttu-id="034c5-113">[**WINBIO \_ BIR \_ 資料**](winbio-bir-data.md)結構，其中包含由 Windows 生物特徵辨識架構 (WBF) 所建立的已處理或未處理生物特徵辨識資訊的大小（以位元組為單位）和位移。</span><span class="sxs-lookup"><span data-stu-id="034c5-113">A [**WINBIO\_BIR\_DATA**](winbio-bir-data.md) structure that contains the size, in bytes, and offset of processed or unprocessed biometric information created by the Windows Biometric Framework (WBF).</span></span>

</dd> <dt>

<span data-ttu-id="034c5-114">**VendorDataBlock**</span><span class="sxs-lookup"><span data-stu-id="034c5-114">**VendorDataBlock**</span></span>
</dt> <dd>

<span data-ttu-id="034c5-115">[**WINBIO \_ BIR \_ 資料**](winbio-bir-data.md)結構，其中包含廠商感應器和軟體所提供的已處理或未處理生物特徵辨識資訊的大小（以位元組為單位）和位移。</span><span class="sxs-lookup"><span data-stu-id="034c5-115">A [**WINBIO\_BIR\_DATA**](winbio-bir-data.md) structure that contains the size, in bytes, and offset of processed or unprocessed biometric information provided by vendor sensors and software.</span></span>

</dd> <dt>

<span data-ttu-id="034c5-116">**SignatureBlock**</span><span class="sxs-lookup"><span data-stu-id="034c5-116">**SignatureBlock**</span></span>
</dt> <dd>

<span data-ttu-id="034c5-117">選擇性的 [**WINBIO \_ BIR \_ 資料**](winbio-bir-data.md) 結構，其中包含數位簽章消息驗證程式代碼的大小（以位元組為單位）和位移 (MAC) ，可用來驗證 BIR 的完整性。</span><span class="sxs-lookup"><span data-stu-id="034c5-117">An optional [**WINBIO\_BIR\_DATA**](winbio-bir-data.md) structure that contains the size, in bytes, and offset of the digital signature message authentication code (MAC) that can be used to verify the integrity of the BIR.</span></span> <span data-ttu-id="034c5-118">如果有的話，簽章或 MAC 必須涵蓋標頭和資料區塊。</span><span class="sxs-lookup"><span data-stu-id="034c5-118">If present, the signature or MAC must cover the header and data blocks.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="034c5-119">備註</span><span class="sxs-lookup"><span data-stu-id="034c5-119">Remarks</span></span>

<span data-ttu-id="034c5-120">使用位移而非指標，可讓您輕鬆地序列化 BIR，以及在32和64位環境之間或使用者和核心模式之間進行較不復雜的轉譯。</span><span class="sxs-lookup"><span data-stu-id="034c5-120">The use of offsets rather than pointers allows for easy serialization of the BIR and for less complicated translation between 32 and 64-bit environments or between user and kernel mode.</span></span>

<span data-ttu-id="034c5-121">BIR 與常見的生物特徵辨識 Exchange 格式架構相容 (CBEFF) 由 NIST 6529-A 所定義。</span><span class="sxs-lookup"><span data-stu-id="034c5-121">The BIR is compatible with the Common Biometric Exchange Format Framework (CBEFF) defined by NIST 6529-A.</span></span>

<span data-ttu-id="034c5-122">如果此結構包含 *StandardDataBlock* 值， *HeaderBlock* 參數所指定之標頭的 *型* 別參數必須設定為 **WINBIO \_ ANSI \_ 381 \_ 格式 \_ 類型**。</span><span class="sxs-lookup"><span data-stu-id="034c5-122">If this structure contains a *StandardDataBlock* value, the *Type* parameter of the header specified by the *HeaderBlock* parameter must be set to **WINBIO\_ANSI\_381\_FORMAT\_TYPE**.</span></span> <span data-ttu-id="034c5-123">這是目前 Windows 生物特徵辨識架構版本所支援的唯一標準資料格式。</span><span class="sxs-lookup"><span data-stu-id="034c5-123">This is the only standard data format supported by the current version of the Windows Biometric Framework.</span></span>

## <a name="requirements"></a><span data-ttu-id="034c5-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="034c5-124">Requirements</span></span>



| <span data-ttu-id="034c5-125">需求</span><span class="sxs-lookup"><span data-stu-id="034c5-125">Requirement</span></span> | <span data-ttu-id="034c5-126">值</span><span class="sxs-lookup"><span data-stu-id="034c5-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="034c5-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="034c5-127">Minimum supported client</span></span><br/> | <span data-ttu-id="034c5-128">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="034c5-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="034c5-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="034c5-129">Minimum supported server</span></span><br/> | <span data-ttu-id="034c5-130">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="034c5-130">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="034c5-131">標頭</span><span class="sxs-lookup"><span data-stu-id="034c5-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="034c5-132"><dt>Winbio \_ 類型 .h (包含 Winbio .h) </dt></span><span class="sxs-lookup"><span data-stu-id="034c5-132"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="034c5-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="034c5-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="034c5-134">用戶端應用程式結構</span><span class="sxs-lookup"><span data-stu-id="034c5-134">Client Application Structures</span></span>](client-application-structures.md)
</dt> <dt>

[<span data-ttu-id="034c5-135">**WINBIO \_ BIR \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="034c5-135">**WINBIO\_BIR\_DATA**</span></span>](winbio-bir-data.md)
</dt> <dt>

[<span data-ttu-id="034c5-136">**WINBIO \_ BIR \_ 標頭**</span><span class="sxs-lookup"><span data-stu-id="034c5-136">**WINBIO\_BIR\_HEADER**</span></span>](winbio-bir-header.md)
</dt> </dl>

 

 





