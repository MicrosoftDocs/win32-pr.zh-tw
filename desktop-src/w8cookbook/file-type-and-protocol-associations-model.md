---
title: 檔案類型和 URI 關聯模型
description: 檔案類型和 URI 關聯模型
ms.assetid: 4DE7DD08-088A-4E09-B1C7-AE9033EA533D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aabcdb40bd38aeee24ee0e5d86f11651633a7eead1748810e8c1c6a846827690
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028856"
---
# <a name="file-type-and-uri-associations-model"></a>檔案類型和 URI 關聯模型

## <a name="platforms"></a>平台

 **客戶** 端-Windows 8  
**伺服器**-Windows Server 2012  



## <a name="description"></a>描述

Windows 8 中的檔案類型和 URI 關聯模型已變更。 應用程式無法再以程式設計的方式將自己設定為檔案類型或 URI 的預設處理常式。 相反地，使用者現在一律會控制檔案類型或 URI 配置的預設處理常式。

## <a name="manifestation"></a>表現

這項變更對使用者的呈現方式取決於應用程式的設計方式，例如：

-   許多應用程式會在每次執行時查看它們是否為預設值，如果不是，則會提示使用者將其設定為預設值。 不過，因為應用程式無法再精確地查詢，以判斷哪一個應用程式是檔案類型或 URI 配置的預設處理常式，所以這些作業都無法運作。
-   許多應用程式都有內建的對話方塊或功能表，或在其安裝程式中，指定應用程式應作為預設值的檔案類型。 不過，因為應用程式無法再以程式設計的方式，將本身設定為檔案類型或 URI 配置的預設處理常式，所以無法再運作。

## <a name="mitigation"></a>降低

使用者可以執行幾項工作來容納這些變更：

-   系統會提示使用者內容選擇預設的應用程式來處理檔案類型、URI 配置，或兩者都未指定時
-   使用者可以選擇在安裝可處理檔案類型或 URI 配置的新應用程式之後，變更其預設處理常式。
-   [預設程式] 控制台可讓使用者設定應用程式的預設值，或為檔案類型、URI 配置或兩者設定：應用程式可以連結至 [控制台]
-   您可以從 Windows 檔案總管變更預設值

## <a name="solution"></a>解決方案

由於這些變更，我們提供了此 API 指引：

-   [IApplicationAssociationRegistration](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration) API 內某些方法呼叫的功能已變更，因此不應再使用。

    -   **請勿** 呼叫 [QueryAppIsDefault](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefault) / [QueryAppIsDefaultAll](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefaultall)判斷應用程式是否為預設值
    -   如果有任何) 是目前預設值，**請勿** 呼叫 [QueryCurrentDefault](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-querycurrentdefault)來判斷哪個應用程式 (
    -   **請勿** 呼叫 [SetAppIsDefault](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-setappasdefault) / [SetAppIsDefaultAll](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-setappasdefaultall)來設定預設應用程式

-   接下來的指引是：

    -   **請勿** 查詢以查看哪一個應用程式是檔案類型或 URI 配置的預設處理常式

    -   **請勿** 嘗試監視檔案類型或 URI 配置的預設處理常式中的變更

    -   **請勿** 嘗試將應用程式設定為檔案類型或 URI 配置的預設處理常式

    -   **請勿** 嘗試從應用程式內管理檔案類型或 URI 配置的預設值

    -   如果您想要允許您應用程式的使用者存取預設管理 UI (應用程式內的管理 UI 已不再支援，**請** 與 [[設定預設程式](../shell/default-programs.md)] 控制台整合) 

        -   呼叫 [IApplicationAssociationRegistrationUI：： LaunchAdvancedAssociationUI](/windows/win32/api/shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui) 可讓使用者存取指定應用程式的 [[設定預設程式](../shell/default-programs.md)] 控制台頁面

## <a name="tests"></a>測試

-   測試以確認應用程式在 [設定預設程式] 控制台中正確註冊
-   測試以確認應用程式正確註冊，以顯示在其所註冊要處理的檔案類型、URI 配置或兩者的 OpenWith 清單中
-   測試以確認應用程式已安裝，且使用者叫用您的應用程式已註冊要處理的檔案類型、URI 配置或兩者時，出現新的代理程式更新

## <a name="resources"></a>資源

-   [Windows 8 Desktop 應用程式中檔案類型和 URI 關聯的最佳作法](/previous-versions/windows/desktop/legacy/cc144156(v=vs.85))
-   [檔案類型關聯和自動播放組建會議簡報](https://channel9.msdn.com/events/BUILD/BUILD2011/PLAT-282T)

 

 