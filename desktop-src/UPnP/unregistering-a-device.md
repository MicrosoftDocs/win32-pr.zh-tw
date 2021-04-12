---
title: 取消註冊裝置
description: 使用 IUPnPRegistrar UnregisterDevice 方法將裝置取消註冊。
ms.assetid: 4f7624e3-4d60-406d-8521-1dfc9aee4408
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4c480433e3d8dbf4ff823728281018801ec35c1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462420"
---
# <a name="unregistering-a-device"></a>取消註冊裝置

使用 [**IUPnPRegistrar：： UnregisterDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-unregisterdevice) 方法將裝置取消註冊。 您可以根據 *fPermanent* 的值，以暫時或永久的 (移除裝置主機) 移除裝置的註冊。 如果裝置將會重新註冊，且裝置應該使用相同的 UDN，則開發人員應暫時移除裝置。 否則，就會永久移除裝置。

用來取消註冊的 GUID 不是 UDN。 您必須使用 [**IUPnPRegistrar：： >registerdevice.js**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdevice) 或 [**IUPnPRegistrar：： RegisterRunningDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice)傳回給您的識別碼。

> [!Note]  
> 您可以釋放 [**IUPnPRegistrar**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpregistrar) 物件。 只有識別碼必須快取。

 

如果 *fPermanent* 為 **FALSE**，則會暫時移除裝置。 使用 [**IUPnPReregistrar**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpreregistrar) 介面重新註冊裝置。 [**IUPnPReregistrar：： ReregisterDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpreregistrar-reregisterdevice)和 [**IUPnPReregistrar：： ReregisterRunningDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpreregistrar-reregisterrunningdevice)方法會使用相同的 UDN 或 UDNs，如果是嵌套裝置，則是由裝置主機先前為未註冊的裝置所產生。

如果 *fPermanent* 為 **TRUE**，則會從裝置主機永久移除裝置。 在同一部電腦上再次註冊此裝置，會建立與先前建立的不同 UDN。

> [!Note]  
> 當裝置在同一部電腦上註冊多次時，裝置主機會為裝置的每個實例產生不同的 UDNs。

 

 

 




