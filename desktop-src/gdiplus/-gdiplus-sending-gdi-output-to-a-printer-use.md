---
description: 使用 Windows GDI + 在印表機上進行繪製，類似于使用 GDI + 在電腦螢幕上繪製。 若要在印表機上繪圖，請取得印表機的裝置內容控制碼，然後將該控制碼傳遞給圖形的函式。
ms.assetid: a76cca57-6ed8-44cd-a9f6-f2692d14b68a
title: 將 GDI+ 輸出傳送至印表機
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96c1c4f6c05e4918663284e6d7747952040dcddf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026591"
---
# <a name="sending-gdi-output-to-a-printer"></a>將 GDI+ 輸出傳送至印表機

使用 Windows GDI + 在印表機上進行繪製，類似于使用 GDI + 在電腦螢幕上繪製。 若要在印表機上繪圖，請取得印表機的裝置內容控制碼，然後將該控制碼傳遞給 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 的函式。

下列主控台應用程式會在名為 Myprinter.local 的印表機上繪製線條、矩形和橢圓形：


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

   // Get a device context for the printer.
   HDC hdcPrint = CreateDC(NULL, TEXT("\\\\printserver\\print1"), NULL, NULL);

   DOCINFO docInfo;
   ZeroMemory(&docInfo, sizeof(docInfo));
   docInfo.cbSize = sizeof(docInfo);
   docInfo.lpszDocName = "GdiplusPrint";

   StartDoc(hdcPrint, &docInfo);
   StartPage(hdcPrint);
      Graphics* graphics = new Graphics(hdcPrint);
      Pen* pen = new Pen(Color(255, 0, 0, 0));
      graphics->DrawLine(pen, 50, 50, 350, 550);
      graphics->DrawRectangle(pen, 50, 50, 300, 500);
      graphics->DrawEllipse(pen, 50, 50, 300, 500);
      delete pen;
      delete graphics;
   EndPage(hdcPrint);
   EndDoc(hdcPrint);
   
   DeleteDC(hdcPrint);
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



在上述程式碼中， [StartDoc](/windows/win32/api/wingdi/nf-wingdi-startdocw) 和 [EndDoc](/windows/win32/api/wingdi/nf-wingdi-enddoc) 函式的呼叫之間有三個 gdi + 繪製命令，每個命令都會接收印表機裝置內容控制碼。 StartDoc 和 EndDoc 之間的所有圖形命令都會路由傳送至暫存中繼檔。 呼叫 EndDoc 之後，印表機驅動程式會將中繼檔中的資料轉換成使用特定印表機所需的格式。

> [!Note]  
> 如果未針對使用中的印表機啟用幕後處理，則圖形輸出不會路由至中繼檔。 相反地，印表機驅動程式會處理個別的圖形命令，然後傳送至印表機。

 

一般來說，您不會想要在先前的主控台應用程式中硬式編碼印表機的名稱。 將名稱硬式編碼的另一種替代方式是呼叫 [GetDefaultPrinter](../printdocs/getdefaultprinter.md) 來取得預設印表機的名稱。 呼叫 GetDefaultPrinter 之前，您必須配置夠大的緩衝區以容納印表機名稱。 您可以藉由呼叫 GetDefaultPrinter，並傳遞 **Null** 做為第一個引數，來判斷所需的緩衝區大小。

> [!Note]  
> 只有在 Windows 2000 和更新版本才支援 [GetDefaultPrinter](../printdocs/getdefaultprinter.md) 函數。

 

下列主控台應用程式會取得預設印表機的名稱，然後在該印表機上繪製一個矩形和一個橢圓形。 [**圖形：:D rawrectangle**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint))呼叫會在對 [StartPage](/windows/win32/api/wingdi/nf-wingdi-startpage)和 [EndPage](/windows/win32/api/wingdi/nf-wingdi-endpage)的呼叫之間，因此矩形本身會在頁面上。 同樣地，橢圓形本身也位於頁面上。


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

   DWORD size;
   HDC hdcPrint;

   DOCINFO docInfo;
   ZeroMemory(&docInfo, sizeof(docInfo));
   docInfo.cbSize = sizeof(docInfo);
   docInfo.lpszDocName = "GdiplusPrint";

   // Get the size of the default printer name.
   GetDefaultPrinter(NULL, &size);

   // Allocate a buffer large enough to hold the printer name.
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

      StartDoc(hdcPrint, &docInfo);
         Graphics* graphics;
         Pen* pen = new Pen(Color(255, 0, 0, 0));

         StartPage(hdcPrint);
            graphics = new Graphics(hdcPrint);
            graphics->DrawRectangle(pen, 50, 50, 200, 300);
            delete graphics;
         EndPage(hdcPrint);

         StartPage(hdcPrint);
            graphics = new Graphics(hdcPrint);
            graphics->DrawEllipse(pen, 50, 50, 200, 300);
            delete graphics;
         EndPage(hdcPrint);

         delete pen;
      EndDoc(hdcPrint);

      DeleteDC(hdcPrint);
   }

   delete buffer;

   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



 

 
