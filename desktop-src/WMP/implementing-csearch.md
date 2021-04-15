---
title: 執行 CSearch
description: 執行 CSearch
ms.assetid: 3041807a-e7e0-4022-ab90-a8b846bafc0e
keywords:
- Windows Media Player 外掛程式、CSearch 類別
- 外掛程式，CSearch 類別
- 使用者介面外掛程式、CSearch 類別
- UI 外掛程式、CSearch 類別
- CSearch 類別
- 程式設計指南，使用者介面外掛程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f36c6446ca0eb6b1cc9dfb5f45044493c2a8fd6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507132"
---
# <a name="implementing-csearch"></a>執行 CSearch

**IWMPPluginUI** 介面有幾個方法，這些方法會在外掛程式實例的生命週期期間，Windows Media Player 于不同的時間呼叫。 Wizard 提供這些方法的基本執行，以及類別的函式和函式，以及其他類別的方法。 您必須修改搜尋 .h 檔案，以便 Windows Media Player 可以與 UI 通訊，如下一節所述。

若要讓 CPluginWindow 類別擁有私用成員變數 m spCore 的存取權 \_ ，您必須在 CSearch 類別定義中建立 friend 類別宣告，如下列程式碼片段所示：


```C++
class ATL_NO_VTABLE CSearch : 
    public CComObjectRootEx<CComSingleThreadModel>,
    public CComCoClass<CSearch, &CLSID_Search>,
    public IWMPPluginUI
{

friend class CPluginWindow;

// Rest of class definition...

}

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**消費者介面外掛程式程式設計指南**](user-interface-plug-ins-programming-guide.md)
</dt> </dl>

 

 




