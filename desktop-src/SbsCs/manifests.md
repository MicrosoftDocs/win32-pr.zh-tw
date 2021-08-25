---
description: 資訊清單是隨附的 XML 檔案，並描述並存元件或隔離的應用程式。
ms.assetid: 53c4c2e6-fff9-4506-b7e0-d091d2ec9883
title: 資訊清單
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 974aaea3dad60c80456d0acd085d610c81b93716342962abcd465adaf9efdf48
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119977208"
---
# <a name="manifests"></a>資訊清單

資訊清單是隨附的 XML 檔案，並描述並存元件或隔離的應用程式。 資訊清單可透過元件的 **assemblyIdentity** 元素來唯一識別元件。 它們包含傳統上儲存在登錄中的系結和啟用（例如 COM 類別、介面和類型程式庫）所使用的資訊。 資訊清單也會指定組成元件的檔案，而且如果元件作者想要建立版本，則可能包含 Windows 類別。 並存元件並未在系統上註冊，但可供系統上的應用程式和其他元件在資訊清單檔案中指定相依性。

資訊清單檔案可讓系統管理員和應用程式在部署後管理並存元件版本。 每個並存元件都必須有相關聯的資訊清單。 安裝 Windows XP 時，會安裝[支援的 Microsoft 並存元件](supported-microsoft-side-by-side-assemblies.md)及其資訊清單。 如果您開發自己的並存元件，您也必須安裝資訊清單檔案。 如需詳細資訊，請參閱 [安裝並存元件](installing-side-by-side-assemblies.md) 和 [資訊清單檔案參考](manifest-files-reference.md)。

資訊清單和設定檔案未當地語系化。

下列類型的資訊清單會搭配並存元件使用：

-   [元件資訊清單](assembly-manifests.md) 會描述並存元件。 它們可用來管理並存元件的名稱、版本、資源和相依元件。 [共用元件](/windows/desktop/Msi/shared-assemblies)的資訊清單會儲存在系統的 WinSxS 資料夾中。 私用組件資訊清單會儲存為 DLL 或應用程式資料夾中的資源
-   [應用程式資訊清單](application-manifests.md) 會描述 [隔離的應用程式](isolated-applications.md)。 它們可用來管理應用程式在執行時間時應系結的共用並存元件名稱和版本。 應用程式資訊清單會複製到與應用程式可執行檔相同的資料夾中，或包含在應用程式的可執行檔中做為資源。
-   [應用程式佈建檔](application-configuration-files.md)是用來覆寫和重新導向並存元件和應用程式所使用之相依元件版本的資訊清單。
-   [Publisher 設定檔](publisher-configuration-files.md)案是用來將並存元件版本重新導向至另一個相容版本的資訊清單。 重新導向元件的版本應該具有與原始版本相同的主要. 次要值。

 

 
