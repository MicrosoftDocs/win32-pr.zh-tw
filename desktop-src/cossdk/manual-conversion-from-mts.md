---
description: 從 MTS 手動轉換
ms.assetid: 7ecc64a8-783d-4238-8b63-8e9c76382723
title: 從 MTS 手動轉換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2e5fab25721738d497c943a166f899c73927b13
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103688827"
---
# <a name="manual-conversion-from-mts"></a>從 MTS 手動轉換

您可能會想要隔離將 MTS 套件轉換為 COM + 應用程式，使其不在 Windows 安裝程式的範圍內。 下列程式提供另一種方法：

1.  使用 MTS 2.0 套件匯出功能來匯出 MTS 套件， (產生 MTS 套件檔案和其他檔案的集合) 。
2.  刪除 MTS 套件及升級 Windows，或執行 Windows 的全新安裝。
3.  使用 [元件服務] 系統管理工具的 [應用程式安裝] 嚮導，在 Windows 2000 或更新版本的系統上安裝 MTS 套件 ( pak) 檔案。 您也必須在 **HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別 \\ APPID \\ RunAs** 的系統登錄中，重設應用程式的「執行身分」身分識別。

> [!Note]  
> 只有自動轉換程式 (透過 Windows 安裝程式或執行 MTSTOCOM 公用程式) 產生 MTSTOCOM 記錄檔。 遵循手動轉換程式時，不會產生此檔案。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[從 MTS 自動轉換](automatic-conversion-from-mts.md)
</dt> <dt>

[COM + 轉換結果和問題](com--conversion-results-and-issues.md)
</dt> <dt>

[MTS 管理程式庫](mts-administration-library.md)
</dt> </dl>

 

 



