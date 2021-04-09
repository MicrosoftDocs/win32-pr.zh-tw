---
title: 使用 QueryService 來取出 IAccessible 物件的原生介面
description: 伺服器開發人員可以使用這項技術，將指標公開給 IAccessible 物件的自訂檔節點。 這假設您已經公開 IAccessible 物件。 這項技術可讓用戶端從 IAccessible 物件取得自訂物件。
ms.assetid: aaa0e840-f8c2-4f3d-9d97-1910f00c1041
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29d971462154eb12789a74e8cc6edb5aed68c84b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023772"
---
# <a name="use-queryservice-to-retrieve-a-native-interface-for-an-iaccessible-object"></a>使用 QueryService 來取出 IAccessible 物件的原生介面

伺服器開發人員可以使用這項技術，將指標公開給 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 物件的自訂檔節點。 這假設您已經公開 **IAccessible** 物件。 這項技術可讓用戶端從 **IAccessible** 物件取得自訂物件。

**若要公開 IAccessible (伺服器的原生物件模型)**

1.  在 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)物件上加入 **IServiceProvider** 介面的支援。
2.  定義 GUID，代表從 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 物件取得自訂介面的功能。 這稱為服務識別碼。 如果您有自訂介面，您可以使用 GUIDGEN.EXE 來產生服務識別碼，或重複使用介面識別碼。
3.  執行 **IServiceProvider：： QueryService** 方法，如此一來，當使用此程式稍早定義的服務識別碼呼叫自訂介面時，它就會傳回該介面的指標。 **QueryService** 應該針對所有其他服務識別碼值傳回 **Null** 。
4.  發佈服務識別碼，讓用戶端可以使用它。

用戶端可以使用此功能，從 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 物件取得自訂物件的指標。

**從 IAccessible (用戶端取得自訂物件的指標)**

1.  [](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) \_ 在 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)介面指標上呼叫 QueryInterface (IID IServiceProvider) ，以取得 **IServiceProvider** 介面指標。
2.  使用已發佈的服務識別碼呼叫 **IServiceProvider：： QueryService** ，以取得 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)之自訂物件的指標。
3.  如果不再需要，請釋放 **IServiceProvider** 介面。

若要跨進程使用，伺服器可能需要向元件物件模型註冊傳回的介面 (COM) 。

Microsoft Internet Explorer 4.0 和更新版本使用此技術。 它可讓用戶端取得對應至 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)物件的 **IHTMLElement2** 介面指標。

 

 