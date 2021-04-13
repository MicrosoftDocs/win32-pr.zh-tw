---
description: 本主題包含在 DirectShow 中播放教學課程音訊/影片的程式碼。
ms.assetid: d1a4ee7d-b05d-4050-b0a5-25c28157646f
title: 主要 .cpp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e84d164b31ad02006b61cef6b055cbb3c466983a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104509965"
---
# <a name="maincpp"></a><span data-ttu-id="f1276-103">主要 .cpp</span><span class="sxs-lookup"><span data-stu-id="f1276-103">main.cpp</span></span>

<span data-ttu-id="f1276-104">本主題包含 [在 DirectShow 中播放教學課程音訊/影片](audio-video-playback-in-directshow.md)的程式碼。</span><span class="sxs-lookup"><span data-stu-id="f1276-104">This topic contains code for the tutorial [Audio/Video Playback in DirectShow](audio-video-playback-in-directshow.md).</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="f1276-105">相關主題</span><span class="sxs-lookup"><span data-stu-id="f1276-105">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1276-106">在 DirectShow 播放音訊/影片</span><span class="sxs-lookup"><span data-stu-id="f1276-106">Audio/Video Playback in DirectShow</span></span>](audio-video-playback-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="f1276-107">DirectShow 播放範例</span><span class="sxs-lookup"><span data-stu-id="f1276-107">DirectShow Playback Example</span></span>](directshow-playback-example.md)
</dt> </dl>

 

 



