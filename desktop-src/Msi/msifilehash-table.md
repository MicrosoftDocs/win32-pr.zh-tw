---
description: MsiFileHash 資料表是用來儲存 Windows Installer 封裝所提供之原始程式檔的128位雜湊。 雜湊會分割成 4 32 位值，並儲存在資料表的個別資料行中。
ms.assetid: 972a2784-418d-4cb3-b13c-df89b079e94c
title: MsiFileHash 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fc43c7fd812781057ec0be271ffc370a6b5eb2e3054926e1f969383c0fb390c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118944945"
---
# <a name="msifilehash-table"></a>MsiFileHash 資料表

**MsiFileHash** 資料表是用來儲存 Windows Installer 封裝所提供之原始程式檔的128位雜湊。 雜湊會分割成 4 32 位值，並儲存在資料表的個別資料行中。

Windows安裝程式可以使用檔案雜湊來偵測和消除不必要的檔案複製。 儲存在 **MsiFileHash** 資料表中的檔案雜湊，可能會與使用者電腦上呼叫 [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha)所取得的現有檔案雜湊進行比較。 **MsiFileHash** 資料表只能搭配未建立版本檔使用。

**MsiFileHash** 資料表具有下列資料行。



| Column    | 類型                               | 答案 | Nullable |
|-----------|------------------------------------|-----|----------|
| 檔案\_    | [識別碼](identifier.md)       | Y   | N        |
| 選項   | [整數](integer.md)             | N   | N        |
| HashPart1 | [DoubleInteger](doubleinteger.md) | N   | N        |
| HashPart2 | [DoubleInteger](doubleinteger.md) | N   | N        |
| HashPart3 | [DoubleInteger](doubleinteger.md) | N   | N        |
| Hashpart4 | [DoubleInteger](doubleinteger.md) | N   | N        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>檔\_
</dt> <dd>

檔案 [資料表](file-table.md)的外鍵。 72字元字串。

</dd> <dt>

<span id="Options"></span><span id="options"></span><span id="OPTIONS"></span>選項
</dt> <dd>

此資料行必須是0，並保留供日後使用。

</dd> <dt>

<span id="HashPart1"></span><span id="hashpart1"></span><span id="HASHPART1"></span>HashPart1
</dt> <dd>

第一個32位的雜湊。 您必須藉由呼叫 [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) 或 [**get-filehash 方法**](installer-filehash.md)來取得此欄位中輸入的檔案雜湊。 請勿使用其他方法。

</dd> <dt>

<span id="HashPart2"></span><span id="hashpart2"></span><span id="HASHPART2"></span>HashPart2
</dt> <dd>

第二個32位的雜湊。 您必須藉由呼叫 [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) 或 [**get-filehash 方法**](installer-filehash.md)來取得此欄位中輸入的檔案雜湊。 請勿使用其他雜湊方法。

</dd> <dt>

<span id="HashPart3"></span><span id="hashpart3"></span><span id="HASHPART3"></span>HashPart3
</dt> <dd>

第三個32位的雜湊。 您必須藉由呼叫 [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) 或 [**get-filehash 方法**](installer-filehash.md)來取得此欄位中輸入的檔案雜湊。 請勿使用其他方法。

</dd> <dt>

<span id="HashPart4"></span><span id="hashpart4"></span><span id="HASHPART4"></span>HashPart4
</dt> <dd>

第四個32位的雜湊。 您必須藉由呼叫 [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) 或 [**get-filehash 方法**](installer-filehash.md)來取得此欄位中輸入的檔案雜湊。 請勿使用其他方法。

</dd> </dl>

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE60](ice60.md)  
[ICE66](ice66.md)  
</dl>

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha)
</dt> <dt>

[預設檔案版本控制](default-file-versioning.md)
</dt> </dl>

 

 



