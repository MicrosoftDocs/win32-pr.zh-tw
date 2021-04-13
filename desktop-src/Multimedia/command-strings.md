---
title: 命令字串
description: 命令字串
ms.assetid: ca9ca153-f2bf-45ed-84e6-44e86e8efaed
keywords:
- MCI 命令字串，關於
- MCI 命令字串，語法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b62013abff091f668a3b045e9f3ca2e8745f0d9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104374985"
---
# <a name="command-strings"></a>命令字串

若要傳送字串命令至 MCI 裝置，請使用 [**mciSendString**](/previous-versions//dd757161(v=vs.85)) 函式，其中包含字串命令的參數和任何傳回信息的緩衝區。

如果成功， **mciSendString** 函數會傳回零。 如果函式失敗，則傳回值的低序位文字會包含錯誤碼。 您可以將此錯誤碼傳遞至 [**mciGetErrorString**](/previous-versions//dd757158(v=vs.85)) 函式，以取得錯誤的文字描述。

## <a name="syntax-of-command-strings"></a>命令字串的語法

MCI 命令字串使用一致的動詞物件修飾詞語法。 每個命令字串都包含一個命令、一個裝置識別碼和一個命令引數。 某些命令的引數是選擇性的，有些則是必要的。

命令字串的格式如下：

*命令裝置 \_ 識別碼引數*

這些元件包含下列資訊：

-   此 *命令* 會指定 MCI 命令，例如 [ [**開啟**](open.md)]、[ [**關閉**](close.md)] 或 [ [**播放**](play.md)]。
-   *裝置 \_ 識別碼* 可識別 MCI 驅動程式的實例。 裝置 *\_ 識別碼* 會在裝置開啟時建立。
-   *引數* 會指定命令所使用的旗標和變數。 旗標是使用 MCI 命令辨識的關鍵字。 變數是適用于 MCI 命令或旗標的數位或字串。

    例如， **play** 命令會使用引數「from *position* 」和「to *position* 」來表示要開始和結束播放的位置。 您可以依任何順序列出與命令搭配使用的旗標。 當您使用具有與其相關聯之變數的旗標時，您必須提供變數的值。

    未指定的 (和選擇性) 命令引數採用預設值。

下列範例函式會傳送具有 "from" 和 "to" 旗標的 [**play**](play.md) 命令。


```C++
BOOL PlayFromTo(LPTSTR lpstrAlias, DWORD dwFrom, DWORD dwTo) 
{ 
    TCHAR achCommandBuff[128]; 
    int result;
    MCIERROR err;

    // Form the command string.
    result = _stprintf_s(
        achCommandBuff, 
        TEXT("play %s from %u to %u"), 
        lpstrAlias, dwFrom, dwTo); 

    if (result == -1)
    {
        return FALSE;
    }

    // Send the command string.
    err = mciSendString(achCommandBuff, NULL, 0, NULL); 
    if (err != 0)
    {
        return FALSE;
    }

    return TRUE;
} 
```



## <a name="data-types-for-command-variables"></a>命令變數的資料類型

您可以針對命令字串中的變數使用下列資料類型。



| **Data type**        | **說明**                                                                                                                                                                                                                                                                                                                                                |
|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 字串              | 字串資料類型會以開頭和尾端的空白字元和引號分隔。 MCI 從字串移除單引號。 若要在字串中放入引號，請使用一組您想要內嵌引號的雙引號。 若要使用空字串，請使用以開頭和尾端空格分隔的兩個引號。 |
| 帶正負號的長整數 | 帶正負號的長整數資料類型會以開頭和尾端空格分隔。 除非另有指定，否則整數可以是正數或負數。 如果您使用負整數，則不應以空格分隔減號和第一個數位。                                                                                                    |
| 矩形           | 矩形資料類型是四個帶正負號短值的排序清單。 空白字元會分隔此資料類型，並分隔清單中的每個整數。                                                                                                                                                                                                              |



 

 

 