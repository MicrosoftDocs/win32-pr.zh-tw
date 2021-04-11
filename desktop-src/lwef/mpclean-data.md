---
title: 'MPCLEAN_DATA 結構 (MpClient .h) '
description: 傳遞給清除回呼函數的通知資料。
ms.assetid: 475A6525-5BD8-4B29-A684-53EE2758C790
keywords:
- MPCLEAN_DATA 結構舊版 Windows 環境功能
- PMPCLEAN_DATA 結構指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPCLEAN_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89f0c7e867918b6567279be7c41ce72e7e396576
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685789"
---
# <a name="mpclean_data-structure"></a><span data-ttu-id="ac150-105">MPCLEAN \_ 資料結構</span><span class="sxs-lookup"><span data-stu-id="ac150-105">MPCLEAN\_DATA structure</span></span>

<span data-ttu-id="ac150-106">傳遞給清除回呼函數的通知資料。</span><span class="sxs-lookup"><span data-stu-id="ac150-106">Notification data passed to clean callback function.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac150-107">語法</span><span class="sxs-lookup"><span data-stu-id="ac150-107">Syntax</span></span>


```C++
typedef struct tagMPCLEAN_DATA {
  MPTHREAT_ID      ThreatID;
  MPTHREAT_ACTION  ThreatAction;
  DWORD            dwStatus;
  PMPRESOURCE_INFO ResourceInfo;
} MPCLEAN_DATA, *PMPCLEAN_DATA;
```



## <a name="members"></a><span data-ttu-id="ac150-108">成員</span><span class="sxs-lookup"><span data-stu-id="ac150-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="ac150-109">**ThreatID**</span><span class="sxs-lookup"><span data-stu-id="ac150-109">**ThreatID**</span></span>
</dt> <dd>

<span data-ttu-id="ac150-110">類型： **MPTHREAT \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="ac150-110">Type: **MPTHREAT\_ID**</span></span>

</dd> <dd>

<span data-ttu-id="ac150-111">**MPNOTIFY \_ clean \_ 威脅 \_** 的威脅識別碼開始 / **MPNOTIFY \_ 乾淨 \_ 威脅 \_ 成功** / **MPNOTIFY \_ 清除 \_ 威脅 \_ 失敗** 事件。</span><span class="sxs-lookup"><span data-stu-id="ac150-111">Threat identifier for the **MPNOTIFY\_CLEAN\_THREAT\_START**/**MPNOTIFY\_CLEAN\_THREAT\_SUCCEEDED**/**MPNOTIFY\_CLEAN\_THREAT\_FAILED** events.</span></span> <span data-ttu-id="ac150-112">設定用來識別防毒軟體相關威脅的位位。</span><span class="sxs-lookup"><span data-stu-id="ac150-112">Upper bit is set to identify antivirus-related threats.</span></span>

</dd> <dt>

<span data-ttu-id="ac150-113">**ThreatAction**</span><span class="sxs-lookup"><span data-stu-id="ac150-113">**ThreatAction**</span></span>
</dt> <dd>

<span data-ttu-id="ac150-114">類型： **[ **MPTHREAT \_ 動作**](mpthreat-action.md)**</span><span class="sxs-lookup"><span data-stu-id="ac150-114">Type: **[**MPTHREAT\_ACTION**](mpthreat-action.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ac150-115">**MPNOTIFY \_ clean \_ 威脅 \_** 的威脅動作開始 / **MPNOTIFY \_ 乾淨 \_ 威脅 \_ 成功** / **MPNOTIFY \_ 清除 \_ 威脅 \_ 失敗** 事件。</span><span class="sxs-lookup"><span data-stu-id="ac150-115">Threat action for the **MPNOTIFY\_CLEAN\_THREAT\_START**/**MPNOTIFY\_CLEAN\_THREAT\_SUCCEEDED**/**MPNOTIFY\_CLEAN\_THREAT\_FAILED** events.</span></span> <span data-ttu-id="ac150-116">請參閱 [**MPTHREAT \_ 動作**](mpthreat-action.md)。</span><span class="sxs-lookup"><span data-stu-id="ac150-116">See [**MPTHREAT\_ACTION**](mpthreat-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="ac150-117">**dwStatus**</span><span class="sxs-lookup"><span data-stu-id="ac150-117">**dwStatus**</span></span>
</dt> <dd>

<span data-ttu-id="ac150-118">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="ac150-118">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="ac150-119">與所採取動作相關聯的其他狀態或動作。</span><span class="sxs-lookup"><span data-stu-id="ac150-119">Additional status or actions associated with the action taken.</span></span> <span data-ttu-id="ac150-120">這是 [**MPSTATUS \_ 旗**](mpstatus-flag.md)標的位旗標組合。</span><span class="sxs-lookup"><span data-stu-id="ac150-120">This is a combination of bit flags from [**MPSTATUS\_FLAG**](mpstatus-flag.md).</span></span>

</dd> <dt>

<span data-ttu-id="ac150-121">**ResourceInfo**</span><span class="sxs-lookup"><span data-stu-id="ac150-121">**ResourceInfo**</span></span>
</dt> <dd>

<span data-ttu-id="ac150-122">類型： **PMPRESOURCE \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="ac150-122">Type: **PMPRESOURCE\_INFO**</span></span>

</dd> <dd>

<span data-ttu-id="ac150-123">**MPNOTIFY \_ clean \_ 威脅 \_** 的資源資訊開始 / **MPNOTIFY \_ 乾淨 \_ 威脅 \_ 成功** / **MPNOTIFY \_ 清除 \_ 威脅 \_ 失敗** 的事件。</span><span class="sxs-lookup"><span data-stu-id="ac150-123">Resource information for the **MPNOTIFY\_CLEAN\_THREAT\_START**/**MPNOTIFY\_CLEAN\_THREAT\_SUCCEEDED**/**MPNOTIFY\_CLEAN\_THREAT\_FAILED** events.</span></span> <span data-ttu-id="ac150-124">請參閱 [**MPRESOURCE \_ 資訊**](mpresource-info.md)。</span><span class="sxs-lookup"><span data-stu-id="ac150-124">See [**MPRESOURCE\_INFO**](mpresource-info.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ac150-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="ac150-125">Requirements</span></span>



| <span data-ttu-id="ac150-126">需求</span><span class="sxs-lookup"><span data-stu-id="ac150-126">Requirement</span></span> | <span data-ttu-id="ac150-127">值</span><span class="sxs-lookup"><span data-stu-id="ac150-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ac150-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ac150-128">Minimum supported client</span></span><br/> | <span data-ttu-id="ac150-129">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ac150-129">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="ac150-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ac150-130">Minimum supported server</span></span><br/> | <span data-ttu-id="ac150-131">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ac150-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ac150-132">標頭</span><span class="sxs-lookup"><span data-stu-id="ac150-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac150-133"><dt>MpClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="ac150-133"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac150-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ac150-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac150-135">**MPRESOURCE \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="ac150-135">**MPRESOURCE\_INFO**</span></span>](mpresource-info.md)
</dt> <dt>

[<span data-ttu-id="ac150-136">**MPSTATUS \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="ac150-136">**MPSTATUS\_FLAG**</span></span>](mpstatus-flag.md)
</dt> <dt>

[<span data-ttu-id="ac150-137">**MPTHREAT \_ 動作**</span><span class="sxs-lookup"><span data-stu-id="ac150-137">**MPTHREAT\_ACTION**</span></span>](mpthreat-action.md)
</dt> </dl>

 

 





