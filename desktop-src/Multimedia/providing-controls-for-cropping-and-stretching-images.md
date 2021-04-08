---
title: 提供用於裁剪和延展影像的控制項
description: 提供用於裁剪和延展影像的控制項
ms.assetid: cc62d70d-3f5f-477c-bc09-ab8ab0a9dce3
keywords:
- MCIWndGetSource 宏
- MCIWndPutSource 宏
- MCIWndGetDest 宏
- MCIWndPutDest 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cd0889b40204e7c99ec782e454dba2cdeebfe79
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103681735"
---
# <a name="providing-controls-for-cropping-and-stretching-images"></a>提供用於裁剪和延展影像的控制項

MCIWnd 可讓您裁剪和延展影片剪輯的影像。 若要瞭解這些功能，您必須瞭解 *框架大小*、 *來源矩形*、 *目的地矩形* 和 *播放區域* 之間的關聯性。

影片剪輯由數個框架組成，每個都包含一個影像。 影片剪輯的框架大小是目前畫面格的影像大小。 影片剪輯通常有一個畫面格大小，因為剪輯中的所有影像大小都相同。

來源矩形是重迭影片剪輯框架的矩形區域。 來源矩形會定義播放期間顯示之每個畫面格的部分。 使用 MCIWnd 載入影片剪輯時，來源矩形會使用與影片剪輯的初始框架相同的維度和位置進行初始化。

目的地矩形是定義虛擬播放視窗的矩形區域。 目的地矩形會從影片剪輯的每個畫面格接收來源矩形的影像資料。 當來源和目的地矩形維度不同時，MCIWnd 會視需要以水準和垂直方式調整影像資料以填滿目的地矩形。 使用 MCIWnd 載入影片剪輯時，會使用與影片剪輯的初始框架相同的維度和位置來初始化目的地矩形。

播放區域是 MCIWnd 視窗中應用程式用來顯示影片剪輯的部分。 播放區域是 MCIWnd 視窗的工作區，或工作區中排除 MCIWnd 工具列的部分。 使用 MCIWnd 載入影片剪輯時，會使用與影片剪輯的初始框架相同的維度和位置來初始化播放區域。

您可以使用 [**MCIWndGetSource**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetsource) 和 [**MCIWndPutSource**](/windows/desktop/api/Vfw/nf-vfw-mciwndputsource) 宏來改變來源矩形，以裁剪影片剪輯。 裁剪影像只會決定播放期間顯示的畫面格部分;它不會改變所播放檔案的內容。 裁剪影像之前，您可以使用 **MCIWndGetSource** 來取出來源矩形的目前大小。 計算來源矩形的新大小和位置之後，您可以使用 **MCIWndPutSource** 來設定來源矩形的裁剪界限。

您可以使用 [**MCIWndGetDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdest) 和 [**MCIWndPutDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndputdest) 宏來改變目的地矩形，以延展影片剪輯。 當您延展影片剪輯時，您會以垂直、水準或雙向方式加長或縮短影片剪輯的框架大小。 在延展影像之前，您可以使用 **MCIWndGetDest** 來取出目的地矩形目前的大小和位置。 **MCIWndPutDest** 宏可讓您重新定義目的地矩形。 延展可能會在播放期間扭曲影像，但不會改變所播放檔案的內容。

如果目的地矩形的大小變得大於播放區域，您可以使用 **MCIWndPutDest** 來指定播放區域的哪個部分會顯示影片剪輯。

> [!Note]  
> [**MCIWndPutDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndputdest)宏不會變更播放區域的大小。 若要將 MCIWnd 視窗和目的地矩形伸展，您需要知道 [MCIWnd] 視窗的目前大小，並根據目的地矩形來發出新的視窗尺寸。 您可以使用 [GetWindowRect](/windows/win32/api/winuser/nf-winuser-getwindowrect) 函數，並使用 [SetWindowPos](/windows/win32/api/winuser/nf-winuser-setwindowpos) 函數來調整 MCIWnd 視窗的大小，以抓取 MCIWnd 視窗維度。

 

 

 