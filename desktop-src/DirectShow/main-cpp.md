---
description: 本文包含 DirectShow 中教學課程音訊/影片播放的主要 .cpp 檔案程式碼。
ms.assetid: d1a4ee7d-b05d-4050-b0a5-25c28157646f
title: 主要 .cpp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eae95293e5f9f3f6511834ff030898c770c673d60ea761353f4637cb583e5c15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073102"
---
# <a name="maincpp"></a>主要 .cpp

本主題包含 DirectShow 中的教學課程[音訊/影片播放](audio-video-playback-in-directshow.md)程式碼。


```C++
// THIS CODE AND INFORMATION IS PROVIDED "AS IS" WITHOUT WARRANTY OF
// ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO
// THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A
// PARTICULAR PURPOSE.
//
// Copyright (c) Microsoft Corporation. All rights reserved.


#include <new>
#include <windows.h>
#include <dshow.h>
#include "playback.h"

#pragma comment(lib, "strmiids")

DShowPlayer *g_pPlayer = NULL;

LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam);
void CALLBACK OnGraphEvent(HWND hwnd, long eventCode, LONG_PTR param1, LONG_PTR param2);
void OnChar(HWND hwnd, wchar_t c);
void OnFileOpen(HWND hwnd);
void OnPaint(HWND hwnd);
void OnSize(HWND hwnd);
void NotifyError(HWND hwnd, PCWSTR pszMessage);

int WINAPI wWinMain(HINSTANCE hInstance, HINSTANCE, PWSTR pCmdLine, int nCmdShow)
{
    if (FAILED(CoInitializeEx(NULL, COINIT_MULTITHREADED | COINIT_DISABLE_OLE1DDE)))
    {
        NotifyError(NULL, L"CoInitializeEx failed.");
        return 0;
    }

    // Register the window class.
    const wchar_t CLASS_NAME[]  = L"Sample Window Class";
    
    WNDCLASS wc = { };
    wc.lpfnWndProc   = WindowProc;
    wc.hInstance     = hInstance;
    wc.lpszClassName = CLASS_NAME;

    RegisterClass(&wc);

    HWND hwnd = CreateWindowEx(0, CLASS_NAME, L"DirectShow Playback", 
        WS_OVERLAPPEDWINDOW, CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, 
        CW_USEDEFAULT, NULL, NULL, hInstance, NULL);

    if (hwnd == NULL)
    {
        NotifyError(NULL, L"CreateWindowEx failed.");
        return 0;
    }

    ShowWindow(hwnd, nCmdShow);

    // Run the message loop.

    MSG msg = { };
    while (GetMessage(&msg, NULL, 0, 0))
    {
        TranslateMessage(&msg);
        DispatchMessage(&msg);
    }
    return 0;
}

LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
    case WM_CHAR:
        OnChar(hwnd, (wchar_t)wParam);
        return 0;

    case WM_CREATE:
        g_pPlayer = new (std::nothrow) DShowPlayer(hwnd);
        if (g_pPlayer == NULL)
        {
            return -1;
        }
        return 0;

    case WM_DESTROY:
        delete g_pPlayer;
        PostQuitMessage(0);
        return 0;

    case WM_DISPLAYCHANGE:
        g_pPlayer->DisplayModeChanged();
        break;

    case WM_ERASEBKGND:
        return 1;

    case WM_PAINT:
        OnPaint(hwnd);
        return 0;

    case WM_SIZE:
        OnSize(hwnd);
        return 0;

    case WM_GRAPH_EVENT:
       g_pPlayer->HandleGraphEvent(OnGraphEvent);
       return 0;
    }
    return DefWindowProc(hwnd, uMsg, wParam, lParam);
}

void OnPaint(HWND hwnd)
{
    PAINTSTRUCT ps;
    HDC hdc;

    hdc = BeginPaint(hwnd, &ps);

    if (g_pPlayer->State() != STATE_NO_GRAPH && g_pPlayer->HasVideo())
    {
        // The player has video, so ask the player to repaint. 
        g_pPlayer->Repaint(hdc);
    }
    else
    {
        FillRect(hdc, &ps.rcPaint, (HBRUSH) (COLOR_WINDOW+1));
    }

    EndPaint(hwnd, &ps);
}

void OnSize(HWND hwnd)
{
    if (g_pPlayer)
    {
        RECT rc;
        GetClientRect(hwnd, &rc);

        g_pPlayer->UpdateVideoWindow(&rc);
    }
}

void CALLBACK OnGraphEvent(HWND hwnd, long evCode, LONG_PTR param1, LONG_PTR param2)
{
    switch (evCode)
    {
    case EC_COMPLETE:
    case EC_USERABORT:
        g_pPlayer->Stop();
        break;

    case EC_ERRORABORT:
        NotifyError(hwnd, L"Playback error.");
        g_pPlayer->Stop();
        break;
    }
}

void OnChar(HWND hwnd, wchar_t c)
{
    switch (c)
    {
    case L'o':
    case L'O':
        OnFileOpen(hwnd);
        break;

    case L'p':
    case L'P':
        if (g_pPlayer->State() == STATE_RUNNING)
        {
            g_pPlayer->Pause();
        }
        else
        {
            g_pPlayer->Play();
        }
        break;
    }
}

void OnFileOpen(HWND hwnd)
{
    OPENFILENAME ofn;
    ZeroMemory(&ofn, sizeof(ofn));

    WCHAR szFileName[MAX_PATH];
    szFileName[0] = L'\0';

    ofn.lStructSize = sizeof(ofn);
    ofn.hwndOwner = hwnd;
    ofn.hInstance = GetModuleHandle(NULL);
    ofn.lpstrFilter = L"All (*.*)/0*.*/0";
    ofn.lpstrFile = szFileName;
    ofn.nMaxFile = MAX_PATH;
    ofn.Flags = OFN_FILEMUSTEXIST;

    HRESULT hr;

    if (GetOpenFileName(&ofn))
    {
        hr = g_pPlayer->OpenFile(szFileName);

        InvalidateRect(hwnd, NULL, FALSE);

        if (SUCCEEDED(hr))
        {
            // If this file has a video stream, notify the video renderer 
            // about the size of the destination rectangle.
            OnSize(hwnd);
        }
        else
        {
            NotifyError(hwnd, TEXT("Cannot open this file."));
        }
    }
}

void NotifyError(HWND hwnd, PCWSTR pszMessage)
{
    MessageBox(hwnd, pszMessage, TEXT("Error"), MB_OK | MB_ICONERROR);
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow 中的音訊/影片播放](audio-video-playback-in-directshow.md)
</dt> <dt>

[DirectShow播放範例](directshow-playback-example.md)
</dt> </dl>

 

 



