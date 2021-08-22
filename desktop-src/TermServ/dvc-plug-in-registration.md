---
title: DVC 外掛程式註冊
description: 描述遠端桌面連線 (RDC) 用戶端的動態虛擬通道 (DVC) 外掛程式專案的語法。
ms.assetid: cda4f8c9-867a-41ac-894a-4296d5912b2b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88d3660b4d9c704c9a59335cede886085f13414991dc2dc913185d407e0a3c54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119515525"
---
# <a name="dvc-plug-in-registration"></a>DVC 外掛程式註冊

遠端桌面連線 (RDC) 用戶端使用下列其中一種方法來註冊動態虛擬通道 (DVC) 外掛程式：

-   叫用遠端桌面通訊協定 (RDP) ActiveX 控制項的 [**IMsTscAdvancedSettings：:p \_ PluginDlls**](imstscadvancedsettings-plugindlls.md)方法。 多個專案必須以逗號分隔。
-   在啟動遠端桌面連線 (RDC) 用戶端進程的電腦上，將外掛程式專案寫入至下列位置：

    **HKEY \_目前的 \_ 使用者** \\ **軟體** \\ **Microsoft** \\ **終端機伺服器用戶端** \\ **預設** 的 \\ **載入** \\ **_宏唯一外掛程式名稱_**

    > [!Note]  
    > 如果不存在，您必須建立 *唯一的外掛程式名稱* 子機碼。 *唯一的外掛程式名稱* 子機碼名稱是可識別外掛程式的任一字元串。 字串可以是任一字元的組合。

     

    在 *[唯一外掛程式名稱]* 底下，您必須加入可識別外掛程式的專案。

    專案名稱 = **名稱**

    資料類型 = **REG \_ SZ** 或 **reg \_ EXPAND \_ sz**

在這兩種情況下，專案值都必須符合下列其中一種格式：

<dl> <dt>

<span id="Plug-inDLLName__CLSID_"></span><span id="plug-indllname__clsid_"></span><span id="PLUG-INDLLNAME__CLSID_"></span>"*外掛程式 inDLLName*： {*CLSID*}"
</dt> <dd>

外掛程式不一定會在 Windows 登錄中註冊為元件物件模型 (COM) 物件，但是 DLL 會實作為同進程 COM 物件。 RDC 用戶端會載入 *外掛程式* 所指定的 DLL，並使用 *CLSID* 直接取出 COM 物件。

</dd> <dt>

<span id="Plug-inDLLName"></span><span id="plug-indllname"></span><span id="PLUG-INDLLNAME"></span>"*InDLLName*"
</dt> <dd>

DLL 會實 [**VirtualChannelGetInstance**](virtualchannelgetinstance.md) 函式，並依名稱匯出它。 RDC 用戶端將使用 **VirtualChannelGetInstance** 函式來取得 DLL 所執行之所有外掛程式的 [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) 介面指標。

</dd> <dt>

<span id="_CLSID_"></span><span id="_clsid_"></span>"{*CLSID*}"
</dt> <dd>

RDC 用戶端會將外掛程式具現化為搭配 *CLSID* 使用 [**COCREATEINSTANCE**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)的一般 COM 物件。

</dd> </dl>

> [!Note]  
> *外掛程式 inDLLName* 代表 .dll 檔案的完整路徑和檔案名。 如果資料類型是 **REG \_ EXPAND \_ SZ**，則路徑可以包含在執行時間展開的未展開環境變數。

 

當遠端桌面連線 (RDC) 用戶端完成其初始化時，它會針對每個已註冊的外掛程式執行下列各項：

1.  使用上述其中一個方法，針對每個外掛程式取得 [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) 介面的實例。
2.  呼叫每個 [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin)介面的 [**Initialize**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-initialize)方法。
3.  如果用戶端連接多次至相同或不同的伺服器，則可能會有多個 [**連線**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-connected) 和 [**中斷**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-disconnected) 連接方法的呼叫。
4.  外掛程式應處理的最後一個呼叫已 [**終止**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-terminated)。 這是遠端桌面連線 (RDC) 用戶端即將卸載外掛程式的信號。

 

 