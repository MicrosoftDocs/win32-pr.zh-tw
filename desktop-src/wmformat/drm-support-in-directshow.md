---
title: DirectShow 中的 DRM 支援
description: DirectShow 中的 DRM 支援
ms.assetid: f464d4a4-3478-489a-b9ce-8ab1acabc3c8
keywords:
- Windows媒體格式 SDK，DirectShow 中的 DRM 支援
- Windows媒體格式 SDK，DirectShow
- 'Windows媒體格式 SDK、數位版權管理 (DRM) '
- Advanced Systems Format (ASF) 、DirectShow 中的 DRM 支援
- ASF (Advanced Systems Format) ，DirectShow 中的 DRM 支援
- Advanced Systems Format (ASF) ，DirectShow
- ASF (Advanced Systems Format) ，DirectShow
- 'Advanced Systems Format (ASF) 、數位版權管理 (DRM) '
- 'ASF (Advanced Systems Format) 、數位版權管理 (DRM) '
- DirectShow，DRM 支援
- 數位版權管理 (DRM) ，DirectShow
- DRM (數位版權管理) ，DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4b3de3ca80d1b3b2fe27c9af590fe0cba0202b1fdd9b6fc322d8ed1c1871536
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930878"
---
# <a name="drm-support-in-directshow"></a>DirectShow 中的 DRM 支援

在 DirectShow 中讀取和寫入受 DRM 保護的檔案的完成方式基本上與直接使用 Windows 媒體格式 SDK 時相同。 首先，您需要 wmstubdrm 靜態程式庫，它是與 Microsoft 分開取得的。 此外，您必須執行 **IKeyProvider** 介面，讓您的應用程式在啟用 DRM 時存取 Windows 媒體格式 SDK 執行時間物件。

套用 DRM 第1版保護時，請使用 [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)介面，如 [DIRECTSHOW 中讀取 ASF 檔中](reading-asf-files-in-directshow.md)所述。 套用 DRM 版本7保護時，請在 [WM ASF 寫入](wm-asf-writer-filter.md)器篩選器上呼叫 **QueryService** 來取得 [**IWMDRMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter)介面，如本主題稍後的程式碼片段所示。

所有其他 DRM 專屬設定都與 [啟用 DRM 支援](enabling-drm-support.md)中所述的設定完全相同。 使用 **QueryService** 從 [WM ASF 讀取](wm-asf-reader-filter.md)器篩選器取得 [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)介面。

DirectX 9.0 包含 PlayWndASF 的已啟用 drm DirectShow 播放機應用程式範例，其中示範了 drm 第1版和第7版授權取得。 這個範例也包含 **CKeyProvider** 類別的實作為支援 **IKeyProvider** 介面的。

 

 




