---
description: 持續性記憶體 (PM) 技術可提供非暫時性媒體的位元組層級存取，同時也能大幅減少儲存或取得資料的延遲。
ms.assetid: 68BF6074-09CB-4D6E-8BFD-FBA297391286
title: Windows NVML 整合中的持續性記憶體程式設計
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 750a05f28ca4698091f79b1004bbbb00ff69752e0ff45f2153cc4f0b7fe20a26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951048"
---
# <a name="persistent-memory-programming-in-windows---nvml-integration"></a>Windows NVML 整合中的持續性記憶體程式設計

持續性記憶體 (PM) 技術可提供非暫時性媒體的位元組層級存取，同時也能大幅減少儲存或取得資料的延遲。 它會在系統的記憶體和傳統儲存體之間建立新的層。 任何相依于或透過快速寫入持續媒體進行調整的程式，都可以從 PM 獲益。

本文的目的是要說明如何將非動態記憶體程式庫 (NVML) 整合到 Visual Studio 專案中，以方便使用。

> [!Note]  
> 持續性記憶體有時也稱為儲存體類別記憶體 (SCM) 。

 

## <a name="pm-and-nvml"></a>PM 和 NVML

持續性記憶體的第一次支援是在 Windows Server 2016 和 Windows 10 周年更新 (1607) 引進。 若要快速流覽，請參閱這兩個 Channel9 影片：

-   [在 Windows Server 2016 中使用非揮發性記憶體 (NVDIMM-N) 做為區塊存放裝置](https://channel9.msdn.com/Events/Build/2016/P466)
-   [在 Windows Server 2016 中使用非揮發性記憶體 (NVDIMM-N) 做為位元組可定址存放裝置](https://channel9.msdn.com/Events/Build/2016/P470)

為了協助開發人員充分利用持續性記憶體供應專案的優點，Microsoft 也提供了將非動態記憶體程式庫 (NVML) Windows 的工作。 此程式庫提供各種工具，可讓應用程式持續記憶體感知。 例如，它包含的程式碼可讓您輕鬆地建立 PM 感知的索引鍵/值存放區，以取得非常快速的查閱和商店。 您可以在 [NVM 程式庫](https://pmem.io/nvml/)中找到 NVML 的詳細資訊，包括範例。

## <a name="integrating-nvml-into-a-visual-studio-project"></a>將 NVML 整合至 Visual Studio Project

1. 下載 NVML 程式庫檔案和標頭

-   NVML 會在 GitHub 上進行維護。 您可以自行編譯來源，或直接從這裡下載已編譯的二進位檔： [NVML 版本 1.2-Windows Technical Preview](https://github.com/pmem/pmdk/releases/tag/1.2%2Bwtp1)。

2. 將程式庫檔案和標頭放在您選擇的目錄中，例如： "C： \\ NVML \\ lib" 和 "c： \\ NVML \\ inc."。

3. 設定您的專案，如下所示：

-   開啟您的 visual studio 專案，然後在 [方案總管] 中，以滑鼠右鍵按一下您的專案名稱。
-   在產生的快顯視窗底部開啟專案的 [設定] 窗格。
-   流覽至 [設定屬性-> C/c + +]，然後將儲存標頭的資料夾 (C： \\ NVML \\ inc.) 新增至 [其他 Include 目錄] 欄位。
-   接下來，流覽至 [設定內容-> 連結器]，然後將儲存程式庫的資料夾 (C： \\ NVML \\ lib) 新增至 [其他程式庫目錄] 欄位

4. 接下來，請確定您將專案的目標設為 Windows Server 2016 或 Windows 10 周年更新：

-   流覽至 [設定屬性-> 一般]，並將 [目標平臺版本] 欄位設定為 "10.0.14393.0" 和
-   流覽至 [設定屬性-> C/c + +]，然後將 [NTDDI \_ VERSION = NTDDI \_ WIN10 \_ RS1;] 新增至 [預處理器] 欄位。

5. 在您的程式碼中包含標頭，並連結至所需的程式庫

-   至此，您可以直接在程式碼中包含您想要在程式碼中使用的標頭檔，就像任何其他標頭檔一樣。 例如，若要使用 libpmem：
    -   新增 " \# include <libpmem .h>" 和
    -   將 "libpmem" 新增至 [設定屬性-> 連結器-> 輸入-> 其他相依性]

至此，您已準備好直接在程式碼中呼叫程式庫的函式，並利用這些函式。

 

 



