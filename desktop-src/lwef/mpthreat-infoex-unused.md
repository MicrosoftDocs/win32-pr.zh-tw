---
title: 'MPTHREAT_INFOEX_UNUSED 結構 (MpClient .h) '
description: 非行為修改類型威脅的虛擬結構。
ms.assetid: 3C5305CD-D533-47B5-ADD3-BD8DA05F2046
keywords:
- MPTHREAT_INFOEX_UNUSED 結構舊版 Windows 環境功能
- PMPTHREAT_INFOEX_UNUSED 結構指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPTHREAT_INFOEX_UNUSED
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fed78d904bd03fee17676dced7c828aaea8d319d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104537"
---
# <a name="mpthreat_infoex_unused-structure"></a><span data-ttu-id="879cb-105">MPTHREAT \_ INFOEX \_ 未使用的結構</span><span class="sxs-lookup"><span data-stu-id="879cb-105">MPTHREAT\_INFOEX\_UNUSED structure</span></span>

<span data-ttu-id="879cb-106">非行為修改類型威脅的虛擬結構。</span><span class="sxs-lookup"><span data-stu-id="879cb-106">Dummy structure for non-behavior modification type threats.</span></span>

## <a name="syntax"></a><span data-ttu-id="879cb-107">語法</span><span class="sxs-lookup"><span data-stu-id="879cb-107">Syntax</span></span>


```C++
typedef struct tagMPTHREAT_INFOEX_UNUSED {
  DWORD dwNone;
} MPTHREAT_INFOEX_UNUSED, *PMPTHREAT_INFOEX_UNUSED;
```



## <a name="members"></a><span data-ttu-id="879cb-108">成員</span><span class="sxs-lookup"><span data-stu-id="879cb-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="879cb-109">**dwNone**</span><span class="sxs-lookup"><span data-stu-id="879cb-109">**dwNone**</span></span>
</dt> <dd>

<span data-ttu-id="879cb-110">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="879cb-110">Type: **DWORD**</span></span>

<span data-ttu-id="879cb-111"></dd> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="879cb-111"></dd> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="879cb-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="879cb-112">Requirements</span></span>



| <span data-ttu-id="879cb-113">需求</span><span class="sxs-lookup"><span data-stu-id="879cb-113">Requirement</span></span> | <span data-ttu-id="879cb-114">值</span><span class="sxs-lookup"><span data-stu-id="879cb-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="879cb-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="879cb-115">Minimum supported client</span></span><br/> | <span data-ttu-id="879cb-116">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="879cb-116">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="879cb-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="879cb-117">Minimum supported server</span></span><br/> | <span data-ttu-id="879cb-118">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="879cb-118">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="879cb-119">標頭</span><span class="sxs-lookup"><span data-stu-id="879cb-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="879cb-120"><dt>MpClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="879cb-120"><dt>MpClient.h</dt></span></span> </dl> |



 

 





