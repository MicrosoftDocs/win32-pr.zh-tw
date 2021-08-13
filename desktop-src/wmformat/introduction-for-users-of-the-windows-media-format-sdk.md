---
title: Windows 媒體格式 SDK 的使用者簡介
description: Windows 媒體格式 SDK 的使用者簡介
ms.assetid: 21f06c43-213e-4fbf-a33a-c1890b4b40ce
keywords:
- Windows媒體格式 SDK，DRM 用戶端擴充 Api
- Windows媒體格式 SDK，用戶端擴充 Api
- Windows媒體格式 SDK，擴充的 Api
- Windows媒體格式 SDK，Api
- 'Windows媒體格式 SDK、數位版權管理 (DRM) '
- 數位版權管理 (DRM) 、用戶端擴充 Api
- DRM (數位版權管理) 、用戶端擴充 Api
- 數位版權管理 (DRM) 、擴充的 Api
- DRM (數位版權管理) 、擴充的 Api
- 數位版權管理 (DRM) 、Api
- DRM (數位版權管理) ，Api
- DRM 用戶端擴充 Api，關於
- 用戶端擴充 Api，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eb1994e5e4960613e992f198833f2fb2e3ff2a21181e98bae5d6823fbb31a8c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119392558"
---
# <a name="introduction-for-users-of-the-windows-media-format-sdk"></a>Windows 媒體格式 SDK 的使用者簡介

Windows 媒體 DRM 用戶端擴充 api 所提供的許多功能，與 Windows 媒體格式 SDK 的物件所提供的功能相同。 Windows 媒體格式 SDK 為開發人員提供了建立、存取和操作使用 Advanced Systems 格式 (ASF) 檔案結構所需的物件。 因為 Windows 媒體 drm 是為了保護 ASF 檔案，所以 Windows 媒體格式 SDK 中已包含用戶端 drm 功能。

Windows 媒體 DRM 用戶端擴充 api 會與 Microsoft 的新一代數位媒體平臺（Microsoft 媒體基礎 SDK）一起發行。 媒體基礎將包含與 Windows 媒體格式 SDK 的部分功能重迭的 ASF 功能。 因為現在有兩個可操作 ASF 檔案的 Microsoft sdk，所以用戶端 DRM 功能會與 Windows 媒體格式 SDK 分開，以 Windows 媒體 DRM 用戶端擴充 api。 這些 api 可由 Windows 媒體格式 sdk 和媒體基礎 SDK 的使用者存取。 目前，這些 api 包含在 Windows 媒體格式 sdk 安裝套件中，並記載為 Windows 媒體格式 sdk 的一部分。 不過，Windows 媒體 DRM 用戶端擴充 api 會在自己的程式庫中執行，並擁有自己的標頭檔。 安裝 Windows 媒體格式 sdk 之後，您可以使用這些 api，而不需在應用程式中包含任何 Windows 媒體格式 SDK 標頭或程式庫。

如果您開發使用 Windows 媒體格式 SDK 的應用程式，您必須決定是要使用 SDK 提供的 DRM 功能，還是使用 Windows 媒體 DRM 用戶端擴充 api。 雖然這兩個 sdk 的許多功能都非常類似，但 Windows 媒體 DRM 用戶端擴充 api 提供下列功能，而這些功能不適用於舊版 DRM 常式的使用者：

-   能夠匯入協力廠商 rights management 系統所保護的內容。
-   將受 Windows 媒體 DRM 保護的內容匯出至協力廠商版權管理系統的能力。
-   在授權存放中直接列舉授權。
-   以金鑰識別碼為基礎的簡單、匯總的許可權查詢 (不需要載入媒體檔案) 。
-   使用標準媒體基礎介面（ **IMFContentEnabler**）更新撤銷的元件的能力。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**關於 Windows 媒體 DRM 用戶端擴充 api**](about-the-windows-media-drm-client-extended-apis.md)
</dt> </dl>

 

 




