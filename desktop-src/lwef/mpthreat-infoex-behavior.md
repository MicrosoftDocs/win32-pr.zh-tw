---
title: 'MPTHREAT_INFOEX_BEHAVIOR 結構 (MpClient .h) '
description: 包含行為修改特定的資訊。
ms.assetid: 762E755F-5BA1-476D-B395-6617093309C5
keywords:
- MPTHREAT_INFOEX_BEHAVIOR 結構舊版 Windows 環境功能
- PMPTHREAT_INFOEX_BEHAVIOR 結構指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPTHREAT_INFOEX_BEHAVIOR
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cb0bc00aeb56aec38b88f2590211c705079834f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686326"
---
# <a name="mpthreat_infoex_behavior-structure"></a><span data-ttu-id="16cb0-105">MPTHREAT \_ INFOEX \_ 行為結構</span><span class="sxs-lookup"><span data-stu-id="16cb0-105">MPTHREAT\_INFOEX\_BEHAVIOR structure</span></span>

<span data-ttu-id="16cb0-106">包含行為修改特定的資訊。</span><span class="sxs-lookup"><span data-stu-id="16cb0-106">Contains behavior modification-specific information.</span></span>

## <a name="syntax"></a><span data-ttu-id="16cb0-107">語法</span><span class="sxs-lookup"><span data-stu-id="16cb0-107">Syntax</span></span>


```C++
typedef struct tagMPTHREAT_INFOEX_BEHAVIOR {
  ULARGE_INTEGER         SignatureID;
  ULONGLONG              EngineVersion;
  ULONGLONG              ASDeltaSignatureVersion;
  ULONGLONG              AVDeltaSignatureVersion;
  MP_HASH_TYPE           HashType;
  DWORD                  FidelityValue;
  MP_MIDL_STRING  LPWSTR HashValue;
  MP_MIDL_STRING  LPWSTR TargetFileName;
  MP_MIDL_STRING  LPWSTR TargetFileHash;
} MPTHREAT_INFOEX_BEHAVIOR, *PMPTHREAT_INFOEX_BEHAVIOR;
```



## <a name="members"></a><span data-ttu-id="16cb0-108">成員</span><span class="sxs-lookup"><span data-stu-id="16cb0-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="16cb0-109">**SignatureID**</span><span class="sxs-lookup"><span data-stu-id="16cb0-109">**SignatureID**</span></span>
</dt> <dd>

<span data-ttu-id="16cb0-110">類型： **ULARGE \_ 整數**</span><span class="sxs-lookup"><span data-stu-id="16cb0-110">Type: **ULARGE\_INTEGER**</span></span>

</dd> <dd>

<span data-ttu-id="16cb0-111">偵測時引擎提供的行為修改簽章識別碼。</span><span class="sxs-lookup"><span data-stu-id="16cb0-111">Behavior modification signature ID given by the engine at the time of detection.</span></span>

</dd> <dt>

<span data-ttu-id="16cb0-112">**EngineVersion**</span><span class="sxs-lookup"><span data-stu-id="16cb0-112">**EngineVersion**</span></span>
</dt> <dd>

<span data-ttu-id="16cb0-113">類型： **ULONGLONG**</span><span class="sxs-lookup"><span data-stu-id="16cb0-113">Type: **ULONGLONG**</span></span>

</dd> <dd>

<span data-ttu-id="16cb0-114">引擎模組版本。</span><span class="sxs-lookup"><span data-stu-id="16cb0-114">Engine module version.</span></span>

</dd> <dt>

<span data-ttu-id="16cb0-115">**ASDeltaSignatureVersion**</span><span class="sxs-lookup"><span data-stu-id="16cb0-115">**ASDeltaSignatureVersion**</span></span>
</dt> <dd>

<span data-ttu-id="16cb0-116">類型： **ULONGLONG**</span><span class="sxs-lookup"><span data-stu-id="16cb0-116">Type: **ULONGLONG**</span></span>

</dd> <dd>

<span data-ttu-id="16cb0-117">防毒軟體簽章版本。</span><span class="sxs-lookup"><span data-stu-id="16cb0-117">Antispyware signature version.</span></span>

</dd> <dt>

<span data-ttu-id="16cb0-118">**AVDeltaSignatureVersion**</span><span class="sxs-lookup"><span data-stu-id="16cb0-118">**AVDeltaSignatureVersion**</span></span>
</dt> <dd>

