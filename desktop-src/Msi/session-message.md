---
description: Session 物件的 Message 方法會執行任何已啟用的記錄作業，並順延強制與引擎相關聯的 UI 處理常式物件。 您可以選擇性地為各種訊息類型啟用記錄。 請參閱 EnableLog 方法。
ms.assetid: 09053700-a641-4970-bf55-d7c81f345257
title: Session 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.Message
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e20cfebe0a3359a99770cbd242501649bf93f86e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995077"
---
# <a name="sessionmessage-method"></a>Session 方法

[**Session**](session-object.md)物件的 **Message** 方法會執行任何已啟用的記錄作業，並順延強制與引擎相關聯的 UI 處理常式物件。 您可以選擇性地為各種訊息類型啟用記錄。 請參閱 [**EnableLog**](installer-enablelog.md) 方法。

如果記錄欄位0包含格式化字串，則會使用它來格式化其他欄位中的資料。 否則，如果訊息是錯誤、警告或使用者訊息，則會嘗試使用訊息類型和傳回值記錄之欄位1中找到的錯誤號碼，在目前資料庫的錯誤資料表中尋找訊息範本。

## <a name="syntax"></a>語法


```JScript
Session.Message(
  kind,
  record
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*類別* 
</dt> <dd>

*Kind* 參數必須是下列值之一。 若要顯示含有推播按鈕和圖示的訊息方塊，請將 [**MessageBox**](/windows/win32/api/winuser/nf-winuser-messagebox)和 [**MessageBoxEx**](/windows/win32/api/winuser/nf-winuser-messageboxexa)所使用的標準訊息方塊樣式新增至 **msiMessageTypeError**、 **msiMessageTypeWarning** 或 **msiMessageTypeUser**，以計算 *類型* 的值。 如需詳細資訊，請參閱下面的「備註」一節。



| 常數                                                                                                                                                                                                                                                                                                                 | 意義                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiMessageTypeFatalExit"></span><span id="msimessagetypefatalexit"></span><span id="MSIMESSAGETYPEFATALEXIT"></span><dl> <dt>**msiMessageTypeFatalExit**</dt> <dt>&H00000000</dt> </dl>                     | 提前終止，可能是記憶體不足。<br/>                                                                              |
| <span id="msiMessageTypeError"></span><span id="msimessagetypeerror"></span><span id="MSIMESSAGETYPEERROR"></span><dl> <dt>**msiMessageTypeError**</dt> <dt>&H01000000</dt> </dl>                                     | 格式化的錯誤訊息， \[ 1 \] 是 [錯誤資料表](error-table.md)中的訊息編號。<br/>                                               |
| <span id="msiMessageTypeWarning"></span><span id="msimessagetypewarning"></span><span id="MSIMESSAGETYPEWARNING"></span><dl> <dt>**msiMessageTypeWarning**</dt> <dt>&H02000000</dt> </dl>                             | 格式化的警告訊息， \[ 1 \] 是 [錯誤資料表](error-table.md)中的訊息編號。<br/>                                             |
| <span id="msiMessageTypeUser_"></span><span id="msimessagetypeuser_"></span><span id="MSIMESSAGETYPEUSER_"></span><dl> <dt> **msiMessageTypeUser**</dt> <dt>&H03000000</dt> </dl>                                     | 使用者要求訊息， \[ 1 \] 是 [錯誤資料表](error-table.md)中的訊息編號。<br/>                                                  |
| <span id="msiMessageTypeInfo"></span><span id="msimessagetypeinfo"></span><span id="MSIMESSAGETYPEINFO"></span><dl> <dt>**msiMessageTypeInfo**</dt> <dt>&H04000000</dt> </dl>                                         | 記錄檔的資訊性訊息，不會顯示。<br/>                                                                                 |
| <span id="msiMessageTypeFilesInUse"></span><span id="msimessagetypefilesinuse"></span><span id="MSIMESSAGETYPEFILESINUSE"></span><dl> <dt>**msiMessageTypeFilesInUse**</dt> <dt>&H05000000</dt> </dl>                 | 使用中需要取代的檔案清單。<br/>                                                                                    |
| <span id="msiMessageTypeResolveSource"></span><span id="msimessagetyperesolvesource"></span><span id="MSIMESSAGETYPERESOLVESOURCE"></span><dl> <dt>**msiMessageTypeResolveSource**</dt> <dt>&H06000000</dt> </dl>     | 要求判斷有效的來源位置。<br/>                                                                                     |
| <span id="msiMessageTypeOutOfDiskSpace"></span><span id="msimessagetypeoutofdiskspace"></span><span id="MSIMESSAGETYPEOUTOFDISKSPACE"></span><dl> <dt>**msiMessageTypeOutOfDiskSpace**</dt> <dt>&H07000000</dt> </dl> | 磁碟空間不足的訊息。<br/>                                                                                                  |
| <span id="msiMessageTypeActionStart"></span><span id="msimessagetypeactionstart"></span><span id="MSIMESSAGETYPEACTIONSTART"></span><dl> <dt>**msiMessageTypeActionStart**</dt> <dt>&H08000000</dt> </dl>             | 動作的開頭， \[ 1 個 \] 動作名稱、 \[ 2 個 \] 描述、 \[ 3 \] 個 ACTIONDATA 訊息的範本。<br/>                                    |
| <span id="msiMessageTypeActionData"></span><span id="msimessagetypeactiondata"></span><span id="MSIMESSAGETYPEACTIONDATA"></span><dl> <dt>**msiMessageTypeActionData**</dt> <dt>&H09000000</dt> </dl>                 | 動作資料。 記錄欄位會對應至 ACTIONSTART 訊息的範本。<br/>                                                     |
| <span id="msiMessageTypeProgress"></span><span id="msimessagetypeprogress"></span><span id="MSIMESSAGETYPEPROGRESS"></span><dl> <dt>**msiMessageTypeProgress**</dt> <dt>&H0A000000</dt> </dl>                         | 進度列資訊。 請參閱下方的記錄欄位描述。<br/>                                                             |
| <span id="msiMessageTypeCommonData_"></span><span id="msimessagetypecommondata_"></span><span id="MSIMESSAGETYPECOMMONDATA_"></span><dl> <dt> **msiMessageTypeCommonData**</dt> <dt>&H0B000000</dt> </dl>             | 若要啟用 [取消] 按鈕，請將 \[ 1 設定 \] 為2，並將 \[ 2 設定 \] 為1。 <br/> 若要停用 [取消] 按鈕，請將 \[ 1 設定 \] 為2， \[ 2 \] 為0<br/> |



 

</dd> <dt>

*記錄* 
</dt> <dd>

包含訊息特定欄位的必要 [**記錄**](record-object.md) 物件。

</dd> </dl>

## <a name="return-value"></a>傳回值



| 常數                                                                                              | 值         |
|-------------------------------------------------------------------------------------------------------|---------------|
| <dl> <dt>**msiMessageStatusError**</dt> </dl>  | -1<br/> |
| <dl> <dt>**msiMessageStatusNone**</dt> </dl>   | 0<br/>  |
| <dl> <dt>**msiMessageStatusOk**</dt> </dl>     | 1<br/>  |
| <dl> <dt>**msiMessageStatusCancel**</dt> </dl> | 2<br/>  |
| <dl> <dt>**msiMessageStatusAbort**</dt> </dl>  | 3<br/>  |
| <dl> <dt>**msiMessageStatusRetry**</dt> </dl>  | 4<br/>  |
| <dl> <dt>**msiMessageStatusIgnore**</dt> </dl> | 5<br/>  |
| <dl> <dt>**msiMessageStatusYes**</dt> </dl>    | 6<br/>  |
| <dl> <dt>**msiMessageStatusNo**</dt> </dl>     | 7<br/>  |



 

## <a name="remarks"></a>備註

**訊息記錄欄位**

以下描述當 msiMessageTypeProgress 傳遞為訊息類型時的記錄欄位定義。

欄位1指定進度訊息的類型。 其他欄位的意義會根據此欄位中的值而定。 可以設定為欄位1的可能值如下所示。



| 訊息名稱     | 值 | 欄位1描述                                                                                                 |
|------------------|-------|---------------------------------------------------------------------------------------------------------------------|
| MasterReset      | 0     | 重設進度列，並在橫條圖中設定預期的總刻度數。                                         |
| ActionInfo       | 1     | 提供目前動作要傳送的進度訊息相關資訊。                                 |
| ProgressReport   | 2     | 遞增進度列。                                                                                        |
| ProgressAddition | 3     | 啟用動作 (例如 CustomAction) ，將刻度加入進度列的預期進度總數。 |



 

欄位2的意義取決於 [欄位 1] 中的值，如下所示。



| 欄位1值 | 欄位2描述                                                                                        |
|---------------|------------------------------------------------------------------------------------------------------------|
| 0             | 進度列中預期的總刻度數。                                                        |
| 1             | 進度列針對每個 ActionData 訊息移動的刻度數目。 如果欄位3為0，則會忽略此欄位。 |
| 2             | 進度列移動的刻度數目。                                                                |
| 3             | 要加入至總預期進度的刻度數目。                                                         |



 

欄位3的意義取決於 [欄位 1] 中的值，如下所示。



| 欄位1值 | 欄位3值 | 欄位3描述                                                                                             |
|---------------|---------------|-----------------------------------------------------------------------------------------------------------------|
| 0             | 0             | 轉寄進度列 (從左至右)                                                                             |
|               | 1             | 回溯進度列 (向左)                                                                            |
| 1             | 0             | 目前的動作將會傳送明確的 ProgressReport 訊息。                                                  |
|               | 1             | 每次傳送 ActionData 訊息時，依欄位2中指定的刻度數目遞增進度列。 |
| 2             | 未使用        |                                                                                                                 |
| 3             | 未使用        |                                                                                                                 |



 

欄位4的意義取決於 [欄位 1] 中的值，如下所示。



| 欄位1值 | 欄位4值 | 欄位4描述                                                                                                                                 |
|---------------|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| 0             | 0             | 執行正在進行中。 在此情況下，UI 可以計算並顯示剩餘的時間。                                                      |
|               | 1             | 建立執行腳本。 在此情況下，UI 可能會顯示一則訊息，等候安裝程式完成準備安裝時請稍候。 |
| 1             | 未使用        |                                                                                                                                                     |
| 2             | 未使用        |                                                                                                                                                     |
| 3             | 未使用        |                                                                                                                                                     |



 

**顯示訊息方塊**

若要顯示含有推播按鈕和圖示的訊息方塊，請將 **MessageBox** 和 **MessageBoxEx** 所使用的標準訊息方塊樣式新增至 **msiMessageTypeError**、 **msiMessageTypeWarning** 或 **msiTypeUser**，以計算 *類型* 的值。 VBScript 的可用推播按鈕選項有 vbOKOnly (MB \_ OK) 、vbOKCancel (MB \_ OKCANCEL) 、VBABORTRETRYIGNORE (MB \_ ABORTRETRYIGNORE) 、vbYesNoCancel (MB \_ YESNOCANCEL) 、vbYesNo (Mb \_ YESNO) 和 vbRetryCancel (mb \_ RETRYCANCEL) 。 VBScript 的可用圖示選項有 vbCritical (MB \_ ICONERROR) 、vbQuestion (MB \_ ICONQUESTION) 、VBEXCLAMATION (mb \_ ICONWARNING) 和 vbInformation (mb \_ ICONINFORMATION) 。

例如，下列呼叫會傳送具有 vbExclamation 圖示和 vbYesNo 按鈕的 **msiMessageTypeError** 訊息。


```VB
Session.Message &H01000034, record
```



如果自訂動作呼叫 **訊息** 方法，自訂動作應該能夠處理使用者的取消作業，而且應該會傳回 **msiDoActionStatusUserExit**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ >isession 定義為 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 
