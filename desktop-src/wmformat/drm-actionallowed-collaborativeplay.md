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
# <a name="drm_actionallowed_collaborativeplay"></a>DRM \_ ActionAllowed \_ CollaborativePlay

**DRM \_ ActionAllowed \_ CollaborativePlay** 屬性會指出授權是否允許共同播放內容。

## <a name="global-constant"></a>全域常數

g \_ wszWMDRM \_ ActionAllowed \_ CollaborativePlay

## <a name="data-type"></a>資料類型

**WMT \_ 類型 \_ BOOL**

## <a name="remarks"></a>備註

共同作業的播放適合用來在使用點對點服務的共同作業會話中播放受保護的內容。 例如，MSN Messenger 2004 的使用者可以在 MusicMix 會話中播放受保護的內容。 此許可權只能用來一次將受保護的檔案提供給單一會話，且參與會話的所有使用者都必須在線上才能轉譯內容。

這是使用 [**IWMDRMReader：： GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty)取出的唯讀屬性。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DRM 屬性**](drm-properties.md)
</dt> </dl>

 

 




