---
title: 稽核
description: Windows篩選 Platform (WFP) 提供防火牆和 IPsec 相關事件的審核。
ms.assetid: 30ff9cf7-bf93-4979-bacd-d76e5dadbef6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 854841685bab015fc0b9a4bc985762df46a7f0c89eae3d38b4b63e081107b70b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015406"
---
# <a name="auditing"></a>稽核

Windows 篩選平台 (WFP) 提供防火牆和 IPsec 相關事件的審核。 這些事件會儲存在系統安全性記錄檔中。

已審核的事件如下所示。



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>審核分類</th>
<th>稽核子類別</th>
<th>已審核的事件</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>原則變更<br/> {6997984D-797A-11D9-BED3-505054503030}<br/></td>
<td>篩選平臺原則變更<br/> {0CCE9233-69AE-11D9-BED3-505054503030}<br/></td>
<td><blockquote>
[!Note]<br />
數位代表事件檢視器 (eventvwr.exe) 所顯示的事件識別碼。
</blockquote>
<br/> 新增和移除 WFP 物件：<br/>
<ul>
<li>5440已新增持續性標注</li>
<li>5441已新增開機時間或持續性篩選</li>
<li>5442持續性提供者已新增</li>
<li>已新增5443持續性提供者內容</li>
<li>5444已新增持續性子層</li>
<li>5446已新增或移除執行時間標注</li>
<li>5447已新增或移除執行時間篩選</li>
<li>5448已新增或移除執行時間提供者</li>
<li>5449已新增或移除執行時間提供者內容</li>
<li>5450已新增或移除的執行時間子圖層</li>
</ul></td>
</tr>
<tr class="even">
<td>物件存取<br/> {6997984A-797A-11D9-BED3-505054503030}<br/></td>
<td>篩選平臺封包捨棄 <br/> {0CCE9225-69AE-11D9-BED3-505054503030}<br/></td>
<td>由 WFP 捨棄的封包：<br/>
<ul>
<li>5152封包已捨棄</li>
<li>5153封包被否決</li>
</ul></td>
</tr>
<tr class="odd">
<td>物件存取<br/></td>
<td>篩選平臺連接 <br/> {0CCE9226-69AE-11D9-BED3-505054503030}<br/></td>
<td>允許和封鎖的連接：<br/>
<ul>
<li>允許5154接聽</li>
<li>5155接聽封鎖</li>
<li>允許的5156連接</li>
<li>5157連接已封鎖</li>
<li>5158允許系結</li>
<li>5159系結已封鎖</li>
</ul>
<blockquote>
[!Note]<br />
允許的連接不一定會審核相關篩選的識別碼。 除非使用下列篩選準則的子集，否則 TCP 的 FilterID 會是0： UserID、AppID、Protocol、Remote Port。
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>物件存取<br/></td>
<td>其他物件存取事件<br/> {0CCE9227-69AE-11D9-BED3-505054503030}<br/></td>
<td><blockquote>
[!Note]<br />
此子類別可進行許多審核。 以下列出 WFP 特定的審核。
</blockquote>
<br/> 拒絕服務防護狀態：<br/>
<ul>
<li>5148 WFP DoS 預防模式已啟動</li>
<li>5149 WFP DoS 防護模式已停止</li>
</ul></td>
</tr>
<tr class="odd">
<td>登入/登出<br/> {69979849-797A-11D9-BED3-505054503030}<br/></td>
<td>IPsec 主要模式<br/> {0CCE9218-69AE-11D9-BED3-505054503030}<br/></td>
<td>IKE 和 AuthIP 主要模式協商：<br/>
<ul>
<li>4650，已建立4651安全性關聯</li>
<li>4652，4653協商失敗</li>
<li>4655安全性關聯已結束</li>
</ul></td>
</tr>
<tr class="even">
<td>登入/登出<br/></td>
<td>IPsec 快速模式 <br/> {0CCE9219-69AE-11D9-BED3-505054503030}<br/></td>
<td>IKE 和 AuthIP 快速模式協商：<br/>
<ul>
<li>已建立5451安全性關聯</li>
<li>5452安全性關聯已結束</li>
<li>4654協商失敗</li>
</ul></td>
</tr>
<tr class="odd">
<td>登入/登出 <br/></td>
<td>IPsec 延伸模式<br/> {0CCE921A-69AE-11D9-BED3-505054503030}<br/></td>
<td>AuthIP 延伸模式的協商：<br/>
<ul>
<li>4978不正確協商封包</li>
<li>已建立4979、4980、4981、4982安全性關聯</li>
<li>4983，4984協商失敗</li>
</ul></td>
</tr>
<tr class="even">
<td>系統<br/> {69979848-797A-11D9-BED3-505054503030}<br/></td>
<td>IPsec 驅動程式<br/> {0CCE9213-69AE-11D9-BED3-505054503030}<br/></td>
<td>IPsec 驅動程式丟棄的封包：<br/>
<ul>
<li>4963已卸載輸入純文字封包</li>
</ul></td>
</tr>
</tbody>
</table>



 

預設會停用 WFP 的審核。

您可以透過群組原則物件編輯器 MMC 嵌入式管理單元、[本機安全性原則] MMC 嵌入式管理單元或 auditpol.exe 命令，針對每個類別啟用審核。

例如，若要啟用原則變更事件的審核，您可能會：

-   使用群組原則物件編輯器

    1.  執行 **gpedit.msc**。
    2.  展開 [本機電腦原則]。
    3.  展開 [電腦設定]。
    4.  展開 \[Windows 設定\]。
    5.  展開 [安全性設定]。
    6.  展開 [本機原則]。
    7.  按一下 [稽核原則]。
    8.  按兩下 [稽核原則變更]，以啟動 [屬性] 對話方塊。
    9.  檢查 [成功] 和 [失敗] 核取方塊。

-   使用本機安全性原則

    1.  執行 **secpol.msc services.msc**。
    2.  展開 [本機原則]。
    3.  按一下 [稽核原則]。
    4.  按兩下 [稽核原則變更]，以啟動 [屬性] 對話方塊。
    5.  檢查 [成功] 和 [失敗] 核取方塊。

-   使用 auditpol.exe 命令

    -   **auditpol/set/category：「原則變更」/success： enable/failure： enable**

只能透過 auditpol.exe 命令以個別子類別為基礎來啟用審核。

審核分類和子類別目錄名稱已當地語系化。 為了避免針對審核腳本進行當地語系化，可能會使用對應的 Guid 來取代名稱。

例如，若要啟用篩選平臺原則變更事件的審核，您可以使用下列其中一個命令：

-   **auditpol/set/subcategory：「篩選平臺原則變更」/success： enable/failure： enable**
-   **auditpol/set/subcategory： "{0CCE9233-69AE-11D9-BED3-505054503030}"/success： enable/failure： enable**

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Auditpol](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc731451(v=ws.11))
</dt> <dt>

[事件記錄檔](/previous-versions/orphan-topics/ws.10/dd996684(v=ws.10))
</dt> <dt>

[群組原則](/windows/deployment/deploy-whats-new)
</dt> </dl>

