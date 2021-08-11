---
description: 本主題包含教學課程如何使用媒體基礎來播放媒體檔案的資源檔。
ms.assetid: 5454c92b-5f71-4be3-ac98-b2195c482ea4
title: player .rc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6489fce2f63c9abc394fbcac1ecb122bffee9896084674d3fc7f846b2e983890
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118239230"
---
# <a name="playerrc"></a>player .rc

本主題包含教學課程 [如何使用媒體基礎來播放媒體](how-to-play-unprotected-media-files.md)檔案的資源檔。


```C++
// Microsoft Visual C++ generated resource script.
//
#include "resource.h"

#include "windows.h"

/////////////////////////////////////////////////////////////////////////////
#undef APSTUDIO_READONLY_SYMBOLS

/////////////////////////////////////////////////////////////////////////////
// English (U.S.) resources

#if !defined(AFX_RESOURCE_DLL) || defined(AFX_TARG_ENU)
#ifdef _WIN32
LANGUAGE LANG_ENGLISH, SUBLANG_ENGLISH_US
#pragma code_page(1252)
#endif //_WIN32

/////////////////////////////////////////////////////////////////////////////
//
// Menu
//

IDC_MFPLAYBACK MENU 
BEGIN
    POPUP "&File"
    BEGIN
        MENUITEM "&Open File",                  ID_FILE_OPENFILE
        MENUITEM "Open &Url",                   ID_FILE_OPENURL
        MENUITEM SEPARATOR
        MENUITEM "E&xit",                       IDM_EXIT
    END
END


/////////////////////////////////////////////////////////////////////////////
//
// Dialog
//

IDD_OPENURL DIALOGEX 0, 0, 186, 90
STYLE DS_SETFONT | DS_MODALFRAME | DS_FIXEDSYS | WS_POPUP | WS_CAPTION | WS_SYSMENU
CAPTION "Open URL"
FONT 8, "MS Shell Dlg", 400, 0, 0x1
BEGIN
    DEFPUSHBUTTON   "OK",IDOK,75,69,50,14
    PUSHBUTTON      "Cancel",IDCANCEL,129,69,50,14
    EDITTEXT        IDC_EDIT_URL,7,21,172,14,ES_AUTOHSCROLL
    LTEXT           "Enter the URL to open:",IDC_STATIC,7,7,104,8
END

#endif    // English (U.S.) resources
/////////////////////////////////////////////////////////////////////////////

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體會話播放範例](media-session-playback-example.md)
</dt> <dt>

[音訊/視訊播放](audio-video-playback.md)
</dt> </dl>

 

 



