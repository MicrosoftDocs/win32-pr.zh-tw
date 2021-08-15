---
description: 本主題說明如何在 Microsoft DirectShow 中將元件實作為動態連結程式庫 (DLL) 。
ms.assetid: cb935c26-2dc9-4ab3-810d-b63f1018a62a
title: DLL 函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f8c10951c63e14656fa967693145444c5d5fbffd96a2b11fa9ae4201ac89ae7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117821082"
---
# <a name="dll-functions"></a>DLL 函數

本主題說明如何在 Microsoft DirectShow 中將元件實作為動態連結程式庫 (DLL) 。

DLL 必須執行下列函式，才能註冊、取消註冊，並將其載入至記憶體。

-   [*DllMain*](/windows/desktop/Dlls/dllmain)： DLL 進入點。 名稱 *DllMain* 是程式庫定義函數名稱的預留位置。 DirectShow 的執行會使用名稱 **DllEntryPoint**。 如需詳細資訊，請參閱 Platform SDK。
-   [**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject)：建立 class factory 實例。 如上一節所述。
-   [**DllCanUnloadNow**](/windows/desktop/api/combaseapi/nf-combaseapi-dllcanunloadnow)：查詢是否可以安全地卸載 DLL。
-   [**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver)：建立 DLL 的登錄專案。
-   [**DllUnregisterServer**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver)：移除 DLL 的登錄專案。

在這些情況下，前三個是由 DirectShow 所執行。 如果您的 factory 範本在 [**m \_ lpfnInit**](cfactorytemplate-m-lpfninit.md) 成員變數中提供初始化函式，則會從 DLL 進入點函數內部呼叫該函式。 如需有關系統何時呼叫 DLL 進入點函數的詳細資訊，請參閱 [*DllMain*](/windows/desktop/Dlls/dllmain)。

您必須執行 [**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver)和 [**DllUnregisterServer**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver)，但 DirectShow 會提供名為 [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md)的函式來執行必要的工作。 您的元件可以直接包裝此函式，如下列範例所示：


```C++
STDAPI DllRegisterServer()
{
    return AMovieDllRegisterServer2( TRUE );
}

STDAPI DllUnregisterServer()
{
    return AMovieDllRegisterServer2( FALSE );
}
```



不過，在 [**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver) 和 [**DllUnregisterServer**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver) 中，您可以視需要自訂註冊程式。 如果您的 DLL 包含篩選器，您可能需要執行一些額外的工作。 如需詳細資訊，請參閱[如何註冊 DirectShow 篩選](how-to-register-directshow-filters.md)。

在模組定義中 ( .def) 檔案中，匯出所有 DLL 函式，但不包括進入點函數。 以下是 .def 檔案的範例：


```C++
EXPORTS
    DllGetClassObject PRIVATE
    DllCanUnloadNow PRIVATE
    DllRegisterServer PRIVATE
    DllUnregisterServer PRIVATE
```



您可以使用 Regsvr32.exe 公用程式來註冊 DLL。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[如何建立 DirectShow 篩選 DLL](how-to-create-a-dll.md)
</dt> </dl>

 

 
