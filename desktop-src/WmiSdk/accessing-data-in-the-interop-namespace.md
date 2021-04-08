---
description: 關聯提供者可讓 Windows Management Instrumentation (WMI) 用戶端，以從不同的命名空間來進行設定檔和相關聯的類別實例。
ms.assetid: 00c654d1-a5de-40c5-a190-99382949486a
ms.tgt_platform: multiple
title: 存取 Interop 命名空間中的資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a217a7a44651b1a6c94476b53193eedac7f0d43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945114"
---
# <a name="accessing-data-in-the-interop-namespace"></a>存取 Interop 命名空間中的資料

關聯提供者可讓 Windows Management Instrumentation (WMI) 用戶端，以從不同的命名空間來進行設定檔和相關聯的類別實例。

關聯提供者和類別位於 \\ \\ 根 \\ interop 命名空間中。 如需詳細資訊，請參閱 [跨命名空間關聯的遍歷](cross-namespace-association-traversal.md) 和 [寫入關聯提供者](writing-an-association-provider-for-interop.md)。

關聯提供者會公開標準設定檔，例如電源設定檔。 下列範例會使用電源設定檔來說明如何透過 interop 命名空間來探索及存取資料。

Windows PowerShell 提供簡單的機制，可透過適當的關聯、取出裝置設定檔，以及呼叫方法來進行。

## <a name="enumerating-profiles-in-the-rootinterop-namespace"></a>列舉根/interop 命名空間中的設定檔

下列 Windows PowerShell 命令會列舉 Windows 7 電腦上的分散式管理工作強制 ([DMTF](https://www.dmtf.org/standards/wsman)) 支援的設定檔：


```PowerShell
Get-WmiObject CIM_RegisteredProfile  -namespace root\interop
```



## <a name="retrieving-instances-of-a-specific-device-profile"></a>正在抓取特定裝置設定檔的實例

下列 Windows PowerShell 命令會透過 [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85))來傳回指定之設定檔的所有實例：


```PowerShell
Get-WmiObject -namespace root\interop -query "Associators of {CIM_RegisteredProfile.InstanceID='Power Supply'}"
```



## <a name="assigning-the-power-profile-to-a-variable"></a>將電源設定檔指派給變數

下列 Windows PowerShell 命令會將電源設定檔實例指派給變數：


```PowerShell
$pplan = Get-WmiObject -query "Select * from Win32_PowerPlan" -Namespace root\cimv2\power
```



## <a name="enumerating-the-power-plans-on-a-computer"></a>列舉電腦上的電源計劃

下列 Windows PowerShell 命令會列舉可用的電源設定檔方案：


```PowerShell
$pplan
```



## <a name="calling-a-method"></a>呼叫方法

下列 Windows PowerShell 命令會呼叫電源計劃的 [**啟動**](/previous-versions/windows/desktop/powerwmiprov/activate-win32-powerplan) 方法：


```PowerShell
$pplan[2].Activate()
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[跨命名空間關聯的遍歷](cross-namespace-association-traversal.md)
</dt> <dt>

[撰寫關聯提供者](writing-an-association-provider-for-interop.md)
</dt> <dt>

[**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85))
</dt> <dt>

[**Win32 \_ PowerPlan**](/previous-versions/windows/desktop/legacy/dd904531(v=vs.85))
</dt> </dl>

 

 
