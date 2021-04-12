---
title: 'WINBIO_BIR_DATA 結構 (Winbio \_ 類型 .h) '
description: 指定生物特徵辨識資訊區塊的大小（以位元組為單位）和位移。
ms.assetid: 2f73eb1f-f1a1-4831-a8f7-eec28aa51645
keywords:
- WINBIO_BIR_DATA 結構 Windows 生物特徵辨識架構 API
topic_type:
- apiref
api_name:
- WINBIO_BIR_DATA
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41ebf7b157c5bd806442cdc120350a89ce646f9e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384597"
---
# <a name="winbio_bir_data-structure"></a><span data-ttu-id="96555-104">WINBIO \_ BIR \_ 資料結構</span><span class="sxs-lookup"><span data-stu-id="96555-104">WINBIO\_BIR\_DATA structure</span></span>

<span data-ttu-id="96555-105">**WINBIO \_ BIR \_ 資料** 結構會指定以位元組為單位的大小，以及辨識項資訊區塊的位移。</span><span class="sxs-lookup"><span data-stu-id="96555-105">The **WINBIO\_BIR\_DATA** structure specifies the size, in bytes, and the offset of a block of biometric information.</span></span> <span data-ttu-id="96555-106">[**WINBIO \_ BIR**](winbio-bir.md)結構會使用此結構來指定生物特徵辨識資訊記錄的各個部分所在的位置。</span><span class="sxs-lookup"><span data-stu-id="96555-106">This structure is used by the [**WINBIO\_BIR**](winbio-bir.md) structure to specify where the various parts of a biometric information record are located.</span></span>

## <a name="syntax"></a><span data-ttu-id="96555-107">語法</span><span class="sxs-lookup"><span data-stu-id="96555-107">Syntax</span></span>


```C++
typedef struct _WINBIO_BIR_DATA {
  ULONG Size;
  ULONG Offset;
} WINBIO_BIR_DATA;
```



## <a name="members"></a><span data-ttu-id="96555-108">成員</span><span class="sxs-lookup"><span data-stu-id="96555-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="96555-109">**大小**</span><span class="sxs-lookup"><span data-stu-id="96555-109">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="96555-110">生物特徵辨識資訊的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="96555-110">Size, in bytes, of the biometric information.</span></span>

</dd> <dt>

<span data-ttu-id="96555-111">**Offset**</span><span class="sxs-lookup"><span data-stu-id="96555-111">**Offset**</span></span>
</dt> <dd>

<span data-ttu-id="96555-112">[**WINBIO \_ BIR**](winbio-bir.md)結構開頭的位移（以位元組為單位），表示生物特徵辨識資訊。</span><span class="sxs-lookup"><span data-stu-id="96555-112">Offset, in bytes from the beginning of the [**WINBIO\_BIR**](winbio-bir.md) structure, of the biometric information.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="96555-113">備註</span><span class="sxs-lookup"><span data-stu-id="96555-113">Remarks</span></span>

<span data-ttu-id="96555-114">使用位移而非指標，可讓您輕鬆地序列化 BIR，以及在32和64位環境之間或使用者和核心模式之間進行較不復雜的轉譯。</span><span class="sxs-lookup"><span data-stu-id="96555-114">The use of offsets rather than pointers allows for easy serialization of the BIR and for less complicated translation between 32 and 64-bit environments or between user and kernel mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="96555-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="96555-115">Requirements</span></span>



| <span data-ttu-id="96555-116">需求</span><span class="sxs-lookup"><span data-stu-id="96555-116">Requirement</span></span> | <span data-ttu-id="96555-117">值</span><span class="sxs-lookup"><span data-stu-id="96555-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96555-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="96555-118">Minimum supported client</span></span><br/> | <span data-ttu-id="96555-119">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="96555-119">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="96555-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="96555-120">Minimum supported server</span></span><br/> | <span data-ttu-id="96555-121">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="96555-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="96555-122">標頭</span><span class="sxs-lookup"><span data-stu-id="96555-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="96555-123"><dt>Winbio \_ 類型 .h (包含 Winbio .h) </dt></span><span class="sxs-lookup"><span data-stu-id="96555-123"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96555-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="96555-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96555-125">用戶端應用程式結構</span><span class="sxs-lookup"><span data-stu-id="96555-125">Client Application Structures</span></span>](client-application-structures.md)
</dt> <dt>

[<span data-ttu-id="96555-126">**WINBIO \_ BIR**</span><span class="sxs-lookup"><span data-stu-id="96555-126">**WINBIO\_BIR**</span></span>](winbio-bir.md)
</dt> <dt>

[<span data-ttu-id="96555-127">**WINBIO \_ BIR \_ 標頭**</span><span class="sxs-lookup"><span data-stu-id="96555-127">**WINBIO\_BIR\_HEADER**</span></span>](winbio-bir-header.md)
</dt> </dl>

 

 





