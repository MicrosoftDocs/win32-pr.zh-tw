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
# <a name="self-registration"></a><span data-ttu-id="25df0-103">Self-Registration</span><span class="sxs-lookup"><span data-stu-id="25df0-103">Self-Registration</span></span>

<span data-ttu-id="25df0-104">隨著元件軟體持續以市場的形式成長，將會有更多的實例，讓使用者以單一 DLL 或 EXE 模組的形式取得新的軟體元件，例如從線上服務下載新元件，或從磁片磁碟機上的朋友接收一個新元件時。</span><span class="sxs-lookup"><span data-stu-id="25df0-104">As component software continues to grow as a market, there will be more and more instances where a user obtains a new software component as a single DLL or EXE module, such as when downloading a new component from an on-line service or receiving one from a friend on a floppy disk.</span></span> <span data-ttu-id="25df0-105">在這些情況下，要求使用者經過冗長的安裝程式或安裝程式並不可行。</span><span class="sxs-lookup"><span data-stu-id="25df0-105">In these cases, it is not practical to require the user to go through a lengthy installation procedure or setup program.</span></span> <span data-ttu-id="25df0-106">除了透過 [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2)處理的授權問題之外，安裝程式通常會建立必要的登錄專案，讓元件在 COM 和 OLE 內容中正確執行。</span><span class="sxs-lookup"><span data-stu-id="25df0-106">Besides the licensing issues, which are handled through [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2), an installation procedure typically creates the necessary registry entries for a component to run properly in the COM and OLE context.</span></span>

<span data-ttu-id="25df0-107">自我註冊是一種標準方法，可讓伺服器模組將本身的登錄作業（登錄和取消註冊）封裝到模組本身。</span><span class="sxs-lookup"><span data-stu-id="25df0-107">Self-registration is the standard means through which a server module can package its own registry operations, both registration and unregistration, into the module itself.</span></span> <span data-ttu-id="25df0-108">與透過 [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2)處理的授權搭配使用時，伺服器可以成為完全獨立的模組，而不需要外部安裝程式或 .reg 檔案。</span><span class="sxs-lookup"><span data-stu-id="25df0-108">When used with licensing handled through [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2), a server can become an entirely self-contained module with no need for external installation programs or .reg files.</span></span>

<span data-ttu-id="25df0-109">任何自行註冊模組（DLL 或 EXE）應該先在其版本資訊資源的 [StringFileInfo](/windows/desktop/menurc/stringfileinfo-block) 區段中包含 "OleSelfRegister" 字串，如下所示。</span><span class="sxs-lookup"><span data-stu-id="25df0-109">Any self-registering module, DLL or EXE, should first include an "OleSelfRegister" string in the [StringFileInfo](/windows/desktop/menurc/stringfileinfo-block) section of its version information resource, as shown here.</span></span>

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

<span data-ttu-id="25df0-110">這項資料的存在可讓任何感興趣的合作物件（例如希望整合這個新元件的應用程式）判斷伺服器是否支援自我註冊，而不需要先載入 DLL 或 EXE。</span><span class="sxs-lookup"><span data-stu-id="25df0-110">The existence of this data allows any interested party, such as an application that wishes to integrate this new component, to determine whether the server supports self-registration without having to load the DLL or EXE first.</span></span>

<span data-ttu-id="25df0-111">如果伺服器封裝在 DLL 模組中，DLL 必須匯出函式 [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) 和 [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver)。</span><span class="sxs-lookup"><span data-stu-id="25df0-111">If the server is packaged in a DLL module, the DLL must export the functions [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) and [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver).</span></span> <span data-ttu-id="25df0-112">任何想要指示伺服器自行註冊 (也就是其 Clsid 和類型程式庫識別碼) 的任何應用程式都可以透過 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)函數取得 **DllRegisterServer** 的指標。</span><span class="sxs-lookup"><span data-stu-id="25df0-112">Any application that wishes to instruct the server to register itself (that is, all its CLSIDs and type library IDs) can obtain a pointer to **DllRegisterServer** through the [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) function.</span></span> <span data-ttu-id="25df0-113">在 **DllRegisterServer** 內，dll 會建立所有必要的登錄專案，並為所有 [InprocServer32](inprocserver32.md) 或 [InprocHandler32](inprochandler32.md) 專案儲存 DLL 的正確路徑。</span><span class="sxs-lookup"><span data-stu-id="25df0-113">Within **DllRegisterServer**, the DLL creates all its necessary registry entries, storing the correct path to the DLL for all [InprocServer32](inprocserver32.md) or [InprocHandler32](inprochandler32.md) entries.</span></span>

