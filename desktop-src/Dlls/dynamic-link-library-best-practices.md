---
description: 建立 Dll 為開發人員帶來一些挑戰。
ms.assetid: 44EFC4B5-7A2F-43A6-914E-D4EB7446AC35
title: Dynamic-Link 程式庫的最佳作法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95d02314b15a13de7658c0b87ba7cd998f48a0a3d9f2f2682b36539bd9f5bde3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119696574"
---
# <a name="dynamic-link-library-best-practices"></a>Dynamic-Link 程式庫的最佳作法

* * 更新日期： * *

-   2006 5 月17日

**重要 API**

-   [**DllMain**](dllmain.md)
-   [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa)
-   [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa)

建立 Dll 為開發人員帶來一些挑戰。 Dll 沒有系統強制的版本控制。 當系統上有多個版本的 DLL 時，容易被覆寫，且缺少版本控制架構會建立相依性和 API 衝突。 開發環境中的複雜性、載入器的執行和 DLL 相依性已建立脆弱數的載入順序和應用程式行為。 最後，許多應用程式都依賴 Dll 並且具有複雜的相依性集合，讓應用程式能夠正常運作。 本檔提供 DLL 開發人員協助建立更健全、可攜且可擴充之 Dll 的指導方針。

[**DllMain**](dllmain.md)內的不當同步處理可能會導致應用程式鎖死，或存取未初始化 DLL 中的資料或程式碼。 從 **DllMain** 內呼叫特定函式會造成這類問題。

![載入程式庫時會發生什麼事](images/fig1.png)

## <a name="general-best-practices"></a>一般最佳作法

當持有載入器鎖定時，會呼叫 [**DllMain**](dllmain.md) 。 因此，可在 **DllMain** 內呼叫的函式上強加了重大限制。 因此， **DllMain** 的設計目的是要使用 Microsoft® Windows® API 的一小部分來執行最少的初始化工作。 您無法在 **DllMain** 中呼叫任何直接或間接嘗試取得載入器鎖定的函式。 否則，您將會引入應用程式鎖死或損毀的可能性。 **DllMain** 執行中的錯誤可能會危害整個進程及其所有線程。

理想的 [**DllMain**](dllmain.md) 會是空的存根。 不過，由於許多應用程式的複雜性，這通常太過嚴格。 好用的 **DllMain** 經驗法則是盡可能將最多的初始化延後。 延遲初始化可提高應用程式的可靠性，因為在保留載入器鎖定時，不會執行此初始化。 此外，延遲初始化可讓您安全地使用更多的 Windows API。

某些初始化工作無法延後。 例如，如果檔案的格式不正確或包含垃圾，則相依于設定檔的 DLL 應該無法載入。 對於這種初始化類型，DLL 應該嘗試執行動作並快速失敗，而不是藉由完成其他工作來浪費資源。

您永遠不應該從 [**DllMain**](dllmain.md)內執行下列工作：

-    (直接或間接) 呼叫 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 或 [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) 。 這可能會造成鎖死或損毀。
-    (直接或間接) 呼叫 [**GetStringTypeA**](/windows/desktop/api/winnls/nf-winnls-getstringtypea)、 [**GetStringTypeEx**](/windows/win32/api/stringapiset/nf-stringapiset-getstringtypeexw)或 [**GetStringTypeW**](/windows/desktop/api/stringapiset/nf-stringapiset-getstringtypew) 。 這可能會造成鎖死或損毀。
-   與其他執行緒同步處理。 這可能會造成鎖死。
-   取得由等候取得載入器鎖定的程式碼所擁有的同步處理物件。 這可能會造成鎖死。
-   使用 [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)初始化 COM 執行緒。 在某些情況下，此函式可以呼叫 [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa)。
-   呼叫登錄功能。 這些函式會在 Advapi32.dll 中實作為。 如果 Advapi32.dll 未在您的 DLL 之前初始化，則 DLL 可以存取未初始化的記憶體，並使進程損毀。
-   呼叫 [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa)。 建立進程可以載入另一個 DLL。
-   呼叫 [**ExitThread**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibraryandexitthread)。 在 DLL 卸離期間結束執行緒可能會再次取得載入器鎖定，導致鎖死或損毀。
-   呼叫 [**CreateThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createthread)。 如果您沒有與其他執行緒進行同步處理，則建立執行緒可能會運作，但這是有風險的。
-   建立具名管道或其他命名物件 (僅 Windows 2000) 。 在 Windows 2000 中，命名物件是由終端機服務 DLL 提供。 如果這個 DLL 未初始化，則對 DLL 的呼叫可能會導致處理常式損毀。
-   使用 Run-Time (CRT) 的記憶體管理函數。 如果 CRT DLL 未初始化，這些函式的呼叫可能會導致處理常式損毀。
-   User32.dll 或 Gdi32.dll 中呼叫函數。 某些函式會載入另一個可能不會初始化的 DLL。
-   使用 managed 程式碼。

