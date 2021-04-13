---
title: 在中繼資料編輯器中查看 DRM 屬性
description: 在中繼資料編輯器中查看 DRM 屬性
ms.assetid: e25fb8c8-8f4d-40fd-aa6f-675921e0ccdd
keywords:
- Windows Media Format SDK，DRM 屬性查看
- 數位版權管理 (DRM) ，屬性查看
- DRM (數位版權管理) ，屬性查看
- Windows Media Format SDK，中繼資料編輯器
- 數位版權管理 (DRM) ，中繼資料編輯器
- DRM (數位版權管理) ，中繼資料編輯器
- Windows Media Format SDK，IWMDRMEditor 介面
- 數位版權管理 (DRM) ，IWMDRMEditor 介面
- DRM (數位版權管理) 、IWMDRMEditor 介面
- 中繼資料編輯器，DRM 屬性查看
- 中繼資料編輯器，IWMDRMEditor 介面
- IWMDRMEditor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a8541444ad7704ecc340476929f1205f11ccd61
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104314316"
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

 

 




