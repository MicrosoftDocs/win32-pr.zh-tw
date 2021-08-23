---
title: 若要建立轉散發設定
description: 若要建立轉散發設定
ms.assetid: cf2c8fa1-cfd6-47cc-b572-ba1b95d59105
keywords:
- Windows媒體格式 SDK，軟體轉散發
- Advanced Systems Format (ASF) 、軟體轉散發
- ASF (Advanced Systems Format) ，軟體轉散發
- Windows媒體格式 SDK，轉散發
- Advanced Systems Format (ASF) ，轉散發
- ASF (Advanced Systems Format) ，轉散發
- 軟體轉散發，建立
- 軟體轉散發，WMFDist.exe
- 轉散發，建立
- 轉散發，WMFDist.exe
- WMFDist.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bb26b63a2379a72e2d97df876d91d8c57a6da9249c4e40525e81edacaf86542
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027296"
---
# <a name="to-create-a-redistribution-setup"></a>若要建立轉散發設定

1.  讓您的安裝程式常式先安裝應用程式檔，並進行必要的設定，再叫用轉散發套件。
2.  安裝 WMFDist.exe。 您可以使用/Q：旗標來執行無訊息自動安裝，並在應用程式安裝期間隱藏轉散發安裝程式的使用者介面。 然後，您的常式必須偵測到結束時是否需要重新開機。

    例如：

    ```C++
    WMFDist.exe /Q:A
    ```

    

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**軟體轉散發**](software-redistribution.md)
</dt> </dl>

 

 




