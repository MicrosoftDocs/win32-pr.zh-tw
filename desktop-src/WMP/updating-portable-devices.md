---
title: 更新可攜式裝置
description: 更新可攜式裝置
ms.assetid: 2827e71b-f5e9-4403-9763-043239c4a216
keywords:
- Windows Media Player 線上商店，更新可攜式裝置
- 線上商店，更新可攜式裝置
- 輸入1個線上商店，更新可攜式裝置
- Windows Media Player 線上商店、可攜式裝置
- 線上商店、可攜式裝置
- 輸入1個線上商店、可攜式裝置
- 更新可攜式裝置
- 可攜式裝置，更新
- 可攜式裝置，Windows Media Player 線上商店
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b29f5314f4eba1af43b3858304f02f8a7e0107df
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104314226"
---
# <a name="updating-portable-devices"></a>更新可攜式裝置

Windows Media Player 可讓使用者與可攜式裝置同步處理數位媒體內容。 這可能包含從線上商店購買或出租的音樂內容。 在某些情況下，線上商店提供者可能會想要在管理存放區所提供的內容時，撰寫程式碼以在連接的可攜式裝置上運作。 為了讓線上商店外掛程式有機會使用連線的裝置，Windows Media Player 會呼叫 [IWMPContentPartner：： UpdateDevice](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-updatedevice) ，並提供可攜式裝置的正式名稱。 如果外掛程式程式碼判斷必須使用連線的裝置來完成一些工作，則在 \_ 繼續執行工作之前，它必須立即從呼叫 **UpdateDevice** 傳回 S OK。 如果沒有要執行的工作，外掛程式應該會傳回錯誤碼。

當外掛程式完成使用裝置時，它必須呼叫 [IWMPContentPartnerCallback：： UpdateDeviceComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-updatedevicecomplete) ，以通知 Windows Media Player 裝置可供使用。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**類型1線上商店的程式設計指南**](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




