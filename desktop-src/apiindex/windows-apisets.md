---
description: API 集合是核心 OS 中 Win32 Api 的功能群組。 它們提供與指定的 WIN32 API 定義所在的主機 DLL 以及 API 所屬的功能群組之間的架構分隔。
title: Windows API 集合
ms.topic: article
ms.date: 10/14/2020
ms.openlocfilehash: 15c8e6ad8124abf06e6ab3c2a8ca2bcd83772855
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/18/2020
ms.locfileid: "104463980"
---
# <a name="windows-api-sets"></a>Windows API 集合

所有版本的 Windows 10 都會共用作業系統元件的通用基底，稱為 *核心 os* (在某些內容中，這個通用基底也稱為 *OneCore*) 。 在核心 OS 元件中，Win32 Api 會組織成稱為 *API 集合* 的功能群組。

API 集的目的是要提供與主機 DLL （在其中執行指定的 WIN32 API）和 API 所屬的功能合約之間的架構分隔。 將 API 集合提供給開發人員與合約之間的分離，可為開發人員提供許多工程優勢。 尤其是在您的程式碼中使用 API 集合，可以改善與所有 Windows 10 裝置的相容性。

API 集合專門解決下列案例：

- 雖然電腦上支援完整的 WIN32 API 範圍，但其他 Windows 10 裝置（例如 HoloLens、Xbox 和其他執行 Windows 10 的裝置）都只能使用 WIN32 API 的子集。 API 集合名稱提供查詢機制，可完全偵測是否有任何特定裝置上的 API。

- 某些 WIN32 API 的執行會存在於不同 Windows 10 裝置上具有不同名稱的 Dll 中。 偵測 API 可用性和延遲載入 Api 時，在偵測 api 可用性和延遲載入 Api 時使用 API 集合名稱（而不是 DLL 名稱）會提供正確的執行路由，不論 API 實際上的執行位置

如需詳細資訊，請參閱 [api 集載入](api-set-loader-operation.md) 器作業和偵測 [api 設定的可用性](detect-api-set-availability.md)。

## <a name="linking-to-umbrella-libraries"></a>連結至傘程式庫

為了讓您更輕鬆地將程式碼限制為核心 OS 所支援的 Win32 Api，我們提供一系列的一系列 *傘程式庫*。 例如，名為 OneCore 的傘程式庫會針對所有 Windows 10 裝置通用的 Win32 Api 子集提供匯出。

傘程式庫中的 Api 可以跨各種模組來實行。 傘程式庫會將這些詳細資料抽象化，讓您的程式碼更能在 Windows 10 版本和裝置之間移植。 與其連結至程式庫（例如 kernel32.dll .lib 和 advapi32.dll），只需將您的桌面應用程式或驅動程式連結至包含您感興趣之核心作業系統 Api 集合的傘程式庫。

如需詳細資訊，請參閱 [Windows 傘程式庫](windows-umbrella-libraries.md)。

## <a name="api-set-contract-names"></a>API 集合合約名稱

API 集會以強式合約名稱來識別，並遵循程式庫載入器所能辨識的這些標準慣例。 

- 名稱的開頭必須是字串 **api** 或 **ext**。 
    - 以 **api** 開頭的名稱，代表保證存在於所有 Windows 10 版本上的 api。
    - 以 **ext** 開頭的名稱代表可能不存在於所有 Windows 10 版本上的 api。
- 名稱的結尾必須是序列 **l \<n\> - \<n\> - \<n\>**，其中 **n** 是由十進位數所組成。
- 名稱的本文可以是英數位元，也可以是連字號 (**-**) 。
- 名稱不區分大小寫。

以下是 API 集合約名稱的一些範例：

- **api-ms-win--ums-l1-1-0**
- **ext-ms-ole32.lib-l1-1-5**
- **ext-ms-ntuser.man-window-l1-1-0**
- **ext-ms-ntuser.man-window-l1-1-1**

您可以在載入器作業的內容（例如 [LoadLibrary](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 或 [P/Invoke](/dotnet/standard/native-interop/pinvoke) ）中使用 api 集合名稱，而不是 DLL 模組名稱，以確保在目前的裝置上實際實作為 API 的位置，使其正確路由。 但是，當您這樣做時，您必須在合約名稱的結尾附加字串 **.dll** 。 這是載入器必須正常運作的需求，且不會被視為合約名稱的一部分。 雖然合約名稱在此內容中看起來類似 DLL 名稱，但它們基本上與 DLL 模組名稱不同，而且不會直接參考磁片上的檔案。

除了在載入器作業中附加字串 **.dll** 之外，API 集合合約名稱也應視為與特定合約版本對應的不彈性識別碼。

## <a name="identifying-api-sets-for-win32-apis"></a>識別 Win32 Api 的 API 集合

若要識別特定的 WIN32 API 是否屬於某個 API 集合，請參閱 API 參考檔中的需求資料表。 如果 API 屬於 API 集，則文章中的需求資料表會列出 api 集合名稱，以及 api 首次引進 API 集的 Windows 版本。 如需屬於 API 集合的 Api 範例，請參閱下列文章：

- [AllowSetForegroundWindow](/windows/win32/api/winuser/nf-winuser-allowsetforegroundwindow)
- [FindWindowsEx](/windows/win32/api/winuser/nf-winuser-findwindowexa)
- [GetClassFile](/windows/win32/api/objbase/nf-objbase-getclassfile)

## <a name="in-this-section"></a>本節內容

* [API 集合載入器作業](api-set-loader-operation.md)
* [偵測 API 集合可用性](detect-api-set-availability.md)
* [Windows 傘程式庫](windows-umbrella-libraries.md)