---
description: 從 INF 檔案取出安裝資訊之後，您可以使用數個檔案處理功能來安裝 INF 區段中所列的檔案。
ms.assetid: 4e6042a0-36a9-4f74-b6cc-554e7f7aa2d9
title: 從 INF 檔案安裝
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bc3642edfb7abc2864c2c0784c79fbb21612fb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850820"
---
# <a name="installing-from-an-inf-file"></a>從 INF 檔案安裝

從 INF 檔案取出安裝資訊之後，您可以使用數個檔案處理功能來安裝 INF 區段中所列的檔案。 低層級的功能（例如 [**SetupInstallFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea) 和 [**SetupInstallFileEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa) ）會安裝單一檔案。

另外還有一些函數可以處理壓縮檔案。 [**SetupGetFileCompressionInfo**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetfilecompressioninfoa)函數會傳回壓縮檔案的相關資訊。 這項資訊接著可供 [**SetupDecompressOrCopyFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupdecompressorcopyfilea) 用來複製，並在必要時展開檔案。

高階功能（例如 [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)、 [**SetupInstallFilesFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilesfrominfsectiona)和 [**SetupInstallServicesFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallservicesfrominfsectiona) ）會在 **安裝** 或 **服務** 區段中處理安裝作業。 其中， **SetupInstallFromInfSection** 是最具彈性的，因為它可以執行在 INF 檔案的 [ **安裝** ] 區段中所列的任何類型的安裝操作。 這包括 **安裝** 區段的 **AddReg**、 **DelReg**、 **UpdateInis** 或 **UpdateIniField** 行中所列的登錄和 INI 作業。

[**SetupInstallFilesFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilesfrominfsectiona)和 [**SetupInstallServicesFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallservicesfrominfsectiona)函式會將 [**安裝** 或 **服務**] 區段中的作業分別排入至現有的檔案佇列。 請注意，您必須分別呼叫 SetupInstallFromInfSection 和 SetupInstallServicesFromInfSection，以佇列作業和服務。 如需詳細資訊，請參閱檔案 [佇列](file-queues.md)。

相反地， [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) 函式會建立並終結其本身的內部佇列。 **SetupInstallFromInfSection** 的常見用途是在所有檔案都成功複製之後呼叫它，以執行登錄和 INI 交易。

在 Windows 2000 上，DLL 檔案可以自行註冊，方法是在其 **安裝** 區段中包含 **RegisterDlls** 指示詞的 INF 檔案上呼叫 [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) 。 **SetupInstallFromInfSection** 也可以從64位進程自行註冊32位 dll。

在64位作業系統上，您可以呼叫 [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) ，以在登錄的32位部分執行作業。 若要將登錄機碼新增至登錄的32位部分，請 \_ \_ 在 INF 的 **ADDREG** 行中包含 FLG ADDREG 32BITKEY 旗標。 若只要在登錄的32位部分中刪除登錄機碼，請 \_ \_ 在 **DELREG** 行中包含 FLG DELREG 32BITKEY 機碼。 若只要在登錄的32位部分中設定或清除二進位值，請 \_ \_ 在 **BITREG** 行中包含 FLG BITREG 32BITKEY。

除了先前所列的函式，安裝程式 API 還包含可將檔案安裝作業（依檔案或 INF 區段）進行佇列的功能。 如需詳細資訊，請參閱檔案 [佇列](file-queues.md)。

 

 



