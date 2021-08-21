---
description: 描述在 WQL WHERE 子句中支援使用的日期格式。
ms.assetid: 24d70b7f-681b-4a36-bb67-beaf69f4919f
ms.tgt_platform: multiple
title: WQL-Supported 日期格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0451778d82905b5ec74d4e6feecb62a63ab630d83a9a5db81f2a10a0488b7c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118106972"
---
# <a name="wql-supported-date-formats"></a>WQL-Supported 日期格式

除了 WMI **DATETIME** 格式之外，還支援下列日期格式以用於 WQL **WHERE** 子句。

不同地區設定的顯示時間格式不同。 連接至遠端電腦的腳本必須以適用于目的電腦地區設定的格式來指定時間。

例如，美國日期和時間格式為 MM DD-YYYY。 如果美國電腦上的腳本連接到格式為 DD-YYYY 的地區設定中的目的電腦，則查詢會在目的電腦上處理為 DD MM。 若要避免地區設定之間的不同結果，請使用 [**日期時間**](datetime.md) 格式。 如需詳細資訊，請參閱 [日期和時間格式](date-and-time-format.md)。



<table>
<thead>
<tr class="header">
<th>格式</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>週一 [th] dd [，] [yy] yy</td>
<td>月份 (拼寫出或縮寫為三個字母) 、日、選擇性的逗號，以及兩個或四位數年份。<br/> <dl> 1932年1月21日<br />
32年1月21日<br />
Jan 21 1932<br />
Jan 21 32<br />
</dl></td>
</tr>
<tr class="even">
<td>週一 [th] [，] yyyy</td>
<td>月份 (拼寫出或縮寫為三個字母) 、選擇性逗號和四位數年份。<br/> <dl> 1932年1月<br />
Jan 1932<br />
</dl></td>
</tr>
<tr class="odd">
<td>星期一 [th] [yy] yy dd</td>
<td>月份 (拼寫出或縮寫為三個字母) 、二或四位數年份和日。<br/> <dl> 1932 21 年1月<br />
Jan 32 21<br />
</dl></td>
</tr>
<tr class="even">
<td>dd 週一 [th] [，] [] [yy] yy</td>
<td>月中的日、月 (拼寫出或縮寫為三個字母) 、選擇性的逗號、選擇性的空格，以及兩個或四位數年份。<br/> <dl> 1932年1月21日<br />
21 Jan32<br />
</dl></td>
</tr>
<tr class="odd">
<td>dd [yy] yy 週一 [th]</td>
<td>月份的日期、兩位數或四位數年份，以及月份 (以三個字母) 拼寫或縮寫。<br/> <dl> 21 1932 年1月<br />
</dl></td>
</tr>
<tr class="even">
<td>[yy] yy 週一 [th] dd</td>
<td>兩位數或四位數年份、月份 (拼出或縮寫為三個字母) 和日。<br/> <dl> 1932年1月21日<br />
</dl></td>
</tr>
<tr class="odd">
<td>yyyy 週一 [th]</td>
<td>有兩個或四位數年份和月份 (拼出或縮寫以三個字母為) 。<br/> <dl> 1932 Jan<br />
</dl></td>
</tr>
<tr class="even">
<td>yyyy dd 週一 [th]</td>
<td>有兩個或四位數年份、日和月 (拼出或縮寫以三個字母為) 。<br/> <dl> 1932 21 年1月<br />
</dl></td>
</tr>
<tr class="odd">
<td>MM {/-.}dd {/-.}[yy] yy</td>
<td>月、日和兩位數或四位數年份。 請注意，分隔符號必須相同。<br/></td>
</tr>
<tr class="even">
<td>dd {/-.}MM {/-.}[yy] yy</td>
<td>當月、month 和二或四位數年份的日期。 請注意，分隔符號必須相同。<br/></td>
</tr>
<tr class="odd">
<td>MM {/-.}[yy] yy {/-.}Dd</td>
<td>Month、二或四位數年份和日。 請注意，分隔符號必須相同。<br/></td>
</tr>
<tr class="even">
<td>dd {/-.}[yy] yy {/-.}MM</td>
<td>月份的日期、二或四位數年份和月份。 請注意，分隔符號必須相同。<br/></td>
</tr>
<tr class="odd">
<td>[yy] yy {/-.}dd {/-.}MM</td>
<td>二或四位數年份、日和月。 請注意，分隔符號必須相同。<br/></td>
</tr>
<tr class="even">
<td>[yy] yy {/-.}MM {/-.}Dd</td>
<td>二或四位數年份、月份和日。 請注意，分隔符號必須相同。<br/></td>
</tr>
<tr class="odd">
<td>[yy] yyMMdd</td>
<td>沒有空格的兩個或四位數年份、月份和日。<br/></td>
</tr>
<tr class="even">
<td>yyyy [MM [dd]]</td>
<td>有兩個或四位數年份、選擇性月份和選用日，不含空格。<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[WHERE 子句](where-clause.md)
</dt> </dl>

 

 




