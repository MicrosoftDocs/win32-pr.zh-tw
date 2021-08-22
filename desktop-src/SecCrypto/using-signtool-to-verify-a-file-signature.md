---
description: 說明如何使用 SignTool 來驗證檔案簽章。
ms.assetid: 9c40a397-19ea-4600-97ee-987dd10f4ef8
title: 使用 SignTool 來驗證檔案簽章
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 137a4117b64ca5d62ee2ffe5fb80a7e0751d91f840ce1270482d9e114f4dd61b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118896691"
---
# <a name="using-signtool-to-verify-a-file-signature"></a>使用 SignTool 來驗證檔案簽章

下列命令會驗證名為 *MyControl.exe* 之檔案的簽章：

**SignTool 確認** *MyControl.exe*

如果上述範例失敗，可能是簽章使用程式碼簽署憑證。 [SignTool](signtool.md)預設為驗證 Windows 的驅動程式原則。

下列命令會使用預設驗證驗證原則來驗證簽章：

**SignTool 確認/pa** *MyControl.exe*

下列命令會驗證可能已在目錄中簽署的系統檔案：

**SignTool 確認/a** *SysFile.dll*

下列命令會驗證在名為 *MyCat.cat* 的目錄中簽署的系統檔案：

**SignTool 驗證/c** *MyCat.cat* *MyFile.ini*

針對任何 [SignTool](signtool.md) 驗證，您可以取得憑證的簽署者。 下列命令會驗證系統檔案並顯示簽署者憑證：

**SignTool 確認/v** *MyControl.exe*

[SignTool](signtool.md) 會傳回命令列文字，指出簽章檢查的結果。 此外，SignTool 會傳回零的結束代碼，表示執行成功，一個用於失敗的執行，另二個則表示執行完成但出現警告。

如需 [SignTool](signtool.md)的詳細資訊，請參閱 [SignTool](signtool.md)。

 

 



