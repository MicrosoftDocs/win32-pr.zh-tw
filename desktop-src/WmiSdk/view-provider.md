---
description: 視圖提供者是實例和方法提供者，可根據其他類別的實例建立新的類別。
ms.assetid: e1992e10-647b-4747-8f3d-b437ef7f3770
ms.tgt_platform: multiple
title: 視圖提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e49154504dfb2f71ec19c2275851befbdbf9a48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850747"
---
# <a name="view-provider"></a>視圖提供者

視圖提供者是實例和方法提供者，可根據其他類別的實例建立新的類別。 您可以使用視圖提供者，從不同的來源類別、不同的命名空間或不同的電腦取得屬性，並將屬性結合成單一類別。

作為實例和方法提供者，視圖提供者支援標準 [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) 介面和下列 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) 方法：

-   [**CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync)
-   [**ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)
-   [**ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)
-   [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)
-   [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)

如需有關用來定義 View 提供者類別之限定詞的詳細資訊，請參閱 [View provider 的特定限定詞](qualifiers-specific-to-the-view-provider.md)。

如需有關 views 的詳細資訊，請參閱將 [類別連結在一起](linking-classes-together.md)。

64位平臺上有兩個版本的 View provider。 如需詳細資訊，請參閱 [在64位電腦上取得和提供資料](getting-and-providing-data-on-a-64-bit-computer.md)。

視圖提供者會在 ViewProv.dll 中執行。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[WMI 提供者](wmi-providers.md)
</dt> </dl>

 

 



