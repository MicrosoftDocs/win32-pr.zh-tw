---
description: 系統會維護快取，顯示其用於通用、父視窗和視窗裝置內容的顯示裝置內容。
ms.assetid: b017453a-c2c5-4bb1-ae46-f303d5e200ca
title: 顯示裝置內容快取
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d96bbf8cb388e31e43a0eacf9200b638fe8a232749dd5e2ef8ab67318b30d9de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062428"
---
# <a name="display-device-context-cache"></a>顯示裝置內容快取

系統會維護快取，顯示其用於通用、父視窗和視窗裝置內容的顯示裝置內容。 每當應用程式呼叫 [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) 或 [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) 函式時，系統就會從快取中抓取裝置內容;當應用程式後續呼叫 [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) 或 [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) 函式時，系統會將 DC 傳回給快取。

快取可保存的裝置內容數量沒有預先決定的限制;如果沒有可用的快取，系統會建立新的顯示裝置內容。 如此一來，應用程式一次可以有超過五個來自快取的作用中裝置內容。 不過，應用程式必須在使用之後繼續釋出這些裝置內容。 由於快取的新顯示裝置內容會在應用程式的堆積空間中配置，因此無法釋出裝置內容最後都會耗用所有可用的堆積空間。 系統會在無法為新的裝置內容配置空間時傳回錯誤，以指出此失敗。 與快取無關的其他函數也可能會傳回錯誤。

 

 



