---
title: 如何呼叫 WMI 方法
description: WMI 的主要用途是提供類別和實例的存取權，以代表網路上的物件。
ms.assetid: 8d559eee-3dbf-4132-b1c0-a6925b8feb56
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9d1de14f06388454228528d5a419b551ae2ed0d72c82e3b78c9e04855db6619
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051046"
---
# <a name="how-to-call-a-wmi-method"></a>如何呼叫 WMI 方法

WMI 的主要用途是提供類別和實例的存取權，以代表網路上的物件。 提供者支援這些類別和實例。 例如，所有代表您企業上標準硬體裝置的實例（例如 [**win32 \_ PhysicalMemory**](/windows/desktop/CIMWin32Prov/win32-physicalmemory) 或 [**win32 \_ 印表機**](/windows/desktop/CIMWin32Prov/win32-printer)）都受到 win32 提供者的支援。 同樣地，您可以透過事件記錄檔提供者，以及透過登錄提供者的登錄來存取事件記錄檔。

WMI 在介面（例如 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) 或腳本物件，例如 [**SWbemServices**](swbemservices.md)）中所實行的方法，主要是用來一般取得和操作任何提供者所提供的資料。 例如，您可以使用 [**SWbemServices InstancesOf**](swbemservices-instancesof.md) ，在企業電腦的子集中取得 [**Win32 \_ 進程**](/windows/desktop/CIMWin32Prov/win32-process) 的所有實例。 然後，您可以在每個 **win32 \_ 處理** 程式物件上呼叫 Win32 提供者方法 [**GetOwnerSid**](/windows/desktop/CIMWin32Prov/getownersid-method-in-class-win32-process) 。

在下列範例中， [**GetOwnerSid**](/windows/desktop/CIMWin32Prov/getownersid-method-in-class-win32-process) 方法會在處理常式物件上被稱為 automation 方法。 WMI 方法（例如針對 [**SWbemObject**](swbemobject.md)所定義的 [**路徑 \_**](swbemobject-path-.md)方法）也可以在 **處理** 程式物件上呼叫。


```VB
Set ProcessCollection = _
    GetObject("WinMgmts:").InstancesOf("Win32_Process")

For Each Process In ProcessCollection
    SID = Process.GetOwnerSid
Next
```



使用 WMI 方法的實際處理方式，與使用任何其他 Windows COM 或 automation 介面相同。 如需詳細資訊，請參閱 [COM](../cossdk/component-services-portal.md) 和 [建立 WMI 應用程式或腳本](creating-a-wmi-application-or-script.md)。 如需 WMI 所支援介面的詳細資訊，請參閱適用于 wmi 的 [COM api](com-api-for-wmi.md) 和 [適用于 WMI 的腳本 API](scripting-api-for-wmi.md)。

如需詳細資訊，請參閱 [操作類別和實例資訊](manipulating-class-and-instance-information.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[呼叫方法](calling-a-method.md)
</dt> </dl>

 

 
