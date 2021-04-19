---
title: 'MPTHREAT_DATA 結構 (MpClient .h) '
description: 因為威脅偵測或修改而傳遞的通知資料。
ms.assetid: 07A2F88B-9D58-44EC-86D0-BDCC1DF44B94
keywords:
- MPTHREAT_DATA 結構舊版 Windows 環境功能
- PMPTHREAT_DATA 結構指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPTHREAT_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cafbb11dbb3b1a34b38ffd0448db96fd1409efd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106995587"
---
# <a name="mpthreat_data-structure"></a><span data-ttu-id="2fa7b-105">MPTHREAT \_ 資料結構</span><span class="sxs-lookup"><span data-stu-id="2fa7b-105">MPTHREAT\_DATA structure</span></span>

<span data-ttu-id="2fa7b-106">因為威脅偵測或修改而傳遞的通知資料。</span><span class="sxs-lookup"><span data-stu-id="2fa7b-106">Notification data passed due to threat detection or modification.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fa7b-107">語法</span><span class="sxs-lookup"><span data-stu-id="2fa7b-107">Syntax</span></span>


```C++
typedef struct tagMPTHREAT_DATA {
  MPTHREAT_ID     ThreatID;
  DWORD           dwSessionID;
  MPTHREAT_ACTION ThreatAction;
  DWORD           dwStatus;
} MPTHREAT_DATA, *PMPTHREAT_DATA;
```



## <a name="members"></a><span data-ttu-id="2fa7b-108">成員</span><span class="sxs-lookup"><span data-stu-id="2fa7b-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="2fa7b-109">**ThreatID**</span><span class="sxs-lookup"><span data-stu-id="2fa7b-109">**ThreatID**</span></span>
</dt> <dd>

<span data-ttu-id="2fa7b-110">類型： **MPTHREAT \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="2fa7b-110">Type: **MPTHREAT\_ID**</span></span>

</dd> <dd>

<span data-ttu-id="2fa7b-111">威脅識別碼。</span><span class="sxs-lookup"><span data-stu-id="2fa7b-111">Threat identifier.</span></span> <span data-ttu-id="2fa7b-112">設定用來識別防毒軟體相關威脅的位位。</span><span class="sxs-lookup"><span data-stu-id="2fa7b-112">Upper bit is set to identify antivirus-related threats.</span></span>

</dd> <dt>

<span data-ttu-id="2fa7b-113">**dwSessionID**</span><span class="sxs-lookup"><span data-stu-id="2fa7b-113">**dwSessionID**</span></span>
</dt> <dd>

<span data-ttu-id="2fa7b-114">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="2fa7b-114">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="2fa7b-115">與威脅相關聯的會話。</span><span class="sxs-lookup"><span data-stu-id="2fa7b-115">Session associated with the threat.</span></span> <span data-ttu-id="2fa7b-116">如果沒有會話特定資訊可供使用，則設定為-1。</span><span class="sxs-lookup"><span data-stu-id="2fa7b-116">Set to -1 if no session specific information is available.</span></span>

</dd> <dt>

<span data-ttu-id="2fa7b-117">**ThreatAction**</span><span class="sxs-lookup"><span data-stu-id="2fa7b-117">**ThreatAction**</span></span>
</dt> <dd>

<span data-ttu-id="2fa7b-118">類型： **[ **MPTHREAT \_ 動作**](mpthreat-action.md)**</span><span class="sxs-lookup"><span data-stu-id="2fa7b-118">Type: **[**MPTHREAT\_ACTION**](mpthreat-action.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2fa7b-119">已嘗試 **MPNOTIFY \_ 威脅 \_ 清除 \_ 成功** / **MPNOTIFY \_ 威脅 \_ 清除 \_ 失敗** 事件的威脅動作。</span><span class="sxs-lookup"><span data-stu-id="2fa7b-119">Threat action tried for the **MPNOTIFY\_THREAT\_CLEAN\_SUCCEEDED**/**MPNOTIFY\_THREAT\_CLEAN\_FAILED** events.</span></span>

</dd> <dt>

<span data-ttu-id="2fa7b-120">**dwStatus**</span><span class="sxs-lookup"><span data-stu-id="2fa7b-120">**dwStatus**</span></span>
</dt> <dd>

<span data-ttu-id="2fa7b-121">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="2fa7b-121">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="2fa7b-122">與所採取動作相關聯的其他狀態或動作。</span><span class="sxs-lookup"><span data-stu-id="2fa7b-122">Additional status or actions associated with the action taken.</span></span> <span data-ttu-id="2fa7b-123">這是 [**MPSTATUS \_ 旗**](mpstatus-flag.md)標的位旗標組合。</span><span class="sxs-lookup"><span data-stu-id="2fa7b-123">This is a combination of bit flags from [**MPSTATUS\_FLAG**](mpstatus-flag.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2fa7b-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="2fa7b-124">Requirements</span></span>



| <span data-ttu-id="2fa7b-125">需求</span><span class="sxs-lookup"><span data-stu-id="2fa7b-125">Requirement</span></span> | <span data-ttu-id="2fa7b-126">值</span><span class="sxs-lookup"><span data-stu-id="2fa7b-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2fa7b-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2fa7b-127">Minimum supported client</span></span><br/> | <span data-ttu-id="2fa7b-128">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2fa7b-128">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="2fa7b-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2fa7b-129">Minimum supported server</span></span><br/> | <span data-ttu-id="2fa7b-130">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2fa7b-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2fa7b-131">標頭</span><span class="sxs-lookup"><span data-stu-id="2fa7b-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="2fa7b-132"><dt>MpClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="2fa7b-132"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2fa7b-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2fa7b-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fa7b-134">**MPSTATUS \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="2fa7b-134">**MPSTATUS\_FLAG**</span></span>](mpstatus-flag.md)
</dt> <dt>

[<span data-ttu-id="2fa7b-135">**MPTHREAT \_ 動作**</span><span class="sxs-lookup"><span data-stu-id="2fa7b-135">**MPTHREAT\_ACTION**</span></span>](mpthreat-action.md)
</dt> </dl>

 

 





