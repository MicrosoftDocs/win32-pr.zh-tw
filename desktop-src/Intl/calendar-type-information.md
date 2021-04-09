---
description: 本主題描述 EnumCalendarInfo、EnumCalendarInfoEx、EnumCalendarInfoExEx、GetCalendarInfo 和 GetCalendarInfoEx 函式中所使用 (CALTYPE 資料類型) 的行事曆類型資訊。
ms.assetid: 33361a97-0f27-477a-a0ee-3d4d3aaeaacf
title: 行事曆類型資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17a8e334a1b05f372f51c81ab8158294d46eebfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851831"
---
# <a name="calendar-type-information"></a>行事曆類型資訊

本主題描述 [**EnumCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoa)、 [**EnumCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexa)、 [**EnumCalendarInfoExEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexex)、 [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa)和 [**GetCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoex) 函式中所使用 (CALTYPE 資料類型) 的行事曆類型資訊。 [**SetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-setcalendarinfoa)函式也會使用其中的一些值。

下列 CALTYPE 常數可以與任何其他 CALTYPE 常數一起使用。



| 常數                     | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CAL \_ NOUSEROVERRIDE          | **Windows Me/98、windows 2000：** 使用系統預設值，而不是使用者的選擇。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| CAL \_ 傳回 \_ 所有格 \_ 名稱 | **Windows 7 和更新版本：** 以每月的所有格名稱形式取出 [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa) 的結果，這是月份名稱與其他專案合併時所使用的名稱。 例如，在「烏克蘭」中，當月份單獨命名時，1月的對等專案會寫入「Січень」。 不過，當月份名稱用於組合時（例如，在2003年1月5日的日期）中，會使用名稱的所有格形式。 針對烏克蘭範例，所有格月份名稱會顯示為 "5 січня 2003"。 如需詳細資訊，請參閱 [LOCALE 傳回 \_ 所屬的 \_ \_ 名稱](locale-return-constants.md)。 |
| CAL \_ 傳回 \_ 編號          | **Windows Me/98、windows 2000：** 以數位而非字串形式取出 [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa) 的結果。 這僅適用于從 CAL I 開始的值 \_ 。                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| CAL \_ 使用 \_ CP \_ ACP            | **Windows Me/98、windows 2000：** 使用系統 ANSI 字碼頁 (ACP) ，而不是字串轉譯的地區設定字碼頁。 這僅適用于 ANSI 版本的函式，例如 **EnumCalendarInfoA**。                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

