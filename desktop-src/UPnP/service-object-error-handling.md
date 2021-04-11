---
title: 服務物件錯誤處理
description: 當服務物件中發生錯誤時，呼叫 IDispatch 調用的傳回值應該會出現 \_ E \_ 例外狀況，而中 EXCEPTINFO 結構的 pExceptInfo 參數指標應填入。
ms.assetid: 1b08c404-69f2-4b0d-9231-c2bd242e124d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fd39d08dc7ca5152ca412df1a6fb67d6df524f2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092811"
---
# <a name="service-object-error-handling"></a>服務物件錯誤處理

當服務物件中發生錯誤時，呼叫 [**IDispatch：： Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke)的傳回值應該會出現 \_ E \_ 例外狀況，並在中填入 [**EXCEPTINFO**](/windows/win32/api/oaidl/ns-oaidl-excepinfo)結構的 *pExceptInfo* 參數指標。

具體而言，裝置主機會使用 [**EXCEPTINFO**](/windows/win32/api/oaidl/ns-oaidl-excepinfo)結構的 **bstrSource** 和 **bstrDescription** 成員，以 upnp 技術建立 upnp 錯誤回應;**bstrSource** 是錯誤碼，而 **bstrDescription** 則是錯誤描述。

 

 