<span data-ttu-id="25df0-114">當應用程式想要從系統中移除元件時，它應該呼叫 [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver)來取消註冊該元件。</span><span class="sxs-lookup"><span data-stu-id="25df0-114">When an application wishes to remove the component from the system, it should unregister that component by calling [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver).</span></span> <span data-ttu-id="25df0-115">在此呼叫中，伺服器會完全移除先前在 [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver)中建立的專案。</span><span class="sxs-lookup"><span data-stu-id="25df0-115">Within this call, the server removes exactly those entries it previously created in [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver).</span></span> <span data-ttu-id="25df0-116">伺服器不應該盲目移除其類別的所有專案，因為其他軟體可能已儲存額外的專案，例如 [TreatAs](treatas.md) 金鑰。</span><span class="sxs-lookup"><span data-stu-id="25df0-116">The server should not blindly remove all entries for its classes because other software may have stored additional entries, such as a [TreatAs](treatas.md) key.</span></span>

<span data-ttu-id="25df0-117">如果伺服器封裝在 EXE 模組中，則想要註冊伺服器的應用程式會使用命令列引數 **/RegServer** 或 **-RegServer** (不區分大小寫的) 來啟動 EXE 伺服器。</span><span class="sxs-lookup"><span data-stu-id="25df0-117">If the server is packaged in an EXE module, the application wishing to register the server launches the EXE server with the command-line argument **/RegServer** or **-RegServer** (case-insensitive).</span></span> <span data-ttu-id="25df0-118">如果應用程式想要將伺服器取消註冊，它會使用命令列引數 **/UnregServer** 或 **-UnregServer** 啟動 EXE。</span><span class="sxs-lookup"><span data-stu-id="25df0-118">If the application wishes to unregister the server, it launches the EXE with the command-line argument **/UnregServer** or **-UnregServer**.</span></span> <span data-ttu-id="25df0-119">自我註冊 EXE 會偵測這些命令列引數，並在 [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver)和 [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver)中分別叫用 DLL 的相同作業，並在 [LocalServer32](localserver32.md) （而不是 **InprocServer32** 或 **InprocHandler32**）註冊其模組路徑。</span><span class="sxs-lookup"><span data-stu-id="25df0-119">The self-registering EXE detects these command-line arguments and invokes the same operations as a DLL would within [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver)and [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver), respectively, registering its module path under [LocalServer32](localserver32.md) instead of **InprocServer32** or **InprocHandler32**.</span></span>

<span data-ttu-id="25df0-120">伺服器必須註冊 DLL 或 EXE 模組安裝位置的完整路徑，以用於登錄中各自的 **InprocServer32**、 **InprocHandler32** 和 **LocalServer32** 機碼。</span><span class="sxs-lookup"><span data-stu-id="25df0-120">The server must register the full path to the installation location of the DLL or EXE module for their respective **InprocServer32**, **InprocHandler32**, and **LocalServer32** keys in the registry.</span></span> <span data-ttu-id="25df0-121">您可以透過 [**GetModuleFileName**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) 函數輕鬆地取得模組路徑。</span><span class="sxs-lookup"><span data-stu-id="25df0-121">The module path is easily obtained through the [**GetModuleFileName**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="25df0-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="25df0-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="25df0-123">安裝為服務應用程式</span><span class="sxs-lookup"><span data-stu-id="25df0-123">Installing as a Service Application</span></span>](installing-as-a-service-application.md)
</dt> <dt>

[<span data-ttu-id="25df0-124">在安裝時註冊類別</span><span class="sxs-lookup"><span data-stu-id="25df0-124">Registering a Class at Installation</span></span>](registering-a-class-at-installation.md)
</dt> <dt>

[<span data-ttu-id="25df0-125">註冊正在執行的 EXE 伺服器</span><span class="sxs-lookup"><span data-stu-id="25df0-125">Registering a Running EXE Server</span></span>](registering-a-running-exe-server.md)
</dt> <dt>

[<span data-ttu-id="25df0-126">在 ROT 中註冊物件</span><span class="sxs-lookup"><span data-stu-id="25df0-126">Registering Objects in the ROT</span></span>](registering-objects-in-the-rot.md)
</dt> </dl>

 

 