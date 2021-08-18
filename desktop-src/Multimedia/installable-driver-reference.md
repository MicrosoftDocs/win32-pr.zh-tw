---
title: 可安裝的驅動程式參考
description: 可安裝的驅動程式參考
ms.assetid: 869b92f1-2711-4198-9911-3df1ebc58d5f
keywords:
- Windows 多媒體、可安裝的驅動程式參考
- 多媒體、可安裝的驅動程式參考
- 可安裝的驅動程式，參考
- 可安裝的驅動程式參考，關於
- 可安裝驅動程式的參考，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6dd2488f0b07805edbcdc90187309db2a04c9c0ced4f4b5b0af4e50bd983ca4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038638"
---
# <a name="installable-driver-reference"></a>可安裝的驅動程式參考

與可安裝的驅動程式相關聯的函式和訊息會依下列方式分組。

## <a name="loading-and-unloading-drivers"></a>載入和卸載驅動程式

-   [GetDriverModuleHandle](/windows/win32/api/mmiscapi/nf-mmiscapi-getdrivermodulehandle)
-   [OpenDriver](/windows/win32/api/mmiscapi/nf-mmiscapi-opendriver)
-   [SendDriverMessage](/windows/win32/api/mmiscapi/nf-mmiscapi-senddrivermessage)

## <a name="closedriver"></a>CloseDriver

-   [**WINSPOOL.DRV \_ 關閉**](drv-close.md)
-   [**WINSPOOL.DRV \_ DISABLE**](drv-disable.md)
-   [**WINSPOOL.DRV \_ 啟用**](drv-enable.md)
-   [**\_免費 WINSPOOL.DRV**](drv-free.md)
-   [**WINSPOOL.DRV \_ 載入**](drv-load.md)
-   [**WINSPOOL.DRV \_ 開啟**](drv-open.md)

## <a name="configuring-a-driver"></a>設定驅動程式

-   [**WINSPOOL.DRV \_ 設定**](drv-configure.md)
-   [**WINSPOOL.DRV \_ QUERYCONFIGURE**](drv-queryconfigure.md)
-   [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo)

## <a name="installing-a-driver"></a>安裝驅動程式

-   [**WINSPOOL.DRV \_ 安裝**](drv-install.md)
-   [**WINSPOOL.DRV \_ 移除**](drv-remove.md)

## <a name="driver-functions"></a>驅動程式函數

-   [DefDriverProc](/windows/win32/api/mmiscapi/nf-mmiscapi-defdriverproc)
-   [DriverCallback](/windows/win32/api/mmiscapi/nf-mmiscapi-drivercallback)
-   [DriverProc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[可安裝的驅動程式](installable-drivers.md)
</dt> </dl>

 

 