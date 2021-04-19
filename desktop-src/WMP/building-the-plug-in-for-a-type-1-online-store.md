---
title: 建立類型1線上商店的外掛程式
description: 建立類型1線上商店的外掛程式
ms.assetid: 5d38a41f-9859-452b-953f-3449c2b0ce06
keywords:
- Windows Media Player 線上商店、外掛程式
- 線上商店、外掛程式
- 輸入1個線上商店、外掛程式
- Windows Media Player 線上商店，建立外掛程式
- 線上商店，建立外掛程式
- 輸入1個線上商店，建立外掛程式
- Windows Media Player 線上商店、IWMPContentPartner 介面
- 線上商店、IWMPContentPartner 介面
- 輸入1個線上商店、IWMPContentPartner 介面
- 外掛程式，Windows Media Player 線上商店
- 外掛程式，線上商店
- 外掛程式，請輸入1個線上商店
- 外掛程式，IWMPContentPartner 介面
- 外掛程式，建立
- Windows Media Player 外掛程式，請輸入1個線上商店
- Windows Media Player 外掛程式，線上商店
- Windows Media Player 外掛程式，Windows Media Player 線上商店
- Windows Media Player 外掛程式、IWMPContentPartner 介面
- Windows Media Player 外掛程式，建立
- IWMPContentPartner
- 建立外掛程式，請輸入1個線上商店
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36272e3497eebc7b5362d793a0ee265d2c3166fc
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "106968887"
---
# <a name="building-the-plug-in-for-a-type-1-online-store"></a>建立類型1線上商店的外掛程式

類型1線上商店必須提供可實 [**IWMPContentPartner**](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner) 介面的外掛程式。 外掛程式會在與 Windows Media Player 不同的進程中執行。

建立執行跨進程之外掛程式的步驟如下所示：

1.  撰寫您的外掛程式，就好像它是同進程 COM 伺服器一樣。
2.  在使用者的電腦上建立 **DllSurrogate** 登錄專案。 **DllSurrogate** 專案會通知 COM 執行時間應該在預設 DLL 代理的實例（dllhost.exe）中建立您的外掛程式。

如需註冊外掛程式的詳細資訊，請參閱 [類型1線上商店的登錄機碼和專案](registry-keys-and-entries-for-a-type-1-online-store.md)。

您不需要為外掛程式建立任何 proxy 或 stub 程式碼。 所有的封送處理支援都是由 Windows Media Player 提供。

您可以使用線上商店外掛程式嚮導，快速建立可作為起點的外掛程式。 如需詳細資訊，請參閱 [安裝線上商店外掛程式 Wizard](installing-the-online-store-plug-in-wizard.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**類型1線上商店的程式設計指南**](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




