---
title: 'MPSTATUS_DATAEX_UNUSED 結構 (MpClient .h) '
description: 非 SRP 的虛擬結構。
ms.assetid: 396744CE-2435-4591-B0CF-A4392C88640F
keywords:
- MPSTATUS_DATAEX_UNUSED 結構舊版 Windows 環境功能
- PMPSTATUS_DATAEX_UNUSED 結構指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPSTATUS_DATAEX_UNUSED
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfcbc987a97a8cc47501a24e633c5da2d776a42d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106295"
---
# <a name="mpstatus_dataex_unused-structure"></a><span data-ttu-id="e7eba-105">MPSTATUS \_ DATAEX \_ 未使用的結構</span><span class="sxs-lookup"><span data-stu-id="e7eba-105">MPSTATUS\_DATAEX\_UNUSED structure</span></span>

<span data-ttu-id="e7eba-106">非 SRP 的虛擬結構。</span><span class="sxs-lookup"><span data-stu-id="e7eba-106">Dummy structure for non-SRP.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7eba-107">語法</span><span class="sxs-lookup"><span data-stu-id="e7eba-107">Syntax</span></span>


```C++
typedef struct tagMPSTATUS_DATAEX_UNUSED {
  DWORD dwNone;
} MPSTATUS_DATAEX_UNUSED, *PMPSTATUS_DATAEX_UNUSED;
```



## <a name="members"></a><span data-ttu-id="e7eba-108">成員</span><span class="sxs-lookup"><span data-stu-id="e7eba-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="e7eba-109">**dwNone**</span><span class="sxs-lookup"><span data-stu-id="e7eba-109">**dwNone**</span></span>
</dt> <dd>

<span data-ttu-id="e7eba-110">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="e7eba-110">Type: **DWORD**</span></span>

<span data-ttu-id="e7eba-111"></dd> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="e7eba-111"></dd> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="e7eba-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="e7eba-112">Requirements</span></span>



| <span data-ttu-id="e7eba-113">需求</span><span class="sxs-lookup"><span data-stu-id="e7eba-113">Requirement</span></span> | <span data-ttu-id="e7eba-114">值</span><span class="sxs-lookup"><span data-stu-id="e7eba-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e7eba-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e7eba-115">Minimum supported client</span></span><br/> | <span data-ttu-id="e7eba-116">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e7eba-116">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="e7eba-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e7eba-117">Minimum supported server</span></span><br/> | <span data-ttu-id="e7eba-118">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e7eba-118">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e7eba-119">標頭</span><span class="sxs-lookup"><span data-stu-id="e7eba-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7eba-120"><dt>MpClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="e7eba-120"><dt>MpClient.h</dt></span></span> </dl> |



 

 





