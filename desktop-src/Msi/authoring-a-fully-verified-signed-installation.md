---
description: 您可以使用這些指導方針，透過數位簽章來涵蓋整個 Windows Installer 安裝。
ms.assetid: e70eab94-4615-4a73-bccc-e16bd24551f6
title: 撰寫經過完整驗證的已簽署安裝
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9e76bbfb77eab8b020cb1591847d2a36d09c96a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974649"
---
# <a name="authoring-a-fully-verified-signed-installation"></a>撰寫經過完整驗證的已簽署安裝

您可以使用這些指導方針，透過數位簽章來涵蓋整個 Windows Installer 安裝。

Windows Installer 安裝的作者必須遵守下列各項，以確保安裝的所有部分都包含在數位簽章中：

-   使用內部封包檔，或使用已簽署的外部封包檔，並正確地撰寫 [MsiDigitalSignature 資料表](msidigitalsignature-table.md) 和 [MsiDigitalCertificate 資料表](msidigitalcertificate-table.md)。
-   只使用儲存在封裝內或隨封裝一起安裝的自訂動作。
-   簽署安裝套件。
-   在封裝中包含 [MsiPatchCertificate 資料表](msipatchcertificate-table.md) 。 若要啟用 [使用者帳戶控制 (UAC) 修補](user-account-control--uac--patching.md)，此資料表必須包含用來識別用來數位簽署修補程式之簽署者憑證的資訊。 UAC 修補讓安裝套件的作者能夠找出可供非系統管理員使用者未來套用的數位簽署修補程式。

如需示範如何使用自動化撰寫已簽署安裝的範例，請參閱 [使用自動化撰寫經過完整驗證的已簽署安裝](authoring-a-fully-verified-signed-installation-using-automation.md)。

 

 