下列 CALTYPE 常數是互斥的，無法在函式呼叫中彼此組合使用。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>常數</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>CAL_ICALINTVALUE</td>
<td>整數值，表示替代日曆的行事曆類型。</td>
</tr>
<tr class="even">
<td>CAL_ITWODIGITYEARMAX</td>
<td><strong>Windows Me/98、windows 2000：</strong> 整數值，指出兩位數年份範圍的上限。</td>
</tr>
<tr class="odd">
<td>CAL_IYEAROFFSETRANGE</td>
<td>一或多個以 null 終止的字串，指定每個紀元範圍的年份位移。 最後一個字串有額外的終止 null 字元。 此值的格式會視選用行事曆的類型而有所不同。</td>
</tr>
<tr class="even">
<td>CAL_SABBREVDAYNAME1</td>
<td>一周第一天的縮寫原生名稱。</td>
</tr>
<tr class="odd">
<td>CAL_SABBREVDAYNAME2</td>
<td>一周中第二天的縮寫原生名稱。</td>
</tr>
<tr class="even">
<td>CAL_SABBREVDAYNAME3</td>
<td>一周第三天的縮寫原生名稱。</td>
</tr>
<tr class="odd">
<td>CAL_SABBREVDAYNAME4</td>
<td>一周第四天的縮寫原生名稱。</td>
</tr>
<tr class="even">
<td>CAL_SABBREVDAYNAME5</td>
<td>一周第五天的縮寫原生名稱。</td>
</tr>
<tr class="odd">
<td>CAL_SABBREVDAYNAME6</td>
<td>一周第六天的縮寫原生名稱。</td>
</tr>
<tr class="even">
<td>CAL_SABBREVDAYNAME7</td>
<td>一周第七天的縮寫原生名稱。</td>
</tr>
<tr class="odd">
<td>CAL_SABBREVERASTRING</td>
<td><strong>Windows 7 和更新版本：</strong> 紀元的縮寫原生名稱。 完整的紀元是由 CAL_SERASTRING 常數表示。</td>
</tr>
<tr class="even">
<td>CAL_SABBREVMONTHNAME1</td>
<td>年度第一個月的縮寫原生名稱。</td>
</tr>
<tr class="odd">
<td>CAL_SABBREVMONTHNAME2</td>
<td>年度第二個月的縮寫原生名稱。</td>
</tr>
<tr class="even">
<td>CAL_SABBREVMONTHNAME3</td>
<td>年度第三個月的縮寫原生名稱。</td>
</tr>
<tr class="odd">
<td>CAL_SABBREVMONTHNAME4</td>
<td>年度第四個月的縮寫原生名稱。</td>
</tr>
<tr class="even">
<td>CAL_SABBREVMONTHNAME5</td>
<td>年度第五個月的縮寫原生名稱。</td>
</tr>
<tr class="odd">
<td>CAL_SABBREVMONTHNAME6</td>
<td>年度第六個月的縮寫原生名稱。</td>
</tr>
<tr class="even">
<td>CAL_SABBREVMONTHNAME7</td>
<td>年度第七個月的縮寫原生名稱。</td>
</tr>
<tr class="odd">
<td>CAL_SABBREVMONTHNAME8</td>
<td>年度第八個月的縮寫原生名稱。</td>
</tr>
<tr class="even">
<td>CAL_SABBREVMONTHNAME9</td>
<td>年度第九個月的縮寫原生名稱。</td>
</tr>
<tr class="odd">
<td>CAL_SABBREVMONTHNAME10</td>
<td>年度第十個月的縮寫原生名稱。</td>
</tr>
<tr class="even">
<td>CAL_SABBREVMONTHNAME11</td>
<td>年度第十個月的縮寫原生名稱。</td>
</tr>
<tr class="odd">
<td>CAL_SABBREVMONTHNAME12</td>
<td>年度第十二個月的縮寫原生名稱。</td>
</tr>
<tr class="even">
<td>CAL_SABBREVMONTHNAME13</td>
<td>年度第十三個月的縮寫原生名稱（如果有的話）。</td>
</tr>
<tr class="odd">
<td>CAL_SCALNAME</td>
<td>替代行事曆的原生名稱。</td>
</tr>
<tr class="even">
<td>CAL_SDAYNAME1</td>
<td>一周第一天的原生名稱。</td>
</tr>
<tr class="odd">
<td>CAL_SDAYNAME2</td>
<td>一周中第二天的原生名稱。</td>
</tr>
<tr class="even">
<td>CAL_SDAYNAME3</td>
<td>一周第三天的原生名稱。</td>
</tr>
<tr class="odd">
<td>CAL_SDAYNAME4</td>
<td>一周第四天的原生名稱。</td>
</tr>
<tr class="even">
<td>CAL_SDAYNAME5</td>
<td>一周第五天的原生名稱。</td>
</tr>
<tr class="odd">
<td>CAL_SDAYNAME6</td>
<td>一周第六天的原生名稱。</td>
</tr>
<tr class="even">
<td>CAL_SDAYNAME7</td>
<td>一周第七天的原生名稱。</td>
</tr>
<tr class="odd">
<td>CAL_SERASTRING</td>
<td>一或多個以 null 終止的字串，指定每個 Unicode 程式碼點，指定與 CAL_IYEAROFFSETRANGE 相關聯的紀元。 最後一個字串有額外的終止 null 字元。 此值的格式會視選用行事曆的類型而有所不同。</td>
</tr>
<tr class="even">
<td>CAL_SLONGDATE</td>
<td>行事曆類型的完整日期格式。</td>
</tr>
<tr class="odd">
<td>CAL_SMONTHDAY</td>
<td><strong>Windows 7 和更新版本：</strong> 行事曆類型的月份和日期格式。 格式與 CAL_SLONGDATE 的格式類似。 例如，如果月/日模式是完整月份名稱，後面加上前置零的日號，例如 &quot; 9 月 3 &quot; 日，則格式為 &quot; MMMM dd &quot; 。 單引號可以用來插入非格式的字元，例如，以西班牙文表示的「de」。
<blockquote>
[!Note]<br />
這個行事曆類型只支援一種格式。
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>CAL_SMONTHNAME1</td>
<td>年度第一個月的原生名稱。</td>
</tr>
<tr class="odd">
<td>CAL_SMONTHNAME2</td>
<td>年度第二個月的原生名稱。</td>
</tr>
<tr class="even">
<td>CAL_SMONTHNAME3</td>
<td>年度第三個月的原生名稱。</td>
</tr>
<tr class="odd">
<td>CAL_SMONTHNAME4</td>
<td>年度第四個月的原生名稱。</td>
</tr>
<tr class="even">
<td>CAL_SMONTHNAME5</td>
<td>年度第五個月的原生名稱。</td>
</tr>
<tr class="odd">
<td>CAL_SMONTHNAME6</td>
<td>年度第六個月的原生名稱。</td>
</tr>
<tr class="even">
<td>CAL_SMONTHNAME7</td>
<td>年度第七個月的原生名稱。</td>
</tr>
<tr class="odd">
<td>CAL_SMONTHNAME8</td>
<td>年度第八個月的原生名稱。</td>
</tr>
<tr class="even">
<td>CAL_SMONTHNAME9</td>
<td>年度第九個月的原生名稱。</td>
</tr>
<tr class="odd">
<td>CAL_SMONTHNAME10</td>
<td>年度第十個月的原生名稱。</td>
</tr>
<tr class="even">
<td>CAL_SMONTHNAME11</td>
<td>年度第十個月的原生名稱。</td>
</tr>
<tr class="odd">
<td>CAL_SMONTHNAME12</td>
<td>年度第十二個月的原生名稱。</td>
</tr>
<tr class="even">
<td>CAL_SMONTHNAME13</td>
<td>年度第十三個月的原生名稱（如果有的話）。</td>
</tr>
<tr class="odd">
<td>CAL_SSHORTDATE</td>
<td>行事曆類型的簡短日期格式。</td>
</tr>
<tr class="even">
<td>CAL_SSHORTESTDAYNAME1</td>
<td><strong>Windows Vista 和更新版本：</strong> 一周第一天的簡短原生名稱。</td>
</tr>
<tr class="odd">
<td>CAL_SSHORTESTDAYNAME2</td>
<td><strong>Windows Vista 和更新版本：</strong> 一周中第二天的簡短原生名稱。</td>
</tr>
<tr class="even">
<td>CAL_SSHORTESTDAYNAME3</td>
<td><strong>Windows Vista 和更新版本：</strong> 一周第三天的簡短原生名稱。</td>
</tr>
<tr class="odd">
<td>CAL_SSHORTESTDAYNAME4</td>
<td><strong>Windows Vista 和更新版本：</strong> 一周第四天的簡短原生名稱。</td>
</tr>
<tr class="even">
<td>CAL_SSHORTESTDAYNAME5</td>
<td><strong>Windows Vista 和更新版本：</strong> 一周第五天的簡短原生名稱。</td>
</tr>
<tr class="odd">
<td>CAL_SSHORTESTDAYNAME6</td>
<td><strong>Windows Vista 和更新版本：</strong> 一周第六天的簡短原生名稱。</td>
</tr>
<tr class="even">
<td>CAL_SSHORTESTDAYNAME7</td>
<td><strong>Windows Vista 和更新版本：</strong> 一周第七天的簡短原生名稱。</td>
</tr>
<tr class="odd">
<td>CAL_SYEARMONTH</td>
<td><strong>Windows Me/98、windows 2000：</strong> 指定行事曆的年/月格式。</td>
</tr>
</tbody>
</table>



 

> [!Note]  
> 如果一周或某個月份的原生名稱是空字串，則該名稱與對應地區設定資訊中指定的名稱相同，因此不會在此處重複。

 

 

 




