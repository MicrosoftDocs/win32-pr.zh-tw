---
description: 建立 DirectShow 篩選
ms.assetid: fb907263-e7f3-42d6-80f9-a9f16fc21033
title: 建立 DirectShow 篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d87d1983d3bfd42d1a1582ef696b6793acdd0856dde2bd2d589e809acc614314
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119794319"
---
# <a name="building-directshow-filters"></a>建立 DirectShow 篩選

建議使用 DirectShow 基類來執行 DirectShow 篩選。 若要使用基類建立，請執行下列步驟，以及 [設定組建環境](setting-up-the-build-environment.md)所列的步驟：

-   在 SDK 根目錄下的目錄範例 \\ 多媒體 \\ DirectShow BaseClasses 中，建立基類庫 \\ 。 程式庫有兩個版本：零售版 (Strmbase) 和 (Strmbasd .lib) 的 debug 版本。
-   包含標頭檔資料流程 .h。
-   使用 \_ \_ stdcall 呼叫慣例。
-   使用多執行緒 C 執行時間程式庫 (debug 或 retail，如適當的) 。
-   包含匯出 DLL 函式 ( .def) 檔案的定義。 以下是定義檔的範例。 它會假設輸出檔的名稱是 MyFilter.dll。
    ```C++
    LIBRARY MYFILTER.DLL
    EXPORTS 
        DllMain             PRIVATE
        DllGetClassObject   PRIVATE
        DllCanUnloadNow     PRIVATE
        DllRegisterServer   PRIVATE
        DllUnregisterServer PRIVATE
    ```

    

-   連結至下列程式庫檔案。

| 標籤 | 值 |
    |--------------|--------------------------------------|
    | Debug 組建  | Strmbasd .lib、Msvcrtd.lib .lib、Winmm.dll .lib |
    | 零售組建 | Strmbase .lib、Msvcrt.lib .lib、Winmm.dll .lib  |

    

     

-   選擇連結器設定中的 [忽略預設程式庫] 選項。
-   在原始程式碼中宣告 DLL 進入點，如下所示：
    ```C++
    extern "C" BOOL WINAPI DllEntryPoint(HINSTANCE, ULONG, LPVOID);
    BOOL APIENTRY DllMain(HANDLE hModule, DWORD dwReason, LPVOID lpReserved)
    {
        return DllEntryPoint((HINSTANCE)(hModule), dwReason, lpReserved);
    }
    ```

    

舊版本

針對 DirectShow 9.0 之前的基類庫版本，您也必須執行下列動作：

-   針對 debug 組建，請定義預處理器旗標的偵錯工具。

DirectShow 9.0 和更新版本中可用的基類庫版本不需要執行此步驟。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow基類](directshow-base-classes.md)
</dt> <dt>

[撰寫 DirectShow 篩選](writing-directshow-filters.md)
</dt> </dl>

 

 



