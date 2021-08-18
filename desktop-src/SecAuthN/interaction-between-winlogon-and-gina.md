---
description: Winlogon 和 GINA 必須傳達初始化資訊、處理安全的注意順序 (SAS) 監視和通知，以及允許登出和關機活動。
ms.assetid: ea45cd5f-9cb0-41bb-99bf-f84781ae9604
title: Winlogon 和 GINA 之間的互動
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 824c658e4f19b14de339b569a8c9d17992c1b60bb5d4d526de949ce76cd1554d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119482358"
---
# <a name="interaction-between-winlogon-and-gina"></a>Winlogon 和 GINA 之間的互動

[*Winlogon*](../secgloss/w-gly.md) 和 [*GINA*](../secgloss/g-gly.md) 必須傳達初始化資訊、處理 [*安全的注意順序*](../secgloss/s-gly.md) (SAS) 監視和通知，以及允許登出和關機活動。 Winlogon 的狀態會決定呼叫哪個 GINA 函式來處理任何指定的 SAS 事件。 通訊的發生順序如下所示。

> [!Note]  
> Windows Vista 會忽略 GINA dll。

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>事件</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>工作站開機</td>
<td><ol>
<li>Winlogon 會呼叫 GINA 的 <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxnegotiate"><strong>WlxNegotiate</strong></a> 函式，以通知有關所使用之 Winlogon 版本的 GINA。</li>
<li>Winlogon 會呼叫 GINA 的 <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxinitialize"><strong>WlxInitialize</strong></a> 函式，為 GINA 提供支援函式的位址、Winlogon 的控制碼，以及取得 GINA (的 <a href="/windows/desktop/SecGloss/c-gly"><em>內容</em></a> 資訊，以便在所有未來的 GINA) 呼叫中使用。<br/> Winlogon 處於已登出狀態。<br/></li>
</ol></td>
</tr>
<tr class="even">
<td>沒有人登入</td>
<td> (GINA 會監視裝置) 的 SAS 事件。
<ol>
<li>收到 SAS 事件時，GINA 會呼叫 Winlogon 的 <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> 函式。</li>
<li>Winlogon 會呼叫 GINA 的 <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas"><strong>WlxLoggedOutSAS</strong></a> 函式，允許 GINA 處理使用者的識別和驗證資訊。<br/> 登入成功時，Winlogon 會處於登入狀態。<br/></li>
</ol></td>
</tr>
<tr class="odd">
<td>使用者已登入</td>
<td> (GINA 會監視裝置) 的 SAS 事件。
<ol>
<li>收到 SAS 事件時，GINA 會呼叫 Winlogon 的 <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> 函式。</li>
<li>Winlogon 會呼叫 GINA 的 <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS</strong></a> 函式，允許 GINA 將選項呈現給目前登入的使用者。</li>
</ol></td>
</tr>
<tr class="even">
<td>使用者已登入並想要鎖定電腦</td>
<td> (GINA 會監視裝置) 的 SAS 事件。
<ol>
<li>GINA 會呼叫 <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> 函數。</li>
<li>Winlogon 會呼叫 GINA 的 <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS</strong></a> 函式。</li>
<li>GINA 會傳回 WLX_SAS_ACTION_LOCK_WKSTA。<br/> Winlogon 處於工作站鎖定狀態。<br/></li>
</ol></td>
</tr>
<tr class="odd">
<td>使用者已登入、工作站已鎖定，且使用者想要解除鎖定電腦</td>
<td> (GINA 會監視裝置) 的 SAS 事件。
<ol>
<li>GINA 會呼叫 <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> 函數。</li>
<li>Winlogon 會呼叫 GINA 的 <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxwkstalockedsas"><strong>WlxWkstaLockedSAS</strong></a> 函式。</li>
<li>GINA 會傳回 WLX_SAS_ACTION_UNLOCK_WKSTA。</li>
</ol></td>
</tr>
<tr class="even">
<td>使用者已登入，而程式呼叫 <a href="/windows/desktop/api/winuser/nf-winuser-exitwindowsex"><strong>ExitWindowsEx</strong></a> 函式</td>
<td>Winlogon 會呼叫 GINA 的 <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff</strong></a> 函式。</td>
</tr>
<tr class="odd">
<td>使用者已登入，而想要使用 SAS 登出</td>
<td> (GINA 會監視裝置) 的 SAS 事件。
<ol>
<li>GINA 會呼叫 <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> 函數。</li>
<li>Winlogon 會呼叫 GINA 的 <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS</strong></a> 函式。</li>
<li>GINA 會傳回 WLX_SAS_ACTION_LOGOFF。</li>
<li>Winlogon 會呼叫 GINA 的 <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff</strong></a> 函式。</li>
</ol></td>
</tr>
<tr class="even">
<td>使用者已登入，並想要使用 ExitWindowsEx 來登出和關閉<a href="/windows/desktop/api/winuser/nf-winuser-exitwindowsex"> <strong></strong></a></td>
<td><ol>
<li>Winlogon 會呼叫 GINA 的 <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff</strong></a> 函式。</li>
<li>Winlogon 會呼叫 GINA 的 <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxshutdown"><strong>WlxShutdown</strong></a> 函式。</li>
</ol></td>
</tr>
<tr class="odd">
<td>使用者已登入，並想要使用 SAS 登出和關閉</td>
<td> (GINA 會監視裝置) 的 SAS 事件。
<ol>
<li>GINA 會呼叫 <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> 函數。</li>
<li>Winlogon 會呼叫 GINA 的 <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS</strong></a> 函式。</li>
<li>GINA 會傳回 WLX_SAS_ACTION_SHUTDOWN。</li>
<li>Winlogon 會呼叫 GINA 的 <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff</strong></a> 函式。</li>
<li>Winlogon 會呼叫 GINA 的 <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxshutdown"><strong>WlxShutdown</strong></a> 函式。</li>
</ol></td>
</tr>
</tbody>
</table>



 

 

 
