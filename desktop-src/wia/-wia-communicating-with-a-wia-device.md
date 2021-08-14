---
description: 當執行緒主動與 Windows 映像取得通訊時 (wia) 裝置 (例如，傳輸資料或寫入裝置屬性) wia &\# 0034; 鎖定&\# 0034; 裝置。
ms.assetid: 59533937-284a-4732-a73b-d2e0b5a9a370
title: 在多個執行緒或應用程式中與 WIA 裝置通訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6f54cc8fe9a3b60d684ff9a62def2c0cf8862576034b16f58d3dd369d2b8be0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118209262"
---
# <a name="communicating-with-a-wia-device-in-multiple-threads-or-applications"></a>在多個執行緒或應用程式中與 WIA 裝置通訊

當執行緒主動與 Windows 映像取得通訊時 (wia) 裝置 (例如，傳輸資料或寫入裝置屬性) wia 「鎖定」裝置。 當裝置鎖定時，其他執行緒或進程都無法主動與該裝置通訊。

WIA 不會禁止多個執行緒或進程維護單一裝置的連接。 也就是說，裝置只會在實際通訊期間鎖定，而且兩個或多個應用程式可以同時選取單一裝置。

當任何執行緒或應用程式呼叫 [**IWiaDevMgr：： CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) 或 [**IWiaDevMgr2：： CreateDevice**](-wia-iwiadevmgr2-createdevice.md) 建立該裝置的實例時，WIA 都會建立個別的專案樹狀結構。 WIA 會為每個專案樹狀結構維護不同的狀態資訊。 例如，如果執行緒建立特定掃描器的兩個實例，則可以為這兩個實例設定不同的掃描解析度。 在特定實例上呼叫 [**IWiaDataTransfer：： idtGetData**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatatransfer-idtgetdata) 時，WIA 會先將與該實例相關聯的屬性載入至裝置，然後才進行實際的掃描。 這不會影響其他裝置實例的狀態。

如果執行緒目前已鎖定裝置 (它會主動與) 該裝置進行通訊，而另一個執行緒嘗試呼叫與裝置主動通訊的方法，此方法會傳回 WIA \_ 錯誤忙碌的 \_ 錯誤。

一般而言，讀取和寫入裝置屬性需要很少的時間，這些作業很少會造成衝突。 但是，傳輸資料通常需要較長的時間，因此更可能建立裝置存取衝突。 您可以使用程式設計的方式，以避免長時間的裝置作業 (資料傳輸) 在應用程式內的個別執行緒中同時進行。

應用程式絕對不應該假設它是唯一的應用程式，它會在啟動時與 WIA 裝置進行通訊。

 

 



