---
description: 裝置移除通知
ms.assetid: 0b96231a-f990-4c1c-8d00-cafeb3985ab3
title: 裝置移除通知
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3cc73aba6ad02eb1dfba095b6f45b9fa6c067c51dbe165f4ded86141dae1c66
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052018"
---
# <a name="device-removal-notification"></a>裝置移除通知

如果使用者移除圖形所使用的隨插即用裝置，則篩選圖形管理員會張貼 [**EC \_ 裝置 \_ 遺失**](ec-device-lost.md) 事件。 如果裝置再次變成可用，則篩選圖形管理員會將另一個 **EC \_ 裝置 \_ 遺失** 事件張貼。 不過，先前的「capture」篩選狀態不再有效。 應用程式必須重建圖形才能使用裝置。

當新裝置插入時，DirectShow 不會傳送任何事件。 若要瞭解新裝置的可用時間，應用程式可以監視 WM \_ DEVICECHANGE 視窗訊息。 如需詳細資訊，請參閱 Platform SDK 檔中的「裝置管理」。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow 中的事件通知](event-notification-in-directshow.md)
</dt> </dl>

 

 



