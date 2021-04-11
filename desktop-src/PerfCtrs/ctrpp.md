---
description: CTRPP 工具是可剖析和驗證計數器資訊清單的預處理器。
ms.assetid: 3939f6a1-0a94-429d-a71e-b37f045fea13
title: CTRPP
ms.topic: reference
ms.date: 08/17/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- CTRPP
api_type:
- NA
api_location: ''
ms.openlocfilehash: dce12de641dda7b07871a4447190772533598748
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "104321719"
---
# <a name="ctrpp"></a>CTRPP

CTRPP 工具是可剖析並驗證 V2 提供者資訊清單的預處理器。 此工具 `.rc` 會使用提供者的取用者所需的字串產生資源，並使用 `.h` 您用來提供計數器資料的程式碼來產生標頭。 您應該在提供者的組建期間執行 CTRPP 工具。 開發提供者時，您應該使用產生的程式碼作為起點，而不是自行嘗試產生此程式碼。

```syntax
ctrpp -o codeFile -rc rcFile [-legacy] [-MemoryRoutines] [-NotificationCallback] [-prefix prefix] [-ch symFile] [-backcompat] inputFile
```

## <a name="arguments"></a>引數

|選項              |Description
|--------------------|-----------
|*inputFile*         |**必要：** 指定 `.man` 定義您的計數器 (XML 資訊清單) 檔案的名稱。
|**-o** *codeFile*   |**必要：** 指定 `.h` 要由 CTRPP 產生的程式碼檔案名。 這個檔案將包含 C/c + + 內嵌 helper 函式，可簡化您的提供者的初始化和取消初始化。
|**-rc** *rcFile*    |**必要：** 指定 `.rc` CTRPP 要產生的 (資源檔名稱) 。 這個檔案將包含提供者的字串資料表。
|**-ch** *symFile*   |指定 `.h` 要由 CTRPP 產生的選擇性符號檔名稱。 此檔案將包含 C/c + + 符號，以取得提供者中每個 counterset 的名稱和 Guid。
|**-前置** 詞 *前置* 詞|指定在產生的標頭檔中定義的變數和函數所使用的前置詞。
|**-NotificationCallback**|變更 [**CounterInitialize**](counterinitialize.md) 函式的預設簽章，以包含用來指定 [*ControlCallback*](/windows/desktop/api/Perflib/nc-perflib-perflibrequest)、 [*AllocateMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_alloc)和 [*FreeMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_free) 回呼函數名稱的參數。 這個引數的效果與在 `callback` [**provider**](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element) 元素中包含屬性相同。
|**-遷移** *outputFile*|將 `.h` `.rc` *inputFile* 資訊清單升級為最新版本，並將其儲存至 *outputFile*，而不是產生和檔案。 此參數不能搭配其他參數使用。 使用方式：`CTRPP -migrate NewFile.man OldFile.man`
|**-回溯相容性**     |已 **淘汰：** Windows 7 已新增對核心模式提供者的支援。 根據預設，CTRPP 針對核心模式提供者所產生的程式碼將會與舊版的 Windows 不相容 (驅動程式因為缺少 api) 而無法載入 `Pcw***` 。 設定 `-BackCompat` 為啟用與舊版 Windows 的相容性。 驅動程式會以動態方式載入必要的 Api，而產生的程式碼會在 Api 無法使用時，以無訊息方式停用提供者。
|**-MemoryRoutines** |已 **淘汰：** 搭配參數使用時 `-Legacy` ，會在產生的程式碼中包含記憶體常式的範本。 否則，此引數與參數的效果相同 `-NotificationCallback` 。
|**-舊版**         |已 **淘汰：**`*.h` `*.c` `*.rc` 使用 Windows Vista 程式碼範本產生、、和檔案 `*_r.h` (產生 PerfAutoInitialize 和 PerfAutoCleanup，而不是 CounterInitialize 和 CounterCleanup) 。 這個參數可以搭配 **-MemoryRoutines** 和 **-NotificationCallback** 使用，但不能搭配任何其他參數使用。 請勿使用 **-o** 或 **-rc** 參數搭配此參數。 產生的檔案會根據資訊清單的名稱命名，並且會寫入包含資訊清單的目錄。 使用方式：`CTRPP -legacy OldFile.man`

## <a name="remarks"></a>備註

CTRPP 工具會產生 `.h` 程式碼檔案、 `.rc` 資源檔，並選擇性地產生 `.h` 符號檔。

