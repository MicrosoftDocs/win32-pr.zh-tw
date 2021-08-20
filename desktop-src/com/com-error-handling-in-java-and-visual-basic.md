---
title: JAVA 和 Visual Basic 中的 COM 錯誤處理
description: JAVA 和 Visual Basic 中的 COM 錯誤處理
ms.assetid: 1130a038-3c18-4530-a6d7-9f538352297f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ba8e179ca3e7a1d57fdae63e8ad20d14a6fff358fab1fff24bfe7ae8df185d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048516"
---
# <a name="com-error-handling-in-java-and-visual-basic"></a>JAVA 和 Visual Basic 中的 COM 錯誤處理

在 JAVA 或 Microsoft Visual Basic 中進行程式設計時，可在 COM 中使用三個介面和三個函式來提供錯誤處理。 在 JAVA 和 Visual Basic 中，方法呼叫不會傳回 **HRESULT** 作為傳回值。 相反地，這些語言會使用 COM 介面和函式來取得 **HRESULT** 值，以及處理錯誤或例外狀況。  (例外狀況是程式控制項以外的事件，例如檔案問題或不正確參數。 ) 

下表將列出提供 **HRESULT** 支援的三個介面，並簡短說明。



|  介面                                                                        |  描述                                                                                                                    |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**ICreateErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-icreateerrorinfo)<br/>  | 設定錯誤資訊。<br/>                                                                                   |
| [**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo)<br/>        | 從錯誤物件傳回信息。<br/>                                                                 |
| [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo)<br/> | 將物件識別為支援 [**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo) 介面。<br/> |



 

提供 **HRESULT** 的支援的三個函式會在下表中列出並簡短說明。



|    介面       |       描述       |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-createerrorinfo)<br/> | 建立泛型錯誤物件的實例。<br/>                                                                                                            |
| [**GetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-geterrorinfo)<br/>    | 取得上一次呼叫目前邏輯執行緒中的 [**SetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo) 所設定的錯誤資訊指標。<br/> |
| [**SetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo)<br/>    | 為目前執行中的執行緒設定錯誤資訊物件。<br/>                                                                                    |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM 中的錯誤處理](error-handling-in-com.md)
</dt> </dl>

 

