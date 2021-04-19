---
description: 當動作傳回這些錯誤碼時，安裝程式會將下列值寫入記錄檔中。 如需 Windows Installer 函式所傳回之錯誤碼的完整清單，請呼叫 MsiExec.exe 和 InstMsi.exe，請參閱錯誤碼。
ms.assetid: 653bbf45-ac2c-4f8a-a978-960e0c42e6e4
title: 動作傳回值的記錄
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aaaa203fee1fbb02bef070d065a9838383ea588b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997586"
---
# <a name="logging-of-action-return-values"></a>動作傳回值的記錄

當動作傳回這些錯誤碼時，安裝程式會將下列值寫入記錄檔中。 如需 Windows Installer 函式所傳回之錯誤碼的完整清單，請呼叫 MsiExec.exe 和 InstMsi.exe，請參閱 [錯誤碼](error-codes.md)。



| 錯誤碼                       | 函式呼叫傳回的值 MsiExec.exe，以及 InstMsi.exe | 出現在記錄檔中的值。 | Description                                                                                                                                                                                                                                                                     |
|----------------------------------|----------------------------------------------------------------|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ \_ 未 \_ 呼叫錯誤函式     | 1626                                                           | 0                              | 無法執行函數。                                                                                                                                                                                                                                               |
| 錯誤 \_ 成功                   | 0                                                              | 1                              | 已成功完成動作。                                                                                                                                                                                                                                               |
| \_安裝 \_ USEREXIT 時發生錯誤         | 1602                                                           | 2                              | 使用者已取消安裝。                                                                                                                                                                                                                                                   |
| \_安裝 \_ 失敗時發生錯誤          | 1603                                                           | 3                              | 嚴重錯誤。                                                                                                                                                                                                                                                                  |
| \_安裝 \_ 暫止時發生錯誤          | 1604                                                           | 4                              | 安裝已暫停，未完成。                                                                                                                                                                                                                                         |
| 錯誤 \_ 成功                   | 0                                                              | 5                              | 動作已成功完成。                                                                                                                                                                                                                                              |
| 錯誤 \_ 不正確 \_ 控制碼 \_ 狀態    | 1609                                                           | 6                              | 控制碼處於無效狀態。                                                                                                                                                                                                                                              |
| 錯誤 \_ 不正確 \_ 資料             | 1626                                                           | 7                              | 資料無效。                                                                                                                                                                                                                                                            |
| \_安裝 \_ 已在執行中時發生錯誤 \_ | 1618                                                           | 8                              | 其他安裝正在進行。 一次只能有一個安裝可以在 [InstallExecuteSequence](installexecutesequence-table.md)、 [AdminExecuteSequence](adminexecutesequence-table.md)或 [AdvtExecuteSequence](advtexecutesequence-table.md) 資料表中執行動作。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows Installer 記錄](windows-installer-logging.md)
</dt> </dl>

 

 



