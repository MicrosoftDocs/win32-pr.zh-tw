---
title: 網路原則伺服器
description: 網路原則伺服器 (NPS) 是 Microsoft 對遠端驗證撥入使用者服務 (RADIUS) 伺服器和 proxy 的實施。
ms.assetid: d0eb41cb-e9c0-4a60-aeac-77d1dd90a75b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0d1dfc680c8a23ca1e80f52230736b3ab586cc8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315442"
---
# <a name="network-policy-server"></a>網路原則伺服器

## <a name="purpose"></a>目的

網路原則伺服器 (NPS) 是 Microsoft 對遠端驗證撥入使用者服務 (RADIUS) 伺服器和 proxy 的實施。 這是網際網路驗證服務 (IAS) 的後續版本。

NPS 作為 RADIUS 伺服器，可針對無線、驗證交換器，以及遠端存取撥號和虛擬私人網路 (VPN) 連接，執行驗證、授權和帳戶處理。

NPS 也是網路存取保護 (NAP) 的健康情況評估伺服器。 NPS 會執行網路連線嘗試的驗證與授權，並根據設定的系統健康狀態原則，評估電腦的健康狀態，並決定如何限制不符合規範的電腦網路存取或通訊。 這是僅限 NPS 專用的新功能;IAS 不支援此功能。 如需 NPS 新功能的完整清單，請參閱 [網際網路驗證服務和網路原則伺服器](internet-authentication-service-vs-network-policy-server.md) 。

NPS 包含兩個 API 集合： NPS 擴充功能 API 和伺服器資料物件 (SDO) API。 Nps 擴充功能 API 和 SDO API 也都受到 NPS （網際網路驗證服務）的先驅支援。

NPS 擴充功能 API 可用於擴充 NPS 和先前由 IAS 提供的驗證、授權和帳戶處理方法。

您可以使用伺服器資料物件 API，在執行 NPS 或 IAS 的電腦上操作網路原則設定。

> [!Note]  
> NPS 中的網路原則相當於 IAS 中的遠端存取原則。

 

## <a name="developer-audience"></a>開發人員對象

NPS 擴充功能 API 是專為使用 C/c + + 開發軟體的程式設計人員所設計。 程式設計人員應該熟悉網路概念和 RADIUS 通訊協定。 RADIUS 記載于 [rfc 2865](https://www.ietf.org/rfc/rfc2865.txt) 和 [rfc 2866](https://www.ietf.org/rfc/rfc2866.txt)中。

伺服器資料物件 API 是設計來供使用 C/c + + 或 Visual Basic 開發軟體的程式設計人員使用。 程式設計人員應該熟悉 [遠端存取服務](/windows/desktop/RRAS/remote-access-request-for-comments) (RAS) 和 RADIUS 通訊協定。

## <a name="run-time-requirements"></a>執行階段需求求

Windows Server 2008 支援 NPS 擴充功能 API，並安裝 Microsoft 商用網際網路服務 (MCIS) 。

Windows Server 2008 支援 Server Data Objects API。

您可以在 Windows Server 2008 上使用 NPS 安裝 Microsoft 商用網際網路服務 (MCIS) 。

## <a name="in-this-section"></a>本節內容

<dl> <dt>

[概觀](about-network-policy-server.md)
</dt> <dd>

關於 RADIUS、IAS 和 NPS 的一般資訊。

</dd> <dt>

[網路原則伺服器延伸模組 API](ias-extensions.md)
</dt> <dd>

用來執行用於驗證、授權和帳戶處理之延伸模組 Dll 的 API。

</dd> <dt>

[伺服器資料物件 API](server-data-objects.md)
</dt> <dd>

用於管理網路原則設定的 API。

</dd> <dt>

[SQL 可程式性](sql-programmability.md)
</dt> <dd>

用來管理 NPS (IAS) 記錄的預存程式範例。

</dd> </dl>

## <a name="related-topics"></a>相關主題

<dl> <dt>

[TechNet：網路原則伺服器](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11))
</dt> <dt>

[TechNet：網際網路驗證服務](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11))
</dt> <dt>

[網路存取保護](/windows/desktop/NAP/network-access-protection-start-page)
</dt> </dl>

 

 