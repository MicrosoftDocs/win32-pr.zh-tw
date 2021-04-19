---
title: 'MPFASTPATH_DATA 結構 (MpClient .h) '
description: FastPath 更新通知。
ms.assetid: E19F153D-DD46-4E27-9A4B-33586794DAC2
keywords:
- MPFASTPATH_DATA 結構舊版 Windows 環境功能
- PMPFASTPATH_DATA 結構指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPFASTPATH_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2850a48074fee6984564550683c7fe595d0779ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106994977"
---
# <a name="mpfastpath_data-structure"></a><span data-ttu-id="87295-105">MPFASTPATH \_ 資料結構</span><span class="sxs-lookup"><span data-stu-id="87295-105">MPFASTPATH\_DATA structure</span></span>

<span data-ttu-id="87295-106">FastPath 更新通知。</span><span class="sxs-lookup"><span data-stu-id="87295-106">FastPath update notification.</span></span>

## <a name="syntax"></a><span data-ttu-id="87295-107">語法</span><span class="sxs-lookup"><span data-stu-id="87295-107">Syntax</span></span>


```C++
typedef struct tagMPFASTPATH_DATA {
  MP_SIGNATURE_TYPE         SignatureType;
  MP_FASTPATH_TYPE          FastPathSignatureType;
  MP_MIDL_STRING LPWSTR     FastPathSignatureVersion;
  ULARGE_INTEGER            CompilationTimestamp;
  MP_PERSISTENCE_LIMIT_TYPE PersistenceType;
  MP_MIDL_STRING LPWSTR     PersistenceValue;
  MP_MIDL_STRING LPWSTR     PersistencePath;
  MP_REMOVAL_REASON         Reason;
} MPFASTPATH_DATA, *PMPFASTPATH_DATA;
```



## <a name="members"></a><span data-ttu-id="87295-108">成員</span><span class="sxs-lookup"><span data-stu-id="87295-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="87295-109">**SignatureType**</span><span class="sxs-lookup"><span data-stu-id="87295-109">**SignatureType**</span></span>
</dt> <dd>

