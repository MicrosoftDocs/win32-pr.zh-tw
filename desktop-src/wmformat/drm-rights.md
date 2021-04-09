---
title: DRM_Rights
description: '[DRM \_ 許可權] 屬性會指定應用程式在下一次嘗試開啟受保護的檔案時所需的許可權。'
ms.assetid: fbf62e8d-069e-427b-9093-6c579cdaa96a
keywords:
- DRM_Rights windows Media 格式
topic_type:
- apiref
api_name:
- DRM_Rights
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 542e511c11111bb2698d9c936a1f0973a2145c9b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104023022"
---
# <a name="drm_rights"></a><span data-ttu-id="fe9fd-104">DRM \_ 許可權</span><span class="sxs-lookup"><span data-stu-id="fe9fd-104">DRM\_Rights</span></span>

<span data-ttu-id="fe9fd-105">[ **DRM \_ 許可權** ] 屬性會指定應用程式在下一次嘗試開啟受保護的檔案時所需的許可權。</span><span class="sxs-lookup"><span data-stu-id="fe9fd-105">The **DRM\_Rights** property specifies the rights that the application will require in the next attempt to open a protected file.</span></span>

## <a name="global-constant"></a><span data-ttu-id="fe9fd-106">全域常數</span><span class="sxs-lookup"><span data-stu-id="fe9fd-106">Global Constant</span></span>

<span data-ttu-id="fe9fd-107">g \_ wszWMDRM \_ 許可權</span><span class="sxs-lookup"><span data-stu-id="fe9fd-107">g\_wszWMDRM\_Rights</span></span>

## <a name="data-type"></a><span data-ttu-id="fe9fd-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="fe9fd-108">Data Type</span></span>

<span data-ttu-id="fe9fd-109">**WMT \_ 類型 \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="fe9fd-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="fe9fd-110">備註</span><span class="sxs-lookup"><span data-stu-id="fe9fd-110">Remarks</span></span>

<span data-ttu-id="fe9fd-111">這是讀寫屬性，會使用 [**IWMDRMReader：： GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty) 抓取，並使用 [**IWMDRMReader：： SetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-setdrmproperty) 或 [**IWMDRMWriter：： SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute)來設定。</span><span class="sxs-lookup"><span data-stu-id="fe9fd-111">This is a read-write property that is retrieved using [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty) and set using either [**IWMDRMReader::SetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-setdrmproperty) or [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute).</span></span>

<span data-ttu-id="fe9fd-112">下表列出支援的許可權。</span><span class="sxs-lookup"><span data-stu-id="fe9fd-112">The following table lists the supported rights.</span></span>



