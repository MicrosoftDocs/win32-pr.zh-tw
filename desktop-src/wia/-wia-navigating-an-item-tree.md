---
description: 應用程式會流覽 Windows 映像取得 (WIA) 裝置的專案樹狀結構，以尋找並選取該裝置上的影像。 應用程式會使用這項技術來選取並取得影像，而不會向使用者呈現對話方塊。
ms.assetid: 1f124b4a-45fb-4181-b45a-e810a61ac37d
title: 流覽專案樹狀結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 787ff3b53690ae7db4ff69fd5de2f4f4186f8e43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511616"
---
# <a name="navigating-an-item-tree"></a>流覽專案樹狀結構

應用程式會流覽 Windows 映像取得 (WIA) 裝置的專案樹狀結構，以尋找並選取該裝置上的影像。 應用程式會使用這項技術來選取並取得影像，而不會向使用者呈現對話方塊。

WIA 裝置會表示為 [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) 或 [**IWiaItem2**](-wia-iwiaitem2.md) 物件樹狀結構中的根專案。 樹狀結構中的子專案代表掃描器的影像，或是掃描器的掃描張床。

選取 WIA 裝置之後，應用程式會呼叫裝置之 [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem)或 [**IWiaItem2**](-wia-iwiaitem2.md)介面的 [**IWiaItem：： EnumChildItems**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems)方法，以列舉裝置 (影像或掃描張床) 的子專案。 如需相關指示，請參閱 [選取裝置](-wia-selecting-a-device.md)。

[**IWiaItem：： EnumChildItems**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems)方法會為裝置的子專案建立列舉物件，並傳回該物件之 [**IEnumWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwiaitem)介面的指標。 然後，應用程式可以使用 **IEnumWiaItem** 介面的方法，取得裝置專案樹狀結構中專案的指標。

 

 



