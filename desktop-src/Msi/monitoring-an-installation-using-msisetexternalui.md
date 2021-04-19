---
description: 封裝作者可以透過建立可執行應用程式（包含回呼處理常式）來監視內部 Windows Installer 訊息，以接收訊息和功能來起始安裝。
ms.assetid: 0aa8a2d6-f519-4d87-a28f-a11cb546bff5
title: 使用 MsiSetExternalUI 監視安裝
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06cc461845a6db1fab4ede22581093c46c0e76e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978143"
---
# <a name="monitoring-an-installation-using-msisetexternalui"></a><span data-ttu-id="2a949-103">使用 MsiSetExternalUI 監視安裝</span><span class="sxs-lookup"><span data-stu-id="2a949-103">Monitoring an Installation Using MsiSetExternalUI</span></span>

<span data-ttu-id="2a949-104">封裝作者可以透過建立可執行應用程式（包含回呼處理常式）來監視內部 Windows Installer 訊息，以接收訊息和功能來起始安裝。</span><span class="sxs-lookup"><span data-stu-id="2a949-104">Package authors can monitor internal Windows Installer messages through the creation of an executable application that contains both a callback handler to receive the messages and functionality to initiate an installation.</span></span>

<span data-ttu-id="2a949-105">回呼處理常式會符合 INSTALLUI \_ 處理常式原型，而且此回呼處理常式的指標會傳遞至 [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia)。</span><span class="sxs-lookup"><span data-stu-id="2a949-105">The callback handler conforms to the INSTALLUI\_HANDLER prototype, and a pointer to this callback handler is passed to [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia).</span></span> <span data-ttu-id="2a949-106">藉由呼叫 [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta)來起始安裝之後，回呼處理常式會攔截安裝訊息，而封裝作者可以選擇性地顯示或忽略這些訊息。</span><span class="sxs-lookup"><span data-stu-id="2a949-106">Once the installation has been initiated by a call to [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta), installation messages are trapped by the callback handler and the package author can selectively display or ignore any or all of these messages.</span></span>

<span data-ttu-id="2a949-107">如需詳細資訊，請參閱 [使用 MsiSetExternalUI 處理進度訊息](handling-progress-messages-using-msisetexternalui.md)、 [從外部消費者介面處理常式傳回值](returning-values-from-an-external-user-interface-handler.md)，以及 [剖析 Windows Installer 訊息](parsing-windows-installer-messages.md)。</span><span class="sxs-lookup"><span data-stu-id="2a949-107">For more information, see [Handling Progress Messages Using MsiSetExternalUI](handling-progress-messages-using-msisetexternalui.md), [Returning Values from an External User Interface Handler](returning-values-from-an-external-user-interface-handler.md), and [Parsing Windows Installer Messages](parsing-windows-installer-messages.md).</span></span>

<span data-ttu-id="2a949-108">如需使用以記錄為基礎的外部處理常式的詳細資訊，請參閱 [使用 MsiSetExternalUIRecord 監視安裝](monitoring-an-installation-using-msisetexternaluirecord.md)。</span><span class="sxs-lookup"><span data-stu-id="2a949-108">For more information about using a record-based external handler, see [Monitoring an Installation Using MsiSetExternalUIRecord](monitoring-an-installation-using-msisetexternaluirecord.md).</span></span>

 

 



