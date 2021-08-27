---
description: 物件是由標準標頭和物件特有的屬性所組成。 因為所有物件都有相同的結構，所以 Windows 中有一個會維護所有物件的物件管理員。
ms.assetid: 104113f3-bfd1-4ff7-b92f-2f753c0f5185
title: 物件管理員
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b87b239d685d53b29243212e06ba2fd5af20e1249794355ed2169278c7f46c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118885346"
---
# <a name="object-manager"></a>物件管理員

物件是由標準標頭和物件特有的屬性所組成。 因為所有物件都有相同的結構，所以 Windows 中有一個會維護所有物件的物件管理員。

物件標頭包含物件名稱之類的專案，讓其他進程可以依名稱參考物件，並提供安全描述項，讓物件管理員可以控制哪些進程存取系統資源。

物件管理員執行的工作包括下列各項：

-   建立物件
-   確認處理常式具有使用物件的許可權
-   建立物件控制碼，並將其傳回給呼叫者
-   維護資源配額
-   建立重複的控制碼
-   關閉物件的控制碼

 

 



