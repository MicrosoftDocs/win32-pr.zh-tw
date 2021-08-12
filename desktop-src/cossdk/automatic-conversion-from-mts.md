---
description: 從 MTS 自動轉換
ms.assetid: 0848639a-26ce-47ad-8384-8969a7c3bcde
title: 從 MTS 自動轉換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e02cc3889c479d829290b22b71edf13cc4ebc8f419c333d5e99390d47c01da65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118549485"
---
# <a name="automatic-conversion-from-mts"></a>從 MTS 自動轉換

自動轉換會以兩個步驟進行，如下所示：

1.  在 Windows 安裝期間。 轉換是透過 MTSTOCOM 公用程式，由 Windows 的安裝程式處理。
    > [!Note]  
    > 如果步驟1失敗，部分或所有的 MTS 套件實際上可能已轉換，但可能遺漏某些屬性。 在此情況下，請使用 [元件服務] 系統管理工具來確認所有屬性。 MTS 屬性仍會存在於 HKEY \_ 本機電腦 Microsoft 交易) 伺服器之 system registry (的電腦上， \_ \\ \\ 但只能透過 regedit.exe 公用程式存取。

     

2.  最後一次重新開機之後，才會顯示 Windows 登入] 對話方塊。 步驟2會處理需要網路存取的轉換動作， (主要是角色成員建立) 。
    > [!Note]  
    > 如果步驟2因為暫時性網路或網域控制站) 失敗而失敗 (，就可以多次重新執行 MTSTOCOM 轉換公用程式。 若要這樣做，請在命令提示字元中，或從 [**開始**] 功能表選取 [**執行**] 之後，輸入下列命令： **% windir% \\ system32 \\mtstocom.exe**。

     

## <a name="mtstocom-log-file"></a>MTSTOCOM 記錄檔

MTSTOCOM 公用程式會在 Windows 目錄中產生記錄檔 (MTSTOCOM) 。 此記錄檔會保留從 MTS 套件轉換為 COM + 應用程式的記錄。 如果轉換過程中有任何錯誤，最好檢查記錄檔以取得進一步的資訊。 記錄檔會攔截常見的問題，例如不正確使用者或密碼。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM + 轉換結果和問題](com--conversion-results-and-issues.md)
</dt> <dt>

[從 MTS 手動轉換](manual-conversion-from-mts.md)
</dt> <dt>

[MTS 管理程式庫](mts-administration-library.md)
</dt> </dl>

 

 



