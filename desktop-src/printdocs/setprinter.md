---
description: SetPrinter 函式會設定指定印表機的資料，或藉由暫停列印、繼續列印或清除所有列印工作來設定指定印表機的狀態。
ms.assetid: ade367c5-20d6-4da9-bb52-ce6768cf7537
title: 'SetPrinter 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetPrinter
- SetPrinterA
- SetPrinterW
api_type:
- DllExport
api_location:
- WinSpool.drv
- Ext-MS-Win-printer-WinSpool-l1-1-0.dll
- Ext-MS-Win-printer-WinSpool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 5f2c58d97315ff108c8f12bd029849993a307025
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979812"
---
# <a name="setprinter-function"></a>SetPrinter 函式

**SetPrinter** 函式會設定指定印表機的資料，或藉由暫停列印、繼續列印或清除所有列印工作來設定指定印表機的狀態。

## <a name="syntax"></a>語法


```C++
BOOL SetPrinter(
  _In_ HANDLE hPrinter,
  _In_ DWORD  Level,
  _In_ LPBYTE pPrinter,
  _In_ DWORD  Command
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hPrinter* \[在\]
</dt> <dd>

印表機的控制碼。 使用 [**OpenPrinter**](openprinter.md)、 [**OpenPrinter2**](openprinter2.md)或 [**interactivesession.addprinter**](addprinter.md) 函數來取出印表機控制碼。

</dd> <dt>

*層級* \[在\]
</dt> <dd>

函數儲存在 *pPrinter* 所指向之緩衝區中的資料類型。 如果 *命令* 參數不等於零，則 *Level* 參數必須為零。

這個值可以是0、2、3、4、5、6、7、8或9。

</dd> <dt>

*pPrinter* \[在\]
</dt> <dd>

緩衝區的指標，其中包含要針對印表機設定的資料，或包含 *命令* 參數所指定之命令的資訊。 緩衝區中的資料類型取決於 *層級* 的值。



| 層級                                                                                                | 結構                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | 如果 *命令* 參數是 **印表機 \_ 控制 \_ 集 \_ 狀態**， *pPrinter* 必須包含 **DWORD** 值，以指定要設定的新印表機狀態。 如需可能狀態值的清單，請參閱 [**印表機 \_ 資訊 \_ 2**](printer-info-2.md)結構的 **狀態** 成員。 請注意，[ **印表機 \_ 狀態 \_ 暫停** ] 和 [ **印表機 \_ 狀態 \_ 擱置 \_ 刪除** ] 不是要設定的有效狀態值。<br/> 如果 *層級* 為0，但 *命令* 參數不是 **印表機 \_ 控制 \_ 集 \_ 狀態**，則 *pPrinter* 必須是 **Null**。<br/> |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | [**印表機 \_ 資訊 \_ 2**](printer-info-2.md)結構，內含印表機的詳細資訊。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | [**印表機 \_ 資訊 \_ 3**](printer-info-3.md)結構，內含印表機的安全性資訊。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | [**印表機 \_ 資訊 \_ 4**](printer-info-4.md)結構，其中包含最少量的印表機資訊，包括印表機的名稱、伺服器的名稱，以及印表機是否為遠端或本機。<br/>                                                                                                                                                                                                                                                                                                                                         |
| <span id="5"></span><dl> <dt>**5**</dt> </dl> | [**印表機 \_ 資訊 \_ 5**](printer-info-5.md)結構，包含印表機屬性和超時設定等印表機資訊。<br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="6"></span><dl> <dt>**6**</dt> </dl> | [**印表機 \_ 資訊 \_ 6**](printer-info-6.md)結構，指定印表機的狀態值。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="7"></span><dl> <dt>**7**</dt> </dl> | [**印表機 \_ 資訊 \_ 7**](printer-info-7.md)結構。 此結構的 *dwAction* 成員指出 **SetPrinter** 是否應該在目錄服務中發佈、取消發行、重新發行或更新印表機的資料。<br/>                                                                                                                                                                                                                                                                                                                |
| <span id="8"></span><dl> <dt>**8**</dt> </dl> | [**印表機 \_ 資訊 \_ 8**](printer-info-8.md)結構，指定全域預設印表機設定。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="9"></span><dl> <dt>**9**</dt> </dl> | [**印表機 \_ 資訊 \_ 9**](printer-info-9.md)結構，指定每個使用者的預設印表機設定。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

</dd> <dt>

*命令* \[在\]
</dt> <dd>

要執行的動作。

如果 *Level* 參數為非零值，請將此參數的值設定為零。 在此情況下，印表機會保留其目前的狀態，而函式會根據 *Level* 和 *pPrinter* 參數所指定的方式重新配置印表機資料。

如果 *Level* 參數為零，請將此參數的值設定為下列其中一個值。



| 值                                                                                                                                                                                                  | 意義                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PRINTER_CONTROL_PAUSE"></span><span id="printer_control_pause"></span><dl> <dt>**印表機 \_ 控制項 \_ 暫停**</dt> </dl>                 | 暫停印表機。<br/>                                                                                                                       |
| <span id="PRINTER_CONTROL_PURGE"></span><span id="printer_control_purge"></span><dl> <dt>**印表機 \_ 控制項 \_ 清除**</dt> </dl>                 | 刪除印表機中的所有列印工作。<br/>                                                                                                    |
| <span id="PRINTER_CONTROL_RESUME"></span><span id="printer_control_resume"></span><dl> <dt>**印表機 \_ 控制項 \_ 繼續**</dt> </dl>              | 繼續暫停的印表機。<br/>                                                                                                                 |
| <span id="PRINTER_CONTROL_SET_STATUS"></span><span id="printer_control_set_status"></span><dl> <dt>**印表機 \_ 控制 \_ 集 \_ 狀態**</dt> </dl> | 設定印表機狀態。<br/> 將 *pPrinter* 參數設定為 **DWORD** 值的指標，以指定新的印表機狀態。<br/> |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為非零值。

如果此函式失敗，則傳回值為零。

如果 *層級* 為7且發行動作失敗， **SetPrinter** 會傳回 **錯誤 \_ IO \_ 暫** 止，並嘗試在背景中完成動作。 如果 *層級* 為7且更新動作失敗，則 **SetPrinter** 會傳回錯誤檔案，但 **\_ \_ \_ 找不到**。

## <a name="remarks"></a>備註

> [!Note]  
> 這是封鎖或同步函式，可能不會立即傳回。 此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。 從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。

 

您無法使用 **SetPrinter** 來變更預設印表機。

若要修改目前的印表機設定，請呼叫 [**GetPrinter**](getprinter.md) 函式，將目前的設定取出至 [**印表機 \_ 資訊 \_ 2**](printer-info-2.md) 結構，視需要修改該結構的成員，然後再呼叫 **SetPrinter**。

**SetPrinter** 函式會忽略 [**印表機 \_ 資訊 \_ 2**](printer-info-2.md)結構的 **pServerName**、 **AveragePPM**、 **Status** 和 **cJobs** 成員。

暫停印表機會暫停該印表機所有列印工作的排程，但可能正在列印的列印工作除外。 列印工作可以提交到暫停的印表機，但在繼續列印之前，將不會排定在該印表機上列印工作。 如果清除印表機，則會刪除該印表機的所有列印工作，但目前的列印工作除外。

如果您使用 **SetPrinter** 來修改印表機的預設 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) 結構 (全域設定印表機預設值) ，您必須先呼叫 [**DocumentProperties**](documentproperties.md) 函數來驗證 **DEVMODE** 結構。

針對包含安全描述項指標的 [**印表機 \_ 資訊 \_ 2**](printer-info-2.md) 和 [**印表機 \_ 資訊 \_ 3**](printer-info-3.md) 結構，此函式只能設定呼叫者有權修改之安全描述項的元件。 若要設定特定的安全描述項元件，您必須在呼叫 [**OpenPrinter**](openprinter.md) 或 [**OpenPrinter2**](openprinter2.md) 函式來取得印表機的控制碼時，指定必要的存取權限。 下表顯示修改各種安全描述項元件所需的存取權限。



| 存取權限            | 安全描述項元件             |
|------------------------------|-------------------------------------------|
| **寫入 \_ 擁有者**             | 擁有者<br/> 主要群組<br/> |
| **寫入 \_ DAC**               | 任意存取控制清單 (DACL)   |
| **存取 \_ 系統 \_ 安全性** | 系統存取控制清單 (SACL)          |



 

如果安全描述項包含呼叫端沒有修改許可權的元件， **SetPrinter** 就會失敗。 您不想要修改之安全描述項的元件應該是 **Null** 或不存在。 如果您不想要修改安全描述項，並且使用 [**印表機 \_ 資訊 \_ 2**](printer-info-2.md)結構來呼叫 **SetPrinter** ，請將該結構的 **pSecurityDescriptor** 成員設為 **Null**。

網際網路連線防火牆 (ICF) 預設會封鎖印表機埠，但是可以啟用檔案和列印共用的例外狀況。 如果電腦系統管理員呼叫 **SetPrinter** ，則會啟用例外狀況。 如果非系統管理員呼叫它，而且尚未啟用例外狀況，則呼叫會失敗。

您可以使用層級7搭配 [**印表機 \_ 資訊 \_ 7**](printer-info-7.md) 結構，來發佈、取消發行或更新印表機的目錄服務資料。 印表機的目錄服務資料會藉 \_ \* 由呼叫印表機的 [**SetPrinterDataEx**](setprinterdataex.md)函式，包含儲存在 SPLDS 機碼下的所有資料。 在呼叫 **SetPrinter** 之前，請將 **印表機 \_ 資訊 \_ 7** 的 **pszObjectGUID** 成員設為 **Null** ，並將 *dwAction* 成員設定為下列其中一個值。



| 值                             | 描述                                                                                                                                                                                                                                                                                                                                                                             |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **DSPRINT \_ 發行**<br/>   | 發佈目錄服務資料。<br/>                                                                                                                                                                                                                                                                                                                                        |
| **DSPRINT 重新 \_ 發佈**<br/> | 印表機的目錄服務資料會解除發佈，然後再重新發佈，以重新整理已發佈印表機中的所有屬性。 重新發佈也會變更已發行之印表機的 GUID。 如果您懷疑印表機已發佈的資料已損毀，請使用此值。<br/>                                                                                         |
| **DSPRINT \_ 取消發佈**<br/> | Unpublishes 目錄服務資料。<br/>                                                                                                                                                                                                                                                                                                                                      |
| **DSPRINT \_ 更新**<br/>    | 更新目錄服務資料。 這與 **DSPRINT \_ PUBLISH** 相同，不同之處在于如果印表機尚未發佈，則 **SetPrinter** 會失敗，而且 **\_ \_ \_ 找不到錯誤** 檔案。<br/> 使用 **DSPRINT \_ update** 來更新已發行的屬性，但不強制發行。 印表機驅動程式應該一律使用 **DSPRINT \_ UPDATE** ，而不是 **DSPRINT \_ PUBLISH**。<br/> |



 

**DSPRINT \_暫** 止不是 **SetPrinter** 的有效 *dwAction* 值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Winspool.drv (包含) 的 Windows。h </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Winspool.drv .lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv. winspool.drv</dt> </dl>                   |
| Unicode 與 ANSI 名稱<br/>   | **SetPrinterW** (Unicode) 和 **SetPrinterA** (ANSI) <br/>                                           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 函式](printing-and-print-spooler-functions.md)
</dt> <dt>

[**Interactivesession.addprinter**](addprinter.md)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**OpenPrinter2**](openprinter2.md)
</dt> <dt>

[**印表機 \_ 資訊 \_ 2**](printer-info-2.md)
</dt> <dt>

[**印表機 \_ 資訊 \_ 3**](printer-info-3.md)
</dt> <dt>

[**印表機 \_ 資訊 \_ 4**](printer-info-4.md)
</dt> <dt>

[**印表機 \_ 資訊 \_ 5**](printer-info-5.md)
</dt> <dt>

[**印表機 \_ 資訊 \_ 6**](printer-info-6.md)
</dt> <dt>

[**印表機 \_ 資訊 \_ 7**](printer-info-7.md)
</dt> <dt>

[**印表機 \_ 資訊 \_ 8**](printer-info-8.md)
</dt> <dt>

[**印表機 \_ 資訊 \_ 9**](printer-info-9.md)
</dt> <dt>

[**SetPrinterDataEx**](setprinterdataex.md)
</dt> </dl>

 

 




