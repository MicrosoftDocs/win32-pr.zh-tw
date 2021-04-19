---
title: 'WMT_RIGHTS 列舉 (Wmdrmsdk .h) '
description: 定義可在 DRM 授權中指定的許可權。
ms.assetid: 9c034ca0-83e9-4a4c-8e98-96e2a95fd97c
keywords:
- WMT_RIGHTS 列舉 windows 媒體格式
- 列舉 windows 媒體格式
topic_type:
- apiref
api_name:
- WMT_RIGHTS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 644cff9c94876fab11bc9fbe181ac0375d9444fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982057"
---
# <a name="wmt_rights-enumeration"></a><span data-ttu-id="1e0c7-105">WMT \_ 許可權列舉</span><span class="sxs-lookup"><span data-stu-id="1e0c7-105">WMT\_RIGHTS enumeration</span></span>

<span data-ttu-id="1e0c7-106">**WMT \_ 許可權** 列舉類型會定義可在 DRM 授權中指定的許可權。</span><span class="sxs-lookup"><span data-stu-id="1e0c7-106">The **WMT\_RIGHTS** enumeration type defines the rights that may be specified in a DRM license.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e0c7-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1e0c7-107">Syntax</span></span>


```C++
typedef enum WMT_RIGHTS { 
  WMT_RIGHT_PLAYBACK                 = 0x00000001,
  WMT_RIGHT_COPY_TO_NON_SDMI_DEVICE  = 0x00000002,
  WMT_RIGHT_COPY_TO_CD               = 0x00000008,
  WMT_RIGHT_COPY_TO_SDMI_DEVICE      = 0x00000010,
  WMT_RIGHT_ONE_TIME                 = 0x00000020,
  WMT_RIGHT_SAVE_STREAM_PROTECTED    = 0x00000040,
  WMT_RIGHT_COPY                     = 0x00000080,
  WMT_RIGHT_COLLABORATIVE_PLAY       = 0x00000100,
  WMT_RIGHT_SDMI_TRIGGER             = 0x00010000,
  WMT_RIGHT_SDMI_NOMORECOPIES        = 0x00020000
} ;
```



## <a name="constants"></a><span data-ttu-id="1e0c7-108">常數</span><span class="sxs-lookup"><span data-stu-id="1e0c7-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="1e0c7-109"><span id="WMT_RIGHT_PLAYBACK"></span><span id="wmt_right_playback"></span>**WMT \_ 右 \_ 播放**</span><span class="sxs-lookup"><span data-stu-id="1e0c7-109"><span id="WMT_RIGHT_PLAYBACK"></span><span id="wmt_right_playback"></span>**WMT\_RIGHT\_PLAYBACK**</span></span>
</dt> <dd>

<span data-ttu-id="1e0c7-110">指定不受限制地播放內容的許可權。</span><span class="sxs-lookup"><span data-stu-id="1e0c7-110">Specifies the right to play content without restriction.</span></span>

</dd> <dt>

<span data-ttu-id="1e0c7-111"><span id="WMT_RIGHT_COPY_TO_NON_SDMI_DEVICE"></span><span id="wmt_right_copy_to_non_sdmi_device"></span>**將 \_ WMT \_ 右移 \_ 至 \_ 非 \_ SDMI \_ 裝置**</span><span class="sxs-lookup"><span data-stu-id="1e0c7-111"><span id="WMT_RIGHT_COPY_TO_NON_SDMI_DEVICE"></span><span id="wmt_right_copy_to_non_sdmi_device"></span>**WMT\_RIGHT\_COPY\_TO\_NON\_SDMI\_DEVICE**</span></span>
</dt> <dd>

<span data-ttu-id="1e0c7-112">指定將內容複寫到裝置的許可權，不符合 (SDMI) 的安全數位音樂方案。</span><span class="sxs-lookup"><span data-stu-id="1e0c7-112">Specifies the right to copy content to a device not compliant with the Secure Digital Music Initiative (SDMI).</span></span>

</dd> <dt>

<span data-ttu-id="1e0c7-113"><span id="WMT_RIGHT_COPY_TO_CD"></span><span id="wmt_right_copy_to_cd"></span>**WMT \_ RIGHT \_ 複製 \_ 到 \_ CD**</span><span class="sxs-lookup"><span data-stu-id="1e0c7-113"><span id="WMT_RIGHT_COPY_TO_CD"></span><span id="wmt_right_copy_to_cd"></span>**WMT\_RIGHT\_COPY\_TO\_CD**</span></span>
</dt> <dd>

