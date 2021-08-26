---
title: 開發通用 Windows 平臺 (UWP) 應用程式
description: 開發通用 Windows 平臺 (UWP) 應用程式
ms.assetid: 215256D7-CBBA-43B0-A99C-490A25D1F82C
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 332864b00614ceb494b2832c0b565a5a10819d631ecb6c4098284a94ad2c038e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119935438"
---
# <a name="develop-universal-windows-platform-uwp-apps"></a>開發通用 Windows 平臺 (UWP) 應用程式

我們鼓勵所有 desktop (Win32) 應用程式 isv，透過) 將您的桌面應用程式帶入[通用 Windows 平臺 (UWP 傳統型橋接器](https://developer.microsoft.com/windows/bridges/desktop/)。 [Windows 市集](https://blogs.windows.com/buildingapps/2016/02/04/windows-store-trends-february-2016/)中也支援 UWP app，這可讓您更容易地將使用者自動更新至一致的版本，減低您的支援成本。

如果您的桌面應用程式無法使用傳統型橋接器進行轉換，強烈建議您使用遵循最佳作法的安裝程式，並確定已完整測試。 安裝程式是您的使用者或客戶首次使用您的應用程式體驗。 很多時候安裝程式無法正常運作，或未經過所有案例的完整測試。 [Windows 應用程式認證套件](https://dev.windows.com/develop/app-certification-kit)可協助您測試 Win32 應用程式的安裝和卸載，並協助您識別使用未記載的 api，以及在使用者執行之前的其他基本效能相關最佳做法問題。

## <a name="best-practices"></a>最佳做法：

-   使用可在 32 位元及 64 位元版本 Windows 中運作的安裝程式。
-   將您的安裝程式設計為在多種案例上執行 (使用者或電腦層級)。
-   將所有的 Windows 可轉散發檔案保留在原始封裝中 – 如果您重新封裝這些檔案，可能會破壞安裝程式。
-   為您的安裝程式排程開發時間—這些通常會在軟體開發週其中忽略為可交付項目。

 

 




