---
description: 使用 MakeCert 命令，利用 Internet Explorer 4.0 版或更新版本所提供的選項來建立測試憑證。
ms.assetid: 5dbcc8d0-ffd1-4418-adf6-a9805280ee6d
title: 使用 MakeCert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 068b10d5ce50141ff657379f9c5106cf2733d969
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691400"
---
# <a name="using-makecert"></a>使用 MakeCert

下列範例會使用 [MakeCert](makecert.md) 命令，利用 Internet Explorer 4.0 版或更新版本所提供的選項來建立測試憑證。

-   建立由預設測試根目錄發出的憑證。 將憑證儲存至檔案。

    **MakeCert** *MyNew .cer*

-   建立由預設測試根目錄發出的憑證。 將它儲存至憑證存放區。

    **MakeCert-ss** *MyNewStore*

-   建立由預設測試根目錄發出的憑證。 建立金鑰容器，並將憑證儲存至存放區和檔案。

    **MakeCert-sk** *MyNewKey* **-ss** *MyNewStore* *MyNew .cer*

-   建立由預設測試根目錄發出的憑證。 建立私密金鑰檔案，並將憑證儲存至存放區和檔案。

    **MakeCert-sv** *MyKeyFile* **-ss** *MyNewStore* *MyNew .cer*

-   建立由預設測試根目錄發出的憑證。 建立金鑰容器、將憑證儲存至存放區和檔案，然後將私密金鑰匯出。

    **MakeCert-sk** *MyNewKey* **-ss** *MyNewStore* *MyNew .cer* **-pe**

-   使用預設的測試根目錄來建立憑證。 將憑證儲存到存放區。 然後讓新建立的憑證發出另一個憑證。 將第二個憑證儲存至另一個存放區。

    **MakeCert-sk** *MyNewKey* **-ss** *MyNewStore* **MakeCert-是** *MyNewStore* **-ss** *AnotherStore*

-   使用預設的測試根目錄來建立憑證。 將憑證儲存至 [我的存放區]。 然後使用新建立的憑證建立另一個憑證。 如果我的存放區中有一個以上的憑證，則必須使用其一般名稱來識別憑證。

    **MakeCert-sk** *MyNewKey* **-n "CN = XXZZYY"-ss my MakeCert-是 my in "XXZZYY"-ss** *AnotherStore*

-   使用預設的測試根目錄來建立憑證。 將憑證儲存到 MY store 和檔案。 然後使用新建立的 *MyNew* 憑證來建立另一個憑證。 如果我的存放區中有一個以上的憑證，請使用憑證檔案名來唯一識別第一個憑證。

    **MakeCert-sk** *MyNewKey* **-n "CN = XXZZYY"-ss my** *MyNew .Cer* **MakeCert-是我的 ic** *MyNew .cer* **-ss** *AnotherStore*

 

 



