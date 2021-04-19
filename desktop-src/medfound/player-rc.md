---
description: 本主題包含教學課程如何使用媒體基礎來播放媒體檔案的資源檔。
ms.assetid: 5454c92b-5f71-4be3-ac98-b2195c482ea4
title: player .rc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73ed6537a42b572d88571a5d81abb97f6fb7fe35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977203"
---
# <a name="playerrc"></a><span data-ttu-id="db35e-103">player .rc</span><span class="sxs-lookup"><span data-stu-id="db35e-103">player.rc</span></span>

<span data-ttu-id="db35e-104">本主題包含教學課程 [如何使用媒體基礎來播放媒體](how-to-play-unprotected-media-files.md)檔案的資源檔。</span><span class="sxs-lookup"><span data-stu-id="db35e-104">This topic contains the resource file for the tutorial [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md).</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="db35e-105">相關主題</span><span class="sxs-lookup"><span data-stu-id="db35e-105">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db35e-106">媒體會話播放範例</span><span class="sxs-lookup"><span data-stu-id="db35e-106">Media Session Playback Example</span></span>](media-session-playback-example.md)
</dt> <dt>

[<span data-ttu-id="db35e-107">音訊/視訊播放</span><span class="sxs-lookup"><span data-stu-id="db35e-107">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> </dl>

 

 



