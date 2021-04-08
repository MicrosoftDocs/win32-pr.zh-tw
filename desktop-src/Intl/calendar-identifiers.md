---
description: 本主題定義 (資料類型 CALID) 的行事曆識別碼，用來指定不同的行事曆。
ms.assetid: ba2e841e-e24e-476a-851e-a29b3af4f04d
title: 行事曆識別碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab9b931aea4a186af0849dfe8f6642c53744d364
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690255"
---
# <a name="calendar-identifiers"></a>行事曆識別碼

本主題定義 (資料類型 CALID) 的行事曆識別碼，用來指定不同的行事曆。 當您使用下列 NLS 函數和回呼函式時，您的應用程式可以使用這些識別碼，這些函數具有採用 CALID 資料類型的參數：

-   [**ConvertSystemTimeToCalDateTime**](convertsystemtimetocaldatetime.md)
-   [**EnumCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoa)
-   [**EnumCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexa)
-   [**EnumCalendarInfoExEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexex)
-   [**EnumCalendarInfoProcEx**](/previous-versions/windows/desktop/legacy/dd317807(v=vs.85))
-   [**EnumDateFormatsProcEx**](/previous-versions/windows/desktop/legacy/dd317814(v=vs.85))
-   [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa)
-   [**GetCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoex)
-   [**GetCalendarSupportedDateRange**](getcalendarsupporteddaterange.md)
-   [**IsCalendarLeapYear**](iscalendarleapyear.md)
-   [**SetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-setcalendarinfoa)

以下是定義的值。 所有其他值都是保留的。 這些值無法彼此結合。



行事曆識別碼

意義

1

CAL \_ 西曆

西曆 (當地語系化) 

2

CAL \_ \_ 美國西曆

西曆 (的英文字串一律) 

3

CAL \_ 日本

日文天皇紀元

4

CAL \_ 臺灣

臺灣日曆

5

CAL \_ 韓國

韓文 Tangun 紀元

6

CAL \_ 回曆

阿拉伯 (阿拉伯陰曆) 

7

CAL \_ 泰文

泰文

8

CAL \_ 希伯來文

希伯來文 (陰曆) 

9

CAL \_ 西曆 \_ （ \_ 法文）

Gregorian Middle East French

10

CAL \_ 西曆 \_ 阿拉伯

Gregorian Arabic

11

CAL \_ 西曆 \_ XLIT \_ 英文

西曆（英文）

12

CAL \_ 西曆 \_ XLIT \_ 法文

西曆（法文）

23

CAL \_ UMALQURA

**Windows Vista 和更新版本：** (阿拉伯文陰曆) 行事曆的 Um Al



 

> [!Note]  
> 識別碼 CAL \_ 西曆 \_ XLIT \_ 法文和 CAL UMALQURA 之間的編號間隔是刻意的 \_ 。 CAL UMALQURA 的指示項 \_ 是23，不是13。

 

此外， [**EnumCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoa) 和 [**EnumCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexa) 可讓您使用值列舉所有行事 \_ \_ 歷來要求所有適用行事曆的列舉。

值

意義

0xffffffff

列舉 \_ 所有行事 \_ 曆

所有適用于指定地區設定的行事曆



 

 

 
