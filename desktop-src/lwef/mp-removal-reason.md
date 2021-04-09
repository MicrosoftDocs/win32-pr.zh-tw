---
title: 'MP_REMOVAL_REASON 列舉 (MpClient .h) '
description: FastPath 簽章移除原因。
ms.assetid: A09B4903-E53C-4DA1-BD0B-6DE0124FCAB3
keywords:
- MP_REMOVAL_REASON 列舉舊版 Windows 環境功能
- PMP_REMOVAL_REASON 列舉指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MP_REMOVAL_REASON
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03ce70f46bd95d4183343990b40594326ed5d3b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686329"
---
# <a name="mp_removal_reason-enumeration"></a><span data-ttu-id="7e2b4-105">MP \_ 移除 \_ 原因列舉</span><span class="sxs-lookup"><span data-stu-id="7e2b4-105">MP\_REMOVAL\_REASON enumeration</span></span>

<span data-ttu-id="7e2b4-106">FastPath 簽章移除原因。</span><span class="sxs-lookup"><span data-stu-id="7e2b4-106">FastPath signature removal reason.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e2b4-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7e2b4-107">Syntax</span></span>


```C++
typedef enum tagMP_REMOVAL_REASON { 
  MP_REMOVAL_UNKNOWN    = 0,
  MP_REMOVAL_MANUAL     = 1,
  MP_REMOVAL_AUTOMATIC  = 2
} MP_REMOVAL_REASON, *PMP_REMOVAL_REASON;
```



## <a name="constants"></a><span data-ttu-id="7e2b4-108">常數</span><span class="sxs-lookup"><span data-stu-id="7e2b4-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="7e2b4-109"><span id="MP_REMOVAL_UNKNOWN"></span><span id="mp_removal_unknown"></span>**MP \_ 移除 \_ 不明**</span><span class="sxs-lookup"><span data-stu-id="7e2b4-109"><span id="MP_REMOVAL_UNKNOWN"></span><span id="mp_removal_unknown"></span>**MP\_REMOVAL\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="7e2b4-110">不明。</span><span class="sxs-lookup"><span data-stu-id="7e2b4-110">Unknown.</span></span>

</dd> <dt>

<span data-ttu-id="7e2b4-111"><span id="MP_REMOVAL_MANUAL"></span><span id="mp_removal_manual"></span>**MP \_ 移除 \_ 手動**</span><span class="sxs-lookup"><span data-stu-id="7e2b4-111"><span id="MP_REMOVAL_MANUAL"></span><span id="mp_removal_manual"></span>**MP\_REMOVAL\_MANUAL**</span></span>
</dt> <dd>

<span data-ttu-id="7e2b4-112">手動。</span><span class="sxs-lookup"><span data-stu-id="7e2b4-112">Manual.</span></span>

</dd> <dt>

<span data-ttu-id="7e2b4-113"><span id="MP_REMOVAL_AUTOMATIC"></span><span id="mp_removal_automatic"></span>**\_自動移除 \_ MP**</span><span class="sxs-lookup"><span data-stu-id="7e2b4-113"><span id="MP_REMOVAL_AUTOMATIC"></span><span id="mp_removal_automatic"></span>**MP\_REMOVAL\_AUTOMATIC**</span></span>
</dt> <dd>

<span data-ttu-id="7e2b4-114">自動。</span><span class="sxs-lookup"><span data-stu-id="7e2b4-114">Automatic.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7e2b4-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="7e2b4-115">Requirements</span></span>



| <span data-ttu-id="7e2b4-116">需求</span><span class="sxs-lookup"><span data-stu-id="7e2b4-116">Requirement</span></span> | <span data-ttu-id="7e2b4-117">值</span><span class="sxs-lookup"><span data-stu-id="7e2b4-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7e2b4-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7e2b4-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7e2b4-119">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7e2b4-119">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="7e2b4-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7e2b4-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7e2b4-121">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7e2b4-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7e2b4-122">標頭</span><span class="sxs-lookup"><span data-stu-id="7e2b4-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e2b4-123"><dt>MpClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="7e2b4-123"><dt>MpClient.h</dt></span></span> </dl> |



 

 





