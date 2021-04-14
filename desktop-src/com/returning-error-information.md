---
title: 傳回錯誤資訊
description: 傳回錯誤資訊
ms.assetid: 4206f2e5-db01-458c-93cb-10c5cd4a4536
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 303db82dc220d09d4db7f52bf4c04ad1e5ca691f
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104382914"
---
# <a name="returning-error-information"></a>傳回錯誤資訊

使用 COM 錯誤處理介面和函式，您可以藉由執行下列步驟來傳回錯誤資訊：

1.  執行 [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo) 介面。
2.  若要建立泛型錯誤物件的實例，請呼叫 [**CreateErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-createerrorinfo) 函數。
3.  若要設定其內容，請使用 [**ICreateErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-icreateerrorinfo) 方法。
4.  若要將錯誤物件與目前的邏輯執行緒產生關聯，請呼叫 [**SetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo) 函數。

錯誤處理介面會建立和管理 error 物件，此物件會提供錯誤的相關資訊。 錯誤物件與發生錯誤的物件不同。 它是與目前執行中線程相關聯的個別物件。

 

 