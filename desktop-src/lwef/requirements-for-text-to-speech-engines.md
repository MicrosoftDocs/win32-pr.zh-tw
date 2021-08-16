---
title: 文字轉換語音引擎的需求
description: 文字轉換語音引擎的需求
ms.assetid: 21d19949-c9b4-4d9c-9684-6d15162f7a7d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3025be266d0aa40cd5a3bca6adb63e333310df444be7bd07e3a72b0f10b9c49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118746413"
---
# <a name="requirements-for-text-to-speech-engines"></a>文字轉換語音引擎的需求

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

引擎必須完全符合 SAPI 4.0 規範。 此外，引擎也必須支援下列用於標記文字和書簽通知的 SAPI 介面。 這些介面可讓 Microsoft 代理程式將文字輸出的步調和字元的字組文字提示保持一致，並將字元的嘴 (或對等的) 與說話的單字進行同步處理。

-   [ITTSCentralW](ittscentralw.md)
-   [ITTSNotifySinkW](ittsnotifysinkw.md)
-   [ITTSBufNotifySinkW](ittsbufnotifysinkw.md)
-   [ITTSAttributesW](ittsattributesw.md)

 

 