下列工作可以安全地在 **DllMain** 內執行：

-   在編譯時期初始化靜態資料結構和成員。
-   建立並初始化同步處理物件。
-   配置記憶體並初始化動態資料結構， (避免上列函式。 ) 
-    (TLS) 設定執行緒區域儲存區。
-   開啟、讀取和寫入檔案。
-   在 Kernel32.dll (中呼叫函式，但) 上列函數除外。
-   將全域指標設定為 Null，並將動態成員的初始化設為 off。 在 Microsoft Windows Vista™中，您可以使用一次性的初始化函式，以確保程式碼區塊只會在多執行緒環境中執行一次。

## <a name="deadlocks-caused-by-lock-order-inversion"></a>鎖定順序反轉造成的鎖死

當您使用多個同步處理物件（例如鎖定）來執行程式碼時，請務必遵守鎖定順序。 當需要一次取得多個鎖定時，您必須定義稱為鎖定階層或鎖定順序的明確優先順序。 例如，如果在程式碼中的某個位置之前取得鎖定 A，並且在程式碼中的其他位置取得鎖定 B，則鎖定順序為 A、B、C，而此順序應該在整個程式碼中遵循。 當未遵循鎖定順序時，就會發生鎖定順序反轉，例如，如果在鎖定 A 之前取得鎖定 B，鎖定順序反轉可能會導致難以進行偵錯工具的鎖死。 為了避免這類問題，所有線程都必須以相同的順序取得鎖定。

請務必注意，載入器會呼叫已取得載入器鎖定的 [**DllMain**](dllmain.md) ，因此載入器鎖定在鎖定階層中應該具有最高的優先順序。 另請注意，程式碼只需要取得適當的同步處理所需的鎖定;不需要取得階層中定義的每個單一鎖定。 例如，如果程式碼區段只需要鎖定 A 和 C 以進行適當的同步處理，則程式碼在取得鎖定 C 之前，應該會取得鎖定 A;程式碼也不需要取得鎖定 B。此外，DLL 程式碼無法明確取得載入器鎖定。 如果程式碼必須呼叫可間接取得載入器鎖定的 API （例如 [**GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) ），而且程式碼也必須取得私用鎖定，則程式碼應該在取得鎖定 P 之前呼叫 **GetModuleFileName** ，藉此確保遵守載入順序。

[圖 2] 是說明鎖定順序反轉的範例。 假設有一個 DLL 的主執行緒包含 [**DllMain**](dllmain.md)。 程式庫載入器會取得載入器鎖定 L，然後呼叫 **DllMain**。 主執行緒會建立同步處理物件 A、B 和 G 以序列化其資料結構的存取，然後嘗試取得 lock G。已成功取得鎖定 G G 的背景工作執行緒會呼叫函數，例如嘗試取得載入器鎖定 L 的 GetModuleHandle。因此，背景工作執行緒會在 L 上遭到封鎖，而主執行緒會在 G 上遭到封鎖，因而產生鎖死。

![鎖定順序反轉造成的鎖死](images/fig2.png)

