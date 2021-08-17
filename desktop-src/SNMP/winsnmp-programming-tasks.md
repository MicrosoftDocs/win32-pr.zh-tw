---
title: WinSNMP 程式設計工作
description: 下表摘要說明您必須執行以編寫 WinSNMP 應用程式程式碼的基本程式設計程式，以及提供這些工作相關資訊的主題。
ms.assetid: 70c24042-bf44-4484-8e5e-d117e2ba28d5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 007ed1a50688ceff7cdd3bfd9916c1726773cf5ecb2e175af99880950c5c3db8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142791"
---
# <a name="winsnmp-programming-tasks"></a>WinSNMP 程式設計工作

下表摘要說明您必須執行以編寫 WinSNMP 應用程式程式碼的基本程式設計程式，以及提供這些工作相關資訊的主題。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>程式設計工作</th>
<th>工作相關的函式和主題</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>開啟 WinSNMP 應用程式。</td>
<td>使用 <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup"><strong>SnmpStartup</strong></a>。 請參閱 <a href="opening-and-closing-a-winsnmp-application.md">開啟和關閉 WinSNMP 應用程式</a>。<br/></td>
</tr>
<tr class="even">
<td>開啟一或多個 WinSNMP 會話。</td>
<td>使用 <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession"><strong>SnmpCreateSession</strong></a>。 請參閱 <a href="opening-and-closing-a-winsnmp-session.md">開啟和關閉 WinSNMP 會話</a>。<br/></td>
</tr>
<tr class="odd">
<td>註冊以接收陷阱或通知。</td>
<td>使用 <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister"><strong>SnmpRegister</strong></a>。 請參閱 <a href="managing-traps-and-notifications.md">管理陷阱和通知</a>。<br/></td>
</tr>
<tr class="even">
<td>建立一或多個變數系結清單，以合併在 PDU 中。</td>
<td>使用 <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl"><strong>SnmpCreateVbl</strong></a>、 <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl"><strong>SnmpDuplicateVbl</strong></a>、 <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetvb"><strong>SnmpSetVb</strong></a>。 請參閱 <a href="working-with-variable-binding-lists.md">使用變數繫結欄位表</a>。<br/>
<blockquote>
[!Note]<br />
應用程式可能需要呼叫其他變數系結 <a href="winsnmp-functions.md">函數</a> ，以建立變數系結清單。
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>建立一或多個用於傳輸和處理的 Pdu。</td>
<td>使用 <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu"><strong>SnmpCreatePDU</strong></a>、 <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata"><strong>SnmpSetPduData</strong></a>、 <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatepdu"><strong>SnmpDuplicatePDU</strong></a>。 請參閱 <a href="working-with-protocol-data-units.md">使用通訊協定資料單位</a>。<br/>
<blockquote>
[!Note]<br />
應用程式可能需要呼叫其他的 <a href="winsnmp-functions.md">pdu 功能</a> 和 WinSNMP <a href="winsnmp-functions.md">公用程式</a> 函式來建立 PDU。
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>提交一或多個 SNMP 操作要求。</td>
<td>使用 <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg"><strong>SnmpSendMsg</strong></a>。 請參閱傳送 <a href="sending-snmp-messages.md">SNMP 訊息</a>。<br/></td>
</tr>
<tr class="odd">
<td>取得 SNMP 作業要求的回應。</td>
<td>使用 <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg"><strong>SnmpRecvMsg</strong></a>。 請參閱 <a href="receiving-snmp-messages.md">接收 SNMP 訊息</a>。<br/></td>
</tr>
<tr class="even">
<td>處理要求回應。</td>
<td>使用應用程式特定邏輯。</td>
</tr>
<tr class="odd">
<td>關閉每個 WinSNMP 會話。</td>
<td>使用 <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose"><strong>SnmpClose</strong></a>。 請參閱 <a href="opening-and-closing-a-winsnmp-session.md">開啟和關閉 WinSNMP 會話</a>。<br/></td>
</tr>
<tr class="even">
<td>關閉 WinSNMP 應用程式。</td>
<td>使用 <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup"><strong>SnmpCleanup</strong></a>。 請參閱 <a href="opening-and-closing-a-winsnmp-application.md">開啟和關閉 WinSNMP 應用程式</a>。<br/></td>
</tr>
</tbody>
</table>



 

下列主題包含有關 WinSNMP 環境特定的其他一般程式設計概念的其他資訊。



| 主題                                                              | 概念                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [一般程式設計工作](general-winsnmp-programming-tasks.md) | [管理物件識別碼](managing-object-identifiers.md)[釋放 WinSNMP 描述](freeing-winsnmp-descriptors.md)項<br/> [設定實體和內容轉譯模式](setting-the-entity-and-context-translation-mode.md)<br/> [管理重新傳輸原則](managing-the-retransmission-policy.md)<br/> [使用多個執行緒撰寫的 WinSNMP 應用程式](writing-winsnmp-applications-with-multiple-threads.md)<br/> [註冊 SNMP 代理程式應用程式](registering-an-snmp-agent-application.md)<br/> |



 

此外，WinSNMP 應用程式可能需要將呼叫併入下列的 WinSNMP 函數： [**SnmpFreeVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl)、 [**SnmpFreeEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity)、 [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor)、 [**SnmpFreeCoNtext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext)和 [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu)。 這可讓 Microsoft WinSNMP 實行釋出 WinSNMP 記憶體物件。 一般來說，當您呼叫 WinSNMP 函式時，必須釋放所有配置的資源。 如需解除配置資源的詳細資訊，請參閱配置 [WinSNMP 記憶體物件](allocating-winsnmp-memory-objects.md)。

 

 





