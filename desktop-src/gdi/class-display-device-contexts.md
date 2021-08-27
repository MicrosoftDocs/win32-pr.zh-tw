---
description: 藉由使用類別裝置內容，應用程式可以針對屬於指定類別的每個視窗使用單一顯示裝置內容。
ms.assetid: fc76abbf-68da-47f2-8145-4fad806297b4
title: 類別顯示裝置內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b8e4ca7f7d51f3dd50f50a07ab44496d56e4a78effb78f33e9eed6f5ffc3745
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062478"
---
# <a name="class-display-device-contexts"></a>類別顯示裝置內容

藉由使用 *類別裝置內容*，應用程式可以針對屬於指定類別的每個視窗使用單一顯示裝置內容。 類別裝置內容通常會搭配使用相同屬性值繪製的控制項視窗使用。 如同私用裝置內容，類別裝置內容會將準備裝置內容以進行繪製所需的時間降到最低。

如果視窗屬於具有 CS CLASSDC 樣式的視窗類別，系統就會為該視窗提供類別裝置內容 \_ 。 系統會在建立屬於類別的第一個視窗時建立裝置內容，然後針對類別中所有後續建立的視窗使用相同的裝置內容。 一開始，類別裝置內容具有與一般裝置內容相同的屬性預設值，但應用程式可以隨時修改這些屬性。 系統會保留所有變更（除了裁剪區域和裝置原點以外），直到類別中的最後一個視窗終結為止。 針對某個視窗所做的變更會套用至該類別中的所有視窗。

應用程式可以在第一個視窗建立之後，隨時使用 [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) 函式來取得類別裝置內容的控制碼。 應用程式可以保留並使用控制碼，而不需要釋放它，因為類別裝置內容不是顯示裝置內容快取的一部分。 如果應用程式在相同的視窗類別中建立另一個視窗，則應用程式必須再次取出類別裝置內容。 抓取裝置內容會設定新視窗的正確裝置原點和裁剪區域。 在應用程式抓取類別中新視窗的類別裝置內容之後，就無法再使用裝置內容在原始視窗中繪製，而不需要再次針對該視窗進行抓取。 一般情況下，每次都必須在視窗中繪製時，應用程式就必須明確地取出視窗的類別裝置內容。

使用類別裝置內容的應用程式應該一律在處理 [**WM \_ 油漆**](wm-paint.md)訊息時呼叫 [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) 。 此函式會設定視窗的正確裝置原點和裁剪區域，並併入更新區域。 如果 **BeginPaint** 將它隱藏，則應用程式也應該呼叫 [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint)來還原插入號。 **EndPaint** 對類別裝置內容沒有任何其他影響。

將 [**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md) 訊息傳送至應用程式時，系統會傳遞類別裝置內容，允許目前的屬性值影響應用程式或系統在處理此訊息時所執行的任何繪製。 使用具有私用裝置內容的視窗時，應用程式可以使用 [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) 來強制系統傳回具有類別裝置內容之視窗的一般裝置內容。

不建議使用類別裝置內容。

 

 
