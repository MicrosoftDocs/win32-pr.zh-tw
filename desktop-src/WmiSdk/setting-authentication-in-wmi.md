---
description: 在呼叫進程以外或遠端 WMI 服務中進行呼叫時，WMI 會使用元件物件模型的分散式版本 (DCOM) 。
ms.assetid: 261b4f18-5de5-4e06-a887-f5afd9c45511
ms.tgt_platform: multiple
title: 在 WMI 中設定驗證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0293d74c528e7c1c0e77a1ffb9f5f9ee7dfd5f00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193634"
---
# <a name="setting-authentication-in-wmi"></a>在 WMI 中設定驗證

在呼叫進程以外或遠端 WMI 服務中進行呼叫時，WMI 會使用元件物件模型的分散式版本 (DCOM) 。 跨進程和遠端呼叫是透過 proxy 進行，需要驗證呼叫進程的認證。

連接到電腦和 WMI 命名空間時，您可以設定驗證等級。 若要連接至 WMI，請在 c + + 中呼叫 [**IWbemLocator：： ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) 。 在腳本或 Visual Basic 中，您可以使用 Wbemscripting.swbemlocator ConnectServer 或透過 [標記](constructing-a-moniker-string.md) 字串連接至 WMI。 DCOM 安全性和 WMI 在電腦之間連接時都需要某些驗證等級。 必要層級會根據您所連接的作業系統而有所不同。 如需詳細資訊，請參閱 [連接到遠端電腦上的 WMI](connecting-to-wmi-on-a-remote-computer.md)。

WMI 通常會在共用服務主機中執行，並與主機中的其他進程共用相同的驗證。 若要以不同層級的驗證執行 WMI 進程，請使用 [**winmgmt**](winmgmt.md) 命令搭配 **/standalonehost** 參數來執行 wmi，並一般設定 wmi 的驗證層級。 如需詳細資訊，請參閱 [維護 WMI 安全性](maintaining-wmi-security.md)。

如需如何為 WMI 連接設定驗證的詳細資訊和程式碼範例，請參閱 [使用 VBScript 設定驗證服務](setting-the-authentication-service-using-vbscript.md) 和 [使用 c + + 設定驗證](setting-authentication-using-c-.md)。 這些主題也包含列出 c + + 和腳本之驗證常數的資料表。

## <a name="using-proxies-in-wmi"></a>在 WMI 中使用 proxy

若要設定 proxy 的驗證，請呼叫 [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) 函數。 如需詳細資訊和程式碼範例，請參閱 [設定 IWbemServices 和其他 proxy 的安全性](setting-the-security-on-iwbemservices-and-other-proxies.md)。

下列 [適用于 WMI 物件的 COM API](com-api-for-wmi.md) 會直接在 c + + 或 c # 中使用 proxy，以呼叫進程外或遠端 WMI 服務：

-   [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)
-   [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject)
-   [**IWbemCallResult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult)
-   [**IWbemRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher)

腳本物件（例如 [**SWbemObject**](swbemobject.md)、 [**SWbemServices**](swbemservices.md)和 [**SWbemRefresher**](swbemrefresher.md) ）不會直接使用 proxy。 相反地，腳本物件代表包裝函式或圖層，可針對上面所列的 WMI 物件呼叫 [COM API](com-api-for-wmi.md) 。 如需在腳本中設定驗證的詳細資訊和程式碼範例，請參閱 [使用 VBScript 設定預設進程安全性層級](setting-the-default-process-security-level-using-vbscript.md)。

 

 
