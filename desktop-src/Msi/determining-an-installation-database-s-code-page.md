---
description: 若要判斷資料庫的字碼頁，請呼叫 MsiDatabaseExport，並將 hDatabase 設為資料庫的控制碼，並將 szTableName 設定為 \_ ForceCodepage。
ms.assetid: afa3fbd9-9f54-4f72-ab5d-cb0dbbd9946c
title: 判斷安裝資料庫的字碼頁
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89825c99e0652c0ef324c99f8906281f3c87ed58bef099886220faa6a9311583
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118637847"
---
# <a name="determining-an-installation-databases-code-page"></a>判斷安裝資料庫的字碼頁

若要判斷資料庫的字碼頁，請呼叫 [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) ，並將 *hDatabase* 設為資料庫的控制碼，並將 *szTableName* 設定為 \_ ForceCodepage。 這會匯出副檔名為 idt 的文字檔。 這個檔案的前兩行是空白的。 第三行是 ANSI 字碼頁編號，後面接著一個索引標籤，再加上名稱 \_ ForceCodepage。 另請參閱匯 [入和匯出資料表的字碼頁處理](code-page-handling-of-imported-and-exported-tables.md)。

使用 [**Export 方法**](database-export.md)來判斷字碼頁的範例，是在公用程式 WiLangId.vbs 的一部分 Windows Installer SDK 中提供。 如需使用 WiLangId.vbs 的詳細資訊，請參閱主題： [管理語言和字碼頁](manage-language-and-codepage.md)。

 

 



