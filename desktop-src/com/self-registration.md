---
title: Self-Registration
description: 自我註冊是一種標準方法，可讓伺服器模組將本身的登錄作業（登錄和取消註冊）封裝到模組本身。
ms.assetid: fb5dcb2b-b0e3-4f37-a8e7-b84b9a265227
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23c95d422213b8e33ac89b89408ed95724f0769b
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104463764"
---
# <a name="self-registration"></a>Self-Registration

隨著元件軟體持續以市場的形式成長，將會有更多的實例，讓使用者以單一 DLL 或 EXE 模組的形式取得新的軟體元件，例如從線上服務下載新元件，或從磁片磁碟機上的朋友接收一個新元件時。 在這些情況下，要求使用者經過冗長的安裝程式或安裝程式並不可行。 除了透過 [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2)處理的授權問題之外，安裝程式通常會建立必要的登錄專案，讓元件在 COM 和 OLE 內容中正確執行。

自我註冊是一種標準方法，可讓伺服器模組將本身的登錄作業（登錄和取消註冊）封裝到模組本身。 與透過 [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2)處理的授權搭配使用時，伺服器可以成為完全獨立的模組，而不需要外部安裝程式或 .reg 檔案。

任何自行註冊模組（DLL 或 EXE）應該先在其版本資訊資源的 [StringFileInfo](/windows/desktop/menurc/stringfileinfo-block) 區段中包含 "OleSelfRegister" 字串，如下所示。

``` syntax
VS_VERSION_INFO VERSIONINFO 
 
 ... 
 
 BEGIN 
   BLOCK "StringFileInfo" 
    BEGIN 
#ifdef UNICODE 
     BLOCK "040904B0" // Lang=US English, CharSet=Unicode 
#else 
     BLOCK "040904E4" // Lang=US English, CharSet=Windows Multilingual 
#endif 
      BEGIN 
       ... 
       VALUE "OLESelfRegister", "\0" 
      END 
 
   ... 
 
   END 
 
 ... 
 
 END 
 
```

這項資料的存在可讓任何感興趣的合作物件（例如希望整合這個新元件的應用程式）判斷伺服器是否支援自我註冊，而不需要先載入 DLL 或 EXE。

如果伺服器封裝在 DLL 模組中，DLL 必須匯出函式 [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) 和 [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver)。 任何想要指示伺服器自行註冊 (也就是其 Clsid 和類型程式庫識別碼) 的任何應用程式都可以透過 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)函數取得 **DllRegisterServer** 的指標。 在 **DllRegisterServer** 內，dll 會建立所有必要的登錄專案，並為所有 [InprocServer32](inprocserver32.md) 或 [InprocHandler32](inprochandler32.md) 專案儲存 DLL 的正確路徑。

當應用程式想要從系統中移除元件時，它應該呼叫 [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver)來取消註冊該元件。 在此呼叫中，伺服器會完全移除先前在 [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver)中建立的專案。 伺服器不應該盲目移除其類別的所有專案，因為其他軟體可能已儲存額外的專案，例如 [TreatAs](treatas.md) 金鑰。

如果伺服器封裝在 EXE 模組中，則想要註冊伺服器的應用程式會使用命令列引數 **/RegServer** 或 **-RegServer** (不區分大小寫的) 來啟動 EXE 伺服器。 如果應用程式想要將伺服器取消註冊，它會使用命令列引數 **/UnregServer** 或 **-UnregServer** 啟動 EXE。 自我註冊 EXE 會偵測這些命令列引數，並在 [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver)和 [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver)中分別叫用 DLL 的相同作業，並在 [LocalServer32](localserver32.md) （而不是 **InprocServer32** 或 **InprocHandler32**）註冊其模組路徑。

伺服器必須註冊 DLL 或 EXE 模組安裝位置的完整路徑，以用於登錄中各自的 **InprocServer32**、 **InprocHandler32** 和 **LocalServer32** 機碼。 您可以透過 [**GetModuleFileName**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) 函數輕鬆地取得模組路徑。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[安裝為服務應用程式](installing-as-a-service-application.md)
</dt> <dt>

[在安裝時註冊類別](registering-a-class-at-installation.md)
</dt> <dt>

[註冊正在執行的 EXE 伺服器](registering-a-running-exe-server.md)
</dt> <dt>

[在 ROT 中註冊物件](registering-objects-in-the-rot.md)
</dt> </dl>

 

 