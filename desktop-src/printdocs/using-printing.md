---
description: 本節說明如何從原生 Windows 桌面程式進行列印。
ms.assetid: C1EDBE38-9D18-41BB-961C-12CF2283C639
title: 桌面應用程式列印
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bf5e0ebab666258f62b1e6bb87497d38a1b521fdde9a7668bb28e3bb3e9868e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112108"
---
# <a name="desktop-app-printing"></a>桌面應用程式列印

本節說明如何從原生 Windows 桌面程式進行列印。

## <a name="overview"></a>概觀

當您從原生 Windows 程式進行列印時，為了提供最佳的使用者體驗，程式必須設計成從專用的執行緒進行列印。 在原生 Windows 程式中，程式會負責管理使用者介面事件和訊息。 列印工作可能需要大量計算的時間，因為應用程式內容是針對印表機呈現，如果在與使用者互動的事件處理相同的執行緒中執行這項處理，則可以防止程式回應使用者互動。

如果您已經熟悉如何撰寫多執行緒原生 Windows 程式，您可以直接前往[如何從 Windows 應用程式進行列印](how-to--print-from-a-windows-application.md)，以及瞭解如何將列印功能新增至您的程式。

### <a name="basic-windows-program-requirements"></a>基本 Windows 計畫需求

為了達到最佳效能和程式回應性，請勿在處理使用者互動的執行緒中執行程式的列印工作處理。

這種從使用者互動的列印區隔將會影響程式管理應用程式資料的方式。 在開始撰寫應用程式之前，您應該徹底瞭解這些含意。 下列主題描述在程式的個別執行緒中處理列印的基本需求。

### <a name="windows-program-basics"></a>Windows程式基本概念

原生 Windows 程式必須提供主視窗程式來處理從作業系統接收的視窗訊息。 Windows 程式中的每個視窗都有對應的 **WndProc** 函式，可處理這些視窗訊息。 執行此函式的執行緒稱為使用者介面或 UI 執行緒。

**使用資源的字串。**  
使用程式資源檔中的字串資源，而不是當您支援另一種語言時，可能需要變更之字串的字串常數。 程式必須先從資源檔取出資源，然後將它複製到本機記憶體緩衝區，程式才能使用字串資源作為字串。 這需要一開始就需要進行一些額外的程式設計，但是未來可以更輕鬆地修改、轉譯和當地語系化程式。  
**在步驟中處理資料。**  
在可能中斷的步驟中處理列印工作。 這種設計可讓使用者在完成之前取消長時間處理作業，並防止程式封鎖可能同時執行的其他程式。  
**使用視窗使用者資料。**  
列印應用程式通常會有數個視窗和執行緒。 若要在不使用靜態的全域變數的情況下，讓執行緒和處理步驟之間的資料保持可用，請參考資料結構，此資料指標是使用它們之視窗的一部分。  


下列程式碼範例會顯示列印應用程式的主要進入點。 這個範例示範如何使用字串資源，而不是字串常數，也會顯示處理常式視窗訊息的主要訊息迴圈。


```C++
int APIENTRY 
wWinMain(
        HINSTANCE hInstance, 
        HINSTANCE hPrevInstance, 
        LPWSTR lpCmdLine, 
        int nCmdShow
)
{
    UNREFERENCED_PARAMETER(hPrevInstance);
    UNREFERENCED_PARAMETER(lpCmdLine);

    MSG msg;
    HACCEL hAccelTable;
    HRESULT hr = S_OK;

    // Register the main window class name
    WCHAR szWindowClass[MAXIMUM_RESOURCE_STRING_LENGTH];            
    LoadString(
        hInstance, 
        IDC_PRINTSAMPLE, 
        szWindowClass, 
        MAXIMUM_RESOURCE_STRING_LENGTH);
    MyRegisterClass(hInstance, szWindowClass);

    // Perform application initialization:
    if (!InitInstance (hInstance, nCmdShow))
    {
        // Unable to initialize this instance of the application
        //  so display error message and exit
        MessageBoxWithResourceString (
            hInstance, 
            GetDesktopWindow(), 
            IDS_ERROR_INSTINITFAIL, 
            IDS_CAPTION_ERROR, 
            (MB_OK | MB_ICONEXCLAMATION));
        return FALSE;
    }    
    
    // Init COM for printing interfaces
    if (FAILED(hr = CoInitializeEx(0, COINIT_MULTITHREADED)))
    {
        // Unable to initialize COM
        //  so display error message and exit
        MessageBoxWithResourceString (
            hInstance, 
            GetDesktopWindow(), 
            IDS_ERROR_COMINITFAIL, 
            IDS_CAPTION_ERROR, 
            (MB_OK | MB_ICONEXCLAMATION));
        return FALSE;
    }

    hAccelTable = LoadAccelerators(
                    hInstance, 
                    MAKEINTRESOURCE(IDC_PRINTSAMPLE));

    // Main message handling loop
    while (GetMessage(&msg, NULL, 0, 0))
    {
        if (!TranslateAccelerator(msg.hwnd, hAccelTable, &msg))
        {
            TranslateMessage(&msg);
            DispatchMessage(&msg);
        }
    }

    // Uninitialize (close) the COM interface
    CoUninitialize();

    return (int) msg.wParam;
}
```



### <a name="document-information"></a>檔資訊

列印的原生 Windows 程式應設計為多執行緒處理。 多執行緒設計的其中一個需求是保護程式的資料元素，讓多個執行緒可以安全地同時使用。 您可以使用同步處理物件和組織資料來保護資料元素，以避免執行緒之間發生衝突。 同時，程式必須在列印時防止變更程式資料。 範例程式使用數個不同的多執行緒程式設計技術。

 **同步處理事件**  
範例程式會使用事件、執行緒控制碼和 wait 函式來同步處理列印執行緒和主要程式之間的處理，以及表示資料正在使用中。  
**應用程式特定的 Windows 訊息**  
範例程式會使用應用程式特定的視窗訊息，讓程式與其他原生 Windows 程式更相容。 將處理常式分成較小的步驟，並在視窗訊息迴圈中將這些步驟排入佇列，可讓 Windows 更容易管理處理，而不會封鎖可能也會在電腦上執行的其他應用程式。  
**資料結構**  
範例程式不是使用物件和類別以物件導向的樣式來撰寫，雖然它會將資料元素分組到資料結構中。 此範例不會使用物件導向的方法，以避免其中一個方法比另一個方法更好或更糟。  
當您設計程式時，可以使用範例程式的函式和資料結構作為起點。 無論您是否決定設計物件導向程式，要記住的重要設計考慮是將相關的資料元素分組，讓您可以視需要在不同的執行緒中安全地使用它們。  


### <a name="printer-device-context"></a>印表機裝置內容

列印時，您可能會想要將內容轉譯為要列印到裝置內容。 [如何：取出印表機裝置內容](retrieving-a-printer-device-context.md) 說明您可以取得印表機裝置內容的不同方式。

## <a name="related-topics"></a>相關主題



[如何從 Windows 應用程式列印](how-to--print-from-a-windows-application.md)


 

 



