---
title: DRM_ActionAllowed_CollaborativePlay
description: DRM \_ ActionAllowed \_ CollaborativePlay 屬性會指出授權是否允許共同播放內容。
ms.assetid: 111e8fa7-ef5a-483a-b930-8a8e5b4d120a
keywords:
- DRM_ActionAllowed_CollaborativePlay windows Media 格式
topic_type:
- apiref
api_name:
- DRM_ActionAllowed_CollaborativePlay
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0268c9c3d70a8f51db390544bf854e5acd5b9e88
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104374530"
---
# <a name="drm_actionallowed_collaborativeplay"></a><span data-ttu-id="b95e8-104">DRM \_ ActionAllowed \_ CollaborativePlay</span><span class="sxs-lookup"><span data-stu-id="b95e8-104">DRM\_ActionAllowed\_CollaborativePlay</span></span>

<span data-ttu-id="b95e8-105">**DRM \_ ActionAllowed \_ CollaborativePlay** 屬性會指出授權是否允許共同播放內容。</span><span class="sxs-lookup"><span data-stu-id="b95e8-105">The **DRM\_ActionAllowed\_CollaborativePlay** attribute indicates whether the license allows the content to be played collaboratively.</span></span>

## <a name="global-constant"></a><span data-ttu-id="b95e8-106">全域常數</span><span class="sxs-lookup"><span data-stu-id="b95e8-106">Global Constant</span></span>

<span data-ttu-id="b95e8-107">g \_ wszWMDRM \_ ActionAllowed \_ CollaborativePlay</span><span class="sxs-lookup"><span data-stu-id="b95e8-107">g\_wszWMDRM\_ActionAllowed\_CollaborativePlay</span></span>

## <a name="data-type"></a><span data-ttu-id="b95e8-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="b95e8-108">Data Type</span></span>

<span data-ttu-id="b95e8-109">**WMT \_ 類型 \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="b95e8-109">**WMT\_TYPE\_BOOL**</span></span>

## <a name="remarks"></a><span data-ttu-id="b95e8-110">備註</span><span class="sxs-lookup"><span data-stu-id="b95e8-110">Remarks</span></span>

<span data-ttu-id="b95e8-111">共同作業的播放適合用來在使用點對點服務的共同作業會話中播放受保護的內容。</span><span class="sxs-lookup"><span data-stu-id="b95e8-111">The collaborative play right applies to playing protected content as part of a collaborative session using peer-to-peer services.</span></span> <span data-ttu-id="b95e8-112">例如，MSN Messenger 2004 的使用者可以在 MusicMix 會話中播放受保護的內容。</span><span class="sxs-lookup"><span data-stu-id="b95e8-112">For example, users of MSN Messenger 2004 can play protected content in a MusicMix session.</span></span> <span data-ttu-id="b95e8-113">此許可權只能用來一次將受保護的檔案提供給單一會話，且參與會話的所有使用者都必須在線上才能轉譯內容。</span><span class="sxs-lookup"><span data-stu-id="b95e8-113">This right can only be used to contribute a protected file to a single session at one time, and all users participating in the session must be online to render the content.</span></span>

<span data-ttu-id="b95e8-114">這是使用 [**IWMDRMReader：： GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty)取出的唯讀屬性。</span><span class="sxs-lookup"><span data-stu-id="b95e8-114">This is a read-only property that is retrieved using [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span>

## <a name="see-also"></a><span data-ttu-id="b95e8-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b95e8-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b95e8-116">**DRM 屬性**</span><span class="sxs-lookup"><span data-stu-id="b95e8-116">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 




