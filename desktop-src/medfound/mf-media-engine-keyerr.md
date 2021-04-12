---
description: 定義媒體引擎的媒體金鑰錯誤碼。
ms.assetid: F6E13260-74A2-40D0-A704-4E1CDB16B8D8
title: MF_MEDIA_ENGINE_KEYERR 列舉
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_MEDIA_ENGINE_KEYERR
api_type:
- HeaderDef
api_location:
- mfmediaengine.h
ms.openlocfilehash: 22dd22a7771f5d1e9466709f0b0da9ee936ef2b9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104321515"
---
# <a name="mf_media_engine_keyerr-enumeration"></a><span data-ttu-id="507cb-103">MF \_ 媒體 \_ 引擎 \_ KEYERR 列舉</span><span class="sxs-lookup"><span data-stu-id="507cb-103">MF\_MEDIA\_ENGINE\_KEYERR enumeration</span></span>

<span data-ttu-id="507cb-104">定義媒體引擎的媒體金鑰錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="507cb-104">Defines media key error codes for the media engine.</span></span>

## <a name="syntax"></a><span data-ttu-id="507cb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="507cb-105">Syntax</span></span>


```C++
typedef enum _MF_MEDIA_ENGINE_KEYERR { 
  MF_MEDIAENGINE_KEYERR_UNKNOWN          = 1,
  MF_MEDIAENGINE_KEYERR_CLIENT           = 2,
  MF_MEDIAENGINE_KEYERR_SERVICE          = 3,
  MF_MEDIAENGINE_KEYERR_OUTPUT           = 4,
  MF_MEDIAENGINE_KEYERR_HARDWARECHANGE   = 5,
  MF_MEDIAENGINE_KEYERR_DOMAIN           = 6
} MF_MEDIA_ENGINE_KEYERR;
```



## <a name="constants"></a><span data-ttu-id="507cb-106">常數</span><span class="sxs-lookup"><span data-stu-id="507cb-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="507cb-107"><span id="MF_MEDIAENGINE_KEYERR_UNKNOWN"></span><span id="mf_mediaengine_keyerr_unknown"></span>**MF \_ MEDIAENGINE \_ KEYERR \_ 不明**</span><span class="sxs-lookup"><span data-stu-id="507cb-107"><span id="MF_MEDIAENGINE_KEYERR_UNKNOWN"></span><span id="mf_mediaengine_keyerr_unknown"></span>**MF\_MEDIAENGINE\_KEYERR\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="507cb-108">發生未知錯誤。</span><span class="sxs-lookup"><span data-stu-id="507cb-108">Unknown error occurred.</span></span>

</dd> <dt>

<span data-ttu-id="507cb-109"><span id="MF_MEDIAENGINE_KEYERR_CLIENT"></span><span id="mf_mediaengine_keyerr_client"></span>**MF \_ MEDIAENGINE \_ KEYERR \_ 用戶端**</span><span class="sxs-lookup"><span data-stu-id="507cb-109"><span id="MF_MEDIAENGINE_KEYERR_CLIENT"></span><span id="mf_mediaengine_keyerr_client"></span>**MF\_MEDIAENGINE\_KEYERR\_CLIENT**</span></span>
</dt> <dd>

<span data-ttu-id="507cb-110">發生用戶端錯誤。</span><span class="sxs-lookup"><span data-stu-id="507cb-110">An error with the client occurred.</span></span>

</dd> <dt>

<span data-ttu-id="507cb-111"><span id="MF_MEDIAENGINE_KEYERR_SERVICE"></span><span id="mf_mediaengine_keyerr_service"></span>**MF \_ MEDIAENGINE \_ KEYERR \_ 服務**</span><span class="sxs-lookup"><span data-stu-id="507cb-111"><span id="MF_MEDIAENGINE_KEYERR_SERVICE"></span><span id="mf_mediaengine_keyerr_service"></span>**MF\_MEDIAENGINE\_KEYERR\_SERVICE**</span></span>
</dt> <dd>

<span data-ttu-id="507cb-112">發生服務錯誤。</span><span class="sxs-lookup"><span data-stu-id="507cb-112">An error with the service occurred.</span></span>

</dd> <dt>

