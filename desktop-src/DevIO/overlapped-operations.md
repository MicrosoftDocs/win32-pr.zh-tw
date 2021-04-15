---
description: 重迭作業可讓執行緒在背景執行耗時的 i/o 作業，讓執行緒可以自由執行其他工作。
ms.assetid: 8c0eb20d-685a-4750-8253-a87089b68509
title: 重迭的作業
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19d8dc9e39386e25129d3e7d7a5281a8299d54ed
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468221"
---
# <a name="overlapped-operations"></a>重迭的作業

重迭作業可讓執行緒在背景執行耗時的 i/o 作業，讓執行緒可以自由執行其他工作。 若要在通訊資源上啟用重迭的 i/o 作業，執行緒必須在控制碼開啟時，于 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)函式中指定檔案 **\_ 旗 \_** 標重迭旗標。 若要執行 [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) 或 [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) 函數做為重迭的作業，呼叫的執行緒必須指定重迭 [**結構的**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) 指標。 重迭 **的結構必須** 包含手動重設的控制碼 (而非自動重設) 事件物件。 在作業完成之前，系統會將事件物件的狀態設定為不會發出信號。」 當作業完成時，系統會將事件物件的狀態設定為收到信號。 執行緒會使用等候函式來檢查事件物件的目前狀態，或等候其狀態收到信號。

[**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex)和 [**WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex)函數只能做為重迭的作業執行。 呼叫執行緒會指定 [**FileIOCompletionRoutine**](/windows/desktop/api/minwinbase/nc-minwinbase-lpoverlapped_completion_routine) 函式的指標，該函式會在重迭的作業完成時執行。 只有當呼叫的執行緒執行可提供警示作業時，才會執行完成常式。

如需事件物件、等候函式、可提供警示等候和完成常式的詳細資訊，請參閱 [關於同步](/windows/desktop/Sync/about-synchronization)處理。

 

 
