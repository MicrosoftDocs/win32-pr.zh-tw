---
description: WMI 是以共用服務主機的一部分執行，預設會透過 DCOM 指派埠。 不過，您可以將 WMI 服務設定為在個別主機中執行為唯一的進程，並指定固定的埠。
ms.assetid: 62908445-2a43-4a20-a998-e497c6ecf48e
ms.tgt_platform: multiple
title: 設定適用于 WMI 的固定埠
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b97ee9d0f2f407c0cae2c9c1466a1904cf79eaecb353b94ac11bb3373367ed2f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050246"
---
# <a name="setting-up-a-fixed-port-for-wmi"></a>設定適用于 WMI 的固定埠

WMI 是以共用服務主機的一部分執行，預設會透過 DCOM 指派埠。 不過，您可以將 WMI 服務設定為在個別主機中執行為唯一的進程，並指定固定的埠。

下列程式是自動化的設定，可讓 WMI 具有固定的埠。 此程式使用 [**winmgmt**](winmgmt.md) 命令列工具。

**設定適用于 WMI 的固定埠**

1.  在命令提示字元中，輸入 **winmgmt-standalonehost**
2.  輸入命令 **net stop "Windows Management Instrumentation"**，或使用 **net stop winmgmt** 的簡短名稱，以停止 WMI 服務
3.  輸入 **net start "Windows Management Instrumentation"** 或 **net start winmgmt** ，以重新開機新服務主機中的 WMI 服務
4.  輸入 **netsh firewall add PORTOPENING TCP 24158 WMIFixedPort** ，為 WMI 服務建立新的埠號碼

若要復原您對 WMI 所做的任何變更，請輸入 **winmgmt/sharedhost**，然後再次停止並啟動 winmgmt 服務。

## <a name="examples"></a>範例

如需針對 WMI 設定固定埠的腳本，請參閱下列腳本庫程式 [代碼範例](https://Gallery.TechNet.Microsoft.Com/Set-WmiSinglePortps1-20fa8389 )。

或是啟用或停用 WMI 埠設定的 PowerShell 程式碼範例，請參閱 TechNet 資源庫上的 [WmiSinglePort](https://Gallery.TechNet.Microsoft.Com/Set-WmiSinglePortps1-20fa8389) 範例。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[連接至遠端電腦上的 WMI](connecting-to-wmi-on-a-remote-computer.md)
</dt> <dt>

[疑難排解遠端 WMI 連接](connecting-to-wmi-remotely-starting-with-vista.md)
</dt> <dt>

[提供者裝載和安全性](provider-hosting-and-security.md)
</dt> </dl>

 

 



