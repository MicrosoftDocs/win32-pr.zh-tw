---
description: 以 JScript 或 Visual Basic 撰寫的自訂動作、腳本版本 (VBScript) 可以呼叫選擇性的函式。 這些函數必須傳回下表所示的其中一個值。
ms.assetid: f05d0b94-e79e-440e-9f2b-99fe0e9e2646
title: JScript 和 VBScript 自訂動作的傳回值
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cae96ecba320914b7b00dfa718deffdd56ae7eaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106980752"
---
# <a name="return-values-of-jscript-and-vbscript-custom-actions"></a>JScript 和 VBScript 自訂動作的傳回值

以 JScript 或 Visual Basic 撰寫的自訂動作、腳本版本 (VBScript) 可以呼叫選擇性的函式。 這些函數必須傳回下表所示的其中一個值。



| 傳回值              | 值        | 描述                                                                                                |
|---------------------------|--------------|------------------------------------------------------------------------------------------------------------|
| msiDoActionStatusNoAction | 0            | 未執行動作。                                                                                       |
| msiDoActionStatusSuccess  | IDOK = 1     | 動作已成功完成。                                                                             |
| msiDoActionStatusUserExit | IDCANCEL = 2 | 使用者提前終止。                                                                             |
| msiDoActionStatusFailure  | IDABORT = 3  | 無法復原的錯誤。 如果在剖析或執行 JScript 或 VBScript 期間發生錯誤，則傳回。 |
| msiDoActionStatusSuspend  | IDRETRY = 4  | 要在稍後繼續執行的暫止順序。                                                                    |
| msiDoActionStatusFinished | IDIGNORE = 5 | 略過其餘的動作。 不是錯誤。                                                                      |



 

請注意，Windows Installer 會在將傳回值寫入記錄檔時，轉譯所有動作的傳回值。 例如，如果動作傳回值在記錄檔中顯示為 1 (一個) ，這表示該動作傳回 msiDoActionStatusSuccess。 如需此轉譯的詳細資訊，請參閱 [動作傳回值的記錄](logging-of-action-return-values.md)。

若要從腳本自訂動作傳回「成功」以外的值，您必須使用自訂動作的函數目標。 目標函數是在 [CustomAction 資料表](customaction-table.md)的目標資料行中指定。

下列腳本範例顯示如何從 VBScript 自訂動作傳回成功或失敗。


```VB
Function MyVBScriptCA()

    If Session.Property("CustomErrorStatus") <> "0" Then
        'return error
        MyVBScriptCA = 3
        Exit Function
    End If

    ' return success
    MyVBScriptCA = 1
    Exit Function

End Function
```



如果這個 VBScript 內嵌在安裝套件的 [二進位資料表](binary-table.md) 中 MyCA.vbs，則腳本的 [CustomAction 資料表](customaction-table.md) 專案如下所示：



| 動作         | 類型 | 來源   | 目標       |
|----------------|------|----------|--------------|
| MyCustomAction | 6    | MyCA.vbs | MyVBScriptCA |



 

 

 



