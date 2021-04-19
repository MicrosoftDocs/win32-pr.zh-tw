---
title: DVC 外掛程式註冊
description: 描述遠端桌面連線 (RDC) 用戶端的動態虛擬通道 (DVC) 外掛程式專案的語法。
ms.assetid: cda4f8c9-867a-41ac-894a-4296d5912b2b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 183c73f5f9dda0321640119b2750776d207973cc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106990896"
---
# <a name="dvc-plug-in-registration"></a><span data-ttu-id="10f05-103">DVC 外掛程式註冊</span><span class="sxs-lookup"><span data-stu-id="10f05-103">DVC plug-in registration</span></span>

<span data-ttu-id="10f05-104">遠端桌面連線 (RDC) 用戶端使用下列其中一種方法來註冊動態虛擬通道 (DVC) 外掛程式：</span><span class="sxs-lookup"><span data-stu-id="10f05-104">The dynamic virtual channel (DVC) plug-in is registered for use by the Remote Desktop Connection (RDC) client using one of the following methods:</span></span>

-   <span data-ttu-id="10f05-105">叫用遠端桌面通訊協定 (RDP) ActiveX 控制項的 [**IMsTscAdvancedSettings：:p \_ PluginDlls**](imstscadvancedsettings-plugindlls.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="10f05-105">Invoking the [**IMsTscAdvancedSettings::put\_PluginDlls**](imstscadvancedsettings-plugindlls.md) method of the Remote Desktop Protocol (RDP) ActiveX control.</span></span> <span data-ttu-id="10f05-106">多個專案必須以逗號分隔。</span><span class="sxs-lookup"><span data-stu-id="10f05-106">Multiple entries must be comma separated.</span></span>
-   <span data-ttu-id="10f05-107">在啟動遠端桌面連線 (RDC) 用戶端進程的電腦上，將外掛程式專案寫入至下列位置：</span><span class="sxs-lookup"><span data-stu-id="10f05-107">Writing the plug-in entry to the following location in the registry on the computer where the Remote Desktop Connection (RDC) client process is started:</span></span>

    <span data-ttu-id="10f05-108">**HKEY \_目前的 \_ 使用者** \\ **軟體** \\ **Microsoft** \\ **終端機伺服器用戶端** \\ **預設** 的 \\ **載入** \\ ***宏唯一外掛程式名稱***</span><span class="sxs-lookup"><span data-stu-id="10f05-108">**HKEY\_CURRENT\_USER**\\**Software**\\**Microsoft**\\**Terminal Server Client**\\**Default**\\**AddIns**\\***unique plug-in name***</span></span>

    > [!Note]  
    > <span data-ttu-id="10f05-109">如果不存在，您必須建立 *唯一的外掛程式名稱* 子機碼。</span><span class="sxs-lookup"><span data-stu-id="10f05-109">You must create the *unique plug-in name* subkey if it does not exist.</span></span> <span data-ttu-id="10f05-110">*唯一的外掛程式名稱* 子機碼名稱是可識別外掛程式的任一字元串。</span><span class="sxs-lookup"><span data-stu-id="10f05-110">The *unique plug-in name* subkey name is an arbitrary string that can identify the plug-in.</span></span> <span data-ttu-id="10f05-111">字串可以是任一字元的組合。</span><span class="sxs-lookup"><span data-stu-id="10f05-111">The string can be any combination of characters.</span></span>

     

    <span data-ttu-id="10f05-112">在 *[唯一外掛程式名稱]* 底下，您必須加入可識別外掛程式的專案。</span><span class="sxs-lookup"><span data-stu-id="10f05-112">Under *unique plug-in name*, you must add an entry that identifies the plug-in.</span></span>

    <span data-ttu-id="10f05-113">專案名稱 = **名稱**</span><span class="sxs-lookup"><span data-stu-id="10f05-113">Entry name = **Name**</span></span>

    <span data-ttu-id="10f05-114">資料類型 = **REG \_ SZ** 或 **reg \_ EXPAND \_ sz**</span><span class="sxs-lookup"><span data-stu-id="10f05-114">Data type = **REG\_SZ** or **REG\_EXPAND\_SZ**</span></span>

<span data-ttu-id="10f05-115">在這兩種情況下，專案值都必須符合下列其中一種格式：</span><span class="sxs-lookup"><span data-stu-id="10f05-115">In both cases, the entry value must conform to one of the following formats:</span></span>

<dl> <dt>

<span data-ttu-id="10f05-116"><span id="Plug-inDLLName__CLSID_"></span><span id="plug-indllname__clsid_"></span><span id="PLUG-INDLLNAME__CLSID_"></span>"*外掛程式 inDLLName*： {*CLSID*}"</span><span class="sxs-lookup"><span data-stu-id="10f05-116"><span id="Plug-inDLLName__CLSID_"></span><span id="plug-indllname__clsid_"></span><span id="PLUG-INDLLNAME__CLSID_"></span>"*Plug-inDLLName*:{*CLSID*}"</span></span>
</dt> <dd>

<span data-ttu-id="10f05-117">外掛程式不一定會在 Windows 登錄中註冊為元件物件模型 (COM) 物件，但是 DLL 會實作為同進程 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="10f05-117">The plug-in is not necessarily registered in the Windows registry as a Component Object Model (COM) object, but the DLL is implemented as an in-process COM object.</span></span> <span data-ttu-id="10f05-118">RDC 用戶端會載入 *外掛程式* 所指定的 DLL，並使用 *CLSID* 直接取出 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="10f05-118">The RDC client will load the DLL specified by *Plug-inDLLName* and retrieve the COM object directly using *CLSID*.</span></span>

</dd> <dt>

<span data-ttu-id="10f05-119"><span id="Plug-inDLLName"></span><span id="plug-indllname"></span><span id="PLUG-INDLLNAME"></span>"*InDLLName*"</span><span class="sxs-lookup"><span data-stu-id="10f05-119"><span id="Plug-inDLLName"></span><span id="plug-indllname"></span><span id="PLUG-INDLLNAME"></span>"*Plug-inDLLName*"</span></span>
</dt> <dd>

<span data-ttu-id="10f05-120">DLL 會實 [**VirtualChannelGetInstance**](virtualchannelgetinstance.md) 函式，並依名稱匯出它。</span><span class="sxs-lookup"><span data-stu-id="10f05-120">The DLL implements the [**VirtualChannelGetInstance**](virtualchannelgetinstance.md) function and exports it by name.</span></span> <span data-ttu-id="10f05-121">RDC 用戶端將使用 **VirtualChannelGetInstance** 函式來取得 DLL 所執行之所有外掛程式的 [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="10f05-121">The RDC client will use the **VirtualChannelGetInstance** function to obtain [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) interface pointers for all of the plug-ins implemented by the DLL.</span></span>

</dd> <dt>

<span data-ttu-id="10f05-122"><span id="_CLSID_"></span><span id="_clsid_"></span>"{*CLSID*}"</span><span class="sxs-lookup"><span data-stu-id="10f05-122"><span id="_CLSID_"></span><span id="_clsid_"></span>"{*CLSID*}"</span></span>
</dt> <dd>

<span data-ttu-id="10f05-123">RDC 用戶端會將外掛程式具現化為搭配 *CLSID* 使用 [**COCREATEINSTANCE**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)的一般 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="10f05-123">The RDC client will instantiate the plug-in as a regular COM object using [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) with the *CLSID*.</span></span>

</dd> </dl>

> [!Note]  
> <span data-ttu-id="10f05-124">*外掛程式 inDLLName* 代表 .dll 檔案的完整路徑和檔案名。</span><span class="sxs-lookup"><span data-stu-id="10f05-124">*Plug-inDLLName* represents the full path and file name of the .dll file.</span></span> <span data-ttu-id="10f05-125">如果資料類型是 **REG \_ EXPAND \_ SZ**，則路徑可以包含在執行時間展開的未展開環境變數。</span><span class="sxs-lookup"><span data-stu-id="10f05-125">If the data type is **REG\_EXPAND\_SZ**, the path can contain unexpanded environment variables that are expanded at runtime.</span></span>

 

<span data-ttu-id="10f05-126">當遠端桌面連線 (RDC) 用戶端完成其初始化時，它會針對每個已註冊的外掛程式執行下列各項：</span><span class="sxs-lookup"><span data-stu-id="10f05-126">When the Remote Desktop Connection (RDC) client finishes its initialization, it will perform the following for every registered plug-in:</span></span>

1.  <span data-ttu-id="10f05-127">使用上述其中一個方法，針對每個外掛程式取得 [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) 介面的實例。</span><span class="sxs-lookup"><span data-stu-id="10f05-127">Obtain an instance of the [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) interface for each plug-in using one of the methods described above.</span></span>
2.  <span data-ttu-id="10f05-128">呼叫每個 [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin)介面的 [**Initialize**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-initialize)方法。</span><span class="sxs-lookup"><span data-stu-id="10f05-128">Call the [**Initialize**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-initialize) method of each [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) interface.</span></span>
3.  <span data-ttu-id="10f05-129">如果用戶端連接多次至相同或不同的伺服器，則可能會有多個 [**連線**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-connected) 和 [**中斷**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-disconnected) 連接方法的呼叫。</span><span class="sxs-lookup"><span data-stu-id="10f05-129">If the client connects multiple times to the same or to a different server, there may be multiple calls to the [**Connected**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-connected) and [**Disconnected**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-disconnected) methods.</span></span>
4.  <span data-ttu-id="10f05-130">外掛程式應處理的最後一個呼叫已 [**終止**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-terminated)。</span><span class="sxs-lookup"><span data-stu-id="10f05-130">The last call that the plug-in should handle is [**Terminated**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-terminated).</span></span> <span data-ttu-id="10f05-131">這是遠端桌面連線 (RDC) 用戶端即將卸載外掛程式的信號。</span><span class="sxs-lookup"><span data-stu-id="10f05-131">It is a signal that the Remote Desktop Connection (RDC) client is about to unload the plug-in.</span></span>

 

 