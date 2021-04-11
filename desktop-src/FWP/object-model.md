---
title: 物件模型
description: 下表列出可透過 Windows 篩選平台 (WFP) 所提供的各種 API 集合來操作的物件類型。
ms.assetid: 6931583f-785c-4e27-b5e4-d185d23a54ee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa90b4757a39617616c6f83b6b79fe322b2e64c8
ms.sourcegitcommit: 60ad94096619da5476f9bbcd4cc231b40b6f5358
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/20/2020
ms.locfileid: "104023086"
---
# <a name="object-model"></a>物件模型

下表列出可透過 Windows 篩選平台 (WFP) 所提供的各種 API 集合來操作的物件類型。



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>物件類型</th>
<th>Description</th>
<th>範例屬性</th>
<th>範例</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>篩選</td>
<td>控制分類的規則。 如果符合條件，則會叫用動作。 <br/> 這是 WFP 公開的最複雜物件，因為它會將所有其他物件類型系結在一起。 <br/></td>
<td><ul>
<li>條件陣列</li>
<li>動作 (允許、封鎖、標注) </li>
<li><a href="filter-weight-assignment.md">Weight</a></li>
<li>Context</li>
</ul></td>
<td>&quot;封鎖 TCP 埠大於1024的流量。&quot; <br/> &quot;未受保護之所有流量的識別碼。&quot;<br/></td>
</tr>
<tr class="even">
<td>圖說文字</td>
<td>參與分類進程的一組函數。<br/> 它可讓您在符合特定條件時進行自訂封包處理。<br/></td>
<td><ul>
<li>識別碼</li>
<li>適用的圖層</li>
</ul></td>
<td>NAT 驅動程式<br/></td>
</tr>
<tr class="odd">
<td>層</td>
<td>篩選引擎中的篩選容器。 <br/> 代表在網路流量處理中叫用篩選引擎的特定點。<br/></td>
<td><ul>
<li>可以新增至圖層之篩選準則的架構</li>
</ul></td>
<td>輸入傳輸層<br/></td>
</tr>
<tr class="even">
<td>子圖層</td>
<td>圖層的子元件，用於 <a href="filter-arbitration.md">篩選仲裁</a>。<br/></td>
<td><ul>
<li>Weight</li>
</ul></td>
<td>IPsec 通道子層<br/></td>
</tr>
<tr class="odd">
<td>提供者</td>
<td>在 WFP 上建立解決方案的原則提供者。<br/> 它僅供管理之用;它不會影響執行時間封包處理。<br/></td>
<td><ul>
<li>識別碼</li>
<li>服務名稱</li>
</ul></td>
<td>具有進階安全性的 Windows 防火牆<br/> 協力廠商 URL 篩選應用程式<br/></td>
</tr>
<tr class="even">
<td>提供者內容</td>
<td>原則提供者用來儲存任意內容資訊的資料 blob。 <br/> 它是用來將自訂設定資訊傳遞給標注。<br/> 使用內容資訊最常見的方式，是讓篩選參考提供者內容。 <br/></td>
<td><ul>
<li>識別碼</li>
<li>資料 blob</li>
</ul></td>
<td>IPsec 會將驗證設定儲存在基礎篩選引擎 ( BFE) 。 &quot; &quot; 篩選準則的內容屬性會指出用於篩選器所描述之流量的驗證設定。<br/> SSL 憑證選取填充碼會將認證資訊儲存在提供者內容中。 <br/></td>
</tr>
</tbody>
</table>



 

WFP API 所公開的物件類型具有一致的語法。 針對所有物件類型，新增、列舉、訂閱等等的動作都很類似。

每個物件類型都是以資料結構來表示 (例如 [**FWPM \_ FILTER0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter0)) 。 為了將 WFP API 所公開的不同資料結構數目降至最低，您可以使用相同的資料結構來加入新物件，以及抓取現有物件。 因此，在加入新的物件時，會忽略每個資料結構中的欄位，因為這些欄位是由基礎篩選引擎填入 (BFE) ，而不是由呼叫端所填入。 例如， **FWPM \_ FILTER0** 資料結構有一個 **filterId** 欄位，其中包含對應 **FWPS \_ FILTER0** 的 **LUID** 。 此 **LUID** 是由 BFE 所指派，因此在 [**FwpmFilterAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0)的呼叫中會忽略此欄位。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[物件管理](object-management.md)
</dt> </dl>

 

 





