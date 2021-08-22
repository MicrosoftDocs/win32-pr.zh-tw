---
description: 安裝程式會提供可操作安裝資料庫中記錄的函式。 這些函數可與使用查詢中所述的函式搭配使用，以在資料庫中進行實際變更。
ms.assetid: 5ea3fb1d-ddcb-4013-84dc-dd6f90c5751a
title: 使用記錄
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12f83159688ec106b8e3cea3021e4352c851620d0e2f89661cee823c1439c120
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119498378"
---
# <a name="working-with-records"></a>使用記錄

安裝程式會提供可操作安裝資料庫中記錄的函式。 這些函數可與 [使用查詢](working-with-queries.md) 中所述的函式搭配使用，以在資料庫中進行實際變更。

下列函數會建立或移除記錄：

-   若要建立資料庫的新記錄，請呼叫 [**MsiCreateRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msicreaterecord) 函數。
-   若要清除記錄中的資料，請呼叫 [**MsiRecordClearData**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordcleardata) 函數，將每個欄位設定為 null。

下列函數會填滿指定的記錄欄位：

-   若要將記錄設定為整數，請呼叫 [**MsiRecordSetInteger**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetinteger) 函數。
-   若要將記錄設定為字串，請呼叫 [**MsiRecordSetString**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstringa) 函數。
-   若要將整個檔案插入資料流程欄位中，請呼叫 [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) 函數。

下列函數會從指定的記錄欄位讀取值：

-   若要從欄位讀取整數值，請呼叫 [**MsiRecordGetInteger**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetinteger) 函數。
-   若要取出字串值，請呼叫 [**MsiRecordGetString**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetstringa) 函數。
-   若要取得資料流程，請呼叫 [**MsiRecordReadStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordreadstream) 函數。
-   若要判斷記錄的特定欄位是否為 null，請呼叫 [**MsiRecordIsNull**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordisnull) 函數。

下列函式是資訊記錄函數：

-   若要取得記錄包含的欄位數目，請呼叫 [**MsiRecordGetFieldCount**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetfieldcount) 函數。
-   若要取得欄位的大小，請呼叫 [**MsiRecordDataSize**](/windows/desktop/api/Msiquery/nf-msiquery-msirecorddatasize) 函數。 **MsiRecordDataSize** 的傳回值是對欄位類型的敏感性。

 

 



