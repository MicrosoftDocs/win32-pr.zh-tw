---
description: 指定提供者裝載模型。 設定這個屬性會使提供者載入具有指定許可權層級的共用主機進程中。
ms.assetid: 1e5c778d-cd29-449b-88e2-fe0c90d0edcd
ms.tgt_platform: multiple
title: 提供者裝載和安全性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fce0853b268f3d0bef0c43cbeabc10651885f0bd3b07f79d5c1b29072b560c1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050486"
---
# <a name="provider-hosting-and-security"></a>提供者裝載和安全性

**\_ \_ Win32Provider** 實例中代表提供者的 [**HostingModel**](--win32provider.md)屬性會指定提供者裝載模型。 設定這個屬性會使提供者載入具有指定許可權層級的共用主機進程中。

## <a name="shared-provider-host-process"></a>共用提供者主機進程

WMI 位於具有多個其他服務的共用服務主機中。 若要避免在提供者失敗時停止所有服務，提供者會載入名為 "Wmiprvse.exe" 的個別主控制項進程。 具有這個名稱的多個進程可以執行。 每個都可以在具有不同安全性的不同帳戶下執行。 請注意，從 Windows Vista 開始，請使用 [**winmgmt**](winmgmt.md)命令，在個別的進程中使用固定通訊埠來執行 WMI。 如需詳細資訊，請參閱 [從 Vista 開始遠端連線到 WMI](connecting-to-wmi-remotely-starting-with-vista.md)。

共用主機可以在 Wmiprvse.exe 主機進程中的下列其中一個系統帳戶下執行：

-   [LocalSystem](/windows/desktop/Services/localsystem-account)
-   [NetworkService](/windows/desktop/Services/networkservice-account)
-   [LocalService](/windows/desktop/Services/localservice-account)

提供者也可以是本機 COM 伺服器 (.exe) 或自我裝載，而不需要 WMI 提供者主機。

## <a name="setting-the-hosting-model"></a>設定裝載模型

因為 LocalSystem 是具有特殊許可權的帳戶，所以建議您在 Wmiprvse.exe 進程中執行提供者時，將 [**HostingModel**](--win32provider.md) 設定為 **NetworkServiceHost** 。 NetworkServiceHost 帳戶適用于不需要廣泛許可權的服務，但需要從遠端與其他系統通訊。

如果您未設定 [**HostingModel**](--win32provider.md) 屬性的值，WMI 會將預設值設定為 **NetworkServiceHostOrSelfHost**。 如果 **HostingModel** 值設定為 **LocalSystemHost**，WMI 會使用追蹤在 Windows 事件記錄檔中產生事件5603和5604。 由於本機 [LocalSystem](/windows/desktop/Services/localsystem-account) 帳戶具有高度許可權，因此不建議使用此設定。 您可以在 **事件檢視器** 中查看這些事件。 如需詳細資訊，請參閱 [追蹤 WMI 活動](tracing-wmi-activity.md)。

