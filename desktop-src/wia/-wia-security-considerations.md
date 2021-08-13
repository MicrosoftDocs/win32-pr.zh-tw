---
description: 本檔提供與 Windows 映像取得相關的安全性考慮 (WIA) 的相關資訊。
ms.assetid: 35455320-7d08-49de-938d-40dc0873917b
title: 安全性考慮： Windows 映像取得
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bb8f78e0f45b5b63d5d8deb8ffdd35bc64ee5566ced65ded30ecc51366c0793
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118439681"
---
# <a name="security-considerations-windows-image-acquisition"></a>安全性考慮： Windows 映像取得

本檔提供與 Windows 映像取得相關的安全性考慮 (WIA) 的相關資訊。 本檔並不提供您需要瞭解的安全性問題，而是將其作為此技術領域的起點和參考。

-   [使用引號括住路徑名稱](#use-quotation-marks-around-path-names)
-   [將已註冊的應用程式放在安全的位置](#place-registered-applications-in-secure-locations)
-   [請勿使用基礎目錄或登錄機碼](#do-not-use-underlying-directories-or-registry-keys)
-   [相關主題](#related-topics)

## <a name="use-quotation-marks-around-path-names"></a>使用引號括住路徑名稱

使用 [**IWiaDevMgr：： RegisterEventCallbackProgram**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackprogram) 註冊應用程式以接收裝置事件時，請務必將應用程式的路徑和檔案名括在引號中。 這可避免路徑被誤解的可能性，以及執行未授權的應用程式。

## <a name="place-registered-applications-in-secure-locations"></a>將已註冊的應用程式放在安全的位置

註冊應用程式以接收裝置事件時，該應用程式可以由任何可存取該裝置的使用者執行。 例如，如果應用程式是針對掃描事件註冊的，則按掃描器上的 [掃描] 按鈕將會導致該應用程式執行。 如果應用程式執行時的許可權高於使用者所擁有的許可權，這會造成潛在的安全性問題。

## <a name="do-not-use-underlying-directories-or-registry-keys"></a>請勿使用基礎目錄或登錄機碼

WIA 會在內部使用數個目錄和登錄機碼來儲存資料或資訊。 請勿直接存取這些目錄或登錄機碼。 相反地，請使用公開的介面方法來指定所取得映射的目錄。

## <a name="related-topics"></a>[相關主題]

-   [Microsoft 安全性](https://www.microsoft.com/security/)
-   [MSDN Library 安全性首頁](https://msdn.microsoft.com/security/default.aspx)
-   [安全性的如何資源](https://www.microsoft.com/technet/solutionaccelerators/howto/sechow.mspx)
-   [TechNet 安全性資源](https://technet.microsoft.com/security/default.aspx)
-   [Windows XP Embedded 開發人員的安全性考慮](/previous-versions/ms838345(v=msdn.10))
-   [安全性最佳作法](../secbp/best-practices-for-the-security-apis.md)

 

 
