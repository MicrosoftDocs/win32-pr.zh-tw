---
description: 圖形類別的其中一個函式會接收裝置內容控制碼和印表機控制碼。
ms.assetid: 9be67cb2-4bf9-4758-af03-7d92dd04feaf
title: 藉由提供印表機控制代碼來最佳化列印
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a247af3de037e220432c424c408b4055690ff861
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972157"
---
# <a name="optimizing-printing-by-providing-a-printer-handle"></a><span data-ttu-id="cca59-103">藉由提供印表機控制代碼來最佳化列印</span><span class="sxs-lookup"><span data-stu-id="cca59-103">Optimizing Printing by Providing a Printer Handle</span></span>

<span data-ttu-id="cca59-104">[**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)類別的其中一個函式會接收裝置內容控制碼和印表機控制碼。</span><span class="sxs-lookup"><span data-stu-id="cca59-104">One of the constructors for the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class receives a device context handle and a printer handle.</span></span> <span data-ttu-id="cca59-105">當您將 Windows GDI + 命令傳送至特定 PostScript 印表機時，如果您使用該特定的函式建立 **圖形** 物件，效能將會更好。</span><span class="sxs-lookup"><span data-stu-id="cca59-105">When you send Windows GDI+ commands to certain PostScript printers, the performance will be better if you create your **Graphics** object with that particular constructor.</span></span>

<span data-ttu-id="cca59-106">下列主控台應用程式會呼叫 [GetDefaultPrinter](../printdocs/getdefaultprinter.md) 來取得預設印表機的名稱。</span><span class="sxs-lookup"><span data-stu-id="cca59-106">The following console application calls [GetDefaultPrinter](../printdocs/getdefaultprinter.md) to get the name of the default printer.</span></span> <span data-ttu-id="cca59-107">程式碼會將印表機名稱傳遞至 [CreateDC](/windows/win32/api/wingdi/nf-wingdi-createdcw) ，以取得印表機的裝置內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="cca59-107">The code passes the printer name to [CreateDC](/windows/win32/api/wingdi/nf-wingdi-createdcw) to obtain a device context handle for the printer.</span></span> <span data-ttu-id="cca59-108">程式碼也會將印表機名稱傳遞至 [OpenPrinter](../printdocs/openprinter.md) ，以取得印表機控制碼。</span><span class="sxs-lookup"><span data-stu-id="cca59-108">The code also passes the printer name to [OpenPrinter](../printdocs/openprinter.md) to obtain a printer handle.</span></span> <span data-ttu-id="cca59-109">裝置內容控制碼和印表機控制碼都會傳遞至 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 的函式。</span><span class="sxs-lookup"><span data-stu-id="cca59-109">Both the device context handle and the printer handle are passed to the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) constructor.</span></span> <span data-ttu-id="cca59-110">然後在印表機上繪製兩個圖形。</span><span class="sxs-lookup"><span data-stu-id="cca59-110">Then two figures are drawn on the printer.</span></span>

> [!Note]  
> <span data-ttu-id="cca59-111">只有在 Windows 2000 和更新版本才支援 [GetDefaultPrinter](../printdocs/getdefaultprinter.md) 函數。</span><span class="sxs-lookup"><span data-stu-id="cca59-111">The [GetDefaultPrinter](../printdocs/getdefaultprinter.md) function is supported only on Windows 2000 and later.</span></span>

 


```
#include <windows.h>
#include <gdiplus.h>
#include <stdio.h>
using namespace Gdiplus;

INT main()
{
   // Initialize GDI+.
   GdiplusStartupInput gdiplusStartupInput;
   ULONG_PTR gdiplusToken;
   GdiplusStartup(&gdiplusToken, &gdiplusStartupInput, NULL);

   DWORD   size;
   HDC     hdcPrint;
   HANDLE  printerHandle;

   DOCINFO docInfo;
   ZeroMemory(&docInfo, sizeof(docInfo));
   docInfo.cbSize = sizeof(docInfo);
   docInfo.lpszDocName = "GdiplusPrint";

   // Get the length of the printer name.
   GetDefaultPrinter(NULL, &size);
   TCHAR* buffer = new TCHAR[size];

   // Get the printer name.
   if(!GetDefaultPrinter(buffer, &size))
   {
      printf("Failure");
   }
   else
   {
      // Get a device context for the printer.
      hdcPrint = CreateDC(NULL, buffer, NULL, NULL);

      // Get a printer handle.
      OpenPrinter(buffer, &printerHandle, NULL);

      StartDoc(hdcPrint, &docInfo);
      StartPage(hdcPrint);
         Graphics* graphics = new Graphics(hdcPrint, printerHandle);
         Pen* pen = new Pen(Color(255, 0, 0, 0));
         graphics->DrawRectangle(pen, 200, 500, 200, 150);
         graphics->DrawEllipse(pen, 200, 500, 200, 150);
         delete(pen);
         delete(graphics);
      EndPage(hdcPrint);
      EndDoc(hdcPrint);

      ClosePrinter(printerHandle);
      DeleteDC(hdcPrint);
   }

   delete buffer;
   
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



 

 
