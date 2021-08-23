---
title: 伺服器指導方針
description: 若要讓 Microsoft Active Accessibility 依照設計的方式運作，伺服器必須提供協助工具資訊給用戶端。
ms.assetid: 88be4bae-fdeb-467c-b5b1-19f2adc0575d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00b92d70a33dc8d397ff84fc3b9901dba044741d3044f6a7b7f6d1226aa5b683
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119614548"
---
# <a name="server-guidelines"></a>伺服器指導方針

若要讓 Microsoft Active Accessibility 依照設計的方式運作，伺服器必須提供協助工具資訊給用戶端。

若要執行 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)，伺服器開發人員必須遵循此基本流程。

1.  為您的自訂使用者介面專案和應用程式的用戶端，執行 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性和方法，以建立可存取的物件。 請務必提供同時支援 **IAccessible** 和 [**IDispatch**](idispatch-interface.md)的雙重介面，讓以 Microsoft Visual Basic 撰寫的用戶端和各種指令碼語言可以取得物件的相關資訊。
2.  呼叫 [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) 以通知用戶端變更您的自訂使用者介面元素。
3.  處理 [**WM \_ GETOBJECT**](wm-getobject.md) 以提供存取權給您的可存取物件。

如需設計可存取物件的建議和指導方針，請參閱 [Active Accessibility 伺服器的開發人員指南](developer-s-guide-for-active-accessibility-servers.md)。

## <a name="in-this-section"></a>本節內容

-   [伺服器如何執行子系識別碼](how-servers-implement-child-ids.md)

 

 




