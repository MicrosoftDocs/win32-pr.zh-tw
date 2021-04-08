---
title: 查看受保護檔案的屬性
description: 查看受保護檔案的屬性
ms.assetid: fbfa1a1b-afd0-4f61-86ae-488716e16355
keywords:
- Windows Media Format SDK，查看受保護檔案的屬性
- Windows Media Format SDK，受保護檔案的屬性
- Windows Media Format SDK，受保護的檔案
- Advanced Systems Format (ASF) ，查看受保護檔案的屬性
- ASF (Advanced Systems Format) ，查看受保護檔案的屬性
- Advanced Systems Format (ASF) 、受保護檔案的屬性
- ASF (Advanced Systems Format) ，受保護檔案的屬性
- Advanced Systems Format (ASF) 、受保護的檔案
- ASF (Advanced 系統格式) 、受保護的檔案
- 數位版權管理 (DRM) ，查看受保護檔案的屬性
- DRM (數位版權管理) ，查看受保護檔案的屬性
- 數位版權管理 (DRM) ，受保護檔案的屬性
- DRM (數位版權管理) ，受保護檔案的屬性
- 數位版權管理 (DRM) 、受保護的檔案
- DRM (數位版權管理) 、受保護的檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 642e9f580c3dffa1d3785985d548a5f971cfc218
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "103681383"
---
# <a name="viewing-attributes-of-protected-files"></a>查看受保護檔案的屬性

在某些情況下，您可能需要在檔案中取出某些 DRM 屬性，而不需要實際存取檔案的內容。 這項功能很有用，例如，應用程式會根據檔案標頭中的資訊，以不同的方式處理批次的檔案。 在舊版的 Windows Media Format SDK 中，應用程式必須連結到 DRM 靜態程式庫，才能開啟任何受保護的檔案。 沒有 DRM 程式庫的應用程式可以使用中繼資料編輯器物件上的 [**IWMDRMEditor：： GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmeditor-getdrmproperty) 介面來檢查特定的 DRM 屬性。

> [!Note]  
> 此 SDK 的 x64 版本不支援 DRM。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**DRM 屬性清單**](drm-attribute-list.md)
</dt> <dt>

[**啟用 DRM 支援**](enabling-drm-support.md)
</dt> <dt>

[**IWMDRMEditor 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor)
</dt> </dl>

 

 




