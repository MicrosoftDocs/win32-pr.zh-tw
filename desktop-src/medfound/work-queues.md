---
description: 在 Microsoft 媒體基礎中，工作佇列是在另一個執行緒上執行非同步作業的有效方式。
ms.assetid: f886d096-b1f5-42e4-8888-501b58bffd50
title: 工作佇列
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15b1e5e8a0a3776f718f645550813bf008b38aee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193008"
---
# <a name="work-queues"></a>工作佇列

在 Microsoft 媒體基礎中，工作佇列是在另一個執行緒上執行非同步作業的有效方式。

此章節包含下列主題。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>主題</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="using-work-queues.md">使用工作佇列</a></td>
<td>描述應用程式或元件如何使用工作佇列來執行非同步作業。</td>
</tr>
<tr class="even">
<td><a href="writing-an-asynchronous-method.md">撰寫非同步方法</a></td>
<td>描述如何撰寫會遵循 <a href="asynchronous-callback-methods.md">非同步回呼方法</a>中所述之 Begin/End 模式的非同步方法。</td>
</tr>
<tr class="odd">
<td><a href="custom-asynchronous-result-objects.md">自訂非同步結果物件</a></td>
<td>描述如何建立 <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult"><strong>IMFAsyncResult</strong></a> 介面的自訂執行。<br/>
<blockquote>
[!Note]<br />
大部分的應用程式都應該使用 <a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult"><strong>MFCreateAsyncResult</strong></a>所提供的庫存實作為。 本主題適用于具有 advanced 需求的應用程式。
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="media-foundation-work-queue-and-threading-improvements.md">工作佇列和執行緒改進</a></td>
<td>描述媒體基礎平臺中工作佇列和執行緒 Windows 8 的增強功能。<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體基礎平臺 Api](media-foundation-platform-apis.md)
</dt> </dl>

 

 