<span data-ttu-id="1e0c7-114">指定將內容複寫到 CD 的許可權。</span><span class="sxs-lookup"><span data-stu-id="1e0c7-114">Specifies the right to copy content to a CD.</span></span>

</dd> <dt>

<span data-ttu-id="1e0c7-115"><span id="WMT_RIGHT_COPY_TO_SDMI_DEVICE"></span><span id="wmt_right_copy_to_sdmi_device"></span>**WMT \_ RIGHT \_ 複製 \_ 到 \_ SDMI \_ 裝置**</span><span class="sxs-lookup"><span data-stu-id="1e0c7-115"><span id="WMT_RIGHT_COPY_TO_SDMI_DEVICE"></span><span id="wmt_right_copy_to_sdmi_device"></span>**WMT\_RIGHT\_COPY\_TO\_SDMI\_DEVICE**</span></span>
</dt> <dd>

<span data-ttu-id="1e0c7-116">指定將內容複寫到符合 SDMI 規範之裝置的許可權。</span><span class="sxs-lookup"><span data-stu-id="1e0c7-116">Specifies the right to copy content to a device compliant with the SDMI.</span></span>

</dd> <dt>

<span data-ttu-id="1e0c7-117"><span id="WMT_RIGHT_ONE_TIME"></span><span id="wmt_right_one_time"></span>**WMT \_ 右移 \_ 一 \_ 次**</span><span class="sxs-lookup"><span data-stu-id="1e0c7-117"><span id="WMT_RIGHT_ONE_TIME"></span><span id="wmt_right_one_time"></span>**WMT\_RIGHT\_ONE\_TIME**</span></span>
</dt> <dd>

<span data-ttu-id="1e0c7-118">指定僅一次播放內容的許可權。</span><span class="sxs-lookup"><span data-stu-id="1e0c7-118">Specifies the right to play content one time only.</span></span>

</dd> <dt>

<span data-ttu-id="1e0c7-119"><span id="WMT_RIGHT_SAVE_STREAM_PROTECTED"></span><span id="wmt_right_save_stream_protected"></span>**WMT \_ 已 \_ 保護正確的儲存 \_ 資料流程 \_**</span><span class="sxs-lookup"><span data-stu-id="1e0c7-119"><span id="WMT_RIGHT_SAVE_STREAM_PROTECTED"></span><span id="wmt_right_save_stream_protected"></span>**WMT\_RIGHT\_SAVE\_STREAM\_PROTECTED**</span></span>
</dt> <dd>

<span data-ttu-id="1e0c7-120">指定從伺服器儲存內容的許可權。</span><span class="sxs-lookup"><span data-stu-id="1e0c7-120">Specifies the right to save content from a server.</span></span>

</dd> <dt>

<span data-ttu-id="1e0c7-121"><span id="WMT_RIGHT_COPY"></span><span id="wmt_right_copy"></span>**WMT \_ RIGHT \_ COPY**</span><span class="sxs-lookup"><span data-stu-id="1e0c7-121"><span id="WMT_RIGHT_COPY"></span><span id="wmt_right_copy"></span>**WMT\_RIGHT\_COPY**</span></span>
</dt> <dd>

<span data-ttu-id="1e0c7-122">指定複製內容的許可權。</span><span class="sxs-lookup"><span data-stu-id="1e0c7-122">Specifies the right to copy content.</span></span> <span data-ttu-id="1e0c7-123">Windows Media DRM 10 會使用 (OPLs) 的輸出保護層級，來控制可將內容複寫到其中的裝置。</span><span class="sxs-lookup"><span data-stu-id="1e0c7-123">Windows Media DRM 10 regulates the devices to which the content can be copied by using output protection levels (OPLs).</span></span>

</dd> <dt>

<span data-ttu-id="1e0c7-124"><span id="WMT_RIGHT_COLLABORATIVE_PLAY"></span><span id="wmt_right_collaborative_play"></span>**WMT \_ RIGHT \_ 協同作業 \_ 播放**</span><span class="sxs-lookup"><span data-stu-id="1e0c7-124"><span id="WMT_RIGHT_COLLABORATIVE_PLAY"></span><span id="wmt_right_collaborative_play"></span>**WMT\_RIGHT\_COLLABORATIVE\_PLAY**</span></span>
</dt> <dd>

