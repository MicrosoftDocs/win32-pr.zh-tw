---
title: Microsoft Windows Media DRM 用戶端功能
description: Microsoft Windows Media DRM 用戶端功能
ms.assetid: 5d726c56-d0f3-4eb8-829f-3a0c1a0e0802
keywords:
- Windows Media Format SDK，函數
- 數位版權管理 (DRM) ，函數
- DRM (數位版權管理) ，函數
- DRM 用戶端擴充 Api，函數
- 用戶端擴充 Api，函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20c1730413a4918b0f748099fbd55714339a7e9b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "106966900"
---
# <a name="microsoft-windows-media-drm-client-functions"></a>Microsoft Windows Media DRM 用戶端功能

下列函式會實作為 Microsoft Windows Media DRM 用戶端擴充 Api 的一部分。



| 函式                                                             | 描述                                                                                                                                                                                     |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WMDRMCreateProvider**](wmdrmcreateprovider.md)                   | 建立可建立其他 DRM 物件的 class factory。 此函式不需要來自 Microsoft 的存根程式庫，並會建立不支援受保護 DRM 功能的物件。 |
| [**WMDRMCreateProtectedProvider**](wmdrmcreateprotectedprovider.md) | 建立可建立其他 DRM 物件的 class factory。 此函式需要來自 Microsoft 的存根程式庫，並建立支援受保護 DRM 功能的物件。                |
| [**WMDRMShutdown**](wmdrmshutdown.md)                               | 釋放 Api 所使用的資源。                                                                                                                                                            |
| [**WMDRMStartup**](wmdrmstartup.md)                                 | 初始化 Api 所使用的資源。                                                                                                                                                         |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**程式設計參考**](drm-programming-reference.md)
</dt> </dl>

 

 




