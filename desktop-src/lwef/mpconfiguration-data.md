---
title: 'MPCONFIGURATION_DATA 結構 (MpClient .h) '
description: 包含設定變更的相關資料，包括舊值和新值。
ms.assetid: AB70B1C0-C148-44BC-8C0E-CC5D2A66BCA5
keywords:
- MPCONFIGURATION_DATA 結構舊版 Windows 環境功能
- PMPCONFIGURATION_DATA 結構指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPCONFIGURATION_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bb54ae4e323f2144dd25c52005d8484b0a207e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024947"
---
# <a name="mpconfiguration_data-structure"></a><span data-ttu-id="11127-105">MPCONFIGURATION \_ 資料結構</span><span class="sxs-lookup"><span data-stu-id="11127-105">MPCONFIGURATION\_DATA structure</span></span>

<span data-ttu-id="11127-106">包含設定變更的相關資料，包括舊值和新值。</span><span class="sxs-lookup"><span data-stu-id="11127-106">Contains data about configuration changes, including the old and new values.</span></span>

## <a name="syntax"></a><span data-ttu-id="11127-107">語法</span><span class="sxs-lookup"><span data-stu-id="11127-107">Syntax</span></span>


```C++
typedef struct tagMPCONFIGURATION_DATA {
  MP_MIDL_STRING LPWSTR ConfigurationName;
  DWORD                 DataType;
  DWORD                 PreviousDataSize;
  BYTE                  *pPreviousData;
  DWORD                 CurrentDataSize;
  BYTE                  *pCurrentData;
} MPCONFIGURATION_DATA, *PMPCONFIGURATION_DATA;
```



## <a name="members"></a><span data-ttu-id="11127-108">成員</span><span class="sxs-lookup"><span data-stu-id="11127-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="11127-109">**ConfigurationName**</span><span class="sxs-lookup"><span data-stu-id="11127-109">**ConfigurationName**</span></span>
</dt> <dd>

<span data-ttu-id="11127-110">類型： **MP \_ MIDL \_ STRING LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="11127-110">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="11127-111">變更的設定名稱。</span><span class="sxs-lookup"><span data-stu-id="11127-111">Name of the configuration that changed.</span></span>

</dd> <dt>

<span data-ttu-id="11127-112">**DataType**</span><span class="sxs-lookup"><span data-stu-id="11127-112">**DataType**</span></span>
</dt> <dd>

<span data-ttu-id="11127-113">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="11127-113">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="11127-114">使用的資料類型。</span><span class="sxs-lookup"><span data-stu-id="11127-114">The type of data used.</span></span>

</dd> <dt>

<span data-ttu-id="11127-115">**PreviousDataSize**</span><span class="sxs-lookup"><span data-stu-id="11127-115">**PreviousDataSize**</span></span>
</dt> <dd>

<span data-ttu-id="11127-116">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="11127-116">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="11127-117">先前資料的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="11127-117">Size of previous data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="11127-118">**pPreviousData**</span><span class="sxs-lookup"><span data-stu-id="11127-118">**pPreviousData**</span></span>
</dt> <dd>

<span data-ttu-id="11127-119">類型： \**BYTE \** _</span><span class="sxs-lookup"><span data-stu-id="11127-119">Type: \**BYTE\** _</span></span>

</dd> <dd>

<span data-ttu-id="11127-120">先前資料的指標。</span><span class="sxs-lookup"><span data-stu-id="11127-120">Pointer to previous data.</span></span>

</dd> <dt>

<span data-ttu-id="11127-121">_ *CurrentDataSize*\*</span><span class="sxs-lookup"><span data-stu-id="11127-121">_ *CurrentDataSize*\*</span></span>
</dt> <dd>

<span data-ttu-id="11127-122">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="11127-122">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="11127-123">新資料的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="11127-123">Size of new data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="11127-124">**pCurrentData**</span><span class="sxs-lookup"><span data-stu-id="11127-124">**pCurrentData**</span></span>
</dt> <dd>

<span data-ttu-id="11127-125">類型：**位元組 \***</span><span class="sxs-lookup"><span data-stu-id="11127-125">Type: **BYTE\***</span></span>

</dd> <dd>

<span data-ttu-id="11127-126">新資料的指標。</span><span class="sxs-lookup"><span data-stu-id="11127-126">Pointer to new data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="11127-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="11127-127">Requirements</span></span>



| <span data-ttu-id="11127-128">需求</span><span class="sxs-lookup"><span data-stu-id="11127-128">Requirement</span></span> | <span data-ttu-id="11127-129">值</span><span class="sxs-lookup"><span data-stu-id="11127-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="11127-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="11127-130">Minimum supported client</span></span><br/> | <span data-ttu-id="11127-131">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="11127-131">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="11127-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="11127-132">Minimum supported server</span></span><br/> | <span data-ttu-id="11127-133">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="11127-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="11127-134">標頭</span><span class="sxs-lookup"><span data-stu-id="11127-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="11127-135"><dt>MpClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="11127-135"><dt>MpClient.h</dt></span></span> </dl> |



 

 





