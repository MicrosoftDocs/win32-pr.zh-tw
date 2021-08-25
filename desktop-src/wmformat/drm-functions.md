---
title: Microsoft Windows 媒體 DRM 用戶端函式
description: Microsoft Windows 媒體 DRM 用戶端函式
ms.assetid: 5d726c56-d0f3-4eb8-829f-3a0c1a0e0802
keywords:
- Windows媒體格式 SDK，函式
- 數位版權管理 (DRM) ，函數
- DRM (數位版權管理) ，函數
- DRM 用戶端擴充 Api，函數
- 用戶端擴充 Api，函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73aaf5f3c536027801a85f8d38120e6e14c5d366a6d727498a5bc1d1200cb041
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119931168"
---
# <a name="microsoft-windows-media-drm-client-functions"></a>Microsoft Windows 媒體 DRM 用戶端函式

下列函式會實作為 Microsoft Windows 媒體 DRM 用戶端擴充 api 的一部分。



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

 

 




