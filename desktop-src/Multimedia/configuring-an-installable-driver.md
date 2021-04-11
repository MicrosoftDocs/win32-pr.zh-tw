---
title: 設定可安裝的驅動程式
description: 設定可安裝的驅動程式
ms.assetid: c81f4bcb-38c6-42f1-a50d-1f700c6a3c37
keywords:
- 可安裝的驅動程式，設定
- 設定可安裝的驅動程式
- OpenDriver 函式
- SendDriverMessage 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ad0ad16d719152dba0dc0b2ca6224122831a0ce
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023306"
---
# <a name="configuring-an-installable-driver"></a><span data-ttu-id="bd474-107">設定可安裝的驅動程式</span><span class="sxs-lookup"><span data-stu-id="bd474-107">Configuring an Installable Driver</span></span>

<span data-ttu-id="bd474-108">若要指示可安裝的驅動程式來執行有用的工作，您必須使用 [OpenDriver](/windows/win32/api/mmiscapi/nf-mmiscapi-opendriver) 函式來開啟驅動程式，並使用 [SendDriverMessage](/windows/win32/api/mmiscapi/nf-mmiscapi-senddrivermessage) 函式來傳送訊息。</span><span class="sxs-lookup"><span data-stu-id="bd474-108">To direct an installable driver to carry out useful tasks, you must open the driver by using the [OpenDriver](/windows/win32/api/mmiscapi/nf-mmiscapi-opendriver) function and send it messages by using the [SendDriverMessage](/windows/win32/api/mmiscapi/nf-mmiscapi-senddrivermessage) function.</span></span> <span data-ttu-id="bd474-109">下列範例顯示如何指示驅動程式顯示其設定對話方塊。</span><span class="sxs-lookup"><span data-stu-id="bd474-109">The following example shows how to direct the driver to display its configuration dialog box.</span></span>


```C++
LONG MyConfigureDriver()
{
    HDRVR hdrvr;
    DRVCONFIGINFO dci;
    LONG lRes;

    // Open the driver (no additional parameters needed this time).
    if ((hdrvr = OpenDriver(L"\\samples\\sample.drv", 0, 0)) == 0) {
        // Can't open the driver
        return DRVCNF_CANCEL;
    }

    // Make sure driver has a configuration dialog box.
    if (SendDriverMessage(hdrvr, DRV_QUERYCONFIGURE, 0, 0) != 0) {
        // Set the DRVCONFIGINFO structure and send the message
        dci.dwDCISize = sizeof (dci);
        dci.lpszDCISectionName = (LPWSTR)0;
        dci.lpszDCIAliasName = (LPWSTR)0;
        lRes = SendDriverMessage(hdrvr, DRV_CONFIGURE, 0, (LONG)&dci);
     }

    // Close the driver (no additional parameters needed this time).
    CloseDriver(hdrvr, 0, 0);

    return lRes;
}
 
```



 

 