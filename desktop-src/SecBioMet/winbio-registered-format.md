---
title: 'WINBIO_REGISTERED_FORMAT 結構 (Winbio \_ 類型 .h) '
description: 將已註冊的資料格式指定為擁有者/格式組。
ms.assetid: a178840e-81cc-4dd3-9d80-a181fa7fa888
keywords:
- WINBIO_REGISTERED_FORMAT 結構 Windows 生物特徵辨識架構 API
- PWINBIO_REGISTERED_FORMAT 結構指標 Windows 生物特徵辨識架構 API
topic_type:
- apiref
api_name:
- WINBIO_REGISTERED_FORMAT
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f45293fe95627c7dfad4c9c51eb7fa74ad1738c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508595"
---
# <a name="winbio_registered_format-structure"></a><span data-ttu-id="f2dbb-105">WINBIO \_ 已註冊的 \_ 格式結構</span><span class="sxs-lookup"><span data-stu-id="f2dbb-105">WINBIO\_REGISTERED\_FORMAT structure</span></span>

<span data-ttu-id="f2dbb-106">**WINBIO \_ 註冊的 \_ 格式** 結構會將已註冊的資料格式指定為擁有者/格式組。</span><span class="sxs-lookup"><span data-stu-id="f2dbb-106">The **WINBIO\_REGISTERED\_FORMAT** structure specifies a registered data format as an owner/format pair.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2dbb-107">語法</span><span class="sxs-lookup"><span data-stu-id="f2dbb-107">Syntax</span></span>


```C++
typedef struct _WINBIO_REGISTERED_FORMAT {
  USHORT Owner;
  USHORT Type;
} WINBIO_REGISTERED_FORMAT, *PWINBIO_REGISTERED_FORMAT;
```



## <a name="members"></a><span data-ttu-id="f2dbb-108">成員</span><span class="sxs-lookup"><span data-stu-id="f2dbb-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="f2dbb-109">**擁有者**</span><span class="sxs-lookup"><span data-stu-id="f2dbb-109">**Owner**</span></span>
</dt> <dd>

<span data-ttu-id="f2dbb-110">IBIA (國際生物特徵辨識產業關聯) 指派的擁有者值。</span><span class="sxs-lookup"><span data-stu-id="f2dbb-110">An IBIA (International Biometric Industry Association) assigned owner value.</span></span>

</dd> <dt>

<span data-ttu-id="f2dbb-111">**型別**</span><span class="sxs-lookup"><span data-stu-id="f2dbb-111">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="f2dbb-112">擁有者指派的格式。</span><span class="sxs-lookup"><span data-stu-id="f2dbb-112">An owner assigned format.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f2dbb-113">備註</span><span class="sxs-lookup"><span data-stu-id="f2dbb-113">Remarks</span></span>

<span data-ttu-id="f2dbb-114">由於 Windows 目前僅支援指紋辨識器，因此應該在 **WINBIO \_ 註冊的 \_ 格式** 結構中使用下列值。</span><span class="sxs-lookup"><span data-stu-id="f2dbb-114">Because Windows currently supports only fingerprint readers, the following values should be used in the **WINBIO\_REGISTERED\_FORMAT** structure.</span></span>



| <span data-ttu-id="f2dbb-115">常數</span><span class="sxs-lookup"><span data-stu-id="f2dbb-115">Constant</span></span>                                    | <span data-ttu-id="f2dbb-116">意義</span><span class="sxs-lookup"><span data-stu-id="f2dbb-116">Meaning</span></span>                                                                                                               |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2dbb-117">WINBIO \_ ANSI \_ 381 \_ 格式的 \_ 擁有者</span><span class="sxs-lookup"><span data-stu-id="f2dbb-117">WINBIO\_ANSI\_381\_FORMAT\_OWNER</span></span><br/> | <span data-ttu-id="f2dbb-118">資訊技術標準的國際委員會 (INCITS) 技術委員會 M1 (生物特徵辨識) 。</span><span class="sxs-lookup"><span data-stu-id="f2dbb-118">InterNational Committee for Information Technology Standards (INCITS) technical committee M1 (biometrics).</span></span><br/> |
| <span data-ttu-id="f2dbb-119">WINBIO \_ ANSI \_ 381 \_ 格式 \_ 類型</span><span class="sxs-lookup"><span data-stu-id="f2dbb-119">WINBIO\_ANSI\_381\_FORMAT\_TYPE</span></span><br/>  | <span data-ttu-id="f2dbb-120">ANSI INCITS 381 以映射為基礎的資料交換格式。</span><span class="sxs-lookup"><span data-stu-id="f2dbb-120">ANSI INCITS 381 finger image based data interchange format.</span></span><br/>                                                |



 

## <a name="requirements"></a><span data-ttu-id="f2dbb-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="f2dbb-121">Requirements</span></span>



| <span data-ttu-id="f2dbb-122">需求</span><span class="sxs-lookup"><span data-stu-id="f2dbb-122">Requirement</span></span> | <span data-ttu-id="f2dbb-123">值</span><span class="sxs-lookup"><span data-stu-id="f2dbb-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2dbb-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f2dbb-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f2dbb-125">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f2dbb-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="f2dbb-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f2dbb-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f2dbb-127">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f2dbb-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="f2dbb-128">標頭</span><span class="sxs-lookup"><span data-stu-id="f2dbb-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2dbb-129"><dt>Winbio \_ 類型 .h (包含 Winbio .h) </dt></span><span class="sxs-lookup"><span data-stu-id="f2dbb-129"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2dbb-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f2dbb-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2dbb-131">用戶端應用程式結構</span><span class="sxs-lookup"><span data-stu-id="f2dbb-131">Client Application Structures</span></span>](client-application-structures.md)
</dt> <dt>

[<span data-ttu-id="f2dbb-132">**WINBIO \_ ANSI \_ 381 \_ 格式常數**</span><span class="sxs-lookup"><span data-stu-id="f2dbb-132">**WINBIO\_ANSI\_381\_FORMAT Constants**</span></span>](winbio-ansi-381-format-constants.md)
</dt> <dt>

[<span data-ttu-id="f2dbb-133">**WINBIO \_ BDB \_ ANSI \_ 381 \_ 標頭**</span><span class="sxs-lookup"><span data-stu-id="f2dbb-133">**WINBIO\_BDB\_ANSI\_381\_HEADER**</span></span>](winbio-bdb-ansi-381-header.md)
</dt> <dt>

[<span data-ttu-id="f2dbb-134">**WINBIO \_ BIR \_ 標頭**</span><span class="sxs-lookup"><span data-stu-id="f2dbb-134">**WINBIO\_BIR\_HEADER**</span></span>](winbio-bir-header.md)
</dt> </dl>

 

 