<span data-ttu-id="1e0c7-125">指定在線上案例中播放內容的許可權，其中多個參與者可將歌曲從其集合投稿至共用播放清單。</span><span class="sxs-lookup"><span data-stu-id="1e0c7-125">Specifies the right to play content as part of an online scenario where multiple participants can contribute songs from their collection to a shared playlist.</span></span>

</dd> <dt>

<span data-ttu-id="1e0c7-126"><span id="WMT_RIGHT_SDMI_TRIGGER"></span><span id="wmt_right_sdmi_trigger"></span>**WMT \_ RIGHT \_ SDMI \_ 觸發程式**</span><span class="sxs-lookup"><span data-stu-id="1e0c7-126"><span id="WMT_RIGHT_SDMI_TRIGGER"></span><span id="wmt_right_sdmi_trigger"></span>**WMT\_RIGHT\_SDMI\_TRIGGER**</span></span>
</dt> <dd>

<span data-ttu-id="1e0c7-127">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="1e0c7-127">Reserved for future use.</span></span> <span data-ttu-id="1e0c7-128">請勿使用。</span><span class="sxs-lookup"><span data-stu-id="1e0c7-128">Do not use.</span></span>

</dd> <dt>

<span data-ttu-id="1e0c7-129"><span id="WMT_RIGHT_SDMI_NOMORECOPIES"></span><span id="wmt_right_sdmi_nomorecopies"></span>**WMT \_ RIGHT \_ SDMI \_ NOMORECOPIES**</span><span class="sxs-lookup"><span data-stu-id="1e0c7-129"><span id="WMT_RIGHT_SDMI_NOMORECOPIES"></span><span id="wmt_right_sdmi_nomorecopies"></span>**WMT\_RIGHT\_SDMI\_NOMORECOPIES**</span></span>
</dt> <dd>

<span data-ttu-id="1e0c7-130">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="1e0c7-130">Reserved for future use.</span></span> <span data-ttu-id="1e0c7-131">請勿使用。</span><span class="sxs-lookup"><span data-stu-id="1e0c7-131">Do not use.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1e0c7-132">備註</span><span class="sxs-lookup"><span data-stu-id="1e0c7-132">Remarks</span></span>

<span data-ttu-id="1e0c7-133">這些值是位旗標，因此可以藉由結合位 **or** 運算子來設定一或多個值。</span><span class="sxs-lookup"><span data-stu-id="1e0c7-133">These values are bit flags, so one or more can be set by combining them with the bitwise **OR** operator.</span></span>

<span data-ttu-id="1e0c7-134">使用 Windows Media DRM 10 時， **WMT \_ right \_ copy \_ 至 \_ 非 \_ sdmi \_ 裝置**、 **WMT \_ right \_ 複製 \_ 到 \_ SDMI \_ 裝置**，並由 **WMT \_ right \_ copy** 取代 **WMT \_ RIGHT \_ 複製 \_ 至 \_ CD** 。</span><span class="sxs-lookup"><span data-stu-id="1e0c7-134">When using Windows Media DRM 10, **WMT\_RIGHT\_COPY\_TO\_NON\_SDMI\_DEVICE**, **WMT\_RIGHT\_COPY\_TO\_SDMI\_DEVICE**, and **WMT\_RIGHT\_COPY\_TO\_CD** are superseded by **WMT\_RIGHT\_COPY**.</span></span> <span data-ttu-id="1e0c7-135">您可以使用 (OPLs) 的輸出保護層級，來指定可複製內容之裝置的限制。</span><span class="sxs-lookup"><span data-stu-id="1e0c7-135">Limitations on the devices to which the content may be copied are specified by using output protection levels (OPLs).</span></span>

## <a name="requirements"></a><span data-ttu-id="1e0c7-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="1e0c7-136">Requirements</span></span>



| <span data-ttu-id="1e0c7-137">需求</span><span class="sxs-lookup"><span data-stu-id="1e0c7-137">Requirement</span></span> | <span data-ttu-id="1e0c7-138">值</span><span class="sxs-lookup"><span data-stu-id="1e0c7-138">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1e0c7-139">標頭</span><span class="sxs-lookup"><span data-stu-id="1e0c7-139">Header</span></span><br/> | <dl> <span data-ttu-id="1e0c7-140"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="1e0c7-140"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e0c7-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1e0c7-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e0c7-142">**列舉類型**</span><span class="sxs-lookup"><span data-stu-id="1e0c7-142">**Enumeration Types**</span></span>](drm-enumeration-types.md)
</dt> </dl>

 

 





