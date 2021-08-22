---
description: 若要建立 Dynamic-Link 程式庫 (DLL) ，您必須建立一或多個原始程式碼檔案，而且可能是用來匯出函數的連結器檔案。
ms.assetid: b66ea0e8-84c3-40be-bf02-765b9dd61f9f
title: Dynamic-Link 程式庫建立
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89047e24fe61483b3ac807b59abc114206a00f9df18566b5fb02947268fbd792
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650448"
---
# <a name="dynamic-link-library-creation"></a>Dynamic-Link 程式庫建立

若要建立 Dynamic-Link 程式庫 (DLL) ，您必須建立一或多個原始程式碼檔案，而且可能是用來匯出函數的連結器檔案。 如果您打算允許使用 DLL 的應用程式使用載入時間動態連結，您也必須建立匯入程式庫。

## <a name="creating-source-files"></a>建立原始檔

DLL 的原始程式檔包含匯出的函式和資料、內建函式和資料，以及 DLL 的選擇性 [進入點函數](dynamic-link-library-entry-point-function.md) 。 您可以使用任何支援建立以 Windows 為基礎之 dll 的開發工具。

如果多執行緒應用程式可能會使用您的 DLL，您應該將 DLL 設為「安全線程」。 您必須同步存取所有 DLL 的全域資料，以避免資料損毀。 您也必須確定您只連結至安全線程的程式庫。 例如，Microsoft Visual C++ 包含多個版本的 C 執行時間程式庫，其中一個不是安全線程，而兩個是。

## <a name="exporting-functions"></a>匯出函式

如何指定要匯出 DLL 中的函式，取決於您用來開發的工具。 某些編譯器可讓您使用函式宣告中的修飾詞，直接在原始程式碼中匯出函式。 其他時候，您必須在傳遞給連結器的檔案中指定匯出。

例如，使用 Visual C++，有兩種可能的方式可以匯出 DLL 函式：使用 [**\_ \_ declspec (dllexport)**](https://msdn.microsoft.com/library/3y1sfaz2(v=VS.71).aspx)修飾詞或模組定義 ( .def) 檔。 如果您使用 **\_ \_ declspec (dllexport)** 修飾詞，就不需要使用 .def 檔。 如需詳細資訊，請參閱 [從 DLL 匯出](/cpp/build/exporting-from-a-dll?view=vs-2019)。

## <a name="creating-an-import-library"></a>建立匯入程式庫

匯入程式庫 ( .lib) 檔案包含連結器解析匯出 DLL 函式外部參考所需的資訊，因此系統可以在執行時間找到指定的 DLL 和匯出的 DLL 函式。 當您建立 DLL 時，可以建立 DLL 的匯入程式庫。

如需詳細資訊，請參閱 [建立匯入程式庫和匯出](/cpp/build/reference/building-an-import-library-and-export-file?view=vs-2019)檔案。

## <a name="using-an-import-library"></a>使用匯入程式庫

例如，若要呼叫 [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) 函數，您必須將程式碼與匯入程式庫的程式庫連結。 原因是， **CreateWindow** 位於名為 User32.dll 的系統 DLL 中，而 mscoree.dll 則是用來解析程式代碼中 User32.dll 匯出函式之呼叫的匯入程式庫。 連結器會建立一個資料表，其中包含每個函式呼叫的位址。 載入 DLL 時，會修正 DLL 中函式的呼叫。 當系統初始化程式時，它會載入 User32.dll，因為進程相依于該 DLL 中匯出的函式，並且會更新函式位址資料表中的專案。 所有的 **CreateWindow** 呼叫都會叫用從 User32.dll 匯出的函式。

如需詳細資訊，請參閱 [以 DLL 隱含連結](/previous-versions/d14wsce5(v=vs.140))。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[建立簡單的動態連結程式庫](creating-a-simple-dynamic-link-library.md)
</dt> <dt>

[Dll (Visual C++) ](/cpp/build/dlls-in-visual-cpp?view=vs-2019)
</dt> </dl>

 

 
