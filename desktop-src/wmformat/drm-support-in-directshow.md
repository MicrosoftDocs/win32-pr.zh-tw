---
title: DirectShow 中的 DRM 支援
description: DirectShow 中的 DRM 支援
ms.assetid: f464d4a4-3478-489a-b9ce-8ab1acabc3c8
keywords:
- Windows Media Format SDK，DirectShow 中的 DRM 支援
- Windows Media Format SDK、DirectShow
- 'Windows Media 格式 SDK、數位版權管理 (DRM) '
- 先進的系統格式 (ASF) 、DirectShow 中的 DRM 支援
- ASF (Advanced Systems Format) 、DirectShow 中的 DRM 支援
- Advanced Systems Format (ASF) 、DirectShow
- ASF (Advanced Systems Format) ，DirectShow
- 'Advanced Systems Format (ASF) 、數位版權管理 (DRM) '
- 'ASF (Advanced Systems Format) 、數位版權管理 (DRM) '
- DirectShow，DRM 支援
- 數位版權管理 (DRM) 、DirectShow
- DRM (數位版權管理) 、DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85a211a3d3b438bac246c0bd90759f648818ac2e
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "103932919"
---
# <a name="drm-support-in-directshow"></a>DirectShow 中的 DRM 支援

在 DirectShow 中讀取和寫入受 DRM 保護的檔案的完成方式基本上與您直接使用 Windows Media Format SDK 的方式相同。 首先，您需要 wmstubdrm 靜態程式庫，它是與 Microsoft 分開取得的。 此外，您必須執行 **IKeyProvider** 介面，讓您的應用程式在啟用 DRM 時存取 Windows MEDIA Format SDK 執行時間物件。

套用 DRM 第1版保護時，請使用 [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) 介面，如在 [DIRECTSHOW 中讀取 ASF](reading-asf-files-in-directshow.md)檔案所述。 套用 DRM 版本7保護時，請在 [WM ASF 寫入](wm-asf-writer-filter.md)器篩選器上呼叫 **QueryService** 來取得 [**IWMDRMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter)介面，如本主題稍後的程式碼片段所示。

所有其他 DRM 專屬設定都與 [啟用 DRM 支援](enabling-drm-support.md)中所述的設定完全相同。 使用 **QueryService** 從 [WM ASF 讀取](wm-asf-reader-filter.md)器篩選器取得 [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)介面。

DirectX 9.0 包含一個範例 PlayWndASF，此為啟用 DRM 的 DirectShow 播放機應用程式，示範 DRM 第1版和第7版授權取得。 這個範例也包含 **CKeyProvider** 類別的實作為支援 **IKeyProvider** 介面的。

 

 