<span data-ttu-id="16cb0-119">類型： **ULONGLONG**</span><span class="sxs-lookup"><span data-stu-id="16cb0-119">Type: **ULONGLONG**</span></span>

</dd> <dd>

<span data-ttu-id="16cb0-120">防毒軟體特徵碼版本</span><span class="sxs-lookup"><span data-stu-id="16cb0-120">Antivirus signature version</span></span>

</dd> <dt>

<span data-ttu-id="16cb0-121">**HashType**</span><span class="sxs-lookup"><span data-stu-id="16cb0-121">**HashType**</span></span>
</dt> <dd>

<span data-ttu-id="16cb0-122">類型： **[ **MP \_ HASH \_ 類型**](mp-hash-type.md)**</span><span class="sxs-lookup"><span data-stu-id="16cb0-122">Type: **[**MP\_HASH\_TYPE**](mp-hash-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="16cb0-123">使用的雜湊類型。</span><span class="sxs-lookup"><span data-stu-id="16cb0-123">Hash type used.</span></span> <span data-ttu-id="16cb0-124">請參閱 [**MP \_ HASH \_ 類型**](mp-hash-type.md)。</span><span class="sxs-lookup"><span data-stu-id="16cb0-124">See [**MP\_HASH\_TYPE**](mp-hash-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="16cb0-125">**FidelityValue**</span><span class="sxs-lookup"><span data-stu-id="16cb0-125">**FidelityValue**</span></span>
</dt> <dd>

<span data-ttu-id="16cb0-126">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="16cb0-126">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="16cb0-127">精確度值。</span><span class="sxs-lookup"><span data-stu-id="16cb0-127">Fidelity value.</span></span>

</dd> <dt>

<span data-ttu-id="16cb0-128">**HashValue**</span><span class="sxs-lookup"><span data-stu-id="16cb0-128">**HashValue**</span></span>
</dt> <dd>

<span data-ttu-id="16cb0-129">類型： **MP \_ MIDL \_ STRING LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="16cb0-129">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="16cb0-130">檔案的雜湊。</span><span class="sxs-lookup"><span data-stu-id="16cb0-130">The hash of the file.</span></span>

</dd> <dt>

<span data-ttu-id="16cb0-131">**TargetFileName**</span><span class="sxs-lookup"><span data-stu-id="16cb0-131">**TargetFileName**</span></span>
</dt> <dd>

<span data-ttu-id="16cb0-132">類型： **MP \_ MIDL \_ STRING LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="16cb0-132">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="16cb0-133">目標檔案的路徑和名稱。</span><span class="sxs-lookup"><span data-stu-id="16cb0-133">The path and name of the targeted file.</span></span>

</dd> <dt>

<span data-ttu-id="16cb0-134">**TargetFileHash**</span><span class="sxs-lookup"><span data-stu-id="16cb0-134">**TargetFileHash**</span></span>
</dt> <dd>

<span data-ttu-id="16cb0-135">類型： **MP \_ MIDL \_ STRING LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="16cb0-135">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="16cb0-136">目標檔案的雜湊。</span><span class="sxs-lookup"><span data-stu-id="16cb0-136">The hash of the targeted file.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="16cb0-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="16cb0-137">Requirements</span></span>



| <span data-ttu-id="16cb0-138">需求</span><span class="sxs-lookup"><span data-stu-id="16cb0-138">Requirement</span></span> | <span data-ttu-id="16cb0-139">值</span><span class="sxs-lookup"><span data-stu-id="16cb0-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="16cb0-140">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="16cb0-140">Minimum supported client</span></span><br/> | <span data-ttu-id="16cb0-141">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="16cb0-141">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="16cb0-142">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="16cb0-142">Minimum supported server</span></span><br/> | <span data-ttu-id="16cb0-143">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="16cb0-143">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="16cb0-144">標頭</span><span class="sxs-lookup"><span data-stu-id="16cb0-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="16cb0-145"><dt>MpClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="16cb0-145"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16cb0-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="16cb0-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16cb0-147">**MP \_ HASH \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="16cb0-147">**MP\_HASH\_TYPE**</span></span>](mp-hash-type.md)
</dt> </dl>

 

 





