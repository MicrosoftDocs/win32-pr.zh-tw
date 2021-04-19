---
title: 'DRM_PLAYLIST_CONTENT_ID 結構 (Drmexternals .h) '
description: DRM \_ 播放清單 \_ 內容 \_ 識別碼結構包含在播放清單燒錄時複製到 CD 的內容相關資訊。
ms.assetid: 124e86ac-b0d4-40b2-868b-fe2fed1898e1
keywords:
- DRM_PLAYLIST_CONTENT_ID 結構 windows 媒體格式
- 結構 windows 媒體格式
topic_type:
- apiref
api_name:
- DRM_PLAYLIST_CONTENT_ID
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f475a8c3620ff1af64cb70914ca1ac591aa55106
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967352"
---
# <a name="drm_playlist_content_id-structure"></a><span data-ttu-id="2f023-105">DRM \_ 播放清單 \_ 內容 \_ 識別碼結構</span><span class="sxs-lookup"><span data-stu-id="2f023-105">DRM\_PLAYLIST\_CONTENT\_ID structure</span></span>

<span data-ttu-id="2f023-106">**DRM \_ 播放清單 \_ 內容 \_ 識別碼** 結構包含在播放清單燒錄時複製到 CD 的內容相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2f023-106">The **DRM\_PLAYLIST\_CONTENT\_ID** structure contains information about content that is to be copied to CD as part of a playlist burn.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f023-107">語法</span><span class="sxs-lookup"><span data-stu-id="2f023-107">Syntax</span></span>


```C++
typedef struct DRM_PLAYLIST_CONTENT_ID {
  LPCWSTR lpcwszV2Header;
  LPCSTR  lpcszV1KID;
  BYTE    *pbOtherData;
  DWORD   cbOtherData;
  DWORD   dwUniqueIDForSession;
  DWORD   dwValidFields;
} ;
```



## <a name="members"></a><span data-ttu-id="2f023-108">成員</span><span class="sxs-lookup"><span data-stu-id="2f023-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="2f023-109">**lpcwszV2Header**</span><span class="sxs-lookup"><span data-stu-id="2f023-109">**lpcwszV2Header**</span></span>
</dt> <dd>

<span data-ttu-id="2f023-110">DRM 標頭。</span><span class="sxs-lookup"><span data-stu-id="2f023-110">DRM header.</span></span> <span data-ttu-id="2f023-111">如果內容受到 Windows Media DRM 第2版或更新版本的保護，請使用這個成員。</span><span class="sxs-lookup"><span data-stu-id="2f023-111">Use this member if the content is protected by Windows Media DRM version 2 or later.</span></span>

</dd> <dt>

<span data-ttu-id="2f023-112">**lpcszV1KID**</span><span class="sxs-lookup"><span data-stu-id="2f023-112">**lpcszV1KID**</span></span>
</dt> <dd>

<span data-ttu-id="2f023-113">金鑰識別碼。</span><span class="sxs-lookup"><span data-stu-id="2f023-113">Key ID.</span></span> <span data-ttu-id="2f023-114">如果內容受到 Windows Media DRM 第1版的保護，請使用這個成員。</span><span class="sxs-lookup"><span data-stu-id="2f023-114">Use this member if the content is protected by Windows Media DRM version 1.</span></span>

</dd> <dt>

<span data-ttu-id="2f023-115">**pbOtherData**</span><span class="sxs-lookup"><span data-stu-id="2f023-115">**pbOtherData**</span></span>
</dt> <dd>

<span data-ttu-id="2f023-116">包含補充資料的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="2f023-116">Buffer containing supplementary data.</span></span>

</dd> <dt>

<span data-ttu-id="2f023-117">**cbOtherData**</span><span class="sxs-lookup"><span data-stu-id="2f023-117">**cbOtherData**</span></span>
</dt> <dd>

<span data-ttu-id="2f023-118">**PbOtherData** 緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="2f023-118">Size of the **pbOtherData** buffer in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="2f023-119">**dwUniqueIDForSession**</span><span class="sxs-lookup"><span data-stu-id="2f023-119">**dwUniqueIDForSession**</span></span>
</dt> <dd>

<span data-ttu-id="2f023-120">要在目前會話中使用之內容的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="2f023-120">Unique identifier for the content to be used in the current session.</span></span>

</dd> <dt>

<span data-ttu-id="2f023-121">**dwValidFields**</span><span class="sxs-lookup"><span data-stu-id="2f023-121">**dwValidFields**</span></span>
</dt> <dd>

<span data-ttu-id="2f023-122">**DWORD** ，表示此結構的有效欄位。</span><span class="sxs-lookup"><span data-stu-id="2f023-122">**DWORD** indicating the valid fields of this structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2f023-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="2f023-123">Requirements</span></span>



| <span data-ttu-id="2f023-124">需求</span><span class="sxs-lookup"><span data-stu-id="2f023-124">Requirement</span></span> | <span data-ttu-id="2f023-125">值</span><span class="sxs-lookup"><span data-stu-id="2f023-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f023-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2f023-126">Minimum supported client</span></span><br/> | <span data-ttu-id="2f023-127">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2f023-127">Windows XP \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="2f023-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2f023-128">Minimum supported server</span></span><br/> | <span data-ttu-id="2f023-129">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2f023-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="2f023-130">版本</span><span class="sxs-lookup"><span data-stu-id="2f023-130">Version</span></span><br/>                  | <span data-ttu-id="2f023-131">Windows Media Format 11 SDK</span><span class="sxs-lookup"><span data-stu-id="2f023-131">Windows Media Format 11 SDK</span></span><br/>                                                    |
| <span data-ttu-id="2f023-132">標頭</span><span class="sxs-lookup"><span data-stu-id="2f023-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f023-133"><dt>Drmexternals。h</dt></span><span class="sxs-lookup"><span data-stu-id="2f023-133"><dt>Drmexternals.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f023-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2f023-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f023-135">**結構**</span><span class="sxs-lookup"><span data-stu-id="2f023-135">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





