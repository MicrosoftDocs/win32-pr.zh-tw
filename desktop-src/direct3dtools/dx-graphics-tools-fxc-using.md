---
title: 離線編譯
description: 效果編譯器工具 (fxc.exe) 是針對 HLSL 著色器的離線編譯所設計。
ms.assetid: 56806335-a0c7-4247-b40d-ba93486a88ac
keywords:
- fxc.exe，離線編譯
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88a15d3a71dbfb79541a75bd38cb28140d832b45e75a88a52b2d0c8988865f12
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119406328"
---
# <a name="offline-compiling"></a>離線編譯

效果編譯器工具 (fxc.exe) 是針對 HLSL 著色器的離線編譯所設計。

## <a name="compiling-with-the-current-compiler"></a>使用目前的編譯器編譯

目前編譯器所支援的著色器模型會顯示在 [設定檔](dx-graphics-tools-fxc-syntax.md)中。 此範例會編譯著色器模型5.1 目標的圖元著色器。

```
fxc /T ps_5_1 /Fo PixelShader1.fxc PixelShader1.hlsl
```

在此範例中：

-   ps \_ 5 \_ 1 是目標設定檔。
-   PixelShader1. fxc.exe 是輸出物件檔案，其中包含已編譯的著色器。
-   PixelShader1。 hlsl 是來源。

```
fxc /Od /Zi /T ps_5_1 /Fo PixelShader1.fxc PixelShader1.hlsl
```

偵錯工具選項包含其他選項，可停用編譯器優化 (Od) 並啟用 (Zi) 的 debug 資訊，例如行號和符號。

如需命令列選項的完整清單，請參閱 [語法](dx-graphics-tools-fxc-syntax.md) 頁面。

## <a name="compiling-with-the-legacy-compiler"></a>使用舊版編譯器進行編譯

從 Direct3D 10 開始，已不再支援某些著色器模型。 這些包括圖元著色器模型： ps \_ 1 \_ 1、ps \_ 1 \_ 2、ps \_ 1 \_ 3 和 ps \_ 1 \_ 4，支援非常有限的資源且相依于硬體。 編譯器已重新設計為著色器模型 2 (或更高的) ，可讓您在編譯時獲得更高的效率。 這當然會要求您在支援著色器模型2和更新版本的硬體上執行。

另請注意，您應該查閱與您的 FXC.EXE 編譯器版本相關聯的 SDK 版本資訊，以瞭解受/Gec 參數影響的行為。

## <a name="using-the-effect-compiler-tool-in-a-subprocess"></a>在子流程中使用效果編譯器工具

如果應用程式以子流程的形式產生 fxc.exe，請務必確保應用程式會檢查並讀取傳遞至 CreateProcess 函數的輸出或錯誤管道中的任何資料。 如果應用程式只會等待子流程完成，而且其中一個管道已滿，則子流程永遠不會完成。

下列範例程式碼說明如何等候子流程，以及讀取附加至子流程的輸出和錯誤管道。 陣列的內容 `WaitHandles` 對應至子流程的控制碼、stdout 的管道和 stderr 的管道。

```cpp
HANDLE WaitHandles[] = {
  piProcInfo.hProcess, hReadOutPipe, hReadErrorPipe
};

const DWORD BUFSIZE = 4096;
BYTE buff[BUFSIZE];

while (1)
{
    DWORD dwBytesRead, dwBytesAvailable;

    dwWaitResult = WaitForMultipleObjects(3, WaitHandles, FALSE, 60000L);

    // Read from the pipes...
    while (PeekNamedPipe(hReadOutPipe, NULL, 0, NULL, &dwBytesAvailable, NULL) && dwBytesAvailable)
    {
        ReadFile(hReadOutPipe, buff, BUFSIZE - 1, &dwBytesRead, 0);
        streamOut << std::string((char*)buff, (size_t)dwBytesRead);
    }
    while (PeekNamedPipe(hReadErrorPipe, NULL, 0, NULL, &dwBytesAvailable, NULL) && dwBytesAvailable)
    {
        ReadFile(hReadErrorPipe, buff, BUFSIZE - 1, &dwBytesRead, 0);
        streamError << std::string((char*)buff, (size_t)dwBytesRead);
    }

    // Process is done, or we timed out:
    if (dwWaitResult == WAIT_OBJECT_0 || dwWaitResult == WAIT_TIMEOUT)
        break;
}
```

如需有關產生進程的詳細資訊，請參閱 [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa)的參考頁面。

## <a name="related-topics"></a>相關主題

* [效果-編譯器工具](fxc.md)