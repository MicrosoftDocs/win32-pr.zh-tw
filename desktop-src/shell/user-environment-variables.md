---
description: 環境變數會指定檔案的搜尋路徑、暫存檔的目錄、應用程式特定的選項，以及其他類似的資訊。
ms.assetid: 6180e54e-4bd9-4692-83fd-f3f7f1d8f8d7
title: 使用者環境變數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf4f898c7a9135c0421fdd67a7bed1d97655556f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991614"
---
# <a name="user-environment-variables"></a>使用者環境變數

環境變數會指定檔案的搜尋路徑、暫存檔的目錄、應用程式特定的選項，以及其他類似的資訊。 系統會維護每個使用者的環境區塊，以及一部電腦的環境區塊。 系統內容區塊代表特定電腦上所有使用者的環境變數。 使用者的環境區塊代表系統為該特定使用者維護的環境變數，包括系統內容變數集。

根據預設，每個進程都會收到其父進程的環境區塊複本。 一般來說，這是登入之使用者的環境區塊。 處理常式可以使用 [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) 或 [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) 函式，為其子進程指定不同的環境區塊。

若要新增或修改環境變數，使用者可從 **主控台** 中選取 [**系統**]，然後選取 [**環境**] 索引標籤。使用者也可以在命令提示字元中使用 **set** 命令來新增或修改環境變數。 使用 **set** 命令建立的環境變數只會套用至其所設定的命令視窗以及其子進程。 如需詳細資訊，請輸入 **set/？** 。

若要取得指定使用者的環境區塊複本，請使用 [**CreateEnvironmentBlock**](/windows/desktop/api/Userenv/nf-userenv-createenvironmentblock) 函數。 若要釋放 **CreateEnvironmentBlock** 所建立的環境區塊，請使用 [**DestroyEnvironmentBlock**](/windows/desktop/api/Userenv/nf-userenv-destroyenvironmentblock) 函數。 這些函數會參考環境區塊的指標。 環境區塊是以 null 結束之 Unicode 字串的陣列。 此清單以兩個 null 結尾 (\\ 0 \\ 0) 。

若要使用指定使用者的環境區塊來展開包含環境變數的字串，請使用 [**ExpandEnvironmentStringsForUser**](/windows/desktop/api/Userenv/nf-userenv-expandenvironmentstringsforusera) 函數。

 

 
