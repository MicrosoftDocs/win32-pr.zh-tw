---
description: 下列功能可讓應用程式儲存、還原和重設裝置內容： SaveDC、RestoreDC 和 ResetDC。
ms.assetid: 22837876-2665-49c6-908e-80e107fc09f4
title: 儲存、還原和重設裝置內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2714360c07f4a4eca354ede5b460864cc897e58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973268"
---
# <a name="saving-restoring-and-resetting-a-device-context"></a>儲存、還原和重設裝置內容

下列功能可讓應用程式儲存、還原和重設裝置內容： [**SaveDC**](/windows/desktop/api/Wingdi/nf-wingdi-savedc)、 [**RestoreDC**](/windows/desktop/api/Wingdi/nf-wingdi-restoredc)和 [**ResetDC**](/windows/desktop/api/Wingdi/nf-wingdi-resetdca)。 SaveDC 函式會在特殊的 GDI 堆疊上記錄目前的 DC 繪圖物件及其屬性和圖形模式。 繪圖應用程式可以在使用者開始繪圖之前呼叫這個函式，並儲存應用程式的原始狀態，為使用者提供乾淨的平板。 若要返回此原始狀態，應用程式會呼叫 RestoreDC 函數。

提供 [**ResetDC**](/windows/desktop/api/Wingdi/nf-wingdi-resetdca)以重設印表機 DC 資料。 應用程式會呼叫此函式，以重設紙張方向、紙張大小、輸出縮放比例、要列印的份數、紙張來源 (或 bin) 、雙工模式等等。 一般而言，應用程式會在使用者變更其中一個印表機選項，且系統已發出 [**WM \_ DEVMODECHANGE**](wm-devmodechange.md) 訊息之後，呼叫此函式。

 

 



