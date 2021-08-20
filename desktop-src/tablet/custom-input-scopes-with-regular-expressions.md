---
description: 您可以使用手寫的正則運算式所組成的語言模型來定義自訂輸入範圍，並將其指派給欄位。例如，如果您要為倉儲元件建立資料庫應用程式，並希望使用者能夠使用 Tablet PC 輸入面板的手寫板來輸入零件編號。 如果元件編號語法包含三個字母，後面接著四個數字，後面接著另一個字母 (例如，ABC1234D) ，則手寫辨識器會因為未在語言模型中定義，而難以辨識這類輸入。 沒有任何預先定義的模擬程式對應到這類語法，Microsoft 也不會針對應用程式可能需要的每個可能欄位包含語法。 手寫的正則運算式提供簡單的方法，讓應用程式針對特定的特殊用途欄位定義自己的語言模型。注意：在使用已啟用筆墨的應用程式中使用 RecognizerCoNtext 物件的「模擬」屬性時，您無法在正則運算式中使用第1版的 factoids。
ms.assetid: 71f80196-0a36-4a14-a115-712bc909f6d7
title: 使用正則運算式的自訂輸入範圍
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2349893e4a4f478924a20877d0dec94d63a8adda8bea17eba8c8f029c63d5077
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118045875"
---
# <a name="custom-input-scopes-with-regular-expressions"></a>使用正則運算式的自訂輸入範圍

您可以使用手寫的正則運算式所組成的語言模型來定義自訂輸入範圍，並將其指派給欄位。

例如，如果您要為倉儲元件建立資料庫應用程式，並希望使用者能夠使用 Tablet PC 輸入面板的手寫板來輸入零件編號。 如果元件編號語法包含三個字母，後面接著四個數字，後面接著另一個字母 (例如，ABC1234D) ，則手寫辨識器會因為未在語言模型中定義，而難以辨識這類輸入。 沒有任何預先定義的模擬程式對應到這類語法，Microsoft 也不會針對應用程式可能需要的每個可能欄位包含語法。 手寫的正則運算式提供簡單的方法，讓應用程式針對特定的特殊用途欄位定義自己的語言模型。

> [!Note]  
> 在使用 [**RecognizerCoNtext**](inkrecognizercontext-class.md)物件之 [[**模擬**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid)] 屬性的啟用筆墨的應用程式中工作時，您無法在正則運算式中使用第1版的 factoids。

 

 

 