### <a name="using-the-generated-resource-file"></a>使用產生的資源檔

CTRPP 工具會產生 `.rc` 資源檔，其中包含提供者 countersets 取用者所需的可當地語系化字串。

> [!IMPORTANT]
> 此檔案中的資源必須包含在提供者二進位檔中，而提供者二進位檔的完整路徑必須在安裝提供者的資訊清單期間註冊。 無法尋找和載入資源的取用者將無法使用您的提供者 countersets。

字串資源應該依照下列方式處理：

- 開發人員編輯提供者資訊清單 (`.man`) 檔案，將 `applicationIdentity` 提供者的屬性設定為提供者二進位 ( 的名稱。Dll。SYS 或。EXE) ，其中包含提供者的字串資源，且將會安裝為提供者元件的一部分。
- CTRPP 工具會讀取提供者資訊清單，並產生檔案 `.rc` 。
- [RC (資源編譯器) ](../menurc/resource-compiler.md)工具會從 CTRPP 產生的檔案編譯資料 `.rc` ，以產生 `.res` 包含二進位資源的檔案。 這可以藉由直接編譯 CTRPP 產生的檔案 `.rc` ，或透過指示詞編譯 `.rc` 包含 CTRPP 產生之檔案的另一個檔案來完成 `.rc` `#include` 。
- 連結器會將 RC 產生之檔案中的資料內嵌 `.res` 至提供者二進位檔。
- 在安裝期間，會將提供者二進位檔複製到使用者的系統，並使用 [lodctr 工具](/windows-server/administration/windows-commands/lodctr)來註冊提供者資訊清單。 Lodctr 工具會將 `applicationIdentity` 提供者資訊清單的屬性轉換為完整路徑，並記錄登錄中提供者二進位檔的完整路徑。
  - 如果提供者二進位檔位於與資訊清單相同的目錄中，請使用： `lodctr.exe /m:"C:\full\manifest\path\manifest.man"` 。 lodctr 會將指定的資訊清單路徑與資訊清單的屬性結合， `applicationIdentity` 以形成完整的路徑。
  - 否則，使用 `lodctr.exe /m:"C:\full\manifest\path\manifest.man" "c:\full\binary\path"`。 lodctr 會將指定的二進位路徑與資訊清單的 `applicationIdentity` 屬性結合，以形成完整的路徑。
  - 為了診斷用途，您可以檢查登錄機碼的值，以檢查記錄的完整路徑 `ApplicationIdentity` `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Perflib\_V2Providers\{<ProviderGuid>}` 。
  - 如果二進位檔使用 MUI 進行當地語系化，請務必複製 MUI 檔案以及二進位檔。
- 在 counterset 集合期間，取用者會使用提供者二進位檔的記錄完整路徑，從提供者二進位的資源中找出並載入必要的字串。

### <a name="using-the-generated-code-file-in-a-user-mode-provider"></a>在使用者模式提供者中使用產生的程式碼檔案

CTRPP 工具會產生 `.h` C/c + + 程式碼檔案。 如果提供者資訊清單的 `providerType` 屬性設定為 `userMode` ，則產生的程式碼檔案將包含下列定義，在撰寫使用者模式提供者時很有説明：

- 名為 [ * **prefix * CounterInitialize**](counterinitialize.md)的提供者初始化函數。
- 名為 [ * **prefix * CounterCleanup**](countercleanup.md)的提供者清除函數。
- 全域 ***提供者** _ 變數，會儲存 _ *_prefix_CounterInitialize** 函式所開啟的提供者控制碼。 變數的名稱是 `symbol` `provider` 資訊清單中元素的屬性值。 此變數應該用於對 `PerfCreateInstance` 、 `PerfDeleteInstance` 和其他 api 的呼叫，以控制您的提供者資料。
- 針對每個 counterset，具有 counterset GUID 的 global ***counterset * GUID** 變數。 變數的名稱是元素屬性的值加上後置字元 `counterSet` `symbol` "GUID"，例如 `MyCounterSetGUID` 。 此變數應該用於對 `PerfCreateInstance` 、 `PerfDeleteInstance` 和其他 api 的呼叫，以控制您的提供者資料。
- 針對每個計數器，具有計數器值的 ***計數器*** 宏 `id` 。 宏的名稱是 `counter` 元素屬性的值 `symbol` 。 在呼叫 `PerfSetCounterRefValue` 、 `PerfSetULongLongCounterValue` 和其他 api 來設定提供者的資料時，應該使用這個宏。

