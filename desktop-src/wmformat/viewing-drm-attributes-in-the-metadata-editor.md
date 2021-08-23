---
title: 在中繼資料編輯器中查看 DRM 屬性
description: 在中繼資料編輯器中查看 DRM 屬性
ms.assetid: e25fb8c8-8f4d-40fd-aa6f-675921e0ccdd
keywords:
- Windows媒體格式 SDK，DRM 屬性查看
- 數位版權管理 (DRM) ，屬性查看
- DRM (數位版權管理) ，屬性查看
- Windows媒體格式 SDK，中繼資料編輯器
- 數位版權管理 (DRM) ，中繼資料編輯器
- DRM (數位版權管理) ，中繼資料編輯器
- Windows媒體格式 SDK，IWMDRMEditor 介面
- 數位版權管理 (DRM) ，IWMDRMEditor 介面
- DRM (數位版權管理) 、IWMDRMEditor 介面
- 中繼資料編輯器，DRM 屬性查看
- 中繼資料編輯器，IWMDRMEditor 介面
- IWMDRMEditor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 129f20457f2e359584e6c37eee499b902988f95c0993cf5cd31a85b81d60d162
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119584818"
---
# <a name="viewing-drm-attributes-in-the-metadata-editor"></a>在中繼資料編輯器中查看 DRM 屬性

中繼資料編輯器會公開 IWMDRMEditor 介面，此介面可讓編輯應用程式檢查受保護 ASF 檔案中 DRM 標頭的某些屬性，以及內容授權中的屬性（如果有的話），即使應用程式沒有 DRM 特定的靜態程式庫，也就是完全啟用 DRM 播放程式和寫入器應用程式所需的 (wmstubdrm .lib) 。

> [!Note]  
> 此 SDK 的 x64 版本不支援 DRM。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**數位 Rights Management 功能**](digital-rights-management-features.md)
</dt> <dt>

[**IWMDRMEditor 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor)
</dt> </dl>

 

 




