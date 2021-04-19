---
title: .NET Framework 預設設定
description: .NET Framework 4.5 是預設值，.NET Framework 3.5 是選擇性的
ms.assetid: 19B53C82-812A-49AC-87C6-C08E7C199208
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab1f91acc8739b2c660bfb1ba1392ea192511d1c
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/10/2020
ms.locfileid: "106991112"
---
# <a name="net-framework-45-is-default-and-net-framework-35-is-optional"></a>.NET Framework 4.5 是預設值，.NET Framework 3.5 是選擇性的

## <a name="platforms"></a>平台

**用戶端**   Windows 8  
**伺服器**   Windows Server 2012  

## <a name="description"></a>Description

預設會在 Windows 8 中啟用 .NET Framework 4.5。 Windows 8 預設不包含 .NET 3.5，但 Windows 8 安裝媒體上有提供適用于 .NET 3.5 的檔案做為選擇性功能。

如果使用者是從 Windows 7 升級至 Windows 8，.NET Framework 3.5 已完全啟用，以確保電腦上的任何應用程式都能正常運作。

## <a name="manifestation"></a>表現

如果使用者執行 Windows 8 的全新安裝，然後安裝需要 .NET Framework 3.5 (或 2.0) 的應用程式，則會觸發必要 .NET 3.5 檔案的要求。 通常會在要求使用者提供許可權) 之後，從 Windows Update (下載遺失的檔案，但如果不能存取 Windows Update，除非已指定遺漏檔案的替代來源，否則啟用 .NET Framework 3.5 將會失敗。

## <a name="mitigation"></a>降低

若只要使用全新的 Windows 8 安裝在測試電腦上啟用 .NET Framework 3.5：

1.  \\ \\ \\ 從裝載的作業系統組建 ISO 映像將來源 sxs 複製到 dotnet35 或類似資料夾。 例如：
    ```
    xcopy e:\sources\sxs\*.* c:\dotnet35 /s
    ```



2.  使用系統管理員許可權來執行此命令列：
    ```
    Dism.exe /online /enable-feature /featurename:NetFX3 /All /Source:c:\dotnet35 /LimitAccess

    ```



> [!Note]  
> \\因為這不是支援的機制，所以不能使用來源 SxS 資料夾做為轉散發機制。



## <a name="solution"></a>解決方法

**針對取用者：**

Windows 8 包含一種機制，可在嘗試安裝可轉散發套件或需要 .NET 3.5 的應用程式安裝程式叫用可轉散發套件時，自動啟用 .NET Framework 3.5。

**針對應用程式開發人員 (和 IT 系統管理員) ：**

IT 系統管理員可以根據已安裝的) ，將 .NET 3.5 應用程式設定為在 .NET 3.5 或 .NET 4.5 (上執行。 若要在3.5 或4.5 上執行受管理的應用程式，只需在應用程式佈建檔中新增一個區段。 這可確保如果已安裝 .NET 3.5，應用程式將會在 .NET 3.5 上執行;否則，應用程式將會在 .NET 4.5 上執行。 以下提供設定檔中其他區段的範例：


```
<configuration>
   <startup>
      <supportedRuntime version="v2.0.50727"/>
      <supportedRuntime version="v4.0" sku=".NETFramework,Version=v4.5"/>
   </startup>
</configuration>
```



**針對企業 Oem：**

若要為 EEAP 組建和沒有 Windows Update 存取權的應用程式啟用 .NET Framework 3.5：

1.  \\ \\ \\ 從裝載的作業系統組建 ISO 映像將來源 sxs 複製到 dotnet35 或類似的資料夾。 例如：
    ```
    xcopy e:\sources\sxs\*.* c:\dotnet35 /s
    ```



2.  設定 regkey：
    ```
    [HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\Servicing]
     LocalSourcePath = c:\dotnet35
    ```



**適用于企業：**

針對設定為使用 WSUS 進行服務的電腦，您可以設定登錄專案以允許電腦使用 Windows Update 來啟用 .NET 3.5，而不是 WSUS (服務仍會從 WSUS 執行（如果您這樣做) ）。

-   設定 regkey：
    ```
    [HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\Servicing]  RepairContentServerSource =DWORD(2)
    ```



此登錄專案也可以透過群組原則 (本機電腦原則-> 電腦設定-> 系統管理範本 > 系統設定。 選取 [指定選用元件安裝和元件修復的設定]。

如果您選取 [連絡人] Windows Update 直接下載修復內容，而不是 Windows Server Update Services (WSUS) ，則任何新增 Windows 功能的嘗試 (例如 .NET Framework 3.5) 或修復功能都會從 Windows Update 觸發檔案下載。 目的電腦需要此選項的網際網路和 WU 存取權。 正常的服務作業如果已設定為來源，則會繼續使用 WSUS。

**關於透過登錄專案設定本機來源位置的注意事項**

IT 系統管理員可以透過登錄專案設定 .NET 3.5 檔案的本機來源位置 (s) ，讓使用者可以使用 [新增/移除 Windows 功能] 對話方塊來啟用具有遺失承載的功能，而不需指定來源位置。 您可以透過群組原則來控制登錄專案的值。

支援此登錄專案：



<table>
<thead>
<tr class="header">
<th>進入</th>
<th>類型</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>本機來源路徑</td>
<td> REG_EXPAND_SZ </td>
<td>預設會使用本機來源路徑)  (s。 可以指定多個路徑;它們應該以; 分隔。 系統會依照指定的順序來搜尋位置。 <br/> 在 DISM 命令列上指定的本機來源位置 (s) ，優先于此登錄專案中指定的位置。 您可以在此登錄專案中指定資料夾位置。 <br/> 您可以使用 Wim，但路徑必須是 WIM 檔案;不需要掛接它，例如： <br/> <dl> wim： \\ machine\share\file.wim：1<br />
</dl> 請注意結尾的1。 您必須指定要在 WIM 檔案中使用之映射的數值索引。 <br/> 若為掛接的 WIM，來源路徑必須參考掛接映射的 windows 目錄，而不是指向掛接點 (例如：/source： <mount_point> \windows，而不是/source： <mount_point>) 。 <br/></td>
</tr>
</tbody>
</table>





## <a name="resources"></a>資源

<dl>

[執行以登錄為基礎的原則](/previous-versions/windows/desktop/Policy/implementing-registry-based-policy)  
</dl>