在函數名稱中， ***前置*** 詞是指 `-prefix` 命令列參數的值。 如果 `-prefix` 未使用參數，函式將會命名為 `CounterInitialize` 和 `CounterCleanup` 。

### <a name="using-the-generated-code-file-in-a-kernel-mode-provider"></a>在核心模式提供者中使用產生的程式碼檔案

CTRPP 工具會產生 `.h` C/c + + 程式碼檔案。 如果提供者資訊清單的 `providerType` 屬性設定為 `kernelMode` ，則產生的程式碼檔案將包含下列定義，在撰寫核心模式提供者的 countersets 時很有説明：

- 名為 <b> *Prefix* Register *counterset*</b>的 counterset 初始化函數。 此函式會填入 [RegInfo](/windows-hardware/drivers/ddi/wdm/ns-wdm-_pcw_registration_information) 結構，然後叫用 [PcwRegister](/windows-hardware/drivers/ddi/wdm/nf-wdm-pcwregister)，將產生的 counterset 註冊控制碼放入全域 ***counterset*** 變數中。
- 名為 <b>*前置* 詞取消註冊 *counterset*</b>的 counterset 清除函數。 此函式會在全域 ***counterset*** 變數中的 counterset 註冊控制碼上叫用 [PcwUnregister](/windows-hardware/drivers/ddi/wdm/nf-wdm-pcwunregister) 。
- 名為 <b> *Prefix* Create *Counterset*</b>的實例建立函數。 此函式會填入 [PcwData](/windows-hardware/drivers/ddi/wdm/ns-wdm-_pcw_data)結構的陣列，然後使用全域 ***counterset*** 變數中的 counterset 註冊控制碼來叫用 [PcwCreateInstance](/windows-hardware/drivers/ddi/wdm/nf-wdm-pcwcreateinstance) 。
- 名為 <b> *Prefix* Close *Counterset*</b>的實例清除函數。 此函式會叫用 [PcwCloseInstance](/windows-hardware/drivers/ddi/wdm/nf-wdm-pcwcloseinstance)。
- 名為「 <b>*前置***</b>詞」的實例報告函式會從 Counterset 回呼函數中使用。 此函數會填入 [PcwData](/windows-hardware/drivers/ddi/wdm/ns-wdm-_pcw_data) 結構的陣列，然後叫用 [PcwAddInstance](/windows-hardware/drivers/ddi/wdm/nf-wdm-pcwaddinstance)。
- **Windows SDK 20H1 和更新版本：** 名為 <b> *Prefix* InitRegistrationInformation *Counterset*</b>的 RegInfo 初始化函數，用於 advanced 案例中。 此函數會填入 [RegInfo](/windows-hardware/drivers/ddi/wdm/ns-wdm-_pcw_registration_information) 結構。 當產生的 <b>*首碼***</b>登錄區不符合您的需求時，例如，當您想要自訂 RegInfo 結構中的值，或當您想要將傳回的控制碼儲存在另一個變數時，就可以使用這個函式。

在函數名稱中， ***前置*** 詞是指 `-prefix` 命令列參數的值。 如果 `-prefix` 未使用參數，函數將不會有前置詞。

> [!NOTE]
> 當您有 Counterset 回呼時，會使用產生的 <b>*前置* 詞 Add *Counterset*</b>函數。 當您沒有 Counterset 回呼時，會使用產生的 <b>*前置* 詞 Create *Counterset*</b>和 <b> *prefix* Close *Counterset*</b>函數。

### <a name="using-the-generated-symbol-file"></a>使用產生的符號檔

如果在命令列上指定 **-ch** 參數，CTRPP 工具將會產生 `.h` 符號檔。 此檔案包含提供者中每個 counterset 的名稱和 Guid 的 C/c + + 符號。 使用 [PerfLib V2 取用者](using-the-perflib-functions-to-consume-counter-data.md)函式撰寫硬式編碼的程式來取用此 counterset 的資料時，可以使用這些符號。

## <a name="requirements"></a>規格需求

|                         ||
|-------------------------|----
| 最低支援的用戶端| \[僅限 Windows Vista 桌面應用程式\]
| 最低支援的伺服器| 僅限 Windows Server 2008 \[ desktop 應用程式\]
