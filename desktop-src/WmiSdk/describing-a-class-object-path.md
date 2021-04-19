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
# <a name="describing-a-class-object-path"></a><span data-ttu-id="18f23-103">描述類別物件路徑</span><span class="sxs-lookup"><span data-stu-id="18f23-103">Describing a Class Object Path</span></span>

<span data-ttu-id="18f23-104">類別物件路徑描述類別在命名空間中的位置。</span><span class="sxs-lookup"><span data-stu-id="18f23-104">A class object path describes the location of a class within a namespace.</span></span>

<span data-ttu-id="18f23-105">您可以使用下列方法來指定物件路徑：</span><span class="sxs-lookup"><span data-stu-id="18f23-105">You can use the following methods to specify an object path:</span></span>

-   <span data-ttu-id="18f23-106">類別的完整物件路徑會將類別名稱附加至命名空間路徑。</span><span class="sxs-lookup"><span data-stu-id="18f23-106">A full object path to a class appends the class name to a namespace path.</span></span>

    <span data-ttu-id="18f23-107">下列範例顯示 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) 類別在 \\ \\ 名為 Admin 之伺服器的根 cimv2 命名空間中的位置。</span><span class="sxs-lookup"><span data-stu-id="18f23-107">The following example shows the location of the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class within the \\root\\cimv2 namespace on the server named Admin.</span></span>

    ``` syntax
    \\Admin\Root\CimV2:Win32_LogicalDisk
    ```

-   <span data-ttu-id="18f23-108">相對物件路徑表示位於目前命名空間中的類別。</span><span class="sxs-lookup"><span data-stu-id="18f23-108">A relative object path represents a class that resides in the current namespace.</span></span> <span data-ttu-id="18f23-109">類別的相對物件路徑只包含類別名稱。</span><span class="sxs-lookup"><span data-stu-id="18f23-109">A relative object path to a class contains only the class name.</span></span>

    <span data-ttu-id="18f23-110">下列範例顯示 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) 類別的相對路徑。</span><span class="sxs-lookup"><span data-stu-id="18f23-110">The following example shows the relative path to the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class.</span></span>

    ``` syntax
    Win32_LogicalDisk
    ```

<span data-ttu-id="18f23-111">當您查詢類別名稱但未指定實例時，WMI 會傳回類別定義。</span><span class="sxs-lookup"><span data-stu-id="18f23-111">When you query for a class name but specify no instances, WMI returns the class definition.</span></span> <span data-ttu-id="18f23-112">下列程式描述如何在 VBScript 中取出類別定義。</span><span class="sxs-lookup"><span data-stu-id="18f23-112">The following procedure describes how to retrieve a class definition in VBScript.</span></span>

<span data-ttu-id="18f23-113">**若要在 VBScript 中取出類別定義**</span><span class="sxs-lookup"><span data-stu-id="18f23-113">**To retrieve a class definition in VBScript**</span></span>

-   <span data-ttu-id="18f23-114">您可以使用具有查詢或 [**GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx)的「標記」連接。</span><span class="sxs-lookup"><span data-stu-id="18f23-114">You can use the moniker connection either with a query or [**GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx).</span></span> <span data-ttu-id="18f23-115">您也可以使用 [**SWbemServices。**](swbemservices-get.md)</span><span class="sxs-lookup"><span data-stu-id="18f23-115">You can also use [**SWbemServices.Get**](swbemservices-get.md).</span></span>

    <span data-ttu-id="18f23-116">下列範例顯示如何使用 [GetObject](/previous-versions//kdccchxa(v=vs.85)) 來取得類別定義。</span><span class="sxs-lookup"><span data-stu-id="18f23-116">The following example shows how to use [GetObject](/previous-versions//kdccchxa(v=vs.85)) to get a class definition.</span></span>

    ```VB
    strComputer = "."
    Set objWMIService = GetObject("winmgmts:" _
       & "{impersonationLevel=impersonate}!\\" _
       & strComputer & "\root\cimv2:Win32_Printer")
    ```

    

    <span data-ttu-id="18f23-117">下列範例顯示如何查詢類別定義。</span><span class="sxs-lookup"><span data-stu-id="18f23-117">The following example shows how to query for a class definition.</span></span>

    ```VB
    strComputer = "."
    Set objWMIService = GetObject("winmgmts:" _
        & "{impersonationLevel=impersonate}!\\" _
        & strComputer & "\root\cimv2")
    Set colInstalledPrinters =  objWMIService.ExecQuery _
        ("Select * from Win32_Printer")
    ```

    

<span data-ttu-id="18f23-118">您可以只指定類別名稱，而不是特定實例的路徑，以在 c + + 中取出類別定義。</span><span class="sxs-lookup"><span data-stu-id="18f23-118">You can retrieve a class definition in C++ by specifying only the class name and no path to a particular instance.</span></span> <span data-ttu-id="18f23-119">下列程式描述如何在 c + + 中取出類別定義。</span><span class="sxs-lookup"><span data-stu-id="18f23-119">The following procedure describes how to retrieve a class definition in C++.</span></span>

<span data-ttu-id="18f23-120">**若要在 c + + 中取出類別定義**</span><span class="sxs-lookup"><span data-stu-id="18f23-120">**To retrieve a class definition in C++**</span></span>

-   <span data-ttu-id="18f23-121">呼叫 [**IWbemServices：： GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) 或 [**Iwbemservices：： GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) 函數。</span><span class="sxs-lookup"><span data-stu-id="18f23-121">Make a call to the [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) or [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) functions.</span></span>

    <span data-ttu-id="18f23-122">下列範例示範如何呼叫 [**IWbemServices：： GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) 函數。</span><span class="sxs-lookup"><span data-stu-id="18f23-122">The following example shows how to call the [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) function.</span></span>

    ```C++
    IWbemServices* pSvcs = 0;

    BSTR Path = SysAllocString(L"Win32_LogicalDisk");
    IWbemClassObject *pDiskClass = 0;
    pSvcs->GetObject(Path, 0, 0, &pDiskClass, 0);
    ```

    

    <span data-ttu-id="18f23-123">上述程式碼範例需要下列 \# include 語句才能正確編譯。</span><span class="sxs-lookup"><span data-stu-id="18f23-123">The previous code example requires the following \#include statement to compile correctly.</span></span>

    ```C++
    #include <wbemidl.h>
    ```

    

 

 
