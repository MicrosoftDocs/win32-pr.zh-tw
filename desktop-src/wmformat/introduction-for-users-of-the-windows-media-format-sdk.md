---
title: Windows Media Format SDK 使用者簡介
description: Windows Media Format SDK 使用者簡介
ms.assetid: 21f06c43-213e-4fbf-a33a-c1890b4b40ce
keywords:
- Windows Media Format SDK，DRM 用戶端擴充 Api
- Windows Media Format SDK，用戶端擴充 Api
- Windows Media Format SDK，擴充的 Api
- Windows Media Format SDK，Api
- 'Windows Media 格式 SDK、數位版權管理 (DRM) '
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
ms.openlocfilehash: 538978305e4df952ed97e063b3512ce9fd5cfc34
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372235"
---
# <a name="introduction-for-users-of-the-windows-media-format-sdk"></a>Windows Media Format SDK 使用者簡介

Windows Media DRM 用戶端擴充 Api 所提供的許多功能，與 Windows Media 格式 SDK 的物件所提供的功能相同。 Windows Media Format SDK 為開發人員提供建立、存取和操作使用 Advanced Systems 格式的媒體檔案所需的物件 (ASF) 檔案結構。 因為 Windows Media DRM 是為了保護 ASF 檔案，所以用戶端 DRM 功能已包含在 Windows Media Format SDK 中。

Windows Media DRM 用戶端擴充 Api 與 Microsoft 的新一代數位媒體平臺（Microsoft 媒體基礎 SDK）一起發行。 媒體基礎將包含與 Windows Media Format SDK 的部分功能重迭的 ASF 功能。 因為現在有兩個可操作 ASF 檔案的 Microsoft Sdk，所以用戶端 DRM 功能會與 Windows media DRM 用戶端擴充 Api 分開。 這些 Api 可由 Windows Media 格式 SDK 和媒體基礎 SDK 的使用者存取。 目前，這些 Api 包含在 Windows Media Format SDK 安裝套件中，並記載為 Windows Media Format SDK 的一部分。 不過，Windows Media DRM 用戶端擴充 Api 會在自己的程式庫中執行，並擁有自己的標頭檔。 在安裝 Windows Media Format SDK 之後，您可以使用它們自己的 Api，而不需在應用程式中包含任何 Windows Media Format SDK 標頭或程式庫。

如果您開發使用 Windows Media 格式 SDK 的應用程式，您必須決定是否要使用 SDK 提供的 DRM 功能，或使用 Windows Media DRM 用戶端擴充 Api。 雖然這兩個 Sdk 的許多功能非常類似，但 Windows Media DRM 用戶端擴充 Api 提供下列功能，而這些功能不適用於舊版 DRM 常式的使用者：

-   能夠匯入協力廠商 rights management 系統所保護的內容。
-   將受 Windows Media DRM 保護的內容匯出至協力廠商版權管理系統的能力。
-   在授權存放中直接列舉授權。
-   以金鑰識別碼為基礎的簡單、匯總的許可權查詢 (不需要載入媒體檔案) 。
-   使用標準媒體基礎介面（ **IMFContentEnabler**）更新撤銷的元件的能力。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**關於 Windows Media DRM 用戶端擴充 Api**](about-the-windows-media-drm-client-extended-apis.md)
</dt> </dl>

 

 




