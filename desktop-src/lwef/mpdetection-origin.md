---
title: 'MPDETECTION_ORIGIN 列舉 (MpClient .h) '
description: 偵測來源。
ms.assetid: 9FEE2FAD-3E44-4134-B968-53E971F6B092
keywords:
- MPDETECTION_ORIGIN 列舉舊版 Windows 環境功能
- PMPDETECTION_ORIGIN 列舉指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPDETECTION_ORIGIN
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed4224aafef2c72db2a8d3b27f338ca83feaf64f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969774"
---
# <a name="mpdetection_origin-enumeration"></a><span data-ttu-id="c9389-105">MPDETECTION \_ 原始列舉</span><span class="sxs-lookup"><span data-stu-id="c9389-105">MPDETECTION\_ORIGIN enumeration</span></span>

<span data-ttu-id="c9389-106">偵測來源。</span><span class="sxs-lookup"><span data-stu-id="c9389-106">Detection origin.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9389-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c9389-107">Syntax</span></span>


```C++
typedef enum tagMPDETECTION_ORIGIN { 
  MPDETECTION_ORIGIN_UNKNOWN        = 0,
  MPDETECTION_ORIGIN_LOCAL_MACHINE  = 1 << 0,
  MPDETECTION_ORIGIN_NETWORKSHARE   = 1 << 1,
  MPDETECTION_ORIGIN_INTERNET       = 1 << 2,
  MPDETECTION_ORIGIN_OUTBOUND       = 1 << 3,
  MPDETECTION_ORIGIN_INBOUND        = 1 << 4
} MPDETECTION_ORIGIN, *PMPDETECTION_ORIGIN;
```



## <a name="constants"></a><span data-ttu-id="c9389-108">常數</span><span class="sxs-lookup"><span data-stu-id="c9389-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="c9389-109"><span id="MPDETECTION_ORIGIN_UNKNOWN"></span><span id="mpdetection_origin_unknown"></span>**MPDETECTION \_ 來源 \_ 不明**</span><span class="sxs-lookup"><span data-stu-id="c9389-109"><span id="MPDETECTION_ORIGIN_UNKNOWN"></span><span id="mpdetection_origin_unknown"></span>**MPDETECTION\_ORIGIN\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="c9389-110">偵測到的威脅來源不明。</span><span class="sxs-lookup"><span data-stu-id="c9389-110">Threat detected origin unknown.</span></span>

</dd> <dt>

<span data-ttu-id="c9389-111"><span id="MPDETECTION_ORIGIN_LOCAL_MACHINE"></span><span id="mpdetection_origin_local_machine"></span>**MPDETECTION \_ 來源 \_ 本機 \_ 電腦**</span><span class="sxs-lookup"><span data-stu-id="c9389-111"><span id="MPDETECTION_ORIGIN_LOCAL_MACHINE"></span><span id="mpdetection_origin_local_machine"></span>**MPDETECTION\_ORIGIN\_LOCAL\_MACHINE**</span></span>
</dt> <dd>

<span data-ttu-id="c9389-112">在本機電腦上偵測到威脅。</span><span class="sxs-lookup"><span data-stu-id="c9389-112">Threat detected on local machine.</span></span>

</dd> <dt>

<span data-ttu-id="c9389-113"><span id="MPDETECTION_ORIGIN_NETWORKSHARE"></span><span id="mpdetection_origin_networkshare"></span>**MPDETECTION \_ 原始 \_ NETWORKSHARE**</span><span class="sxs-lookup"><span data-stu-id="c9389-113"><span id="MPDETECTION_ORIGIN_NETWORKSHARE"></span><span id="mpdetection_origin_networkshare"></span>**MPDETECTION\_ORIGIN\_NETWORKSHARE**</span></span>
</dt> <dd>

<span data-ttu-id="c9389-114">在網路共用上偵測到威脅。</span><span class="sxs-lookup"><span data-stu-id="c9389-114">Threat detected on network share.</span></span>

</dd> <dt>

<span data-ttu-id="c9389-115"><span id="MPDETECTION_ORIGIN_INTERNET"></span><span id="mpdetection_origin_internet"></span>**MPDETECTION \_ 來源 \_ 網際網路**</span><span class="sxs-lookup"><span data-stu-id="c9389-115"><span id="MPDETECTION_ORIGIN_INTERNET"></span><span id="mpdetection_origin_internet"></span>**MPDETECTION\_ORIGIN\_INTERNET**</span></span>
</dt> <dd>

<span data-ttu-id="c9389-116">在網際網路上偵測到威脅。</span><span class="sxs-lookup"><span data-stu-id="c9389-116">Threat detected on internet.</span></span>

</dd> <dt>

<span data-ttu-id="c9389-117"><span id="MPDETECTION_ORIGIN_OUTBOUND"></span><span id="mpdetection_origin_outbound"></span>**MPDETECTION \_ 來源 \_ 輸出**</span><span class="sxs-lookup"><span data-stu-id="c9389-117"><span id="MPDETECTION_ORIGIN_OUTBOUND"></span><span id="mpdetection_origin_outbound"></span>**MPDETECTION\_ORIGIN\_OUTBOUND**</span></span>
</dt> <dd>

<span data-ttu-id="c9389-118">在輸出連接上偵測到威脅。</span><span class="sxs-lookup"><span data-stu-id="c9389-118">Threat detected on an outbound connection.</span></span>

</dd> <dt>

<span data-ttu-id="c9389-119"><span id="MPDETECTION_ORIGIN_INBOUND"></span><span id="mpdetection_origin_inbound"></span>**MPDETECTION \_ 來源 \_ 輸入**</span><span class="sxs-lookup"><span data-stu-id="c9389-119"><span id="MPDETECTION_ORIGIN_INBOUND"></span><span id="mpdetection_origin_inbound"></span>**MPDETECTION\_ORIGIN\_INBOUND**</span></span>
</dt> <dd>

<span data-ttu-id="c9389-120">在輸入連接上偵測到威脅。</span><span class="sxs-lookup"><span data-stu-id="c9389-120">Threat detected on an inbound connection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c9389-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="c9389-121">Requirements</span></span>



| <span data-ttu-id="c9389-122">需求</span><span class="sxs-lookup"><span data-stu-id="c9389-122">Requirement</span></span> | <span data-ttu-id="c9389-123">值</span><span class="sxs-lookup"><span data-stu-id="c9389-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c9389-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c9389-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c9389-125">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c9389-125">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="c9389-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c9389-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c9389-127">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c9389-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c9389-128">標頭</span><span class="sxs-lookup"><span data-stu-id="c9389-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9389-129"><dt>MpClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="c9389-129"><dt>MpClient.h</dt></span></span> </dl> |



 

 





