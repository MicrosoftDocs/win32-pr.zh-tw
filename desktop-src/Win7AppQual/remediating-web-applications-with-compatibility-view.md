---
description: 使用相容性檢視修正 Web 應用程式中的相容性問題
ms.assetid: ACAC2375-EA6C-4AA1-90B7-0BF237A51C02
title: 使用相容性檢視修正 Web 應用程式中的相容性問題
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7dd876dcf8d25ebe7e6cca15ea88bfeba52aa29e3e5d83680815c15f8bda46d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118329507"
---
# <a name="fixing-compatibility-issues-in-web-applications-by-using-compatibility-view"></a>使用相容性檢視修正 Web 應用程式中的相容性問題

本節說明基本的風險降低步驟，以及如何在您立即解決任何問題時規劃未來的應用程式相容性。

WindowsInternet Explorer 在可行時支援舊版 Internet Explorer 模型，讓您開發的網站在較新版本的 Internet Explorer 中繼續以預期的方式運作。 從 Internet Explorer 8 Windows 開始，您可以選擇逐頁逐頁選取轉譯模式，以支援舊版行為。

Internet Explorer 8 包含下列轉譯模式，您可以使用與 X-UA 相容的標頭來設定這些模式。



| 內容值 | 描述                                                                           |
|---------------|---------------------------------------------------------------------------------------|
| IE = 5          | 使用 [不相容] 模式。                                                                      |
| IE = 7          | 請一律使用 Windows Internet Explorer 7 模式。                                          |
| IE = EmulateIE7 | 除非網站具有不相容的 DOCTYPE，否則會顯示 Internet Explorer 7 模式。           |
| IE = 8          | 一律使用 Internet Explorer 8 模式。                                                  |
| IE = EmulateIE8 | 覆寫用戶端電腦上的相容性檢視，並使用 Internet Explorer 8 模式。      |
| IE = 邊緣       | 以最新模式顯示。 在 Internet Explorer 8 中，此值相當於 IE = 8。 |



 

下列主題描述如何使用相容性檢視來更新 web 應用程式。



| 主題                                                                                                  | 描述                                                                    |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [什麼是相容性檢視](what-is-compatibility-view-.md)                                          | 描述相容性檢視。                                                  |
| [為什麼需要相容性檢視？](why-do-you-need-compatibility-view-.md)                         | 描述您應該使用相容性檢視的原因。                               |
| [使用中繼標記以確保未來的相容性](use-the-meta-tag-to-ensure-future-compatibility.md) | 描述如何使用 **中繼** 元素以確保未來的相容性。 |



 

 

 



