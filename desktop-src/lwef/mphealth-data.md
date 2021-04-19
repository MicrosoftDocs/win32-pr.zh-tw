---
title: 'MPHEALTH_DATA 結構 (MpClient .h) '
description: 健康情況通知資料。
ms.assetid: 37A87F77-386A-4508-B338-ED2151518968
keywords:
- MPHEALTH_DATA 結構舊版 Windows 環境功能
- PMPHEALTH_DATA 結構指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPHEALTH_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e729bdea82b6a885b64e95ecd77f9deae6bff4e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966145"
---
# <a name="mphealth_data-structure"></a><span data-ttu-id="d2a49-105">MPHEALTH \_ 資料結構</span><span class="sxs-lookup"><span data-stu-id="d2a49-105">MPHEALTH\_DATA structure</span></span>

<span data-ttu-id="d2a49-106">健康情況通知資料。</span><span class="sxs-lookup"><span data-stu-id="d2a49-106">Health notification data.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2a49-107">語法</span><span class="sxs-lookup"><span data-stu-id="d2a49-107">Syntax</span></span>


```C++
typedef struct tagMPHEALTH_DATA {
  DWORD dwNotificationType;
  DWORD dwNotificationFlag;
} MPHEALTH_DATA, *PMPHEALTH_DATA;
```



## <a name="members"></a><span data-ttu-id="d2a49-108">成員</span><span class="sxs-lookup"><span data-stu-id="d2a49-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="d2a49-109">**dwNotificationType**</span><span class="sxs-lookup"><span data-stu-id="d2a49-109">**dwNotificationType**</span></span>
</dt> <dd>

<span data-ttu-id="d2a49-110">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="d2a49-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="d2a49-111">通知的類型。</span><span class="sxs-lookup"><span data-stu-id="d2a49-111">Type of notification.</span></span>

</dd> <dt>

<span data-ttu-id="d2a49-112">**dwNotificationFlag**</span><span class="sxs-lookup"><span data-stu-id="d2a49-112">**dwNotificationFlag**</span></span>
</dt> <dd>

<span data-ttu-id="d2a49-113">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="d2a49-113">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="d2a49-114">未使用的。</span><span class="sxs-lookup"><span data-stu-id="d2a49-114">Unused.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d2a49-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="d2a49-115">Requirements</span></span>



| <span data-ttu-id="d2a49-116">需求</span><span class="sxs-lookup"><span data-stu-id="d2a49-116">Requirement</span></span> | <span data-ttu-id="d2a49-117">值</span><span class="sxs-lookup"><span data-stu-id="d2a49-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d2a49-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d2a49-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d2a49-119">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d2a49-119">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="d2a49-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d2a49-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d2a49-121">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d2a49-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d2a49-122">標頭</span><span class="sxs-lookup"><span data-stu-id="d2a49-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2a49-123"><dt>MpClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="d2a49-123"><dt>MpClient.h</dt></span></span> </dl> |



 

 





