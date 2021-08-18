---
title: 使用 High-Level 監視設定函數
description: 使用 High-Level 監視設定函數
ms.assetid: 23e5d45d-a924-4119-b21d-b24764b53a94
keywords:
- 監視，函數
- 監視，高階設定函數
- 監視，列舉實體監視器
- 監視，持續設定
- 監視設定、高階設定功能
- 監視設定，函數
- 監視設定，列舉實體監視器
- 監視設定、連續設定
- 列舉實體監視器
- 高階設定函數
- 持續監視設定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 827d19ef0006dc89208061c18ef34c28c8f993c3e0d6ebd0d1c1005daf2cd640
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066598"
---
# <a name="using-the-high-level-monitor-configuration-functions"></a>使用 High-Level 監視設定函數

## <a name="enumerating-physical-monitors"></a>列舉實體監視器

有幾個函式會列舉顯示裝置，包括 [**EnumDisplayMonitors**](/windows/desktop/api/winuser/nf-winuser-enumdisplaymonitors) 和 [**MonitorFromWindow**](/windows/desktop/api/winuser/nf-winuser-monitorfromwindow)。 這些函式記載于 [[多重顯示器](/windows/desktop/gdi/multiple-display-monitors)] 主題底下的 Windows GDI 檔中。 這些函數會傳回 **HMONITOR** 控制碼。 不過，儘管名稱， **HMONITOR** 控制碼也可以與一個以上的實體監視器相關聯。 若要設定監視的設定，應用程式必須藉由呼叫 [**GetPhysicalMonitorsFromHMONITOR**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor)來取得實體監視器的唯一控制碼。

如果您的應用程式使用 Direct3D，您可以藉由呼叫 [**GetPhysicalMonitorsFromIDirect3DDevice9**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromidirect3ddevice9)從 direct3d 裝置取得監視器控制碼。

## <a name="supported-functions"></a>支援的函式

監視器可能不支援所有的監視設定功能。 若要找出監視器支援哪些功能，請呼叫 [**GetMonitorCapabilities**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitorcapabilities)。

## <a name="continuous-monitor-settings"></a>持續監視設定

*持續* 監視設定可以範圍介於最小值和最大值之間。 大部分的高階監視設定函數都會控制連續監視設定。 例如，亮度和對比是連續的設定。

持續監視設定沒有定義的真實世界單位。 這些單位是任意的，而且可能會因不同的製造商而異。 例如，如果兩個監視器具有相同的亮度值，則某個監視器可能會比其他監視器更亮。 一般而言，應用程式會向使用者呈現滑杆控制項或上下按鈕控制項。 然後，使用者可以調整設定，以提供最佳的主觀品質。

## <a name="changes-in-monitor-state"></a>監視狀態的變更

監視器可能會因各種原因而變更狀態，包括：

-   使用者會使用監視的前端面板控制項來變更設定。
-   使用者變更監視器的螢幕解析度、更新頻率或位深度。
-   應用程式會使用低層級的監視功能來變更無法從高階函式存取的設定。
-   應用程式會呼叫 [**RestoreMonitorFactoryColorDefaults**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-restoremonitorfactorycolordefaults) 或 [**RestoreMonitorFactoryDefaults**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-restoremonitorfactorydefaults)。

所有這些事件都可以變更監視設定。 它們也可以變更設定的最小值和最大值。

## <a name="dependencies-among-monitor-settings"></a>監視器設定之間的相依性

變更色溫可能會變更目前的磁片磁碟機並進行設定，相反地，反向也是如此。 這些是高階監視設定功能之間唯一的相依性。 其他設定可能只能透過低層級的監視功能來存取。 這些設定與高階設定之間可能會有相依性。 這些相依性是廠商特定的。 應用程式可以透過數種方式來處理這個問題：

-   只使用高階函數。
-   呼叫低層級函數之後，取得每個監視設定的目前值。 可惜的是，這種方法可能會很慢，因為取得每項設定大約需要40毫秒。
-   使用低層級的函式，只搭配您瞭解其行為的特定監視模型。

## <a name="disabled-monitor-settings"></a>停用的監視器設定

應用程式無法藉由呼叫高階監視功能來停用任何監視設定。 但是，如果應用程式使用低層級的函式來變更高階函式不支援的監視設定，則應用程式可能會不小心停用設定。 此外，使用者可能會使用前端板控制項來停用設定。 這些行為是廠商特定的行為。

如果監視設定變成停用，任何設定或抓取該設定的函式都會失敗，並將最後一個錯誤碼設定為 [ \_ 停用錯誤] \_ 監視 \_ 設定。 發生這種情況時，應用程式可以執行下列其中一項：

-   顯示錯誤訊息，並向使用者建議使用前端板控制項來調整設定。
-   呼叫 [**RestoreMonitorFactoryDefaults**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-restoremonitorfactorydefaults) 函數。 如果監視的「MC \_ 還原 \_ 出廠 \_ 預設值」 \_ 啟用 \_ 監視 \_ 設定功能旗標，則此函式會啟用高階監視功能所支援的所有監視設定。 可惜的是，此函式也會將監視器設定重設為其原廠預設值。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用監視設定](using-monitor-configuration.md)
</dt> </dl>

 

 