---
title: WinMain 應用程式進入點
description: .
ms.assetid: 389da5d4-d0f9-4339-be6c-0f4fecc59316
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bef44c4d31aa53dfd60f579b68c438a539058b85
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104185633"
---
# <a name="winmain-the-application-entry-point"></a>WinMain：應用程式進入點

每個 Windows 程式都包含一個名為 **WinMain** 或 **wWinMain** 的進入點函數。 以下是 **wWinMain** 的簽章。


```C++
int WINAPI wWinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, PWSTR pCmdLine, int nCmdShow);
```



這四個參數為：

-   *hInstance* 稱為「實例的控制碼」或「模組的控制碼」。 作業系統會在載入記憶體時，使用這個值來識別可執行檔 (EXE) 。 某些 Windows 函式需要實例控制碼，例如載入圖示或點陣圖。
-   *hPrevInstance* 沒有任何意義。 它是在16位 Windows 中使用，但現在一律為零。
-   *pCmdLine* 包含命令列引數做為 Unicode 字串。
-   *nCmdShow* 是一個旗標，指出主要應用程式視窗將會最小化、最大化，或正常顯示。

函數會傳回 **int** 值。 作業系統不會使用傳回值，但您可以使用傳回值來將狀態碼傳達給您所撰寫的其他程式。

**WINAPI** 是呼叫慣例。 *呼叫慣例* 會定義函數如何從呼叫端接收參數。 例如，它會定義參數出現在堆疊上的順序。 請務必宣告您的 **wWinMain** 函式，如下所示。

**WinMain** 函式與 **wWinMain** 相同，不同之處在于命令列引數會做為 ANSI 字串傳遞。 慣用的 Unicode 版本。 即使您將程式編譯成 Unicode，也可以使用 ANSI **WinMain** 函數。 若要取得命令列引數的 Unicode 複本，請呼叫 [**GetCommandLine**](/windows/desktop/api/processenv/nf-processenv-getcommandlinea) 函數。 此函數會傳回單一字串中的所有引數。 如果您想要引數做為 *argv* 樣式陣列，請將此字串傳遞給 [**CommandLineToArgvW**](/windows/desktop/api/shellapi/nf-shellapi-commandlinetoargvw)。

編譯器如何知道要叫用 **wWinMain** ，而不是標準 **main** 函數？ 實際的情況是，Microsoft C 執行時間程式庫 (CRT) 提供可呼叫 **WinMain** 或 **wWinMain** 的 **main** 的實。

> [!Note]  
> CRT 會在 **main** 內執行一些額外的工作。 例如，在 **wWinMain** 之前，會呼叫任何靜態初始化運算式。 雖然您可以指示連結器使用不同的進入點函式，但如果您連結至 CRT，則使用預設值。 否則，將會略過 CRT 初始化程式碼，並產生無法預測的結果。  (例如，全域物件將無法正確初始化。 ) 

 

以下是空的 **WinMain** 函數。


```C++
INT WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance,
    PSTR lpCmdLine, INT nCmdShow)
{
    return 0;
}
```



既然您已經有進入點，並且瞭解一些基本的術語和程式碼撰寫慣例，就可以開始建立完整的視窗程式。

## <a name="next"></a>下一個

[模組1。您的第一個 Windows 程式](your-first-windows-program.md)。

 

 