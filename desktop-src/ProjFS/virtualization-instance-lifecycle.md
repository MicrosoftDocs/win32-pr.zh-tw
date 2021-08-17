---
title: 虛擬化實例生命週期
description: ProjFS 虛擬化實例的生命週期總覽。
ms.assetid: <GUID-GOES-HERE>
ms.date: 09/17/2018
ms.topic: article
ms.openlocfilehash: bbaaf5eca5481f3959e3e5afeb36a8cf6b264c939e8eb2cc9d84ba501d3c8530
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117792382"
---
# <a name="virtualization-instance-lifecycle"></a>虛擬化實例生命週期

提供者應用程式會維護一或多個虛擬化實例。  每個虛擬化實例在其生命週期中都會經歷四個階段：

1. 建立
2. 啟動
3. 執行階段
4. 關機

請注意，關閉虛擬化實例之後，提供者不需要重新建立它來重複使用它。  只要重新開機就可以了。

> **注意**：本節說明 ProjFS api 的範例。  每個範例都旨在說明基本的 API 使用方式。  如需這些範例中未使用之選項的檔，請參閱 [PROJFS API 參考](/windows/desktop/api/_projfs)。

## <a name="creating-a-virtualization-root"></a>建立虛擬化根

在提供者可以啟動將專案投射到本機檔案系統中的虛擬化實例之前，必須先建立虛擬化根。  虛擬化根是提供者用來投射目錄和檔案樹狀結構的目錄。

若要建立虛擬化根，提供者必須：

1. 建立做為虛擬化根的目錄。

    提供者會使用 **[CreateDirectory](/windows/desktop/api/fileapi/nf-fileapi-createdirectoryw)** 來建立作為虛擬化根的目錄，例如：

    ```C++
    HRESULT hr;
    const wchar_t* rootName = LR"(C:\virtRoot)";
    if (!CreateDirectoryW(rootName, nullptr))
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
        wprintf(L"Failed to create virtualization root (0x%08x)\n", hr);
        return;
    }
    ```

1. 建立虛擬化實例識別碼。

    每個虛擬化實例都有一個稱為 _虛擬化實例識別碼_ 的唯一識別碼。  系統會使用此值來識別與其內容相關聯的虛擬化實例。

    ```C++
    GUID instanceId;
    hr = CoCreateGuid(&instanceId);
    if (FAILED(hr))
    {
        wprintf(L"Failed to create instance ID (0x%08x)\n", hr);
        return;
    }
    ```

1. 將新目錄標示為虛擬化根。

    提供者會呼叫 **[PrjMarkDirectoryAsPlaceholder](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjmarkdirectoryasplaceholder)** ，將新目錄標示為虛擬化根，並將其指派給虛擬化實例。

    ```C++
    hr = PrjMarkDirectoryAsPlaceholder(rootName,
                                       nullptr,
                                       nullptr,
                                       &instanceId);
    if (FAILED(hr))
    {
        wprintf(L"Failed to mark virtualization root (0x%08x)\n", hr);
        return;
    }
    ```

提供者只需要針對每個虛擬化實例建立虛擬化根。  建立根目錄之後，就可以重複啟動和停止其相關聯的實例，而不需要重新建立根。

## <a name="starting-a-virtualization-instance"></a>啟動虛擬化實例

建立虛擬化根之後，提供者必須啟動虛擬化實例。  這會通知 ProjFS 提供者已準備好接收回呼並提供資料。

若要啟動虛擬化實例，提供者必須：

1. 設定回呼資料表。

    ProjFS 藉由叫用提供者所執行的回呼常式來與提供者通訊。  提供者會在 [PRJ_CALLBACKS](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_callbacks) 結構中填入其回呼常式的指標。

    ```C++
    PRJ_CALLBACKS callbackTable;

    // Supply required callbacks.
    callbackTable.StartDirectoryEnumerationCallback = MyStartEnumCallback;
    callbackTable.EndDirectoryEnumerationCallback = MyEndEnumCallback;
    callbackTable.GetDirectoryEnumerationCallback = MyGetEnumCallback;
    callbackTable.GetPlaceholderInfoCallback = MyGetPlaceholderInfoCallback;
    callbackTable.GetFileDataCallback = MyGetFileDataCallback;

    // The rest of the callbacks are optional.
    callbackTable.QueryFileNameCallback = nullptr;
    callbackTable.NotificationCallback = nullptr;
    callbackTable.CancelCommandCallback = nullptr;
    ```

1. 啟動實例。

    提供者會呼叫 **[PrjStartVirtualizing](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjstartvirtualizing)** 來啟動虛擬化實例。

    ```C++
    PRJ_NAMESPACE_VIRTUALIZATION_CONTEXT instanceHandle;
    hr = PrjStartVirtualizing(rootName,
                              &callbackTable,
                              nullptr,
                              nullptr,
                              &instanceHandle);
    if (FAILED(hr))
    {
        wprintf(L"Failed to start the virtualization instance (0x%08x)\n", hr);
        return;
    }
    ```
    **PrjStartVirtualizing** 的 _instanceHandle_ 參數會傳回虛擬化實例的控制碼。  在呼叫其他 ProjFS Api 時，提供者會使用此控制碼。

## <a name="virtualization-instance-runtime"></a>虛擬化實例執行時間

一旦呼叫 **PrjStartVirtualizing** 傳回，ProjFS 將會叫用提供者的回呼常式，以回應虛擬化實例中的檔案系統作業。  如需提供者如何處理各種檔案系統作業的相關資訊，請參閱下列各節：

* [列舉檔案和目錄](enumerating-files-and-directories.md)
* [提供檔案資料](providing-file-data.md)
* [檔案系統作業通知](file-system-operation-notifications.md)
* [處理視圖變更](handling-view-changes.md)

## <a name="shutting-down-a-virtualization-instance"></a>關閉虛擬化實例

為了告知 ProjFS 提供者想要停止接收回呼並提供資料，提供者必須停止虛擬化實例。  若要這樣做，提供者會呼叫 **[PrjStopVirtualizing](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjstopvirtualizing)**，並將控制碼傳遞給它從 **PrjStartVirtualizing** 呼叫所接收到的虛擬化實例。

```C++
PrjStopVirtualizing(instanceHandle);
```

請注意，在此呼叫傳回之前，ProjFS 可能會繼續叫用提供者的回呼常式。