---
description: 封裝作者可以透過建立可執行應用程式（包含回呼處理常式）來監視內部 Windows Installer 訊息，以接收訊息和功能來起始安裝。
ms.assetid: 0aa8a2d6-f519-4d87-a28f-a11cb546bff5
title: 使用 MsiSetExternalUI 監視安裝
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9660b1454d7e4f3437da6dce41707a1516207d853510e8475837f31e60090b78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118628569"
---
# <a name="monitoring-an-installation-using-msisetexternalui"></a>使用 MsiSetExternalUI 監視安裝

封裝作者可以透過建立可執行應用程式（包含回呼處理常式）來監視內部 Windows Installer 訊息，以接收訊息和功能來起始安裝。

回呼處理常式會符合 INSTALLUI \_ 處理常式原型，而且此回呼處理常式的指標會傳遞至 [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia)。 藉由呼叫 [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta)來起始安裝之後，回呼處理常式會攔截安裝訊息，而封裝作者可以選擇性地顯示或忽略這些訊息。

如需詳細資訊，請參閱[使用 MsiSetExternalUI 處理進度訊息](handling-progress-messages-using-msisetexternalui.md)、[從外部消費者介面處理常式傳回值](returning-values-from-an-external-user-interface-handler.md)，以及[剖析 Windows Installer 訊息](parsing-windows-installer-messages.md)。

如需使用以記錄為基礎的外部處理常式的詳細資訊，請參閱 [使用 MsiSetExternalUIRecord 監視安裝](monitoring-an-installation-using-msisetexternaluirecord.md)。

 

 



