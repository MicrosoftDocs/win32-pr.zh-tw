---
title: 擷取錯誤資訊
description: 擷取錯誤資訊
ms.assetid: 51a0e401-43f2-4738-9799-a96e2580a29f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e26844505b7c5de3e39c3199a6087c94f35bed9f64ef11a65d1c6df9a3dd4e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118309650"
---
# <a name="retrieving-error-information"></a>擷取錯誤資訊

使用 COM 錯誤處理介面和函式時，您可以如下所示取得錯誤資訊：

1.  檢查傳回的值是否代表物件已準備好處理的錯誤。
2.  呼叫 [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) 以取得 [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo) 介面的指標。 然後呼叫 [**ISupportErrorInfo：： InterfaceSupportsErrorInfo**](/windows/win32/api/oaidl/nf-oaidl-isupporterrorinfo-interfacesupportserrorinfo) ，以確認此錯誤是由傳回它的物件所引發，而且錯誤物件與目前的錯誤相關，而不是先前的呼叫。
3.  若要取得錯誤物件的指標，請呼叫 [**GetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-geterrorinfo) 函數。
4.  若要從錯誤物件取出資訊，請使用 [**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo) 方法。

如果物件未準備好處理錯誤，但需要將錯誤資訊向下傳播至呼叫鏈，則應該只將傳回值傳遞給它的呼叫端。 因為 [**GetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-geterrorinfo) 函式會清除錯誤資訊，並將錯誤物件的擁有權傳遞給呼叫者，所以函式只能由處理錯誤的物件呼叫。

 

 