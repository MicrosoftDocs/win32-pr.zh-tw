---
description: 取得印表機裝置內容控制碼的其中一種方式是顯示 [列印] 對話方塊，並允許使用者選擇印表機。
ms.assetid: 73a74186-c916-4ad9-b768-6bc887fd5231
title: 顯示 [列印] 對話方塊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b0d40365c36e3e554812ff137475ab7c6405e91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991362"
---
# <a name="displaying-a-print-dialog-box"></a>顯示 [列印] 對話方塊

取得印表機裝置內容控制碼的其中一種方式是顯示 [列印] 對話方塊，並允許使用者選擇印表機。 [PrintDlg](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85))函式 (顯示對話方塊) 有一個參數是[PrintDlg](/windows/win32/api/commdlg/ns-commdlg-printdlga?redirectedfrom=MSDN)結構的位址。 PRINTDLG 結構有數個成員，但您可以將大部分的成員都設為預設值。 您需要設定的兩個成員為 **lStructSize** 和 **旗標**。 將 **lStructSize** 設定為 PRINTDLG 變數的大小，並將 **旗標** 設定為 PD \_ RETURNDC。 將 **旗標** 設定為 [電腦 \_ RETURNDC] 時，會指定您想要 PrintDlg 函式使用使用者所選印表機的裝置內容控制碼來填滿 **hDC** 欄位。


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
   
   DOCINFO docInfo;
   ZeroMemory(&docInfo, sizeof(docInfo));
   docInfo.cbSize = sizeof(docInfo);
   docInfo.lpszDocName = "GdiplusPrint";
   
   // Create a PRINTDLG structure, and initialize the appropriate fields.
   PRINTDLG printDlg;
   ZeroMemory(&printDlg, sizeof(printDlg));
   printDlg.lStructSize = sizeof(printDlg);
   printDlg.Flags = PD_RETURNDC;
   
   // Display a print dialog box.
   if(!PrintDlg(&printDlg))
   {
      printf("Failure\n");
   }
   else
   {
      // Now that PrintDlg has returned, a device context handle
      // for the chosen printer is in printDlg->hDC.
      
      StartDoc(printDlg.hDC, &docInfo);
      StartPage(printDlg.hDC);
         Graphics* graphics = new Graphics(printDlg.hDC);
         Pen* pen = new Pen(Color(255, 0, 0, 0));
         graphics->DrawRectangle(pen, 200, 500, 200, 150);
         graphics->DrawEllipse(pen, 200, 500, 200, 150);
         graphics->DrawLine(pen, 200, 500, 400, 650);
         delete pen;
         delete graphics;
      EndPage(printDlg.hDC);
      EndDoc(printDlg.hDC); 
   }
   if(printDlg.hDevMode) 
      GlobalFree(printDlg.hDevMode);
   if(printDlg.hDevNames) 
      GlobalFree(printDlg.hDevNames);
   if(printDlg.hDC)
      DeleteDC(printDlg.hDC);
   
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



 

 
