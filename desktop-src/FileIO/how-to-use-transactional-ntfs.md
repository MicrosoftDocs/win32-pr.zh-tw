---
description: 管理交易式 NTFS 中的交易式檔案控制代碼。
ms.assetid: 29879a3f-14b4-462c-a001-46c3c3eb74d1
title: 如何使用交易式 NTFS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8daafd2bc2ee0e695ee3bdede4ac2f62be1000c111d0c544dec877c357f42629
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015276"
---
# <a name="how-to-use-transactional-ntfs"></a>如何使用交易式 NTFS

## <a name="transacted-file-handles"></a>交易的檔案控制代碼

交易式 NTFS (TxF) 將檔案控制代碼系結至交易。 針對處理 (的作業，例如， [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) 和 [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) 函式) ，實際的 API 函式呼叫不會變更。 針對採用名稱的檔案作業，這些作業有明確的交易函式。 例如，不是呼叫 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)，而是呼叫 [**CreateFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda)。 這會建立交易檔案控制代碼，然後用於所有需要控制碼的檔案作業。 使用此控制碼的所有後續作業都是交易作業。

## <a name="basic-txf-usage"></a>基本 TxF 使用方式

下列一系列的步驟代表 TxF 的最基本使用方式。 此外，也支援更複雜的案例，也就是應用程式設計工具的判斷。

1.  藉由呼叫 KTM 函數 [**CreateTransaction**](/windows/desktop/api/ktmw32/nf-ktmw32-createtransaction)或使用 [分散式交易協調器](/previous-versions/windows/desktop/mscs/distributed-transaction-coordinator) (DTC) 的 **IKernelTransaction** 介面，建立交易。
2.  藉由呼叫 [**CreateFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda)取得交易檔案控制代碼 (s) 。
3.  使用交易式檔案控制代碼 (s) ，視需要修改 (s) 的檔案。
4.  關閉與步驟1中建立之交易相關聯的所有交易式檔案控制代碼。
5.  藉由呼叫對應的 KTM 或 DTC 函數來認可或中止交易。

## <a name="key-points-of-the-txf-programming-model"></a>TxF 程式設計模型的重點

當您開發 TxF 應用程式時，您可以考慮使用 TxF 程式設計模型的重點：

-   強烈建議應用程式在認可或回復交易之前，先關閉所有交易的檔案控制代碼。 當交易結束時，系統會使所有交易控制碼失效。 交易結束之後，在交易控制碼上執行的任何作業（除了 close 以外）都會傳回下列錯誤： **錯誤 \_ 控制碼 \_ 不再 \_ \_ 有效**。
-   檔案會被視為儲存裝置。 支援部分更新和完整檔案複寫。 多個交易無法同時修改同一個檔案。
-   記憶體對應 i/o 是透明的，而且與一般檔案 i/o 一致。 應用程式必須在認可交易之前，先排清並關閉已開啟的區段。 若未這麼做，可能會導致交易內對應檔案的部分變更。 如果未完成，則復原會失敗。

## <a name="common-programming-errors"></a>常見的程式設計錯誤

開發交易應用程式時，可能會發生下列常見錯誤：

-   在交易完成之後使用檔案控制代碼。
-   在認可交易之前，無法關閉已刪除之檔案和目錄的控制碼，這會導致無法進行刪除作業。 執行認可之前，必須先發生這個事件，才能將刪除作業視為交易的一部分。 這是因為系統不會實際刪除檔案，直到它的最後一個控制碼關閉為止，即使作業不是交易式，也是 Windows 檔案 i/o 子系統的一部分。
-   無法考慮系統起始的交易復原，可能會在任何時間發生;例如，如果系統資源已用盡，則會回復交易。

 

 
