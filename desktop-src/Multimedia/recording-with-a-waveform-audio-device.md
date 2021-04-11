---
title: 使用 Waveform-Audio 裝置錄製
description: 使用 Waveform-Audio 裝置錄製
ms.assetid: b29a07d1-1b92-4d66-9f2d-ccfbf4074876
keywords:
- mciSendCommand 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb7ab9df07cbe9748fb082239bac20f511010ab3
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314860"
---
# <a name="recording-with-a-waveform-audio-device"></a><span data-ttu-id="23016-104">使用 Waveform-Audio 裝置錄製</span><span class="sxs-lookup"><span data-stu-id="23016-104">Recording with a Waveform-Audio Device</span></span>

<span data-ttu-id="23016-105">下列範例會開啟具有新檔案的波形音訊裝置、指定時間的記錄、播放記錄，並提示使用者儲存錄製（如有需要）。</span><span class="sxs-lookup"><span data-stu-id="23016-105">The following example opens a waveform-audio device with a new file, records for the specified time, plays the recording, and prompts the user to save the recording if desired.</span></span> <span data-ttu-id="23016-106">它會使用 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。</span><span class="sxs-lookup"><span data-stu-id="23016-106">It uses the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function.</span></span>


```C++
// Uses the MCI_OPEN, MCI_RECORD, and MCI_SAVE commands to record and
// save a waveform-audio file. Returns 0L if successful; otherwise,
// it returns an MCI error code.

DWORD recordWAVEFile(DWORD dwMilliSeconds)
{
    UINT wDeviceID;
    DWORD dwReturn;
    MCI_OPEN_PARMS mciOpenParms;
    MCI_RECORD_PARMS mciRecordParms;
    MCI_SAVE_PARMS mciSaveParms;
    MCI_PLAY_PARMS mciPlayParms;

    // Open a waveform-audio device with a new file for recording.
    mciOpenParms.lpstrDeviceType = "waveaudio";
    mciOpenParms.lpstrElementName = "";
    if (dwReturn = mciSendCommand(0, MCI_OPEN,
        MCI_OPEN_ELEMENT | MCI_OPEN_TYPE, 
        (DWORD)(LPVOID) &mciOpenParms))
    {
        // Failed to open device; don't close it, just return error.
        return (dwReturn);
    }

    // The device opened successfully; get the device ID.
    wDeviceID = mciOpenParms.wDeviceID;

    // Begin recording and record for the specified number of 
    // milliseconds. Wait for recording to complete before continuing. 
    // Assume the default time format for the waveform-audio device 
    // (milliseconds).
    mciRecordParms.dwTo = dwMilliSeconds;
    if (dwReturn = mciSendCommand(wDeviceID, MCI_RECORD, 
        MCI_TO | MCI_WAIT, (DWORD)(LPVOID) &mciRecordParms))
    {
        mciSendCommand(wDeviceID, MCI_CLOSE, 0, NULL);
        return (dwReturn);
    }

    // Play the recording and query user to save the file.
    mciPlayParms.dwFrom = 0L;
    if (dwReturn = mciSendCommand(wDeviceID, MCI_PLAY,
        MCI_FROM | MCI_WAIT, (DWORD)(LPVOID) &mciPlayParms))
    {
        mciSendCommand(wDeviceID, MCI_CLOSE, 0, NULL);
        return (dwReturn);
    }
    if (MessageBox(hMainWnd, "Do you want to save this recording?",
        "", MB_YESNO) == IDNO)
    {
        mciSendCommand(wDeviceID, MCI_CLOSE, 0, NULL);
        return (0L);
    }

    // Save the recording to a file named TEMPFILE.WAV. Wait for
    // the operation to complete before continuing.
    mciSaveParms.lpfilename = "tempfile.wav";
    if (dwReturn = mciSendCommand(wDeviceID, MCI_SAVE,
        MCI_SAVE_FILE | MCI_WAIT, (DWORD)(LPVOID) &mciSaveParms))
    {
        mciSendCommand(wDeviceID, MCI_CLOSE, 0, NULL);
        return (dwReturn);
    }

    return (0L);
}
```



 

 