---
title: 'MPNIS_PRI加值稅E_DATA 結構 (MpClient .h) '
description: 私人 NIS 通知。
ms.assetid: 19B4928F-BC78-4DEA-A563-1516B6454465
keywords:
- MPNIS_PRI加值稅E_DATA 結構舊版 Windows 環境功能
- PMPNIS_PRI加值稅E_DATA 結構指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPNIS_PRIVATE_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21340665a32b619c42d7909e8cd1b72ca6d09fb7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685567"
---
# <a name="mpnis_private_data-structure"></a><span data-ttu-id="46858-105">MPNIS \_ 私用 \_ 資料結構</span><span class="sxs-lookup"><span data-stu-id="46858-105">MPNIS\_PRIVATE\_DATA structure</span></span>

<span data-ttu-id="46858-106">私人 NIS 通知。</span><span class="sxs-lookup"><span data-stu-id="46858-106">Private NIS notifications.</span></span>

## <a name="syntax"></a><span data-ttu-id="46858-107">語法</span><span class="sxs-lookup"><span data-stu-id="46858-107">Syntax</span></span>


```C++
typedef struct tagMPNIS_PRIVATE_DATA {
  DWORD dwNotificationType;
  DWORD cbDataSize;
  BYTE  *pbData;
} MPNIS_PRIVATE_DATA, *PMPNIS_PRIVATE_DATA;
```



## <a name="members"></a><span data-ttu-id="46858-108">成員</span><span class="sxs-lookup"><span data-stu-id="46858-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="46858-109">**dwNotificationType**</span><span class="sxs-lookup"><span data-stu-id="46858-109">**dwNotificationType**</span></span>
</dt> <dd>

<span data-ttu-id="46858-110">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="46858-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="46858-111">通知的類型。</span><span class="sxs-lookup"><span data-stu-id="46858-111">Type of notification.</span></span>

</dd> <dt>

<span data-ttu-id="46858-112">**cbDataSize**</span><span class="sxs-lookup"><span data-stu-id="46858-112">**cbDataSize**</span></span>
</dt> <dd>

<span data-ttu-id="46858-113">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="46858-113">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="46858-114">保留資料的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="46858-114">Size of reserved data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="46858-115">**pbData**</span><span class="sxs-lookup"><span data-stu-id="46858-115">**pbData**</span></span>
</dt> <dd>

<span data-ttu-id="46858-116">類型：**位元組 \***</span><span class="sxs-lookup"><span data-stu-id="46858-116">Type: **BYTE\***</span></span>

</dd> <dd>

<span data-ttu-id="46858-117">保留資料的指標。</span><span class="sxs-lookup"><span data-stu-id="46858-117">Pointer to reserved data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="46858-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="46858-118">Requirements</span></span>



| <span data-ttu-id="46858-119">需求</span><span class="sxs-lookup"><span data-stu-id="46858-119">Requirement</span></span> | <span data-ttu-id="46858-120">值</span><span class="sxs-lookup"><span data-stu-id="46858-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="46858-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="46858-121">Minimum supported client</span></span><br/> | <span data-ttu-id="46858-122">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="46858-122">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="46858-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="46858-123">Minimum supported server</span></span><br/> | <span data-ttu-id="46858-124">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="46858-124">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="46858-125">標頭</span><span class="sxs-lookup"><span data-stu-id="46858-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="46858-126"><dt>MpClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="46858-126"><dt>MpClient.h</dt></span></span> </dl> |



 

 





