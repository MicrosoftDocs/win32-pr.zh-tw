---
title: DRM 匯入
description: DRM 匯入
ms.assetid: 5e67a721-830b-4d99-9f90-4cb2d7c61104
keywords:
- Windows媒體格式 SDK，DRM 用戶端擴充 Api
- Windows媒體格式 SDK，用戶端擴充 Api
- Windows媒體格式 SDK，擴充的 Api
- Windows媒體格式 SDK，Api
- 'Windows媒體格式 SDK、數位版權管理 (DRM) '
- Windows媒體格式 SDK，DRM 匯入
- Windows媒體格式 SDK，匯入
- 'Windows媒體格式 SDK，content protection system (CPS) '
- 數位版權管理 (DRM) 、用戶端擴充 Api
- DRM (數位版權管理) 、用戶端擴充 Api
- 數位版權管理 (DRM) 、擴充的 Api
- DRM (數位版權管理) 、擴充的 Api
- 數位版權管理 (DRM) 、Api
- DRM (數位版權管理) ，Api
- 數位版權管理 (DRM) ，匯入
- DRM (數位版權管理) ，匯入
- '數位版權管理 (DRM) 、內容保護系統 (CPS) '
- 'DRM (數位版權管理) 、內容保護系統 (CPS) '
- DRM 用戶端擴充 Api，匯入
- 用戶端擴充 Api，匯入
- 'DRM 用戶端擴充 Api、內容保護系統 (CPS) '
- '用戶端擴充 Api，content protection system (CPS) '
- " (CPS) 的內容保護系統"
- 'CPS (內容保護系統) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 981e601c21dc3ee8f54e256c40453bf24580cf46c261d41ea5dd1d9afa1ffbbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027896"
---
# <a name="drm-import"></a>DRM 匯入

下列各節說明如何將協力廠商內容保護系統 (CPS) 的媒體內容轉換成 Windows 媒體 DRM。 此程式稱為「DRM 匯入」，基本上是由下列步驟所組成：

1.  建立 ASF 檔案。
2.  建立授權。
3.  選擇性地刪除授權。

下列各節將說明 DRM 匯入。



| 區段                                                                              | 描述                                                                          |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [匯入授權和金鑰內容](importing-license-and-key-material.md)         | 描述如何在本機發出授權，並將其匯入 Windows 媒體 DRM。      |
| [檢查憑證撤銷](checking-certificate-revocation.md)               | 說明如何檢查憑證撤銷。                                       |
| [建立 XMR 授權](building-an-xmr-license.md)                               | 說明如何建立 XMR 授權，並將其傳遞至 DRM 子系統。             |
| [建立和初始化 DRM 寫入器](creating-and-initializing-a-drm-writer.md) | 說明如何初始化 ASF 寫入器物件，以準備進行 DRM 匯入。          |
| [加密和匯入媒體範例](encrypting-and-importing-media-samples.md) | 說明如何將個別媒體範例加密並匯入 Windows 媒體 DRM。 |
| [刪除授權](license-deletion.md)                                             | 說明如何刪除本機建立的授權。                                    |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**程式設計指南**](drm-programming-guide.md)
</dt> </dl>

 

 




