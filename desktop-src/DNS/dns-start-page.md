---
title: 網域名稱系統
description: 網域名稱系統 (DNS) （Microsoft Windows 中的定位器服務）是一種業界標準的通訊協定，可在以 IP 為基礎的網路上尋找電腦。
ms.assetid: 4d1c2151-3995-4e7f-881b-4466bd7b7bb7
keywords:
- DNS
- 'DNS， (查看網域名稱系統) '
- 網域名稱系統
- 網域名稱系統，起始頁
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d705c15fccb0ab237bc610ae4129f6d7002c4a2a
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/10/2021
ms.locfileid: "104035322"
---
# <a name="domain-name-system"></a>網域名稱系統

## <a name="purpose"></a>目的

網域名稱系統 (DNS) （Microsoft Windows 中的定位器服務）是一種業界標準的通訊協定，可在以 IP 為基礎的網路上尋找電腦。 IP 網路（例如網際網路和 Windows 網路）依賴以數位為基礎的位址來處理資料。 不過，使用者可以更容易記住名稱位址，因此必須將使用者易記的 (名稱（例如) ）轉譯 `www.microsoft.com` 為網路可 (辨識的位址，例如 207.46.131.137) 簡單) 。

## <a name="where-applicable"></a>適用時

Windows 和 Active Directory 使用 DNS。 DNS 是網際網路和 Active Directory 的主要定位器服務，因此 DNS 被視為適用于 Windows 和 Active Directory 的基礎服務。

## <a name="developer-audience"></a>開發人員對象

Windows 提供的函式可讓應用程式設計人員使用 DNS，例如程式設計 DNS 查詢、記錄比較和名稱查閱。

可程式化 DNS 元件是設計來供 C/C++ 程式設計人員使用。 必須熟悉網路及 DNS。 程式設計人員應該熟悉 IP 通訊協定套件，以及 DNS 通訊協定和 DNS 作業。

## <a name="run-time-requirements"></a>執行階段需求求

所有需要網際網路相容定位器服務的 IP 網路都會使用 DNS。 不過，DNS API 需要 Windows 2000 或更新版本。

## <a name="in-this-section"></a>本節內容



| 主題                                                             | 描述                                                                          |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [DNS 標準檔](dns-standards-documents.md)<br/> | 公用 DNS 標準檔的連結。<br/>                                  |
| [關於 DNS](about-dns.md)<br/>                             | 關於 DNS 的一般資訊。<br/>                                            |
| [DNS 參考](dns-reference.md)<br/>                     | DNS 的參考檔。<br/>                                          |
| [DNS WMI 提供者](dns-wmi-provider.md)<br/>               | DNS WMI 提供者的一般資訊和參考檔。<br/> |
| [詞彙](glossary-gly.md)<br/>                           | DNS 詞彙和定義的詞彙。<br/>                                    |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DHCP](/previous-versions/windows/desktop/dhcp/dhcp-start-page)
</dt> <dt>

[網際網路通訊協定協助程式](/windows/desktop/IpHlp/ip-helper-start-page)
</dt> <dt>

[目錄服務](https://msdn.microsoft.com/library/Dd425378(v=VS.85).aspx)
</dt> </dl>

 

