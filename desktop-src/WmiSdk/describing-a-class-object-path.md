---
description: 類別物件路徑描述類別在命名空間中的位置。
ms.assetid: 5ae95707-d023-4102-9b41-140c54b0c5b7
ms.tgt_platform: multiple
title: 描述類別物件路徑
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1cfd603ea3b6de151d297a7f4b6fc8a2a27dfda
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984637"
---
# <a name="describing-a-class-object-path"></a>描述類別物件路徑

類別物件路徑描述類別在命名空間中的位置。

您可以使用下列方法來指定物件路徑：

-   類別的完整物件路徑會將類別名稱附加至命名空間路徑。

    下列範例顯示 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) 類別在 \\ \\ 名為 Admin 之伺服器的根 cimv2 命名空間中的位置。

    ``` syntax
    \\Admin\Root\CimV2:Win32_LogicalDisk
    ```

-   相對物件路徑表示位於目前命名空間中的類別。 類別的相對物件路徑只包含類別名稱。

    下列範例顯示 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) 類別的相對路徑。

    ``` syntax
    Win32_LogicalDisk
    ```

當您查詢類別名稱但未指定實例時，WMI 會傳回類別定義。 下列程式描述如何在 VBScript 中取出類別定義。

**若要在 VBScript 中取出類別定義**

-   您可以使用具有查詢或 [**GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx)的「標記」連接。 您也可以使用 [**SWbemServices。**](swbemservices-get.md)

    下列範例顯示如何使用 [GetObject](/previous-versions//kdccchxa(v=vs.85)) 來取得類別定義。

    ```VB
    strComputer = "."
    Set objWMIService = GetObject("winmgmts:" _
       & "{impersonationLevel=impersonate}!\\" _
       & strComputer & "\root\cimv2:Win32_Printer")
    ```

    

    下列範例顯示如何查詢類別定義。

    ```VB
    strComputer = "."
    Set objWMIService = GetObject("winmgmts:" _
        & "{impersonationLevel=impersonate}!\\" _
        & strComputer & "\root\cimv2")
    Set colInstalledPrinters =  objWMIService.ExecQuery _
        ("Select * from Win32_Printer")
    ```

    

您可以只指定類別名稱，而不是特定實例的路徑，以在 c + + 中取出類別定義。 下列程式描述如何在 c + + 中取出類別定義。

**若要在 c + + 中取出類別定義**

-   呼叫 [**IWbemServices：： GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) 或 [**Iwbemservices：： GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) 函數。

    下列範例示範如何呼叫 [**IWbemServices：： GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) 函數。

    ```C++
    IWbemServices* pSvcs = 0;

    BSTR Path = SysAllocString(L"Win32_LogicalDisk");
    IWbemClassObject *pDiskClass = 0;
    pSvcs->GetObject(Path, 0, 0, &pDiskClass, 0);
    ```

    

    上述程式碼範例需要下列 \# include 語句才能正確編譯。

    ```C++
    #include <wbemidl.h>
    ```

    

 

 
