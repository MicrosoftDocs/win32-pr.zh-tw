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
ms.openlocfilehash: 60942b9814abd8e1f6317adb976198a5359df358a994035a15ccf0c59ab18dd0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144931"
---
# <a name="configuring-an-installable-driver"></a>設定可安裝的驅動程式

若要指示可安裝的驅動程式來執行有用的工作，您必須使用 [OpenDriver](/windows/win32/api/mmiscapi/nf-mmiscapi-opendriver) 函式來開啟驅動程式，並使用 [SendDriverMessage](/windows/win32/api/mmiscapi/nf-mmiscapi-senddrivermessage) 函式來傳送訊息。 下列範例顯示如何指示驅動程式顯示其設定對話方塊。


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



 

 