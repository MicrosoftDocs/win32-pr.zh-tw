---
title: 關於多媒體檔案 i/o
description: 關於多媒體檔案 i/o
ms.assetid: d72ba20c-0085-4d5c-9fc6-b9024b575027
keywords:
- Windows 多媒體，檔案 i/o
- 多媒體，檔案 i/o
- 多媒體輸入，file i/o
- 多媒體檔案 i/o，關於
- 檔案 i/o，關於
- 輸入和輸出 (i/o) ，關於
- I/o (輸入和輸出) ，關於
- 基本 i/o
- " (RIFF) 的資源交換檔案格式"
- 'RIFF (資源交換檔案格式) '
- RIFF I/O
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fa055411819d719636d2e248ea5c565e3f060d7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106967621"
---
# <a name="about-multimedia-file-io"></a>關於多媒體檔案 i/o

大部分的多媒體應用程式都需要檔案輸入和輸出 (i/o) ，也就是建立、讀取和寫入磁片檔案的能力。 多媒體檔案 i/o 服務提供緩衝和未緩衝處理的檔案 i/o，以及 RIFF 檔案的支援。 這些服務可使用可在應用程式間共用的自訂 i/o 程式進行擴充。

大部分的應用程式只需要基本的檔案 i/o 服務和 RIFF 檔案 i/o 服務。 與檔案 i/o 效能相關的應用程式，例如即時從光碟串流資料的應用程式，可以使用服務直接存取檔案 i/o 緩衝區來將效能優化。 存取自訂存放裝置系統的應用程式（例如檔案封存和資料庫）可以提供自己的 i/o 程式，以讀取和寫入儲存系統的元素。

 

 




