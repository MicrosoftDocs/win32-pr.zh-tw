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
# <a name="optimizing-printing-by-providing-a-printer-handle"></a>藉由提供印表機控制代碼來最佳化列印

[**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)類別的其中一個函式會接收裝置內容控制碼和印表機控制碼。 當您將 Windows GDI + 命令傳送至特定 PostScript 印表機時，如果您使用該特定的函式建立 **圖形** 物件，效能將會更好。

下列主控台應用程式會呼叫 [GetDefaultPrinter](../printdocs/getdefaultprinter.md) 來取得預設印表機的名稱。 程式碼會將印表機名稱傳遞至 [CreateDC](/windows/win32/api/wingdi/nf-wingdi-createdcw) ，以取得印表機的裝置內容控制碼。 程式碼也會將印表機名稱傳遞至 [OpenPrinter](../printdocs/openprinter.md) ，以取得印表機控制碼。 裝置內容控制碼和印表機控制碼都會傳遞至 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 的函式。 然後在印表機上繪製兩個圖形。

> [!Note]  
> 只有在 Windows 2000 和更新版本才支援 [GetDefaultPrinter](../printdocs/getdefaultprinter.md) 函數。

 


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



 

 
