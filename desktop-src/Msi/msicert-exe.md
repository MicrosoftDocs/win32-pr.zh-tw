---
description: Windows安裝程式可以使用數位簽章來偵測損毀的資源。
ms.assetid: fc982813-583b-4fcd-88d8-9de227994e7b
title: Msicert.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1dbe8366093418e74ed4ab1cb8e8c23fb8036eb
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122879737"
---
# <a name="msicertexe"></a>Msicert.exe

Windows安裝程式可以使用數位簽章來偵測損毀的資源。 簽署者憑證可以與要由封裝安裝之外部資源的簽署者憑證進行比較。 如需詳細資訊，請參閱[數位簽章和 Windows Installer](digital-signatures-and-windows-installer.md)。

MsiCert.exe 是一種命令列公用程式，可用來將外部封包檔的數位簽章資訊填入 [MsiDigitalSignature 資料表](msidigitalsignature-table.md) 和 [MsiDigitalCertificate 資料表](msidigitalcertificate-table.md) 。 封包檔必須經過數位簽署並列在 [媒體資料表](media-table.md)中。 MsiCert.exe 使用數位簽署的封包中的簽署者憑證資訊，並且會建立 MsiDigitalSignature 和 MsiDigitalCertificate 資料表，並將其新增至資料庫（如果它們還不存在的話）。

## <a name="syntax"></a>Syntax

**msicert-d** *{database}* **-m** *{媒體輸入}* **-c** *{封包}* **\[ - \] h**

## <a name="command-line-options"></a>命令列選項

命令列選項不區分大小寫，而且可以使用斜線分隔符號，而不是虛線。



| 選項 | 參數        | 描述                                                                                             |
|--------|------------------|---------------------------------------------------------------------------------------------------------|
| -d     | &lt;database&gt; | 正在更新的資料庫 (.msi 檔案) 。                                                         |
| -M     | <media Id> | 封包檔記錄中 [媒體資料表](media-table.md) 的 [DiskId] 欄位中的專案。 |
| -c     | &lt;內閣&gt;  | 數位簽署的封包檔路徑。                                                          |
| -H     |                  | 包含數位簽章的雜湊。 這是選擇性的。                                            |



 

此工具僅適用于[Windows Installer 開發人員的 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows安裝程式開發工具](windows-installer-development-tools.md)
</dt> <dt>

[已發行的版本、工具和可轉散發套件](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



