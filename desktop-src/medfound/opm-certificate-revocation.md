---
description: .
ms.assetid: 21faf809-1335-4d93-be06-628c5a05a4c8
title: OPM 憑證撤銷
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e4b20dc00b0bd23644ef9dca22558a304ca9438
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512588"
---
# <a name="opm-certificate-revocation"></a>OPM 憑證撤銷

OPM) 憑證的輸出保護管理員 (可由 Microsoft 撤銷。 撤銷的憑證清單會儲存在全域撤銷清單中， (GRL) 。 GRL 的格式如下：



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>區段</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>標頭</td>
<td><a href="grl-header.md"><strong>GRL_HEADER</strong></a>結構。</td>
</tr>
<tr class="even">
<td>核心</td>
<td>包含下列撤銷清單：
<ul>
<li>核心二進位檔撤銷</li>
<li>使用者模式二進位撤銷</li>
<li>憑證撤銷</li>
<li>受信任的根 (保留) </li>
</ul>
受信任的根目錄清單目前未使用，並保留供日後使用。</td>
</tr>
<tr class="odd">
<td>可擴充專案</td>
<td>包含其他元件所使用的資訊。 本節與 OPM 無關。</td>
</tr>
<tr class="even">
<td>更新：</td>
<td>包含定義 Windows Update 識別碼的 Guid。 本節包含下列清單的識別碼：
<ul>
<li>核心二進位檔撤銷</li>
<li>使用者模式二進位撤銷</li>
<li>憑證撤銷</li>
</ul>
應用程式可以使用這些識別碼來要求已撤銷之二進位檔的更新版本（如果有的話）。</td>
</tr>
<tr class="odd">
<td>簽名：核心區段</td>
<td>簽署標頭和核心區段。</td>
</tr>
<tr class="even">
<td>簽名：可擴充區段</td>
<td>簽署標頭和可擴充區段。</td>
</tr>
</tbody>
</table>



 

GRL 標頭是一個 [**grl \_ 標頭**](grl-header.md) 結構。 結構的 **dwSequenceNumber** 成員包含 GRL 版本號碼。 每次更新 GRL 並將新版本放置在使用者的電腦上時，這個數位就會遞增。

已撤銷的 OPM 憑證會列在 [核心] 區段的 [憑證撤銷] 清單中。 在 GRL 中的每個核心專案都是一個20位元組陣列，其中包含已撤銷憑證之公開金鑰的 SHA-1 雜湊。

簽章區段包含簽章，可用來驗證 GRL 是否未遭到篡改。 每個簽章區段都包含 MF 簽章結構。 [**\_**](mf-signature.md) 第一個簽章會將標頭加上核心區段。 第二個簽章會簽署標頭加上可延伸區段;此簽章與 OPM 無關。

若要確定 GRL 本身尚未遭篡改，請驗證簽章，如下所示：

1.  找出 MF 簽章 [**結構 \_**](mf-signature.md) 的開始。 在 [**GRL \_ 標頭**](grl-header.md)結構的 **cbSignatureCoreOffset** 成員中會提供 MF 簽章結構的位置。 **\_** 位置會指定為從 GRL 開頭算起的位移（以位元組為單位）。
2.  使用憑證鏈將 MF 簽章結構剖析為 PKCS 7 簽章 [**\_**](mf-signature.md) \# 。
3.  確認憑證鏈對受信任的根。
4.  確認在 EKU 中的分葉憑證具有下列物件識別碼： "1.3.6.1.4.1.311.10.5.4"。
5.  計算包含標頭的位元組雜湊以及 GRL 的核心區段。
6.  確認雜湊符合分葉憑證中的簽章。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[輸出保護管理員](output-protection-manager.md)
</dt> <dt>

[**GRL \_ 標頭**](grl-header.md)
</dt> <dt>

[**MF \_ 簽章**](mf-signature.md)
</dt> </dl>

 

 



