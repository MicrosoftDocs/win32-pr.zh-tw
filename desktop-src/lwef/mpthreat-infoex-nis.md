---
title: 'MPTHREAT_INFOEX_NIS 結構 (MpClient .h) '
description: 包含 NIS 特定的資訊。
ms.assetid: 3887C5BF-B1F6-4420-B40A-9585E44BE7A9
keywords:
- MPTHREAT_INFOEX_NIS 結構舊版 Windows 環境功能
- PMPTHREAT_INFOEX_NIS 結構指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPTHREAT_INFOEX_NIS
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b4ed68432a2d0ebe78535a139fcc7b0882b9ba7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025044"
---
# <a name="mpthreat_infoex_nis-structure"></a><span data-ttu-id="05f9c-105">MPTHREAT \_ INFOEX \_ NIS 結構</span><span class="sxs-lookup"><span data-stu-id="05f9c-105">MPTHREAT\_INFOEX\_NIS structure</span></span>

<span data-ttu-id="05f9c-106">包含 NIS 特定的資訊。</span><span class="sxs-lookup"><span data-stu-id="05f9c-106">Contains NIS-specific information.</span></span>

## <a name="syntax"></a><span data-ttu-id="05f9c-107">語法</span><span class="sxs-lookup"><span data-stu-id="05f9c-107">Syntax</span></span>


```C++
typedef struct tagMPTHREAT_INFOEX_NIS {
  MP_MIDL_STRING LPWSTR SourceIP;
  MP_MIDL_STRING LPWSTR DestinationIP;
  DWORD                 dwSourceport;
  DWORD                 dwDestinationport;
  MP_MIDL_STRING LPWSTR Protocol;
  MP_MIDL_STRING LPWSTR Link;
} MPTHREAT_INFOEX_NIS, *PMPTHREAT_INFOEX_NIS;
```



## <a name="members"></a><span data-ttu-id="05f9c-108">成員</span><span class="sxs-lookup"><span data-stu-id="05f9c-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="05f9c-109">**SourceIP**</span><span class="sxs-lookup"><span data-stu-id="05f9c-109">**SourceIP**</span></span>
</dt> <dd>

<span data-ttu-id="05f9c-110">類型： **MP \_ MIDL \_ STRING LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="05f9c-110">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd></dd> <dt>

<span data-ttu-id="05f9c-111">**DestinationIP**</span><span class="sxs-lookup"><span data-stu-id="05f9c-111">**DestinationIP**</span></span>
</dt> <dd>

<span data-ttu-id="05f9c-112">類型： **MP \_ MIDL \_ STRING LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="05f9c-112">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd></dd> <dt>

<span data-ttu-id="05f9c-113">**dwSourceport**</span><span class="sxs-lookup"><span data-stu-id="05f9c-113">**dwSourceport**</span></span>
</dt> <dd>

<span data-ttu-id="05f9c-114">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="05f9c-114">Type: **DWORD**</span></span>

</dd> <dd></dd> <dt>

<span data-ttu-id="05f9c-115">**dwDestinationport**</span><span class="sxs-lookup"><span data-stu-id="05f9c-115">**dwDestinationport**</span></span>
</dt> <dd>

<span data-ttu-id="05f9c-116">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="05f9c-116">Type: **DWORD**</span></span>

</dd> <dd></dd> <dt>

<span data-ttu-id="05f9c-117">**通訊協定**</span><span class="sxs-lookup"><span data-stu-id="05f9c-117">**Protocol**</span></span>
</dt> <dd>

<span data-ttu-id="05f9c-118">類型： **MP \_ MIDL \_ STRING LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="05f9c-118">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd></dd> <dt>

<span data-ttu-id="05f9c-119">**連結**</span><span class="sxs-lookup"><span data-stu-id="05f9c-119">**Link**</span></span>
</dt> <dd>

<span data-ttu-id="05f9c-120">類型： **MP \_ MIDL \_ STRING LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="05f9c-120">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

<span data-ttu-id="05f9c-121"></dd> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="05f9c-121"></dd> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="05f9c-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="05f9c-122">Requirements</span></span>



| <span data-ttu-id="05f9c-123">需求</span><span class="sxs-lookup"><span data-stu-id="05f9c-123">Requirement</span></span> | <span data-ttu-id="05f9c-124">值</span><span class="sxs-lookup"><span data-stu-id="05f9c-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="05f9c-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="05f9c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="05f9c-126">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="05f9c-126">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="05f9c-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="05f9c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="05f9c-128">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="05f9c-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="05f9c-129">標頭</span><span class="sxs-lookup"><span data-stu-id="05f9c-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="05f9c-130"><dt>MpClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="05f9c-130"><dt>MpClient.h</dt></span></span> </dl> |



 

 





