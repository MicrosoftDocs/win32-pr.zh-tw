---
description: 網路來源驗證
ms.assetid: bffc33ec-0fb0-4bbe-9bac-583b9d4e1153
title: 網路來源驗證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3e90ae7d7a8e4fb29b56aaa1296ba0c5aa44049f801b01a2c7797009ec736aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973037"
---
# <a name="network-source-authentication"></a>網路來源驗證

某些媒體主機在允許存取媒體之前，可能需要來自用戶端應用程式的使用者認證。 使用者認證包括識別和辨識證明，例如使用者名稱和密碼，媒體伺服器會使用這些認證來授與存取權給其所裝載的網路來源。 網路來源可以提供 NTLM、摘要式或基本驗證。

以媒體基礎為基礎的應用程式可以將特定 URL 的使用者認證儲存在公開 [**IMFNetCredential**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential)介面的 *credential* 物件中。 認證物件會儲存加密的認證，並提供方法來傳回信息，例如使用者名稱、密碼和網域。

認證物件會在快取中建立和維護。 [**IMFNetCredentialCache**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialcache)介面所公開的 *認證* 快取物件，提供從認證快取中取得認證物件的方法。

支援驗證的應用程式必須執行 [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) 介面。 媒體基礎不會提供此介面的預設執行。 認證管理員負責收集來自使用者輸入或從持續性儲存區讀取的 URL 所需的認證。

本節包含下列主題：

-   [設定認證管理員](setting-a-credential-manager.md)
-   [使用認證快取](using-the-credential-cache.md)
-   [執行 IMFNetCredentialManager](implementing-imfnetcredentialmanager.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體基礎中的網路功能](networking-in-media-foundation.md)
</dt> </dl>

 

 



