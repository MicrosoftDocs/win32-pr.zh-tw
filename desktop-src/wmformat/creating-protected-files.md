---
title: 建立受保護的檔案
description: 建立受保護的檔案
ms.assetid: 5237e797-72ec-402e-81ec-ab379747e464
keywords:
- Windows媒體格式 SDK，建立受保護的檔案
- Windows媒體格式 SDK，受保護的檔案
- Advanced Systems Format (ASF) ，建立受保護的檔案
- ASF (Advanced Systems Format) ，建立受保護的檔案
- Advanced Systems Format (ASF) 、受保護的檔案
- ASF (Advanced 系統格式) 、受保護的檔案
- Advanced Systems Format (ASF) ，WMStubDRM .lib
- ASF (Advanced Systems Format) ，WMStubDRM .lib
- WMStubDRM .lib，建立受保護的檔案
- WMStubDRM .lib，受保護的檔案
- 數位版權管理 (DRM) ，WMStubDRM .lib
- DRM (數位版權管理) ，WMStubDRM .lib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5be729f04f67e1a2e4319bcc8d267c798942293c2df2ee97dcc6a559af612aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809468"
---
# <a name="creating-protected-files"></a>建立受保護的檔案

若要使用 DRM 第1版或 DRM 版本7和更新版本來建立受保護的數位媒體檔案，請連結至您從 Microsoft 取得的 WMStubDRM .lib 檔案，然後建立寫入器物件。 針對第1版保護，請使用 [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) 介面設定您想要套用的 DRM 屬性。 若為7版和更新版本，請使用 [**IWMDRMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter) 介面方法。

下列主題將詳細說明如何保護檔案。

-   [使用 DRM 第1版保護檔案](protecting-files-with-drm-version-1.md)
-   [使用 DRM 7 版或更新版本保護檔案](protecting-files-with-drm-version-7-or-later.md)

> [!Note]  
> 此 SDK 的 x64 版本不支援 DRM。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**DRM 屬性清單**](drm-attribute-list.md)
</dt> <dt>

[**DRM 屬性**](drm-properties.md)
</dt> <dt>

[**DRM 版本**](drm-versions.md)
</dt> <dt>

[**啟用 DRM 支援**](enabling-drm-support.md)
</dt> <dt>

[**取得必要的 DRM 程式庫**](obtaining-the-required-drm-library.md)
</dt> <dt>

[**讀取受保護的檔案**](reading-protected-files.md)
</dt> </dl>

 

 




