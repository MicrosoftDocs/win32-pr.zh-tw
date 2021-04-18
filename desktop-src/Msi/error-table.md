---
description: 錯誤資料表是用來在處理錯誤時，用來查閱錯誤訊息格式範本，但如果沒有設定格式化範本， (這是) 的一般情況。
ms.assetid: 3c817468-cba7-46bf-9208-5e6699c02fb6
title: 錯誤資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cfcba5f68eb48621891c7a48aeedea2329996f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193114"
---
# <a name="error-table"></a>錯誤資料表

錯誤資料表是用來在處理錯誤時，用來查閱錯誤訊息格式範本，但如果沒有設定格式化範本， (這是) 的一般情況。

錯誤資料表具有下列資料行。



| Column  | 類型                     | 答案 | Nullable |
|---------|--------------------------|-----|----------|
| 錯誤   | [整數](integer.md)   | Y   | N        |
| 訊息 | [範本](template.md) | N   | Y        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>錯誤
</dt> <dd>

請參閱 [Windows Installer 錯誤訊息](windows-installer-error-messages.md) ，以取得錯誤號碼和訊息的清單。

錯誤號碼必須是非負整數。

從25000到30000的範圍會保留給自訂動作的錯誤。 自訂動作的作者可將此範圍用於其自訂動作。

</dd> <dt>

<span id="Message"></span><span id="message"></span><span id="MESSAGE"></span>消息
</dt> <dd>

此資料行包含可當地語系化的錯誤格式設定範本。 錯誤資料表是由初始組建進程產生，以包含 debug 格式範本。

下表列出保留的訊息。 如需出貨和內部錯誤碼的清單，請參閱 [Windows Installer 錯誤訊息](windows-installer-error-messages.md)。



| 錯誤 | 訊息                                                    | 備註                                                                                                                                                                                                      |
|-------|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | {{嚴重錯誤：}}                                          | 嚴重錯誤的標頭前置詞 (INSTALLMESSAGE \_ FATALEXIT) 。 以雙大括弧 {{text}} 括住的文字只會顯示在記錄檔中。 在 UI 中不會向使用者顯示文字。                  |
| 1     | 錯誤 \[ 1 \] 。                                               | 錯誤的標頭前置詞 (INSTALLMESSAGE \_ ERROR)                                                                                                                                                              |
| 2     | 警告 \[ 1 \] 。                                             | 警告的標頭前置詞 (INSTALLMESSAGE \_ 警告)                                                                                                                                                          |
| 3     |                                                            |                                                                                                                                                                                                              |
| 4     | 資訊 \[ 1 \] 。                                                | 參考用訊息的標頭前置詞 (INSTALLMESSAGE \_ 資訊)                                                                                                                                               |
| 5     | 內部錯誤 \[ 1 \] 。 \[2 \] {， \[ 3 \] } {， \[ 4 \] }              | 內部錯誤的標頭前置詞                                                                                                                                                                            |
| 6     |                                                            |                                                                                                                                                                                                              |
| 7     | {{磁片已滿：}}                                            | 磁碟空間不足錯誤的標頭前置詞 (INSTALLMESSAGE \_ OUTOFDISKSPACE) 。 以雙大括弧 {{text}} 括住的文字只會顯示在記錄檔中。 在 UI 中不會向使用者顯示文字。 |
| 8     | 動作 \[ 時間 \] ： \[ 1 \] 。 \[2\]                              |                                                                                                                                                                                                              |
| 9     | \[ProductName\]                                            |                                                                                                                                                                                                              |
| 10    | { \[ 2 \] } {， \[ 3 \] } {， \[ 4 \] }                                  |                                                                                                                                                                                                              |
| 11    | 訊息類型： \[ 1 \] ，引數： \[ 2\]                       |                                                                                                                                                                                                              |
| 12    | = = = 記錄已開始： \[ 日期 \] \[ 時間\] ===                 |                                                                                                                                                                                                              |
| 13    | = = = 記錄已停止： \[ 日期 \] \[ 時間\] ===                 |                                                                                                                                                                                                              |
| 14    | 動作開始 \[ 時間 \] ： \[ 1\]                               |                                                                                                                                                                                                              |
| 15    | 動作結束 \[ 時間 \] ： \[ 1 \] 。 傳回值 \[ 2\]           |                                                                                                                                                                                                              |
| 16    | 剩餘時間： { \[ 1 \] 分鐘} { \[ 2 \] 秒}                    |                                                                                                                                                                                                              |
| 17    | 記憶體不足。 在重試之前關閉其他應用程式 |                                                                                                                                                                                                              |
| 18    | 安裝程式不再回應                          |                                                                                                                                                                                                              |
| 19    | 安裝程式提前終止                           |                                                                                                                                                                                                              |
| 20    | Windows 正在設定 ProductName，請稍候 ... \[ \]    |                                                                                                                                                                                                              |
| 21    | 正在收集必要資訊 .。。                          |                                                                                                                                                                                                              |
| 22    | 正在移除此應用程式的舊版本 .。。             |                                                                                                                                                                                                              |
| 23    | 正在準備移除此應用程式的舊版本 .。。  |                                                                                                                                                                                                              |
| 32    | { \[ ProductName \] } 安裝程式已順利完成。            |                                                                                                                                                                                                              |
| 33    | { \[ ProductName \] } 安裝程式失敗。                            |                                                                                                                                                                                                              |



 

</dd> </dl>

## <a name="remarks"></a>備註

範本不包含欄位1中錯誤號碼的格式設定。 處理錯誤時，安裝程式會根據訊息類型，將標頭前置詞附加至範本。 這些標頭也會儲存在錯誤資料表中。

以雙大括弧 {{text}} 括住的文字只會顯示在記錄檔中。 在 UI 中不會向使用者顯示文字。

您可以使用 Msidb.exe 或 [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)，將當地語系化的錯誤資料表匯入資料庫中。 SDK 針對「 [當地語系化錯誤和 ActionText 資料表](localizing-the-error-and-actiontext-tables.md) 」一節中所列的每一種語言，包含當地語系化的錯誤資料表。 如果未填入錯誤資料表，安裝程式會針對 [**ProductLanguage**](productlanguage.md) 屬性所指定的語言載入當地語系化的字串。

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE40](ice40.md)  
[ICE46](ice46.md)  
</dl>

 

 



