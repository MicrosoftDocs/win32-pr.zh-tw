---
title: 'MPTHREAT_TYPE 列舉 (MpClient .h) '
description: 可能的威脅類型。
ms.assetid: 56061F12-AA89-4203-BED4-99613E24002A
keywords:
- MPTHREAT_TYPE 列舉舊版 Windows 環境功能
- PMPTHREAT_TYPE 列舉指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPTHREAT_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ed823b100c91f259252d7cad71e554099caf6a2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384406"
---
# <a name="mpthreat_type-enumeration"></a><span data-ttu-id="5f8ea-105">MPTHREAT \_ 類型列舉</span><span class="sxs-lookup"><span data-stu-id="5f8ea-105">MPTHREAT\_TYPE enumeration</span></span>

<span data-ttu-id="5f8ea-106">可能的威脅類型。</span><span class="sxs-lookup"><span data-stu-id="5f8ea-106">Possible threat types.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f8ea-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5f8ea-107">Syntax</span></span>


```C++
typedef enum tagMPTHREAT_TYPE { 
  MPTHREAT_TYPE_KNOWNBAD   = 0,
  MPTHREAT_TYPE_BEHAVIOR   = 1,
  MPTHREAT_TYPE_UNKNOWN    = 2,
  MPTHREAT_TYPE_KNOWNGOOD  = 3,
  MPTHREAT_TYPE_NIS        = 4,
  MPTHREAT_TYPE_MAXVALUE   = 4
} MPTHREAT_TYPE, *PMPTHREAT_TYPE;
```



## <a name="constants"></a><span data-ttu-id="5f8ea-108">常數</span><span class="sxs-lookup"><span data-stu-id="5f8ea-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="5f8ea-109"><span id="MPTHREAT_TYPE_KNOWNBAD"></span><span id="mpthreat_type_knownbad"></span>**MPTHREAT \_ 類型 \_ KNOWNBAD**</span><span class="sxs-lookup"><span data-stu-id="5f8ea-109"><span id="MPTHREAT_TYPE_KNOWNBAD"></span><span id="mpthreat_type_knownbad"></span>**MPTHREAT\_TYPE\_KNOWNBAD**</span></span>
</dt> <dd>

<span data-ttu-id="5f8ea-110">透過簽章偵測到已知的不良威脅。</span><span class="sxs-lookup"><span data-stu-id="5f8ea-110">Known bad threat detected via signature.</span></span>

</dd> <dt>

<span data-ttu-id="5f8ea-111"><span id="MPTHREAT_TYPE_BEHAVIOR"></span><span id="mpthreat_type_behavior"></span>**MPTHREAT \_ 類型 \_ 行為**</span><span class="sxs-lookup"><span data-stu-id="5f8ea-111"><span id="MPTHREAT_TYPE_BEHAVIOR"></span><span id="mpthreat_type_behavior"></span>**MPTHREAT\_TYPE\_BEHAVIOR**</span></span>
</dt> <dd>

<span data-ttu-id="5f8ea-112">透過行為監視偵測到可疑的威脅。</span><span class="sxs-lookup"><span data-stu-id="5f8ea-112">Suspicious threat detected via behavior monitoring.</span></span>

</dd> <dt>

<span data-ttu-id="5f8ea-113"><span id="MPTHREAT_TYPE_UNKNOWN"></span><span id="mpthreat_type_unknown"></span>**未知的 MPTHREAT \_ 類型 \_**</span><span class="sxs-lookup"><span data-stu-id="5f8ea-113"><span id="MPTHREAT_TYPE_UNKNOWN"></span><span id="mpthreat_type_unknown"></span>**MPTHREAT\_TYPE\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="5f8ea-114">未知的威脅 (非分類的) 。</span><span class="sxs-lookup"><span data-stu-id="5f8ea-114">Unknown threats (unclassified).</span></span>

</dd> <dt>

<span data-ttu-id="5f8ea-115"><span id="MPTHREAT_TYPE_KNOWNGOOD"></span><span id="mpthreat_type_knowngood"></span>**MPTHREAT \_ 類型 \_ KNOWNGOOD**</span><span class="sxs-lookup"><span data-stu-id="5f8ea-115"><span id="MPTHREAT_TYPE_KNOWNGOOD"></span><span id="mpthreat_type_knowngood"></span>**MPTHREAT\_TYPE\_KNOWNGOOD**</span></span>
</dt> <dd>

<span data-ttu-id="5f8ea-116">已知的良好威脅。</span><span class="sxs-lookup"><span data-stu-id="5f8ea-116">Known good threat.</span></span>

</dd> <dt>

<span data-ttu-id="5f8ea-117"><span id="MPTHREAT_TYPE_NIS"></span><span id="mpthreat_type_nis"></span>**MPTHREAT \_ 類型 \_ NIS**</span><span class="sxs-lookup"><span data-stu-id="5f8ea-117"><span id="MPTHREAT_TYPE_NIS"></span><span id="mpthreat_type_nis"></span>**MPTHREAT\_TYPE\_NIS**</span></span>
</dt> <dd>

<span data-ttu-id="5f8ea-118">NIS 威脅偵測。</span><span class="sxs-lookup"><span data-stu-id="5f8ea-118">NIS threat detection.</span></span>

</dd> <dt>

<span data-ttu-id="5f8ea-119"><span id="MPTHREAT_TYPE_MAXVALUE"></span><span id="mpthreat_type_maxvalue"></span>**MPTHREAT \_ 類型 \_**</span><span class="sxs-lookup"><span data-stu-id="5f8ea-119"><span id="MPTHREAT_TYPE_MAXVALUE"></span><span id="mpthreat_type_maxvalue"></span>**MPTHREAT\_TYPE\_MAXVALUE**</span></span>
</dt> <dd>

<span data-ttu-id="5f8ea-120">可能的最大值。</span><span class="sxs-lookup"><span data-stu-id="5f8ea-120">Maximum value possible.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5f8ea-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="5f8ea-121">Requirements</span></span>



| <span data-ttu-id="5f8ea-122">需求</span><span class="sxs-lookup"><span data-stu-id="5f8ea-122">Requirement</span></span> | <span data-ttu-id="5f8ea-123">值</span><span class="sxs-lookup"><span data-stu-id="5f8ea-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5f8ea-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5f8ea-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5f8ea-125">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5f8ea-125">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="5f8ea-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5f8ea-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5f8ea-127">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5f8ea-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5f8ea-128">標頭</span><span class="sxs-lookup"><span data-stu-id="5f8ea-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f8ea-129"><dt>MpClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="5f8ea-129"><dt>MpClient.h</dt></span></span> </dl> |



 

 