將低耦合提供者的 [**HostingModel**](--win32provider.md) 屬性設定為「分離： Com」。 藉 [**由在 .NET Framework 中新增**](/previous-versions//hh872326(v=vs.85))檢測類別所建立的提供者是低耦合提供者。 不再 ) 支援 (的 **系統管理。** 如需建立低耦合提供者的詳細資訊，請參閱 [在應用程式中併入提供者](incorporating-a-provider-in-an-application.md)。

裝載模型是在代表提供者之 **\_ \_ Win32Provider** 實例的 [**HostingModel**](--win32provider.md)屬性中指定。

**設定提供者的裝載模型**

1.  在定義您提供者的 MOF 檔案中，建立 [**\_ \_ Win32Provider**](--win32provider.md)的實例。
2.  **將名稱屬性中** 的提供者指派給提供者，並將提供者 COM 物件 (clsid) 的類別識別碼指派給 **CLSID** 屬性。

    下列程式碼範例 **會將名稱屬性的** 名稱，以及提供者 COM 物件的 CSLID 指派給 **Clsid** 屬性。

    ``` syntax
    Instance of __Win32Provider as $NewProvider
    {
        Name = "MyProvider";
        Clsid = "{.......}";
    }
    ```

3.  將適當的共用主機值指派給 [**HostingModel**](--win32provider.md) 屬性。 共用的主機值（例如 "NetworkServiceHost"）是在 [**MSFT \_ 提供者**](/previous-versions/windows/desktop/wmisystemprov/msft-providers)類別的 **HostingSpecification** 屬性中定義。

    下列程式碼範例會將共用主機值指派給 [**HostingModel**](--win32provider.md) 屬性。

    ``` syntax
    HostingModel = "NetworkServiceHost";
    ```

下列程式碼範例顯示如何在 NetworkServiceHost 中註冊提供者。

``` syntax
Instance of __Win32Provider as $NewProvider
{
    Name = "MyProvider";
    Clsid = "{.......}";
    HostingModel = "NetworkServiceHost";
}
```

如果您有多個提供者，您可以註冊您的提供者，使其位於特定的實例中，以將它們群組至特定的服務主機。

下列程式碼範例也會在 NetworkServiceHost 中註冊提供者。 [**MSFT \_ 提供者**](/previous-versions/windows/desktop/wmisystemprov/msft-providers)類別會定義兩個合併用來建立 [**\_ \_ Win32Provider**](--win32provider.md) **HostingModel** 屬性之值的值。 在此範例中，"NetworkServiceHost" 值來自 **MSFT \_ 提供者** 的 **HostingSpecification** 屬性，而 "LocalServiceHost" 來自 **HostingGroup** 屬性。

``` syntax
Instance of __Win32Provider as $NewProvider
{
    Name = "MyProvider";
    Clsid = "{.......}";
    HostingModel = "NetworkServiceHost:MySharedHost";
}
```

未分離且裝載于 Wmiprvse 程式中的提供者有特殊開發問題。 如需詳細資訊，請參閱 [偵錯工具提供者](debugging-providers.md)。

如果您要撰寫包含屬性或類別提供者註冊的提供者，則並非所有線程模型都能運作。 如需詳細資訊，請參閱 [選擇正確的註冊](choosing-correct-registration.md)。

## <a name="hostingmodel-values-for-in-process-providers"></a>In-Process 提供者的 HostingModel 值

下列清單針對 Wmiprvse.exe 進程中執行的提供者，列出要在 [**\_ \_ Win32Provider**](--win32provider.md)實例中使用的提供者裝載模型值。



| [ **\_ \_ Win32Provider. HostingModel** 中的值](--win32provider.md) | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SelfHost**                                                       | 提供者會開始使用本機伺服器執行，而不是同進程。 提供者執行之進程的安全性內容會決定提供者的安全性內容。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **LocalSystemHost**                                                | 提供者（如果實作為同進程）會載入至在 [LocalSystem](/windows/desktop/Services/localsystem-account) 內容下執行的共用提供者主機。 從 Windows Vista 開始，如果 WMI 提供者的 [**HostingModel**](--win32provider.md) (**\_ \_ Win32Provider**， **LocalSystemHost** 就不再是預設的裝載模型。未指定 HostingModel 屬性) 。 如需詳細資訊，請參閱 [裝載模型的安全性](#provider-hosting-and-security)。                                                                                                                                                                                                                                                                               |
| **LocalSystemHostOrSelfHost**                                      | 此提供者會自我裝載，或載入至在 [LocalSystem](/windows/desktop/Services/localsystem-account) 帳戶下執行的 Wmiprvse.exe 進程。 由於 LocalSystem 是具有高度許可權的帳戶，因此會在 Security NT 事件記錄檔中產生專案，以通知系統管理員在此受信任狀態下執行的提供者。                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **NetworkServiceHost**                                             | 提供者（如果實作為同進程）會載入至在 [NetworkService](/windows/desktop/Services/networkservice-account) 帳戶下執行的 Wmiprvse.exe 進程。 從 Windows Vista 開始，如果 WMI 提供者的 [**HostingModel**](--win32provider.md) (**\_ \_ Win32Provider**，這就是預設的裝載模型。未指定 HostingModel 屬性) 。 如需詳細資訊，請參閱 [裝載模型的安全性](#provider-hosting-and-security)。<br/> **NetworkServiceHost** 具有有限的許可權，因此可降低權限提高攻擊的可能性。 如果提供者只在本機電腦上運作，請將 [**HostingModel**](--win32provider.md) 屬性設定為 **LocalServiceHost**。<br/> |
| **NetworkServiceHostOrSelfHost**                                   | 此提供者會自我裝載，或載入至在 [NetworkService](/windows/desktop/Services/networkservice-account) 帳戶下執行的 WmiPrvse.exe 進程。 當 **\_ \_ Win32Provider** 中的 [**HostingModel**](--win32provider.md)屬性為 **Null** 時， **NetworkServiceHostOrSelfHost** 是預設的設定。 由於 **NetworkServiceHostOrSelfHost** 是預設值，因此舊版作業系統的提供者可以在 Windows Vista、Windows Server 2008 和更新版本的作業系統中繼續運作。                                                                                                                                                                                                                                             |
| **LocalServiceHost**                                               | 提供者（如果實作為同進程）會載入至 [LocalService](/windows/desktop/Services/localservice-account) 帳戶下執行的 Wmiprvse.exe 進程。 這是建議的服務裝載模型，因為 LocalService 具有有限的許可權。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="hostingmodel-values-for-decoupled-providers"></a>HostingModel 低耦合提供者的值

下列清單列出低耦合提供者的提供者裝載模型值。

<dl> <dt>

<span id="Decoupled_Com"></span><span id="decoupled_com"></span><span id="DECOUPLED_COM"></span>**分離： Com**
</dt> <dd>

提供者是在另一個進程中裝載的低耦合提供者，也就是 WMI 的用戶端。

下列範例顯示 [**HostingModel**](--win32provider.md) 屬性設定為 **FALSE** 的 FoldIdentity 規範，允許提供者模擬用戶端。

``` syntax
Decoupled:Com:FoldIdentity(FALSE)
```

如果未指定 FoldIdentity，FoldIdentity 值預設會設定為 **TRUE** 。 基於安全性理由，建議您不要指定 FoldIdentity (FALSE) 因為具有模擬委派的 rogue 應用程式可能會影響整個網域。

下列範例會以建議的方式顯示 [**HostingModel**](--win32provider.md) 屬性集，相當於設定 FOLDIDENTITY (TRUE) 。

``` syntax
Decoupled:Com
```

</dd> <dt>

<span id="Decoupled_Noncom"></span><span id="decoupled_noncom"></span><span id="DECOUPLED_NONCOM"></span>**分離： Noncom**
</dt> <dd>

僅供內部使用。 不支援。

</dd> </dl>

## <a name="security-of-hosting-models"></a>裝載模型的安全性

在大多數情況下， **LocalSystem** 是不必要的，而且 **NetworkServiceHost** 內容更適合。 大部分的 WMI 提供者都必須模擬用戶端安全性內容，以代表 WMI 用戶端執行要求的作業。 從 Windows Vista 開始，缺少裝載模型定義並執行的 WMI 提供者 **，將無法** 正確執行。 若要修正這種情況，請變更預期的裝載模型，並確定 WMI 提供者程式碼會模擬 WMI 用戶端，以在用戶端安全性內容中執行作業。 LocalSystem 很少需要。 如果您的提供者必須擁有該層級的許可權，請使用 MOF 檔案中的下列語句來指定裝載模型。

``` syntax
HostingModel=LocalSystemHost
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[選擇正確的註冊](choosing-correct-registration.md)
</dt> <dt>

[存取 WMI 命名空間](access-to-wmi-namespaces.md)
</dt> <dt>

[保護 WMI 命名空間](securing-wmi-namespaces.md)
</dt> <dt>

[提供者設定和疑難排解類別](provider-configuration-and-troubleshooting-classes.md)
</dt> <dt>

[**MSFT \_ 提供者**](/previous-versions/windows/desktop/wmisystemprov/msft-providers)
</dt> <dt>

[維護 WMI 安全性](maintaining-wmi-security.md)
</dt> </dl>

 

