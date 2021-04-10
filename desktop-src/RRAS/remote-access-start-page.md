---
title: 遠端存取
description: 使用遠端存取服務 (RAS) 來建立用戶端應用程式。
ms.assetid: 4e6c04d4-f989-4248-901f-ec15f61582da
keywords:
- 遠端存取服務 RAS
- RAS RAS
- 遠端存取服務 RAS、起始頁
- RAS RAS，請參閱遠端存取
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95a4b1c06656b51395c8c4fc666e59d6115bd839
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/20/2020
ms.locfileid: "104092560"
---
# <a name="remote-access"></a>遠端存取

## <a name="purpose"></a>目的

使用遠端存取服務 (RAS) 來建立用戶端應用程式。 這些應用程式會顯示 RAS 通用對話方塊、管理遠端存取連線和裝置，以及操作電話簿專案。 RAS 也為遠端存取服務提供新一代的伺服器功能， (RAS) for Windows。 RRAS 伺服器功能遵循，並以遠端存取服務 (RAS) 為基礎。

## <a name="where-applicable"></a>適用時

遠端存取服務適用于使用廣域網路 (WAN) 連結或虛擬私人網路 (VPN) 的任何計算環境。 RAS 可以透過 WAN 連結或 VPN，將遠端用戶端電腦連線到網路伺服器。 遠端電腦接著會在伺服器的 LAN 上運作，就好像遠端電腦直接連接到 LAN 一樣。 RAS API 可讓程式設計人員以程式設計方式存取 RAS 的功能。

## <a name="developer-audience"></a>開發人員對象

RAS API 是設計來供 C/c + + 程式設計人員使用。 Microsoft Visual Basic 程式設計人員也可能會發現 API 很有用。 程式設計人員應該熟悉網路概念。

## <a name="run-time-requirements"></a>執行階段需求求

只有網路伺服器上才支援 RAS API 中的部分功能，而只有網路用戶端支援其他功能。 如需有關哪些作業系統支援特定功能的詳細資訊，請參閱檔中的需求一節。

您可以藉由安裝[rras](https://www.microsoft.com/ntserver/nts/downloads/winfeatures/rras/rrasdown.asp)可轉散發套件，將 rras 的[增強 RAS 功能](function-comparison-windows-2000-versus-rras-redistributable.md)提供給 Windows NT Server 4.0。 RRAS 的所有功能都整合到 Windows 2000 Server、Windows Server 2003 和 Windows Server 2008 中。 RRAS 應用程式無法在 Windows NT 工作站4.0 或用戶端作業系統（例如 Windows 95）上執行。 如需有關哪些作業系統支援特定功能的詳細資訊，請參閱檔中的需求一節。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                             | 描述                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [遠端存取服務](about-remote-access-service.md)<br/>                               | 遠端存取服務 (RAS) 為執行 Windows 的電腦上的用戶端應用程式提供遠端存取功能。<br/>                                                                                          |
| [遠端存取服務管理](about-remote-access-service-administration.md)<br/> | 遠端存取服務管理提供一組功能，可在 RAS 伺服器上管理使用者權限和埠。 您可以使用這些函數開發 RAS 伺服器管理應用程式。<br/> |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[路由](routing-start-page.md)
</dt> <dt>

[路由通訊協定](routing-protocols-start-page.md)
</dt> </dl>

 

 





