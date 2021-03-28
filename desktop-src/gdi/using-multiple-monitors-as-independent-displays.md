---
description: 使用多個監視器作為獨立顯示器時，桌面會包含一或一組顯示器。
ms.assetid: fbc88c91-3209-4b59-bdbb-0f5ba009a312
title: 使用多個監視器作為獨立顯示器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4761e0e04ae1adaa197b06f04fa36c61ccda3083
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973625"
---
# <a name="using-multiple-monitors-as-independent-displays"></a>使用多個監視器作為獨立顯示器

使用多個監視器作為獨立顯示器時，桌面會包含一或一組顯示器。 這組顯示器一律會包含主要監視器，而且會如本主題的其他章節所述運作。 應用程式可以使用任何其他監視器作為獨立顯示器。

> [!Note]  
> 在 Windows 顯示驅動程式模型 (WDDM) 的驅動程式上，不支援使用其他監視器作為獨立顯示器。

 

「視窗管理員」並不知道任何獨立顯示器。 這些是由應用程式完全控制，且應用程式不能使用任何視窗管理員函式 (所有視窗管理員呼叫都會自動移至主顯示器) 。 每個獨立顯示器都有自己的原點和水準和垂直座標，而且是透過 [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) 或 DirectX 函式（例如 **DIRECTDRAWCREATE**）的 GDI 函數來存取。

若要找出獨立顯示器，請呼叫 [**EnumDisplayDevices**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaydevicesa) ，並 \_ \_ \_ \_ 在 [**顯示 \_ 設備**](/windows/desktop/api/Wingdi/ns-wingdi-display_devicea) 結構中尋找未將顯示裝置附加至桌面旗標的顯示器。

應用程式可以藉由呼叫來開啟顯示器


```C++
hdc = CreateDC(lpszDisplayName, NULL, NULL, lpDevMode);
```



在此呼叫中， *lpszDisplayName* 參數是 [**EnumDisplayDevices**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaydevicesa) 所傳回的其中一個裝置名稱，而 *lpDevMode* 是此裝置之圖形模式的描述。 產生的 hdc 可以用來對裝置執行任何圖形作業。

 

 