| <span data-ttu-id="fe9fd-113">Right</span><span class="sxs-lookup"><span data-stu-id="fe9fd-113">Right</span></span>                                           | <span data-ttu-id="fe9fd-114">字串常值</span><span class="sxs-lookup"><span data-stu-id="fe9fd-114">String literal</span></span>      | <span data-ttu-id="fe9fd-115">Description</span><span class="sxs-lookup"><span data-stu-id="fe9fd-115">Description</span></span>                                                                                                                                                                                                          |
|-------------------------------------------------|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe9fd-116">g \_ wszWMDRM \_ 右 \_ 備份</span><span class="sxs-lookup"><span data-stu-id="fe9fd-116">g\_wszWMDRM\_RIGHT\_BACKUP</span></span>                      | <span data-ttu-id="fe9fd-117">備份</span><span class="sxs-lookup"><span data-stu-id="fe9fd-117">"Backup"</span></span>            | <span data-ttu-id="fe9fd-118">備份授權的許可權。</span><span class="sxs-lookup"><span data-stu-id="fe9fd-118">Right to back up the license.</span></span>                                                                                                                                                                                        |
| <span data-ttu-id="fe9fd-119">g \_ wszWMDRM \_ RIGHT \_ 協同作業 \_ 播放</span><span class="sxs-lookup"><span data-stu-id="fe9fd-119">g\_wszWMDRM\_RIGHT\_COLLABORATIVE\_PLAY</span></span>         | <span data-ttu-id="fe9fd-120">"CollaborativePlay"</span><span class="sxs-lookup"><span data-stu-id="fe9fd-120">"CollaborativePlay"</span></span> | <span data-ttu-id="fe9fd-121">在共同作業播放清單中播放檔案的許可權。</span><span class="sxs-lookup"><span data-stu-id="fe9fd-121">Right to play the file as part of a collaborative playlist.</span></span>                                                                                                                                                          |
| <span data-ttu-id="fe9fd-122">g \_ wszWMDRM \_ RIGHT \_ COPY</span><span class="sxs-lookup"><span data-stu-id="fe9fd-122">g\_wszWMDRM\_RIGHT\_COPY</span></span>                        | <span data-ttu-id="fe9fd-123">"Copy"</span><span class="sxs-lookup"><span data-stu-id="fe9fd-123">"Copy"</span></span>              | <span data-ttu-id="fe9fd-124">將檔案複製到裝置的許可權。</span><span class="sxs-lookup"><span data-stu-id="fe9fd-124">Right to copy the file to a device.</span></span> <span data-ttu-id="fe9fd-125">此許可權會取代較舊的複製許可權 (g \_ wszWMDRM \_ right \_ copy \_ 至 \_ CD、g \_ wszWMDRM \_ right \_ copy \_ 至 \_ 非 \_ SDMI \_ 裝置，以及 g \_ wszWMDRM \_ right \_ 複製 \_ 到 \_ SDMI \_ 裝置) 。</span><span class="sxs-lookup"><span data-stu-id="fe9fd-125">This right supersedes the older copy rights (g\_wszWMDRM\_RIGHT\_COPY\_TO\_CD, g\_wszWMDRM\_RIGHT\_COPY\_TO\_NON\_SDMI\_DEVICE, and g\_wszWMDRM\_RIGHT\_COPY\_TO\_SDMI\_DEVICE).</span></span> |
| <span data-ttu-id="fe9fd-126">g \_ wszWMDRM \_ RIGHT \_ 複製 \_ 到 \_ CD</span><span class="sxs-lookup"><span data-stu-id="fe9fd-126">g\_wszWMDRM\_RIGHT\_COPY\_TO\_CD</span></span>                | <span data-ttu-id="fe9fd-127">"Print. redbook"</span><span class="sxs-lookup"><span data-stu-id="fe9fd-127">"Print.redbook"</span></span>     | <span data-ttu-id="fe9fd-128">將檔案複製到 CD (的紅色書籍格式) 的許可權。在 Windows Media DRM 10 中，此許可權由 g \_ wszWMDRM \_ right COPY 取代 \_ 。</span><span class="sxs-lookup"><span data-stu-id="fe9fd-128">Right to copy the file to a CD (Red Book format).In Windows Media DRM 10, this right is replaced by g\_wszWMDRM\_RIGHT\_COPY.</span></span><br/>                                                                             |
| <span data-ttu-id="fe9fd-129">g \_ wszWMDRM \_ RIGHT \_ COPY \_ 至 \_ 非 \_ SDMI \_ 裝置</span><span class="sxs-lookup"><span data-stu-id="fe9fd-129">g\_wszWMDRM\_RIGHT\_COPY\_TO\_NON\_SDMI\_DEVICE</span></span> | <span data-ttu-id="fe9fd-130">"Transfer. NONSDMI"</span><span class="sxs-lookup"><span data-stu-id="fe9fd-130">"Transfer.NONSDMI"</span></span>  | <span data-ttu-id="fe9fd-131">將檔案複製到非 SDMI 裝置的許可權。在 Windows Media DRM 10 中，此許可權由 g \_ wszWMDRM \_ right COPY 取代 \_ 。</span><span class="sxs-lookup"><span data-stu-id="fe9fd-131">Right to copy the file to a non-SDMI device.In Windows Media DRM 10, this right is replaced by g\_wszWMDRM\_RIGHT\_COPY.</span></span><br/>                                                                                  |
| <span data-ttu-id="fe9fd-132">g \_ wszWMDRM \_ RIGHT \_ 複製 \_ 到 \_ SDMI \_ 裝置</span><span class="sxs-lookup"><span data-stu-id="fe9fd-132">g\_wszWMDRM\_RIGHT\_COPY\_TO\_SDMI\_DEVICE</span></span>      | <span data-ttu-id="fe9fd-133">"Transfer. SDMI"</span><span class="sxs-lookup"><span data-stu-id="fe9fd-133">"Transfer.SDMI"</span></span>     | <span data-ttu-id="fe9fd-134">將檔案複製到符合 SDMI 規範之裝置的許可權。在 Windows Media DRM 10 中，此許可權由 g \_ wszWMDRM \_ right COPY 取代 \_ 。</span><span class="sxs-lookup"><span data-stu-id="fe9fd-134">Right to copy the file to an SDMI-compliant device.In Windows Media DRM 10, this right is replaced by g\_wszWMDRM\_RIGHT\_COPY.</span></span><br/>                                                                           |
| <span data-ttu-id="fe9fd-135">g \_ wszWMDRM \_ 右 \_ 播放</span><span class="sxs-lookup"><span data-stu-id="fe9fd-135">g\_wszWMDRM\_RIGHT\_PLAYBACK</span></span>                    | <span data-ttu-id="fe9fd-136">發出</span><span class="sxs-lookup"><span data-stu-id="fe9fd-136">"Play"</span></span>              | <span data-ttu-id="fe9fd-137">播放媒體檔案的許可權。</span><span class="sxs-lookup"><span data-stu-id="fe9fd-137">Right to play the media file.</span></span>                                                                                                                                                                                        |



 

<span data-ttu-id="fe9fd-138">此屬性包含一或多個以分號分隔之許可權的寬字元字串，例如： L "播放;份CollaborativePlay".</span><span class="sxs-lookup"><span data-stu-id="fe9fd-138">This property contains a wide-character string of one or more rights separated by semicolons, for example: L"Playback;Copy;CollaborativePlay".</span></span>

## <a name="see-also"></a><span data-ttu-id="fe9fd-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fe9fd-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe9fd-140">**DRM 屬性**</span><span class="sxs-lookup"><span data-stu-id="fe9fd-140">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 





