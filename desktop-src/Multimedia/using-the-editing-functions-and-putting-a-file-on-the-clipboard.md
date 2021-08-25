---
title: 使用編輯功能並將檔案放在剪貼簿上
description: 使用編輯功能並將檔案放在剪貼簿上
ms.assetid: 2c69e44a-5f45-45e7-bbad-c593359943a0
keywords:
- EditStreamClone 函式
- EditStreamCopy 函式
- EditStreamCut 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a2f3ad09b882d9df6d9b7603e6f5596789ba32157f6050916ae9212f52395a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119804528"
---
# <a name="using-the-editing-functions-and-putting-a-file-on-the-clipboard"></a>使用編輯功能並將檔案放在剪貼簿上

下列範例會從資料流程的陣列中剪下、複製或刪除區段。 剪下和複製的資料流程會合並到新的檔案中，並放在剪貼簿上。 使用的函數包括 [**EditStreamClone**](/windows/desktop/api/Vfw/nf-vfw-editstreamclone)、 [**EditStreamCopy**](/windows/desktop/api/Vfw/nf-vfw-editstreamcopy)和 [**EditStreamCut**](/windows/desktop/api/Vfw/nf-vfw-editstreamcut)。


```C++
// Global variables 
// gcpavi - count of streams in an AVI file 
// gapavi[] - array of stream-interface pointers, used as data source 
// gapaviSel[] - stream-interface pointers of edited streams 
// galSelStart[] - edit starting point in each stream 
// galSelLen[] - length of edit to make in each stream 
// gapaviTemp[] - array of stream-interface pointers put on clipboard 
// 
// Comment: 
//     The editable streams in gapaviSel have been 
//     initialized with CreateEditableStream. 
 
case MENU_CUT: 
case MENU_COPY: 
case MENU_DELETE: 
{ 
    PAVIFILE pf; 
    int      i; 
 
    // Walk list of selections and make streams out of each section. 
    gcpaviSel = 0;  // index counter for destination streams 
    for (i = 0; i < gcpavi; i++) { 
        if (galSelStart[i] != -1) { 
            if (wParam == MENU_COPY) 
                EditStreamCopy(gapavi[i], &galSelStart[i], 
                &galSelLen[i], &gapaviSel[gcpaviSel++]); 
            else { 
                EditStreamCut(gapavi[i], &galSelStart[i], 
                &galSelLen[i], &gapaviSel[gcpaviSel++]); 
            } 
        } 
    } 
 
. 
. 
. 
    // Put on the clipboard if segment is not deleted. 
    if (gcpaviSel && wParam != MENU_DELETE) { 
        PAVISTREAM   gapaviTemp[MAXNUMSTREAMS]; 
        int i; 
 
        // Clone the edited streams, so that if the user does 
        // more editing, the clipboard won't change. 
        for (i = 0; i < gcpaviSel; i++) { 
            gapaviTemp[i] = NULL; 
            EditStreamClone(gapaviSel[i], &gapaviTemp[i]); 
            // 
            // Place error check here. 
            // 
        } 
 
        // Create a file from the streams and put on clipboard. 
        AVIMakeFileFromStreams(&pf, gcpaviSel, gapaviTemp); 
        AVIPutFileOnClipboard(pf); 
 
        // Release clone streams. 
        for (i = 0; i < gcpaviSel; i++) { 
            AVIStreamRelease(gapaviTemp[i]); 
        } 
 
        // Release file put on clipboard. 
        AVIFileRelease(pf); 
    } 
 
    // Release streams created. 
    for (i = 0; i < gcpaviSel; i++) 
        AVIStreamRelease(gapaviSel[i]); 
} 
 
```



 

 




