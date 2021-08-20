---
description: AddPrinterDriverEx 函式會安裝本機或遠端印表機驅動程式，並連結設定、資料和驅動程式檔案。
ms.assetid: 472adb7d-39cc-4c76-b96c-610ff9d276ad
title: 'AddPrinterDriverEx 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrinterDriverEx
- AddPrinterDriverExA
- AddPrinterDriverExW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 00bd65ad415a97bbab825e4a13c8ad985d1d7f9b79d7b46e3f8f7ea6b5e5f0dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117868807"
---
# <a name="addprinterdriverex-function"></a>AddPrinterDriverEx 函式

**AddPrinterDriverEx** 函式會安裝本機或遠端印表機驅動程式，並連結設定、資料和驅動程式檔案。 除了擁有 [**AddPrinterDriver**](addprinterdriver.md)的功能之外，它也有一些選項可允許嚴格升級、嚴格降級、只複製較新的檔案，以及複製所有檔案 (無論檔案時間戳記) 。

> [!Note]  
> 不再建議您安裝不含驅動程式套件的印表機驅動程式。 請改用 [**InstallPrinterDriverFromPackage**](installprinterdriverfrompackage.md) 。

 

## <a name="syntax"></a>語法


```C++
BOOL AddPrinterDriverEx(
  _In_    LPTSTR pName,
  _In_    DWORD  Level,
  _Inout_ LPBYTE pDriverInfo,
  _In_    DWORD  dwFileCopyFlags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pName* \[在\]
</dt> <dd>

以 null 結束的字串指標，指定應該安裝驅動程式之伺服器的名稱。 如果此參數為 **Null**，則函式會在本機電腦上安裝驅動程式。

</dd> <dt>

*層級* \[在\]
</dt> <dd>

*PDriverInfo* 所指向的結構版本。 此值可以是2、3、4、6或8。

</dd> <dt>

*pDriverInfo* \[in、out\]
</dt> <dd>

包含印表機驅動程式資訊之結構的指標。 它可以是下列其中一項。



| 層級的值                                                                                       | 驅動程式 \_ 資訊 \_ \* 結構                          |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | [**驅動程式 \_ 資訊 \_ 2**](driver-info-2.md)<br/> |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | [**驅動程式 \_ 資訊 \_ 3**](driver-info-3.md)<br/> |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | [**驅動程式 \_ 資訊 \_ 4**](driver-info-4.md)<br/> |
| <span id="6"></span><dl> <dt>**6**</dt> </dl> | [**驅動程式 \_ 資訊 \_ 6**](driver-info-6.md)<br/> |
| <span id="8"></span><dl> <dt>**8**</dt> </dl> | [**驅動程式 \_ 資訊 \_ 8**](driver-info-8.md)<br/> |



 

如果 *pDriverInfo* 所指向之結構的 **PEnvironment** 成員為 **Null**，則此函式會使用目前的呼叫端/用戶端環境，而不是目的地/伺服器的環境。

</dd> <dt>

*dwFileCopyFlags* \[在\]
</dt> <dd>

複製驅動程式檔案的選項。 此參數可以是下列其中一個值。



| 值                                                                                                                                                                                         | 意義                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="APD_COPY_ALL_FILES"></span><span id="apd_copy_all_files"></span><dl> <dt>**APD \_ 複製 \_ 所有 \_ 檔案**</dt> </dl>                | 新增印表機驅動程式，並複製印表機驅動程式目錄中的所有檔案。 此選項會忽略檔案時間戳記。<br/>                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="APD_COPY_FROM_DIRECTORY"></span><span id="apd_copy_from_directory"></span><dl> <dt>**APD \_ \_ 從 \_ 目錄複寫**</dt> </dl> | 使用 [**驅動程式 \_ 資訊 \_ 6**](driver-info-6.md) 結構中指定的完整檔案名來新增印表機驅動程式。 此旗標會與其中一個其他複製旗標一起 Or 運算。 如果設定此旗標，則如果檔案不存在，且 **驅動程式 \_ 資訊 \_ 6** 結構指定這些檔案，則 **AddPrinterDriverEx** 將會失敗。 這些檔案不需要複製到系統的印表機驅動程式目錄。 請參閱備註。<br/> **Windows 2000：** 不支援此旗標。<br/> |
| <span id="APD_COPY_NEW_FILES"></span><span id="apd_copy_new_files"></span><dl> <dt>**APD \_ 複製 \_ 新 \_ 檔案**</dt> </dl>                | 新增印表機驅動程式，並將印表機驅動程式目錄中的檔案，複製到目前使用中的任何對應檔案。 此旗標會模擬 [**AddPrinterDriver**](addprinterdriver.md)的行為。<br/>                                                                                                                                                                                                                                                                                  |
| <span id="APD_STRICT_DOWNGRADE"></span><span id="apd_strict_downgrade"></span><dl> <dt>**APD \_ STRICT \_ 降級**</dt> </dl>           | 只有當印表機驅動程式目錄中的所有檔案都早于目前使用中的任何對應檔案時，才新增印表機驅動程式。<br/>                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="APD_STRICT_UPGRADE"></span><span id="apd_strict_upgrade"></span><dl> <dt>**APD \_ STRICT \_ 升級**</dt> </dl>                 | 只有在印表機驅動程式目錄中的所有檔案都比目前使用中的任何對應檔案更新時，才新增印表機驅動程式。<br/>                                                                                                                                                                                                                                                                                                                                                                              |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為非零值。

如果此函式失敗，則傳回值為零。

如果已知的印表機驅動程式在使用作業系統時發生問題， **AddPrinterDriverEx** 將會失敗，並出現下列其中一個錯誤代碼：



| 錯誤碼                      | 意義                                                                                                                                                   |
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_印表機 \_ 驅動程式 \_ 封鎖錯誤 | 驅動程式無法在作業系統上運作。                                                                                                         |
| 錯誤 \_ 印表機 \_ 驅動程式 \_ 警告  | 作業系統上的驅動程式不可靠。 但是，如果指定了 APD \_ 安裝 \_ 警告 \_ 驅動程式，則會安裝驅動程式，且不會提供任何警告。 |



 

如需詳細資訊，請參閱＜備註＞一節。

## <a name="remarks"></a>備註

> [!Note]  
> 這是封鎖或同步函式，可能不會立即傳回。 此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。 從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。

 

呼叫端必須有 [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants)。

在呼叫 **AddPrinterDriverEx** 函式之前，驅動程式所需的所有檔案都必須複製到系統的印表機驅動程式目錄。 若要取出這個目錄的名稱，請呼叫 [**GetPrinterDriverDirectory**](getprinterdriverdirectory.md) 函式。

若要判斷目前已安裝的印表機驅動程式，請呼叫 [**EnumPrinterDrivers**](enumprinterdrivers.md) 函式。

如果已成功新增印表機驅動程式，此函式會呼叫 DrvDriverEvent (驅動程式 \_ 事件 \_ 初始化、層級、驅動程式 \_ 資訊 \_ \* 、lparam ) 函式，以允許驅動程式在安裝印表機驅動程式期間執行任何必要的初始化工作。 如需有關 **DrvDriverEvent** 的詳細資訊，請參閱 Microsoft Windows 驅動程式開發工具組 (DDK) 

在呼叫 **DrvDriverEvent** 期間，驅動程式不應使用 UI 呼叫。 若要執行 UI 相關的工作，安裝程式應該使用印表機的 .inf 檔案中的 VendorSetup 專案，或針對隨插即用的裝置，安裝程式可以使用裝置特定的共同安裝程式。 如需 VendorSetup 的詳細資訊，請參閱 DDK。

[**驅動程式 \_ 資訊 \_ 6**](driver-info-6.md)結構中所參考的檔案，必須是進行呼叫之來源電腦的本機。 檔案名可以是 UNC 名稱，前提是 UNC 名稱是本機電腦。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Winspool.drv (包含) 的 Windows。h </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Winspool.drv .lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv. winspool.drv</dt> </dl>                   |
| Unicode 與 ANSI 名稱<br/>   | **AddPrinterDriverExW** (Unicode) 和 **AddPrinterDriverExA** (ANSI) <br/>                           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 函式](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrinterDriver**](addprinterdriver.md)
</dt> <dt>

[**驅動程式 \_ 資訊 \_ 2**](driver-info-2.md)
</dt> <dt>

[**驅動程式 \_ 資訊 \_ 3**](driver-info-3.md)
</dt> <dt>

[**驅動程式 \_ 資訊 \_ 4**](driver-info-4.md)
</dt> <dt>

[**驅動程式 \_ 資訊 \_ 6**](driver-info-6.md)
</dt> <dt>

[**DeletePrinterDriverEx**](deleteprinterdriverex.md)
</dt> <dt>

[**EnumPrinterDrivers**](enumprinterdrivers.md)
</dt> <dt>

[**GetPrinterDriverDirectory**](getprinterdriverdirectory.md)
</dt> </dl>

 