<span data-ttu-id="87295-110">Type： **[ **MP \_ SIGNATURE \_ TYPE**](mp-signature-type.md)**</span><span class="sxs-lookup"><span data-stu-id="87295-110">Type: **[**MP\_SIGNATURE\_TYPE**](mp-signature-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="87295-111">簽章類型。</span><span class="sxs-lookup"><span data-stu-id="87295-111">Signature type.</span></span>

</dd> <dt>

<span data-ttu-id="87295-112">**FastPathSignatureType**</span><span class="sxs-lookup"><span data-stu-id="87295-112">**FastPathSignatureType**</span></span>
</dt> <dd>

<span data-ttu-id="87295-113">類型： **[ **MP \_ FASTPATH \_ 類型**](mp-fastpath-type.md)**</span><span class="sxs-lookup"><span data-stu-id="87295-113">Type: **[**MP\_FASTPATH\_TYPE**](mp-fastpath-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="87295-114">FastPath 簽章類型。</span><span class="sxs-lookup"><span data-stu-id="87295-114">FastPath signature type.</span></span>

</dd> <dt>

<span data-ttu-id="87295-115">**FastPathSignatureVersion**</span><span class="sxs-lookup"><span data-stu-id="87295-115">**FastPathSignatureVersion**</span></span>
</dt> <dd>

<span data-ttu-id="87295-116">類型： **MP \_ MIDL \_ STRING LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="87295-116">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="87295-117">FastPath 簽章版本 (選擇性) 。</span><span class="sxs-lookup"><span data-stu-id="87295-117">FastPath signature version (optional).</span></span>

</dd> <dt>

<span data-ttu-id="87295-118">**CompilationTimestamp**</span><span class="sxs-lookup"><span data-stu-id="87295-118">**CompilationTimestamp**</span></span>
</dt> <dd>

<span data-ttu-id="87295-119">類型： **ULARGE \_ 整數**</span><span class="sxs-lookup"><span data-stu-id="87295-119">Type: **ULARGE\_INTEGER**</span></span>

</dd> <dd>

<span data-ttu-id="87295-120">編譯 timestamp (UTC) 。</span><span class="sxs-lookup"><span data-stu-id="87295-120">Compilation timestamp (UTC).</span></span>

</dd> <dt>

<span data-ttu-id="87295-121">**PersistenceType**</span><span class="sxs-lookup"><span data-stu-id="87295-121">**PersistenceType**</span></span>
</dt> <dd>

<span data-ttu-id="87295-122">類型： **[ **MP \_ 持續性 \_ 限制 \_ 類型**](mp-persistence-limit-type.md)**</span><span class="sxs-lookup"><span data-stu-id="87295-122">Type: **[**MP\_PERSISTENCE\_LIMIT\_TYPE**](mp-persistence-limit-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="87295-123">持續性類型 (選擇性) 。</span><span class="sxs-lookup"><span data-stu-id="87295-123">Persistence type (optional).</span></span>

</dd> <dt>

<span data-ttu-id="87295-124">**PersistenceValue**</span><span class="sxs-lookup"><span data-stu-id="87295-124">**PersistenceValue**</span></span>
</dt> <dd>

<span data-ttu-id="87295-125">類型： **MP \_ MIDL \_ STRING LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="87295-125">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="87295-126">持續性值 (選擇性) 。</span><span class="sxs-lookup"><span data-stu-id="87295-126">Persistence value (optional).</span></span>

</dd> <dt>

<span data-ttu-id="87295-127">**PersistencePath**</span><span class="sxs-lookup"><span data-stu-id="87295-127">**PersistencePath**</span></span>
</dt> <dd>

<span data-ttu-id="87295-128">類型： **MP \_ MIDL \_ STRING LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="87295-128">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="87295-129">持續性路徑 (選擇性) 。</span><span class="sxs-lookup"><span data-stu-id="87295-129">Persistence path (optional).</span></span>

</dd> <dt>

<span data-ttu-id="87295-130">**原因**</span><span class="sxs-lookup"><span data-stu-id="87295-130">**Reason**</span></span>
</dt> <dd>

<span data-ttu-id="87295-131">類型： **[ **MP \_ 移除 \_ 原因**](mp-removal-reason.md)**</span><span class="sxs-lookup"><span data-stu-id="87295-131">Type: **[**MP\_REMOVAL\_REASON**](mp-removal-reason.md)**</span></span>

</dd> <dd>

<span data-ttu-id="87295-132">移除簽章的原因。</span><span class="sxs-lookup"><span data-stu-id="87295-132">Reason for signature removal.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="87295-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="87295-133">Requirements</span></span>



| <span data-ttu-id="87295-134">需求</span><span class="sxs-lookup"><span data-stu-id="87295-134">Requirement</span></span> | <span data-ttu-id="87295-135">值</span><span class="sxs-lookup"><span data-stu-id="87295-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="87295-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="87295-136">Minimum supported client</span></span><br/> | <span data-ttu-id="87295-137">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="87295-137">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="87295-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="87295-138">Minimum supported server</span></span><br/> | <span data-ttu-id="87295-139">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="87295-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="87295-140">標頭</span><span class="sxs-lookup"><span data-stu-id="87295-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="87295-141"><dt>MpClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="87295-141"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87295-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="87295-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87295-143">**MP \_ FASTPATH \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="87295-143">**MP\_FASTPATH\_TYPE**</span></span>](mp-fastpath-type.md)
</dt> <dt>

[<span data-ttu-id="87295-144">**MP \_ 持續性 \_ 限制 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="87295-144">**MP\_PERSISTENCE\_LIMIT\_TYPE**</span></span>](mp-persistence-limit-type.md)
</dt> <dt>

[<span data-ttu-id="87295-145">**MP \_ SIGNATURE \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="87295-145">**MP\_SIGNATURE\_TYPE**</span></span>](mp-signature-type.md)
</dt> </dl>

 

 





