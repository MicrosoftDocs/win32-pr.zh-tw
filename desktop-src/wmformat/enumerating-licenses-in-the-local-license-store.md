---
title: 列舉本機授權存放區中的授權
description: 列舉本機授權存放區中的授權
ms.assetid: 1f380b9e-85e4-4190-a809-65dfd4658b7c
keywords:
- Windows媒體格式 SDK，列舉授權
- Windows媒體格式 SDK，授權
- Windows媒體格式 SDK，本機授權存放
- 數位版權管理 (DRM) ，列舉授權
- DRM (數位版權管理) ，列舉授權
- 數位版權管理 (DRM) 、授權
- DRM (數位版權管理) 、授權
- 數位版權管理 (DRM) 的本機授權商店
- DRM (數位版權管理) ，本機授權商店
- DRM 用戶端擴充 Api，列舉授權
- 用戶端擴充 Api，列舉授權
- DRM 用戶端擴充 Api，授權
- 用戶端擴充 Api，授權
- DRM 用戶端擴充 Api，本機授權存放
- 用戶端擴充 Api，本機授權存放
- 授權，列舉
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d27913a5a35ce9af1f5a4d6fa3cbae808bc2abe89afd5edb05aa927fe4c39227
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117848194"
---
# <a name="enumerating-licenses-in-the-local-license-store"></a>列舉本機授權存放區中的授權

「列舉」（Enumeration）是一種程式，可透過逐一逐步執行授權，取得本機授權存放區中授權的相關資訊。 您可以藉由呼叫 [**IWMDRMLicenseManagement：： CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md)來建立授權列舉。

在存放區中列舉授權的最常見原因，是尋找特定授權以解密某些內容。

[**IWMDRMLicense**](iwmdrmlicense.md)介面可作為個別授權結果和列舉值的入口網站。 建立授權列舉時，會將清單中的第一個授權載入 **IWMDRMLicense** 介面。 **IWMDRMLicense** 的大部分方法都可讓您取得授權的相關資訊，或根據授權建立物件以加密或解密內容。 不過，有兩種方法可以控制列舉： [**GetNext**](iwmdrmlicense-getnext.md) 和 [**ResetEnumeration**](iwmdrmlicense-resetenumeration.md)。 **GetNext** 會將清單中的下一個授權載入介面。 **ResetEnumeration** 會將列舉傳回至第一次建立時的狀態。 重設列舉之後，會將清單中的第一個授權載入回 **IWMDRMLicense** 介面。

當您到達清單中的最後一個授權時，下一次的 **GetNext** 呼叫會傳回錯誤，也就是 \_ 沒有 \_ 其他 \_ 專案。

如果您的應用程式使用 DRM 所涵蓋的內容來執行動作，您應該檢查當地授權存放區中的授權，以取得許可權及其他限制因素，例如 (OPLs) 的輸出保護層級。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**從本機授權存放中的授權取得資訊**](getting-information-from-licenses-in-the-local-license-store.md)
</dt> </dl>

 

 




