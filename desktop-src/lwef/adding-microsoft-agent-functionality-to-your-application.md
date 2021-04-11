---
title: 將 Microsoft Agent 功能新增至您的應用程式
description: 將 Microsoft Agent 功能新增至您的應用程式
ms.assetid: 2b4816dd-11bf-4c17-873e-4bdbb7fa1ccf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a2972b0251a4114e5d280d8f739d416ebc5dc1c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314836"
---
# <a name="adding-microsoft-agent-functionality-to-your-application"></a>將 Microsoft Agent 功能新增至您的應用程式

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

若要存取 Microsoft 代理程式的伺服器介面，必須已在目標系統上安裝代理程式。 不支援使用代理程式自行安裝的可執行檔（例如嘗試複製和註冊代理程式元件檔）進行安裝。 這可確保一致且完全的安裝。 請注意，Microsoft 代理程式自行安裝檔案不會安裝在 Microsoft Windows 2000 和更新版本的作業系統上，因為這些版本的作業系統已經包含自己的代理程式版本。

若要在目標系統上成功安裝具有先前 Microsoft Windows 作業系統的代理程式，您也必須確定目標系統有最新版本的 Microsoft Visual C++ 執行時間 (Msvcrt.dll) 、Microsoft 註冊工具 (Regsvr32.dll) 和 Microsoft COM dll。 若要確保目標系統上的必要元件，最簡單的方式就是要求安裝 Microsoft Internet Explorer 3.02 或更新版本。 或者，您可以安裝 Microsoft Visual C++ 中提供的前兩個元件。 必要的 COM dll 可以安裝為 Microsoft DCOM update 的一部分，可在 Microsoft 網站上取得。 您可以在 Microsoft 網站上找到這些元件的進一步資訊和授權資訊。

代理程式的語言元件可以用同樣的方式來安裝。 同樣地，您可以使用這項技術，來安裝可從 Microsoft 代理程式網站散發的 Microsoft 字元 ACS 格式。 字元檔會自動安裝到 Microsoft 代理程式 \\ 字元子目錄。

因為 Microsoft 代理程式的元件是設計為作業系統元件，所以代理程式可能不會卸載。 同樣地，當代理程式已安裝為 Windows 作業系統的一部分時，代理程式自行安裝封包可能無法安裝。

一旦安裝之後，若要呼叫代理程式的介面，請建立伺服器的實例，並向伺服器支援使用標準 COM 慣例的特定介面要求指標。 尤其是，COM 程式庫會提供一個可建立物件實例的 API 函 [**式，並**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)傳回物件的要求介面指標。 要求 **CoCreateInstance** 呼叫中的 [**IAgent**](iagent.md)或 [**IAgentEx**](iagentex.md)介面指標，或在後續的 [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q))呼叫中要求指標。

下列程式碼將在 C/c + + 中說明這種情況。


```
hRes = CoCreateInstance(CLSID_AgentServer,
                     NULL,
                     CLSCTX_SERVER,
                     IID_IAgentEx,
                     (LPVOID *)&amp;pAgentEx);
```



如果 Microsoft 代理程式伺服器正在執行，此函式會連接到伺服器;否則，它會啟動伺服器。

請注意，Microsoft 代理程式伺服器介面通常會包含包含 "Ex" 尾碼的擴充介面。 這些介面衍生自，因此會包含其非 Ex 對應專案的所有功能。 如果您想要使用任何擴充功能，請使用 Ex 介面。

使用 [**SysAllocString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring)來 bstr 配置記憶體之指標的函式。 呼叫者必須負責使用 [**SysFreeString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring)釋放此記憶體。

 

 