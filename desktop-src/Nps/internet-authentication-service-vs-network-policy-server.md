---
title: 網際網路驗證服務 & 網路原則伺服器
description: 瞭解網際網路驗證服務和網路原則伺服器。 網際網路驗證服務 (IAS) 已重新命名 (NPS) 的網路原則伺服器。
ms.assetid: c7c6d1a3-d0c8-469e-ae1e-a848ef7fee2b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dd62a50021c485c7bf51cdc9caff4360e4cc863
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989423"
---
# <a name="internet-authentication-service--network-policy-server"></a>網際網路驗證服務 & 網路原則伺服器

網際網路驗證服務 (IAS) 已重新命名 (NPS) 的網路原則伺服器。

## <a name="internet-authentication-service"></a>網際網路驗證服務

網際網路驗證服務是 Microsoft 對 RADIUS 伺服器和 proxy 的實作為。

網際網路驗證服務支援兩個 API 集： [網路原則伺服器延伸 api](ias-extensions.md) 和 [伺服器資料物件 API](server-data-objects.md)。

如需有關 IAS 的詳細資訊，請參閱 [TechNet： Internet Authentication Service](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11)) 。

## <a name="network-policy-server"></a>網路原則伺服器

網路原則伺服器是 Microsoft 對 RADIUS 伺服器和 proxy 的實施，在從 Windows Server 2008 開始的 Windows 伺服器上也可以使用。

NPS 支援與 IAS 相同的兩個 API 集： [網路原則伺服器延伸 api](ias-extensions.md) 和 [伺服器資料物件 API](server-data-objects.md)。

此外，NPS 還包含一組擴充 IAS 功能的新功能。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>功能</th>
<th>NPS 的新功能</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/NAP/network-access-protection-start-page">網路存取保護 (NAP)</a><br/></td>
<td>NPS 是網路存取保護的中央伺服器。<br/> NPS 支援使用下列其他條件來撰寫原則：<br/>
<ul>
<li>原則到期日。</li>
<li>作業系統版本。</li>
<li>存取用戶端 IP 位址。</li>
<li>健康原則。</li>
<li>允許的 EAP 類型。</li>
<li>HCAP.</li>
</ul>
NPS 支援使用下列其他設定來撰寫原則：<br/>
<ul>
<li>緩刑。</li>
<li>有限的存取權。</li>
<li>限制存取的擴充狀態。</li>
</ul>
透過 NAP 與 CISCO NAC 互通的 NPS。<br/> IAS 不支援 NAP。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/eap/eap-start-page">EAP</a> 原則和 <a href="/windows/win32/eaphost/portal">EAPHost</a> 支援<br/></td>
<td>NPS 使用 EAPHost 來進行 EAP 方法擴充性。 此外，系統管理員也可以設定 EAP 的網路存取原則。<br/> IAS 不支援 EAPHost 整合或原則的 EAP 類型篩選準則。<br/></td>
</tr>
<tr class="odd">
<td>IPv6 支援<br/></td>
<td>NPS 支援 IPv6 環境中的部署。<br/> IAS 不支援 IPv6 網路位址。<br/></td>
</tr>
<tr class="even">
<td>XML 設定<br/></td>
<td>NPS 設定可以用 XML 格式匯入和匯出。<br/> IAS 會使用 Jet 資料庫來儲存服務設定。<br/></td>
</tr>
<tr class="odd">
<td><a href="https://www.niap-ccevs.org/cc-scheme/">一般準則</a> 支援<br/></td>
<td>NPS 已更新，可在必須符合通用準則安全性標準的環境中支援其部署。<br/></td>
</tr>
<tr class="even">
<td><a href="ias-extensions.md">NPS 擴充功能 API</a><br/></td>
<td>NPS 擴充 Dll 會在與 NPS 服務不同的進程中執行。 如果延伸模組 DLL 損毀，NPS 將會繼續執行，且未來的要求將會遭到拒絕。<br/> IAS 擴充 Dll 會在與 IAS 服務相同的進程中執行，而且可能會對服務造成負面影響。<br/></td>
</tr>
<tr class="odd">
<td>管理消費者介面<br/></td>
<td>Nps 管理主控台 (的 nps) 具有新的外觀、改良的可用性，並涵蓋所有新增至 NPS 的新功能。<br/> IAS 會使用 services.msc 管理主控台。<br/></td>
</tr>
<tr class="even">
<td>角色管理工具和伺服器管理員整合<br/></td>
<td>NPS 與伺服器管理員和角色管理工具整合。 這項整合可協助您設定和管理 NPS 以及相關的案例。<br/> 執行 IAS 的電腦上無法使用伺服器管理員。<br/></td>
</tr>
<tr class="odd">
<td>已更新 <a href="/previous-versions/windows/it-pro/windows-server-2003/cc785383(v=ws.10)">Netsh</a>的命令列腳本。<br/></td>
<td>NPS 支援 &quot; Netsh nps &quot; 命令列介面。 &quot;Netsh nps &quot; 包含允許完整設定 nps 的新命令，包括 NAP 功能。<br/> IAS 支援 &quot; Netsh aaaa &quot; 命令列介面。<br/></td>
</tr>
<tr class="even">
<td>原則隔離<br/></td>
<td>NPS 可設定網路原則來源，藉此實現原則隔離。 原則可以設定為僅適用于預先決定的 NAS 類型。<br/> IAS 不支援原則隔離。<br/></td>
</tr>
</tbody>
</table>



 

如需 NPS 的詳細資訊，請參閱 [TechNet：網路原則伺服器](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11)) 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[RADIUS 驗證、授權和帳戶處理](/windows/desktop/Nps/ias-radius-authentication-and-accounting)
</dt> <dt>

[使用網路原則伺服器進行記錄](/windows/desktop/Nps/ias-radius-accounting-packets)
</dt> <dt>

[使用狀態伺服器](/windows/desktop/Nps/ias-working-with-a-state-server)
</dt> </dl>