<span data-ttu-id="507cb-113"><span id="MF_MEDIAENGINE_KEYERR_OUTPUT"></span><span id="mf_mediaengine_keyerr_output"></span>**MF \_ MEDIAENGINE \_ KEYERR \_ 輸出**</span><span class="sxs-lookup"><span data-stu-id="507cb-113"><span id="MF_MEDIAENGINE_KEYERR_OUTPUT"></span><span id="mf_mediaengine_keyerr_output"></span>**MF\_MEDIAENGINE\_KEYERR\_OUTPUT**</span></span>
</dt> <dd>

<span data-ttu-id="507cb-114">發生輸出時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="507cb-114">An error with the output occurred.</span></span>

</dd> <dt>

<span data-ttu-id="507cb-115"><span id="MF_MEDIAENGINE_KEYERR_HARDWARECHANGE_"></span><span id="mf_mediaengine_keyerr_hardwarechange_"></span>**MF \_ MEDIAENGINE \_ KEYERR \_ HARDWARECHANGE**</span><span class="sxs-lookup"><span data-stu-id="507cb-115"><span id="MF_MEDIAENGINE_KEYERR_HARDWARECHANGE_"></span><span id="mf_mediaengine_keyerr_hardwarechange_"></span>**MF\_MEDIAENGINE\_KEYERR\_HARDWARECHANGE**</span></span> 
</dt> <dd>

<span data-ttu-id="507cb-116">發生與硬體變更相關的錯誤。</span><span class="sxs-lookup"><span data-stu-id="507cb-116">An error occurred related to a hardware change.</span></span>

</dd> <dt>

<span data-ttu-id="507cb-117"><span id="MF_MEDIAENGINE_KEYERR_DOMAIN"></span><span id="mf_mediaengine_keyerr_domain"></span>**MF \_ MEDIAENGINE \_ KEYERR \_ 網域**</span><span class="sxs-lookup"><span data-stu-id="507cb-117"><span id="MF_MEDIAENGINE_KEYERR_DOMAIN"></span><span id="mf_mediaengine_keyerr_domain"></span>**MF\_MEDIAENGINE\_KEYERR\_DOMAIN**</span></span>
</dt> <dd>

<span data-ttu-id="507cb-118">發生網域錯誤。</span><span class="sxs-lookup"><span data-stu-id="507cb-118">An error with the domain occurred.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="507cb-119">備註</span><span class="sxs-lookup"><span data-stu-id="507cb-119">Remarks</span></span>

<span data-ttu-id="507cb-120">**MF \_MEDIA \_ ENGINE \_ KEYERR** 是搭配 [**IMFMediaKeySessionNotify：： KeyError**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediakeysessionnotify-keyerror)的 *Code* 參數和 [**IMFMediaKeySession：： GetError**](imfmediakeysession-geterror.md)傳回的程式 *代碼* 值使用。</span><span class="sxs-lookup"><span data-stu-id="507cb-120">**MF\_MEDIA\_ENGINE\_KEYERR** is used with the *code* parameter of [**IMFMediaKeySessionNotify::KeyError**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediakeysessionnotify-keyerror) and the *code* value returned from [**IMFMediaKeySession::GetError**](imfmediakeysession-geterror.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="507cb-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="507cb-121">Requirements</span></span>



| <span data-ttu-id="507cb-122">需求</span><span class="sxs-lookup"><span data-stu-id="507cb-122">Requirement</span></span> | <span data-ttu-id="507cb-123">值</span><span class="sxs-lookup"><span data-stu-id="507cb-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="507cb-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="507cb-124">Minimum supported client</span></span><br/> | <span data-ttu-id="507cb-125">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="507cb-125">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="507cb-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="507cb-126">Minimum supported server</span></span><br/> | <span data-ttu-id="507cb-127">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="507cb-127">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="507cb-128">Idl</span><span class="sxs-lookup"><span data-stu-id="507cb-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="507cb-129"><dt>Mfmediaengine .idl</dt></span><span class="sxs-lookup"><span data-stu-id="507cb-129"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="507cb-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="507cb-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="507cb-131">媒體基礎列舉</span><span class="sxs-lookup"><span data-stu-id="507cb-131">Media Foundation Enumerations</span></span>](media-foundation-enumerations.md)
</dt> </dl>

 

 




