---
title: 傳回錯誤資訊
description: 傳回錯誤資訊
ms.assetid: 4206f2e5-db01-458c-93cb-10c5cd4a4536
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 545c697be7da64362ecce0f5b4c45272832ad682d8b4dd0eb5234620b993e5f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118309640"
---
# <a name="returning-error-information"></a>傳回錯誤資訊

使用 COM 錯誤處理介面和函式，您可以藉由執行下列步驟來傳回錯誤資訊：

1.  執行 [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo) 介面。
2.  若要建立泛型錯誤物件的實例，請呼叫 [**CreateErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-createerrorinfo) 函數。
3.  若要設定其內容，請使用 [**ICreateErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-icreateerrorinfo) 方法。
4.  若要將錯誤物件與目前的邏輯執行緒產生關聯，請呼叫 [**SetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo) 函數。

錯誤處理介面會建立和管理 error 物件，此物件會提供錯誤的相關資訊。 錯誤物件與發生錯誤的物件不同。 它是與目前執行中線程相關聯的個別物件。

 

 