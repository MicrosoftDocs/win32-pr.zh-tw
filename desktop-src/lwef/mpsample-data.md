---
title: 'MPSAMPLE_DATA 結構 (MpClient .h) '
description: 傳遞給範例提交回呼函數的通知資料。
ms.assetid: 58F348C6-411D-4545-9D4D-A80095FD139B
keywords:
- MPSAMPLE_DATA 結構舊版 Windows 環境功能
- PMPSAMPLE_DATA 結構指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPSAMPLE_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24a894638465c0362069b8fdcbacddf98bfdd2c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106296"
---
# <a name="mpsample_data-structure"></a><span data-ttu-id="7cdba-105">MPSAMPLE \_ 資料結構</span><span class="sxs-lookup"><span data-stu-id="7cdba-105">MPSAMPLE\_DATA structure</span></span>

<span data-ttu-id="7cdba-106">傳遞給範例提交回呼函數的通知資料。</span><span class="sxs-lookup"><span data-stu-id="7cdba-106">Notification data passed to the sample submission callback function.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cdba-107">語法</span><span class="sxs-lookup"><span data-stu-id="7cdba-107">Syntax</span></span>


```C++
typedef struct tagMPSAMPLE_DATA {
  DWORD dwSampleIndex;
} MPSAMPLE_DATA, *PMPSAMPLE_DATA;
```



## <a name="members"></a><span data-ttu-id="7cdba-108">成員</span><span class="sxs-lookup"><span data-stu-id="7cdba-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="7cdba-109">**dwSampleIndex**</span><span class="sxs-lookup"><span data-stu-id="7cdba-109">**dwSampleIndex**</span></span>
</dt> <dd>

<span data-ttu-id="7cdba-110">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="7cdba-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="7cdba-111">回報其提交狀態之範例專案的索引。</span><span class="sxs-lookup"><span data-stu-id="7cdba-111">Index of the sample item for which the submission status is reported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7cdba-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="7cdba-112">Requirements</span></span>



| <span data-ttu-id="7cdba-113">需求</span><span class="sxs-lookup"><span data-stu-id="7cdba-113">Requirement</span></span> | <span data-ttu-id="7cdba-114">值</span><span class="sxs-lookup"><span data-stu-id="7cdba-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7cdba-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7cdba-115">Minimum supported client</span></span><br/> | <span data-ttu-id="7cdba-116">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7cdba-116">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="7cdba-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7cdba-117">Minimum supported server</span></span><br/> | <span data-ttu-id="7cdba-118">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7cdba-118">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7cdba-119">標頭</span><span class="sxs-lookup"><span data-stu-id="7cdba-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="7cdba-120"><dt>MpClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="7cdba-120"><dt>MpClient.h</dt></span></span> </dl> |



 

 





