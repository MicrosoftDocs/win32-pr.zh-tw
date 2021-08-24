---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 0D537FD1-AD5C-43CB-989F-4B5B7C0A1208
title: " (隔離的應用程式和並存元件) "
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ac40ba2393bb2d043957e04b8d34ca93fede605bbcd11ad601667e97f79f057
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142715"
---
# <a name="a-isolated-applications-and-side-by-side-assemblies"></a> (隔離的應用程式和並存元件) 

B C [D](d-sbscs-gly.md) E F [G](g-sbscs-gly.md) H [I](i-sbscs-gly.md) J K L [M](m-sbscs-gly.md) N O [P](p-sbscs-gly.md) Q [R](r-sbscs-gly.md) [S](s-sbscs-gly.md) T W X Y Z

<dl> <dt>

<span id="_win32_activation_context_gly"></span><span id="_WIN32_ACTIVATION_CONTEXT_GLY"></span>**啟用內容**
</dt> <dd>

記憶體中的資料結構。 此結構的每個區段都包含可並存感知 API 函式的中繼資料。 例如，一個區段可能會有 dll 載入器所使用的 DLL 重新導向資料，而另一個區段可能會有 COM 伺服器資料。 這項資料可用來將 DLL 的載入重新導向至特定版本、建立 COM 物件，或將視窗建立至與應用程式最相容的版本。

</dd> <dt>

<span id="_win32_application_configuration_gly"></span><span id="_WIN32_APPLICATION_CONFIGURATION_GLY"></span>**應用程式設定**
</dt> <dd>

執行應用程式所需之並存元件的名稱和版本。 使用資訊清單部署應用程式時，會明確定義特定版本之共用並存元件的相依性。 根據預設，資訊清單中指定的元件版本是在啟用時使用的版本。 全域應用程式設定會指定系統上所有應用程式的設定。 每個應用程式設定可以針對每個應用程式覆寫全域應用程式設定。

</dd> <dt>

<span id="_win32_application_configuration_manifest_gly"></span><span id="_WIN32_APPLICATION_CONFIGURATION_MANIFEST_GLY"></span>**應用程式設定資訊清單**
</dt> <dd>

指定完整或部分隔離應用程式所使用之並存元件的檔案。 應用程式設定資訊清單檔案會安裝在與應用程式可執行檔相同的資料夾中。

</dd> <dt>

<span id="_win32_application_manifest_gly"></span><span id="_WIN32_APPLICATION_MANIFEST_GLY"></span>**應用程式資訊清單**
</dt> <dd>

描述隔離應用程式的檔案。 它會指定執行應用程式所需的資訊，包括私用元件的相依性、共用元件的特定版本，以及私用元件的中繼資料。 應用程式資訊清單檔的名稱是應用程式可執行檔的名稱，後接副檔名為 .manifest。 例如，針對 MySampleApp.exe，資訊清單檔會是 MySampleApp.exe 資訊清單。

</dd> <dt>

<span id="_win32_assembly_gly"></span><span id="_WIN32_ASSEMBLY_GLY"></span>**裝配**
</dt> <dd>

命名、系結、版本控制、部署或設定程式設計程式碼區塊的基礎單位。 這些程式碼元件可能放在 Dll 或 COM 元件中。 具有一般功能的應用程式可能會執行稱為模組或程式碼元件的程式設計程式碼共用區塊。 元件安全共用的基礎結構稱為「並存元件共用」。

</dd> <dt>

<span id="_win32_assembly_manifest_gly"></span><span id="_WIN32_ASSEMBLY_MANIFEST_GLY"></span>**組件資訊清單**
</dt> <dd>

並存元件的描述。 它會指定名稱、版本、檔案、元件的資源、元件專案的系結資料，以及其他並存元件的相依性。 組件資訊清單檔可以有任何有效的檔案名，只要後面跟副檔名資訊清單即可。

</dd> </dl>

 

 



