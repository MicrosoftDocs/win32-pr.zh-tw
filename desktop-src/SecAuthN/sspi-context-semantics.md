---
description: 安全性內容是在通訊會話期間有效的一組安全性屬性和規則。
ms.assetid: 6c87448b-5b8d-4694-ac3f-be83a258fbb0
title: SSPI 內容語義
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddadd2c8a76f1fdc151273dca2027b8cb55776a50b78a7c08343c22410ae90e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118916977"
---
# <a name="sspi-context-semantics"></a>SSPI 內容語義

[*安全性內容*](../secgloss/s-gly.md)是在通訊會話期間有效的一組安全性屬性和規則。 這包括主體身分識別的資訊，以及所使用金鑰、密碼和演算法的資訊。 針對 [*安全性支援提供者介面*](../secgloss/s-gly.md) (SSPI) ，安全性內容是一種不透明的結構，此結構是透過包含 [**InitializeSecurityCoNtext (一般)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) 函式和 [**AcceptSecurityCoNtext (一般)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) 函式的結算所建立。

如需內容屬性的詳細資訊，請參閱 [內容需求](context-requirements.md)。

SSPI 模型支援三種類型的安全性內容。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>類型</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="connection-oriented-contexts.md">[連接]</a></td>
<td>連接導向的 <a href="/windows/desktop/SecGloss/c-gly"><em>內容</em></a> 是最常見的安全性內容，而且是最簡單的使用方式。 呼叫端會負責整體訊息格式和訊息中資料的位置。 呼叫端也負責訊息內安全性相關欄位的位置，例如簽章資料的位置。<br/></td>
</tr>
<tr class="even">
<td><a href="datagram-contexts.md">資料包</a></td>
<td><a href="/windows/desktop/SecGloss/d-gly"><em>資料包</em></a>導向內容具有 DCE 樣式資料包通訊的額外支援。 它也可以一般用於資料包導向的傳輸應用程式。<br/>
<blockquote>
<p>[!Important]</p>
<p><a href="microsoft-kerberos.md">Microsoft Kerberos</a>套件不支援使用者到使用者模式中的資料包內容。<br/></p>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="stream-contexts.md">串流</a></td>
<td>資料流程導向內容負責安全性封裝內的封鎖和訊息格式化。 呼叫端不感興趣格式化，而是資料的原始資料流程。<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[內容需求](context-requirements.md)
</dt> <dt>

[連線導向的內容](connection-oriented-contexts.md)
</dt> <dt>

[資料包內容](datagram-contexts.md)
</dt> <dt>

[資料流程內容](stream-contexts.md)
</dt> </dl>

 

 
