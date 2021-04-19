---
title: 使用 Windows Media Player 啟用同步處理
description: 使用 Windows Media Player 啟用同步處理
ms.assetid: a312dfef-ac48-4c58-a59a-b277f5386419
keywords:
- Windows Media 裝置管理員，與 Windows Media Player 同步處理
- 裝置管理員，與 Windows Media Player 同步處理
- 程式設計指南，與 Windows Media Player 同步處理
- 服務提供者，與 Windows Media Player 同步處理
- 建立服務提供者，與 Windows Media Player 同步處理
- 與 Windows Media Player 同步處理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b621be3b17d42368bc859081f47bc29bb2cfc667
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965613"
---
# <a name="enabling-synchronization-with-windows-media-player"></a>使用 Windows Media Player 啟用同步處理

您可以讓裝置參與 Windows Media Player 的自動同步處理。 自動同步處理表示當使用者指定的同步處理裝置連接到電腦時，Windows Media Player 會自動從裝置下載、更新或刪除檔案，而不需要任何額外的使用者輸入。

根據預設，下列裝置會與 Windows Media Player 同步處理：

-   MTP 裝置
-   大量儲存裝置
-   Windows CE (Windows Media Player 10 行動裝置版和更新版本的裝置) 

針對要與 Windows Media Player 同步處理的任何其他裝置，必須符合下列需求：

-   裝置必須公告為 {F33FDC04-D1AC-4E8E-9A30-19BBD4B108AE} 的 PAP 裝置介面
-   服務提供者所傳回的裝置物件必須支援 **IMDSPDevice3** 介面。
-   裝置參數 UseExtendedWmdm 必須設定為 **DWORD** 值1。 如需詳細資訊，請參閱 [裝置參數](device-parameters.md) 。
-   服務提供者應該執行下列介面：

    [**IMDSPDevice3**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice3)

    [**IMDSPObject2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject2)

    [**IMDSPStorage4**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage4)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**建立服務提供者**](creating-a-service-provider.md)
</dt> <dt>

[**裝置參數**](device-parameters.md)
</dt> </dl>

 

 