為了避免鎖定順序反轉所造成的鎖死，所有線程都應該隨時嘗試取得所定義載入順序中的同步處理物件。

## <a name="best-practices-for-synchronization"></a>同步處理的最佳作法

請考慮建立背景工作執行緒作為其初始化一部分的 DLL。 清除 DLL 時，必須與所有工作者執行緒同步處理，以確保資料結構處於一致的狀態，然後終止背景工作執行緒。 目前，沒有直接解決在多執行緒環境中完全同步處理和關閉 Dll 問題的方式。 本節說明在 DLL 關閉期間，執行緒同步處理的最新最佳作法。

進程結束期間在 [**DllMain**](dllmain.md) 中的執行緒同步處理

-   在進程結束時呼叫 [**DllMain**](dllmain.md) 時，會強制清除所有進程的執行緒，而且可能會有位址空間不一致的情況。 在此情況下，不需要同步處理。 換句話說，理想的 DLL 進程卸 \_ \_ 離處理常式是空的。
-   WindowsVista 可確保核心資料結構 (環境變數、目前的目錄、進程堆積等) 處於一致的狀態。 不過，其他資料結構可能已損毀，因此清理記憶體並不安全。
-   需要儲存的持續性狀態必須排清到永久儲存區。

DLL **中 dll** 執行緒卸離 dll 執行緒的執行緒同步處理 \_ \_

-   卸載 DLL 時，不會擲回位址空間。 因此，DLL 預期會執行正常關機。 這包括執行緒同步處理、開啟控制碼、持續狀態和已配置的資源。
-   執行緒同步處理很棘手，因為在 [**DllMain**](dllmain.md) 中等候執行緒結束可能會造成鎖死。 例如，DLL A 會保存載入器鎖定。 它會通知執行緒 T 結束，並等候執行緒結束。 執行緒 T 結束時，載入器會嘗試取得載入器鎖定，以呼叫 dll A 的 **DllMain** 與 dll \_ 執行緒卸 \_ 離。 這會造成鎖死。 若要將鎖死的風險降至最低：
    -   DLL A 會 \_ \_ 在其 [**DLLMAIN**](dllmain.md) 中取得 dll 執行緒的卸離訊息，並設定執行緒 T 的事件，以通知它結束。
    -   執行緒 T 完成其目前的工作，將本身帶入一致的狀態，發出 DLL A 的信號，並無限期等候。 請注意，一致性檢查常式應遵循與 [**DllMain**](dllmain.md) 相同的限制，以避免死結。
    -   DLL A 終止 T，知道它處於一致的狀態。

如果 DLL 在所有線程都已建立之後，但在開始執行之前卸載，執行緒可能會損毀。 如果 DLL **在其初始化** 過程中建立了執行緒，則某些執行緒可能不會完成初始化，而且其 DLL \_ 執行緒 \_ 附加訊息仍在等候傳遞至 DLL。 在此情況下，如果卸載 DLL，它就會開始終止執行緒。 不過，某些執行緒可能會在載入器鎖定之後封鎖。 \_ \_ Dll 執行緒附加訊息會在 dll 未對應時處理，導致進程損毀。

## <a name="recommendations"></a>建議

以下是建議的指導方針：

-   使用應用程式驗證器來攔截 [**DllMain**](dllmain.md)中最常見的錯誤。
-   如果在 [**DllMain**](dllmain.md)內使用私用鎖定，請定義鎖定階層，並以一致的方式使用。 載入器鎖定必須位於此階層的底部。
-   確認沒有任何呼叫相依于另一個可能尚未完全載入的 DLL。
-   在編譯時期以靜態方式執行簡單的初始化，而不是在 [**DllMain**](dllmain.md)中執行。
-   延遲 [**DllMain**](dllmain.md) 中可等候到稍後的任何呼叫。
-   延遲可等候到稍後的初始化工作。 某些錯誤狀況必須及早偵測，如此應用程式才能正常地處理錯誤。 不過，這種早期偵測與可能產生的穩定性會有取捨。 延遲初始化通常是最好的做法。

 

 
