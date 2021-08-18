---
title: IADs 和 IDirectoryObject 介面
description: ADSI 用戶端會使用兩個 COM 介面 IADs 或 IDirectoryObject 中的其中一個來管理和操作目錄服務物件。
ms.assetid: f9c486b0-3dfb-4abf-afbf-08749e04315f
ms.tgt_platform: multiple
keywords:
- IADs ADSI，關於
- IDirectoryObject ADSI，關於
- ADSI ADSI、using、IADs 和 IDirectoryObject 介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dccfa643c0076224abece6f449f20caf5a4de5d378c03d37cf0e2248ed5a50b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117838378"
---
# <a name="the-iads-and-idirectoryobject-interfaces"></a>IADs 和 IDirectoryObject 介面

ADSI 用戶端會使用兩個 COM 介面的其中一個來管理和操作目錄服務物件： [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) 或 [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject)。 **IADs** 是一個 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面，可供晚期繫結的用戶端使用，例如以 Microsoft Visual Basic、JAVA 和各種指令碼語言撰寫的用戶端。 **IDirectoryObject** 是一種 vtable 介面，可讓您直接存取以 C 和 c + + 撰寫的早期繫結用戶端物件。

每個 ADSI 物件都必須同時執行 [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) 和 [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject)。 以 C 或 c + + 等語言撰寫的 ADSI 用戶端（可以直接存取 vtable）可以使用任一種介面，但不能同時在相同的應用程式中使用。 以 Visual Basic 或 JAVA 撰寫的 ADSI 用戶端僅限使用 **IADs**。

[**IADs**](/windows/desktop/api/Iads/nn-iads-iads)介面可讓晚期繫結用戶端利用 ADSI 物件模型的固有維護功能。 這些功能包括屬性快取，可讓用戶端讀取和寫入屬性，而不需要透過網路進行每次呼叫。 此外，用戶端應用程式也能充分利用功能強大的 UI 和 ActiveX 的控制項程式庫，以及更簡單的程式設計樣式。 在傳回時，晚期繫結用戶端必須使用 **VARIANT** 資料類型，這會使用 ADSI 所提供的更豐富原生資料類型來排除。

[**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject)介面讓較早系結的用戶端能夠充分利用原生目錄服務的資料類型，但在上述的成本上，使用屬性快取的效能會稍微低一點。 **IDirectoryObject** 介面會透過單一要求（而不是透過個別的 **get** 和 **put** 呼叫），提供物件屬性的直接線上存取。

 

 