---
description: 下表顯示摘要資訊資料流程屬性集，其中包含屬性、其對應的屬性識別碼、Pid 和類型。
ms.assetid: a5dd014f-21af-41f9-be75-1b139946179d
title: 摘要資訊資料流程屬性集
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d41439e15a59ca1942fcbb49c06067251060935b165d6a34972df868fa7feac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119627048"
---
# <a name="summary-information-stream-property-set"></a>摘要資訊資料流程屬性集

下表顯示摘要資訊資料流程屬性集，其中包含屬性、其對應的屬性識別碼、Pid 和類型。 如需安裝程式如何使用這些屬性的詳細資訊，請參閱 [摘要屬性描述](summary-property-descriptions.md)。 如需有關用來設定摘要資訊屬性之視窗安裝程式函數的詳細資訊，請參閱 [使用摘要資訊資料流程](using-the-summary-information-stream.md)。



| 屬性名稱                                                | 屬性識別碼        | PID | 類型         |
|--------------------------------------------------------------|--------------------|-----|--------------|
| [**字碼頁**](codepage-summary.md)                         | PID \_ 字碼頁      | 1   | VT \_ I2       |
| [**標題**](title-summary.md)                               | PID \_ 標題         | 2   | VT \_ LPSTR    |
| [**主體**](subject-summary.md)                           | PID \_ 主體       | 3   | VT \_ LPSTR    |
| [**作者**](author-summary.md)                             | PID \_ 作者        | 4   | VT \_ LPSTR    |
| [**關鍵字**](keywords-summary.md)                         | PID \_ 關鍵字      | 5   | VT \_ LPSTR    |
| [**註解**](comments-summary.md)                         | PID \_ 批註      | 6   | VT \_ LPSTR    |
| [**範本**](template-summary.md)                         | PID \_ 範本      | 7   | VT \_ LPSTR    |
| [**上次儲存者**](last-saved-by-summary.md)               | PID \_ LASTAUTHOR    | 8   | VT \_ LPSTR    |
| [**修訂編號**](revision-number-summary.md)           | PID \_ REVNUMBER     | 9   | VT \_ LPSTR    |
| [**前次列印時間**](last-printed-summary.md)                 | PID \_ LASTPRINTED   | 11  | VT \_ FILETIME |
| [**建立時間/日期**](create-time-date-summary.md)         | PID \_ 建立 \_ DTM   | 12  | VT \_ FILETIME |
| [**上次儲存時間/日期**](last-saved-time-date-summary.md)  | PID \_ LASTSAVE \_ DTM | 13  | VT \_ FILETIME |
| [**頁面計數**](page-count-summary.md)                     | PID \_ PAGECOUNT     | 14  | VT \_ I4       |
| [**字數統計**](word-count-summary.md)                     | PID \_ WORDCOUNT     | 15  | VT \_ I4       |
| [**字元計數**](character-count-summary.md)           | PID \_ >CHARCOUNT     | 16  | VT \_ I4       |
| [**正在建立應用程式**](creating-application-summary.md) | PID \_ APPNAME       | 18  | VT \_ LPSTR    |
| [**安全性**](security-summary.md)                         | PID \_ 安全性      | 19  | VT \_ I4       |



 

安裝程式目前會為安裝套件、轉換和修補套件維護三種儲存格式。 儲存體的 CLSID 會設定為特定格式的適當格式類別，與儲存體的摘要資訊無關。

 

 



