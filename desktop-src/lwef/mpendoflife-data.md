---
title: 'MPENDOFLIFE_DATA 結構 (MpClient .h) '
description: '\ 0034;生命週期結束 \ 0034;通知資料。'
ms.assetid: 00C2E707-9034-4BBC-99CF-3DFA4B8C08D9
keywords:
- MPENDOFLIFE_DATA 結構舊版 Windows 環境功能
- PMPENDOFLIFE_DATA 結構指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPENDOFLIFE_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e209b9b35a089523815c353e8a750152bf4af75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104850"
---
# <a name="mpendoflife_data-structure"></a><span data-ttu-id="90364-105">MPENDOFLIFE \_ 資料結構</span><span class="sxs-lookup"><span data-stu-id="90364-105">MPENDOFLIFE\_DATA structure</span></span>

<span data-ttu-id="90364-106">「生命週期結束」通知資料。</span><span class="sxs-lookup"><span data-stu-id="90364-106">"End of life" notification data.</span></span>

## <a name="syntax"></a><span data-ttu-id="90364-107">語法</span><span class="sxs-lookup"><span data-stu-id="90364-107">Syntax</span></span>


```C++
typedef struct tagMPENDOFLIFE_DATA {
  FILETIME ftSignatureExpiry;
  FILETIME ftPlatformExpiry;
  BOOL     fAdminControlled;
  BOOL     fEndOfLifeImpendingOrPast;
} MPENDOFLIFE_DATA, *PMPENDOFLIFE_DATA;
```



## <a name="members"></a><span data-ttu-id="90364-108">成員</span><span class="sxs-lookup"><span data-stu-id="90364-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="90364-109">**ftSignatureExpiry**</span><span class="sxs-lookup"><span data-stu-id="90364-109">**ftSignatureExpiry**</span></span>
</dt> <dd>

<span data-ttu-id="90364-110">類型： **FILETIME**</span><span class="sxs-lookup"><span data-stu-id="90364-110">Type: **FILETIME**</span></span>

</dd> <dd>

<span data-ttu-id="90364-111">簽章到期的時間。</span><span class="sxs-lookup"><span data-stu-id="90364-111">Time when the signature expires.</span></span>

</dd> <dt>

<span data-ttu-id="90364-112">**ftPlatformExpiry**</span><span class="sxs-lookup"><span data-stu-id="90364-112">**ftPlatformExpiry**</span></span>
</dt> <dd>

<span data-ttu-id="90364-113">類型： **FILETIME**</span><span class="sxs-lookup"><span data-stu-id="90364-113">Type: **FILETIME**</span></span>

</dd> <dd>

<span data-ttu-id="90364-114">平臺到期的時間。</span><span class="sxs-lookup"><span data-stu-id="90364-114">Time when the platform expires.</span></span>

</dd> <dt>

<span data-ttu-id="90364-115">**fAdminControlled**</span><span class="sxs-lookup"><span data-stu-id="90364-115">**fAdminControlled**</span></span>
</dt> <dd>

<span data-ttu-id="90364-116">類型： **BOOL**</span><span class="sxs-lookup"><span data-stu-id="90364-116">Type: **BOOL**</span></span>

</dd> <dd>

<span data-ttu-id="90364-117">如果系統管理員控制用來顯示通知的原則，則為 True。</span><span class="sxs-lookup"><span data-stu-id="90364-117">True if the administrator controlling the policy for showing the notification.</span></span> <span data-ttu-id="90364-118">如果設定，則會告訴 UI 不要顯示 EOL 通知。</span><span class="sxs-lookup"><span data-stu-id="90364-118">If set, this tells the UI to not show the EOL notification.</span></span>

</dd> <dt>

<span data-ttu-id="90364-119">**fEndOfLifeImpendingOrPast**</span><span class="sxs-lookup"><span data-stu-id="90364-119">**fEndOfLifeImpendingOrPast**</span></span>
</dt> <dd>

<span data-ttu-id="90364-120">類型： **BOOL**</span><span class="sxs-lookup"><span data-stu-id="90364-120">Type: **BOOL**</span></span>

</dd> <dd>

<span data-ttu-id="90364-121">如果「生命週期結束」暫止或超過此值，則為 True。</span><span class="sxs-lookup"><span data-stu-id="90364-121">True if "End of Life" is pending or past.</span></span> <span data-ttu-id="90364-122">如果為 false，則 UI 和用戶端可以清除任何 EOL 相關狀態。</span><span class="sxs-lookup"><span data-stu-id="90364-122">If false, UI and clients can clear any EOL related states.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="90364-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="90364-123">Requirements</span></span>



| <span data-ttu-id="90364-124">需求</span><span class="sxs-lookup"><span data-stu-id="90364-124">Requirement</span></span> | <span data-ttu-id="90364-125">值</span><span class="sxs-lookup"><span data-stu-id="90364-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="90364-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="90364-126">Minimum supported client</span></span><br/> | <span data-ttu-id="90364-127">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="90364-127">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="90364-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="90364-128">Minimum supported server</span></span><br/> | <span data-ttu-id="90364-129">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="90364-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="90364-130">標頭</span><span class="sxs-lookup"><span data-stu-id="90364-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="90364-131"><dt>MpClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="90364-131"><dt>MpClient.h</dt></span></span> </dl> |



 

 





