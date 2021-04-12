---
title: 'MPTHREAT_LOCALIZED_INFO 結構 (MpClient .h) '
description: 威脅的當地語系化資訊。
ms.assetid: 99DC9737-9A61-4407-B544-A7A979C5B556
keywords:
- MPTHREAT_LOCALIZED_INFO 結構舊版 Windows 環境功能
- PMPTHREAT_LOCALIZED_INFO 結構指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPTHREAT_LOCALIZED_INFO
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87ea0bee7c8cae15389b40b64038aad92a56dd5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384601"
---
# <a name="mpthreat_localized_info-structure"></a><span data-ttu-id="3d157-105">MPTHREAT \_ 當地語系化的 \_ 資訊結構</span><span class="sxs-lookup"><span data-stu-id="3d157-105">MPTHREAT\_LOCALIZED\_INFO structure</span></span>

<span data-ttu-id="3d157-106">威脅的當地語系化資訊。</span><span class="sxs-lookup"><span data-stu-id="3d157-106">Localized information for a threat.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d157-107">語法</span><span class="sxs-lookup"><span data-stu-id="3d157-107">Syntax</span></span>


```C++
typedef struct tagMPTHREAT_LOCALIZED_INFO {
  MPTHREAT_ID           ThreatID;
  MP_MIDL_STRING LPWSTR CategoryName;
  MP_MIDL_STRING LPWSTR CategoryDescription;
  MP_MIDL_STRING LPWSTR SeverityName;
  MP_MIDL_STRING LPWSTR SeverityDescription;
  MP_MIDL_STRING LPWSTR ShortDescription;
  MP_MIDL_STRING LPWSTR DefaultActionName;;
  MP_MIDL_STRING LPWSTR Advice;
  MP_MIDL_STRING LPWSTR ThreatUrl;
} MPTHREAT_LOCALIZED_INFO, *PMPTHREAT_LOCALIZED_INFO;
```



## <a name="members"></a><span data-ttu-id="3d157-108">成員</span><span class="sxs-lookup"><span data-stu-id="3d157-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="3d157-109">**ThreatID**</span><span class="sxs-lookup"><span data-stu-id="3d157-109">**ThreatID**</span></span>
</dt> <dd>

<span data-ttu-id="3d157-110">類型： **MPTHREAT \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="3d157-110">Type: **MPTHREAT\_ID**</span></span>

</dd> <dd>

<span data-ttu-id="3d157-111">威脅識別碼。</span><span class="sxs-lookup"><span data-stu-id="3d157-111">Threat identifier.</span></span> <span data-ttu-id="3d157-112">設定用來識別防毒軟體相關威脅的位位。</span><span class="sxs-lookup"><span data-stu-id="3d157-112">Upper bit is set to identify antivirus-related threats.</span></span>

</dd> <dt>

<span data-ttu-id="3d157-113">**CategoryName**</span><span class="sxs-lookup"><span data-stu-id="3d157-113">**CategoryName**</span></span>
</dt> <dd>

<span data-ttu-id="3d157-114">類型： **MP \_ MIDL \_ STRING LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="3d157-114">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="3d157-115">威脅分類，例如特洛伊程式或 keylogger。</span><span class="sxs-lookup"><span data-stu-id="3d157-115">Threat classification, such as a trojan or a keylogger.</span></span>

</dd> <dt>

<span data-ttu-id="3d157-116">**CategoryDescription**</span><span class="sxs-lookup"><span data-stu-id="3d157-116">**CategoryDescription**</span></span>
</dt> <dd>

<span data-ttu-id="3d157-117">類型： **MP \_ MIDL \_ STRING LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="3d157-117">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="3d157-118">威脅類別目錄的描述。</span><span class="sxs-lookup"><span data-stu-id="3d157-118">Description of threat category.</span></span>

</dd> <dt>

<span data-ttu-id="3d157-119">**SeverityName**</span><span class="sxs-lookup"><span data-stu-id="3d157-119">**SeverityName**</span></span>
</dt> <dd>

<span data-ttu-id="3d157-120">類型： **MP \_ MIDL \_ STRING LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="3d157-120">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="3d157-121">威脅嚴重性層級，例如「嚴重」或「適中」。</span><span class="sxs-lookup"><span data-stu-id="3d157-121">Threat severity level, such as severe or moderate.</span></span>

</dd> <dt>

<span data-ttu-id="3d157-122">**SeverityDescription**</span><span class="sxs-lookup"><span data-stu-id="3d157-122">**SeverityDescription**</span></span>
</dt> <dd>

<span data-ttu-id="3d157-123">類型： **MP \_ MIDL \_ STRING LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="3d157-123">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="3d157-124">威脅嚴重性層級的描述。</span><span class="sxs-lookup"><span data-stu-id="3d157-124">Description of threat severity level.</span></span>

</dd> <dt>

<span data-ttu-id="3d157-125">**ShortDescription**</span><span class="sxs-lookup"><span data-stu-id="3d157-125">**ShortDescription**</span></span>
</dt> <dd>

<span data-ttu-id="3d157-126">類型： **MP \_ MIDL \_ STRING LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="3d157-126">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="3d157-127">威脅的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="3d157-127">Short description of threat.</span></span>

</dd> <dt>

<span data-ttu-id="3d157-128">**DefaultActionName;**</span><span class="sxs-lookup"><span data-stu-id="3d157-128">**DefaultActionName;**</span></span>
</dt> <dd>

<span data-ttu-id="3d157-129">類型： **MP \_ MIDL \_ STRING LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="3d157-129">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="3d157-130">引擎建議的預設動作名稱，例如移除或隔離。</span><span class="sxs-lookup"><span data-stu-id="3d157-130">Name of default action, such as remove or quarantine, suggested by engine.</span></span>

</dd> <dt>

<span data-ttu-id="3d157-131">**建議**</span><span class="sxs-lookup"><span data-stu-id="3d157-131">**Advice**</span></span>
</dt> <dd>

<span data-ttu-id="3d157-132">類型： **MP \_ MIDL \_ STRING LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="3d157-132">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="3d157-133">特定威脅的建議。</span><span class="sxs-lookup"><span data-stu-id="3d157-133">Advice for the particular threat.</span></span>

</dd> <dt>

<span data-ttu-id="3d157-134">**ThreatUrl**</span><span class="sxs-lookup"><span data-stu-id="3d157-134">**ThreatUrl**</span></span>
</dt> <dd>

<span data-ttu-id="3d157-135">類型： **MP \_ MIDL \_ STRING LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="3d157-135">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="3d157-136">包含威脅相關資訊之網頁的 URL。</span><span class="sxs-lookup"><span data-stu-id="3d157-136">A URL to a webpage containing information about the threat.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3d157-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="3d157-137">Requirements</span></span>



| <span data-ttu-id="3d157-138">需求</span><span class="sxs-lookup"><span data-stu-id="3d157-138">Requirement</span></span> | <span data-ttu-id="3d157-139">值</span><span class="sxs-lookup"><span data-stu-id="3d157-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3d157-140">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3d157-140">Minimum supported client</span></span><br/> | <span data-ttu-id="3d157-141">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3d157-141">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="3d157-142">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3d157-142">Minimum supported server</span></span><br/> | <span data-ttu-id="3d157-143">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3d157-143">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3d157-144">標頭</span><span class="sxs-lookup"><span data-stu-id="3d157-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d157-145"><dt>MpClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="3d157-145"><dt>MpClient.h</dt></span></span> </dl> |



 

 





