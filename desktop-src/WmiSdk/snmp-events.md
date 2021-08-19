---
description: SNMP 提供者支援寫入至記錄檔和偵錯工具。
ms.assetid: 66627927-2eee-4d56-a74b-f86147ad7711
ms.tgt_platform: multiple
title: SNMP 事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 925ce6bb5eca0a3c067470255296ba6c9f66c0183b2b74aa6cfa4a25824446d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118816644"
---
# <a name="snmp-events"></a>SNMP 事件

SNMP 提供者支援寫入至記錄檔和偵錯工具。

> [!Note]  
> 如需安裝提供者的詳細資訊，請參閱 [設定 WMI SNMP 環境](setting-up-the-wmi-snmp-environment.md)。

 

有幾個登錄機碼和值會定義目前產生的記錄層級和類型：

-   偵錯

    **HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ MICROSOFT \\ WBEM \\ 提供者 \\ 記錄登錄** 機碼包含記錄值，指出是否可以將資訊寫入至偵錯工具。 記錄值會設定為0以停用偵錯工具輸出，或設定為1來啟用它。 記錄是 REG \_ DWORD 值。

-   記錄

    **HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ MICROSOFT \\ WBEM 提供者 \\ \\ 記錄 \\ WBEMSNMP 登錄** 機碼會保存 SNMP 提供者特定的所有記錄資訊。 下表列出與此索引鍵相關聯的值。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>值</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>類型</td>
<td><strong>REG_SZ</strong><br/> 採用下列其中一個值：<br/> &quot;File &quot; = (預設) 將偵測輸出傳送至檔案。<br/> &quot;偵錯工具 &quot; = 將偵測輸出傳送至偵錯工具。<br/></td>
</tr>
<tr class="even">
<td>MaxFileSize</td>
<td><strong>REG_DWORD</strong><br/> 接受從1024到 2 ^ 32-1 的整數值。 此值是記錄檔允許的最大大小（以位元組為單位）。 如果小於1024，記錄機制會使用值1024。 針對此值，建議使用大小下限為 8 KB。 當檔案到達 MaxFileSize 所指定的大小時，檔案名前面會加上 ' ~ ' 字元，並會建立新的檔案。 因此，記錄所需的最大磁碟空間是此值的兩倍。<br/></td>
</tr>
<tr class="odd">
<td>檔案</td>
<td><strong>REG_SZ</strong><br/> 定義當記錄類型設定為 ' File ' 時，要將偵錯工具輸出傳送至其中的檔案名。 預設值為 ' <WBEMLOGS> \wbemsnmp.log. ' 如果 <WBEMLOGS> 無法從 WMI 登錄區段判斷目錄，此值會預設為 ' c:\wbemsnmp.log '。 如果使用共用（例如 \\ machine\share\wbemsnmp.log 或 M:\wbemsnmp.log，其中 M： \\ machine\share），則執行 WMI 的本機系統帳戶必須具有 machine\share. 的讀取/寫入存取權限。 \\<br/></td>
</tr>
<tr class="even">
<td>層級</td>
<td><strong>REG_DWORD</strong><br/> 接受從0到 2 ^ 32-1 的整數值。 值是包含32位的邏輯遮罩。 下列位元遮罩會合並，以定義產生的偵錯工具輸出類型：<br/>
<ul>
<li>0： SNMP 類別提供者 <a href="/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices"><strong>IWbemServices</strong></a> 方法調用</li>
<li>1： SNMP 類別提供者的執行</li>
<li>2： SNMP 執行個體提供者 <a href="/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices"><strong>IWbemServices</strong></a> 方法調用</li>
<li>3： SNMP 執行個體提供者的執行</li>
<li>4： SNMP 類別庫</li>
<li>5： SNMP SMIR</li>
<li>6： SNMP 交互碼</li>
<li>7： SNMP 類型對應程式碼</li>
<li>8： SNMP 執行緒程式碼</li>
<li>9： SNMP 事件提供者介面和實作為</li>
</ul>
將層級設定為 (2 ^ 0 + 2 ^ 8 =) 257 適用于涉及 SNMP 類別提供者 <a href="/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices"><strong>IWbemServices</strong></a> 方法呼叫的作業，以及使用 snmp 執行緒程式碼的作業。<br/></td>
</tr>
</tbody>
</table>



 

 

 




