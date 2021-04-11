---
description: 在電腦升級或電腦對電腦的遷移期間，將會遷移特定憑證存放區中的憑證。
ms.assetid: fe81d578-f2f6-41f0-9ebf-e7bd5532bed9
title: 憑證存放區遷移
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a31b42b83718aa1cab786ad79cc2df754b8fd9b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027241"
---
# <a name="certificate-store-migration"></a>憑證存放區遷移

在電腦升級或電腦對電腦的遷移期間，將會遷移特定憑證存放區中的憑證。 下表列出預設遷移的憑證存放區。 對於系統自動憑證要求設定 (ACR) 存放區，只會遷移 (Ctl) 的 [*憑證信任清單*](../secgloss/c-gly.md) 。 針對以下列出的所有其他存放區，只會遷移憑證。

<table>
<thead>
<tr class="header">
<th>系統/使用者</th>
<th>市集</th>
<th>儲存位置</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>$ {ROWSPAN8} $System $ {REMOVE} $<br />
</td>
<td>ROOT</td>
<td><strong>HKEY_LOCAL_MACHINE</strong> \<strong>軟體</strong> \<strong>Microsoft</strong> \<strong>SystemCertificates</strong> \<strong>根目錄</strong> \<strong>憑證</strong><br/></td>
</tr>
<tr class="even">
<td>MY</td>
<td><strong>HKEY_LOCAL_MACHINE</strong> \<strong>軟體</strong> \<strong>Microsoft</strong> \<strong>SystemCertificates</strong> \<strong>我</strong> \ 的<strong>憑證</strong><br/></td>

</tr>
<tr class="odd">
<td>請求</td>
<td><strong>HKEY_LOCAL_MACHINE</strong> \<strong>軟體</strong> \<strong>Microsoft</strong> \<strong>SystemCertificates</strong> \<strong>要求</strong> \<strong>憑證</strong><br/></td>

</tr>
<tr class="even">
<td>TrustedPublisher</td>
<td><strong>HKEY_LOCAL_MACHINE</strong> \<strong>軟體</strong> \<strong>Microsoft</strong> \<strong>SystemCertificates</strong> \<strong>TrustedPublisher</strong> \<strong>憑證</strong><br/></td>

</tr>
<tr class="odd">
<td>TrustedPeople</td>
<td><strong>HKEY_LOCAL_MACHINE</strong> \<strong>軟體</strong> \<strong>Microsoft</strong> \<strong>SystemCertificates</strong> \<strong>TrustedPeople</strong> \<strong>憑證</strong><br/></td>

</tr>
<tr class="even">
<td>不允許</td>
<td><strong>HKEY_LOCAL_MACHINE</strong> \<strong>軟體</strong> \<strong>Microsoft</strong> \<strong>SystemCertificates</strong> \不<strong>允許</strong> \<strong>憑證</strong><br/></td>

</tr>
<tr class="odd">
<td>CA</td>
<td><strong>HKEY_LOCAL_MACHINE</strong> \<strong>軟體</strong> \<strong>Microsoft</strong> \<strong>SystemCertificates</strong> \<strong>CA</strong> \<strong>憑證</strong><br/></td>

</tr>
<tr class="even">
<td>ACR</td>
<td><strong>HKEY_LOCAL_MACHINE</strong> \<strong>軟體</strong> \<strong>Microsoft</strong> \<strong>SystemCertificates</strong> \<strong>Acr</strong> \<strong>Ctl</strong><br/></td>

</tr>
<tr class="odd">
<td rowspan="7">使用者 $ {REMOVE} $<br />
</td>
<td>ROOT</td>
<td><strong>HKEY_CURRENT_USER</strong> \<strong>軟體</strong> \<strong>Microsoft</strong> \<strong>SystemCertificates</strong> \<strong>根目錄</strong> \<strong>憑證</strong><br/></td>
</tr>
<tr class="even">
<td>MY</td>
<td>file： \\ %APPDATA%\Microsoft\SystemCertificates\My\Certificates</td>

</tr>
<tr class="odd">
<td>請求</td>
<td>file： \\ %APPDATA%\Microsoft\SystemCertificates\Request\Certificates</td>

</tr>
<tr class="even">
<td>TrustedPublisher</td>
<td><strong>HKEY_CURRENT_USER</strong> \<strong>軟體</strong> \<strong>Microsoft</strong> \<strong>SystemCertificates</strong> \<strong>TrustedPublisher</strong> \<strong>憑證</strong><br/></td>

</tr>
<tr class="odd">
<td>TrustedPeople</td>
<td><strong>HKEY_CURRENT_USER</strong> \<strong>軟體</strong> \<strong>Microsoft</strong> \<strong>SystemCertificates</strong> \<strong>TrustedPeople</strong> \<strong>憑證</strong><br/></td>

</tr>
<tr class="even">
<td>不允許</td>
<td><strong>HKEY_CURRENT_USER</strong> \<strong>軟體</strong> \<strong>Microsoft</strong> \<strong>SystemCertificates</strong> \不<strong>允許</strong> \<strong>憑證</strong><br/></td>

</tr>
<tr class="odd">
<td>CA</td>
<td><strong>HKEY_CURRENT_USER</strong> \<strong>軟體</strong> \<strong>Microsoft</strong> \<strong>SystemCertificates</strong> \<strong>CA</strong> \<strong>憑證</strong><br/></td>

</tr>
</tbody>
</table>



 

依預設，應用程式所建立的其他憑證存放區不會遷移。 建立自己的存放區的應用程式會負責遷移其所建立的存放區。 若要建立存放區，建議您在應用程式設定中定義登錄機碼，並使用 **CERT \_ store \_ >prov \_ REG** 存放區提供者在登錄設定中建立存放區。 如需有關遷移應用程式設定的詳細資訊，請參閱 *使用 USMT 3.0* 指南中的 *如何建立自訂 .xml* 檔案主題 [消費者狀態移轉工具 3.0](https://www.microsoft.com/technet/windowsvista/library/91f62fc4-621f-4537-b311-1307df010561.mspx)。  (此資源可能無法在某些語言及國家或地區使用。 ) 

 

 
