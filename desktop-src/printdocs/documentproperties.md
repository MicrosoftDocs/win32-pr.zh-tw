---
description: DocumentProperties 函式會抓取或修改印表機初始化資訊，或顯示指定印表機的印表機設定屬性工作表。
ms.assetid: e89a2f6f-2bac-4369-b526-f8e15028698b
title: 'DocumentProperties 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DocumentProperties
- DocumentPropertiesA
- DocumentPropertiesW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 732cb6901b444117d0599a2899327ebcb749cf74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115793"
---
# <a name="documentproperties-function"></a>DocumentProperties 函式

**DocumentProperties** 函式會抓取或修改印表機初始化資訊，或顯示指定印表機的印表機設定屬性工作表。

## <a name="syntax"></a>語法


```C++
LONG DocumentProperties(
  _In_  HWND     hWnd,
  _In_  HANDLE   hPrinter,
  _In_  LPTSTR   pDeviceName,
  _Out_ PDEVMODE pDevModeOutput,
  _In_  PDEVMODE pDevModeInput,
  _In_  DWORD    fMode
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hWnd* \[在\]
</dt> <dd>

印表機設定屬性工作表的父視窗控制碼。

</dd> <dt>

*hPrinter* \[在\]
</dt> <dd>

印表機物件的控制碼。 使用 [**OpenPrinter**](openprinter.md) 或 [**interactivesession.addprinter**](addprinter.md) 函式來取出印表機控制碼。

</dd> <dt>

*pDeviceName* \[在\]
</dt> <dd>

以 null 結束的字串指標，指定顯示印表機設定屬性工作表之裝置的名稱。

</dd> <dt>

*pDevModeOutput* \[擴展\]
</dt> <dd>

[**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)結構的指標，此結構會接收使用者指定的印表機設定資料。

</dd> <dt>

*pDevModeInput* \[在\]
</dt> <dd>

由作業系統用來初始化屬性工作表控制項的 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) 結構指標。

只有在 *fMode* 參數中設定了 [ **DM \_ in \_ BUFFER** ] 旗標時，才會使用這個參數。 如果未設定 [ **\_ 在 \_ 緩衝區中的 DM** ]，則作業系統會使用印表機的預設 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)。

</dd> <dt>

*fMode* \[在\]
</dt> <dd>

函數所執行的作業。 如果此參數為零，則 **DocumentProperties** 函數會傳回印表機驅動程式的 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) 資料結構所需的位元組數目。 否則，請使用下列一或多個常數來建立這個參數的值。不過請注意，為了變更列印設定，應用程式必須指定至少一個輸入值和一個輸出值。



| 值                                                                                                                                                          | 意義                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DM_IN_BUFFER"></span><span id="dm_in_buffer"></span><dl> <dt>**\_緩衝區中的 DM \_**</dt> </dl>    | 輸入值。 在提示、複製或更新之前，函式會將印表機驅動程式的目前列印設定與 *pDevModeInput* 參數所指定的 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)結構中的設定合併。 函數只會針對由 **DEVMODE** 結構的 **dmFields** 成員所指定的成員，更新結構。 此值也會定義為 **DM \_ MODIFY**。 在合併期間發生衝突的情況下， *pDevModeInput* 所指定的 **DEVMODE** 結構中的設定會覆寫印表機驅動程式目前的列印設定。<br/> |
| <span id="DM_IN_PROMPT"></span><span id="dm_in_prompt"></span><dl> <dt>**DM \_ IN \_ PROMPT**</dt> </dl>    | 輸入值。 此函式會顯示印表機驅動程式的列印設置屬性工作表，然後將印表機的 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) 資料結構中的設定變更為使用者指定的值。 此值也會定義為 **DM \_ 提示**。<br/>                                                                                                                                                                                                                                                                                                         |
| <span id="DM_OUT_BUFFER"></span><span id="dm_out_buffer"></span><dl> <dt>**DM \_ OUT \_ 緩衝區**</dt> </dl> | 輸出值。 函數會將印表機驅動程式的目前列印設定（包括私用資料）寫入 *pDevModeOutput* 參數所指定的 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)資料結構中。 呼叫端必須配置夠大的緩衝區以包含資訊。 如果位 **DM 的 \_ 輸出 \_ 緩衝區** 集很清楚， *pDevModeOutput* 參數可以是 **Null**。 此值也會定義為 **DM \_ 複製**。<br/>                                                                                                                                          |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

如果 *fMode* 參數為零，則傳回值是包含印表機驅動程式初始化資料所需的緩衝區大小。 請注意，如果印表機驅動程式將私用資料附加至結構，此緩衝區可能會大於 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) 結構。

如果函數顯示內容表，則傳回值會是 **IDOK** 或 **IDCANCEL**，視使用者選取的按鈕而定。

如果函式未顯示內容表且成功，則傳回值為 **IDOK**。

如果函式失敗，則傳回值小於零。

## <a name="remarks"></a>備註

> [!Note]  
> 這是封鎖或同步函式，可能不會立即傳回。 此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。 從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。

 

*PDeviceName* 參數所指向的字串可以藉由呼叫 [**GetPrinter**](getprinter.md)函數來取得。

印表機驅動程式實際使用的 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) 結構包含與裝置無關的部分 (如上面所定義) 接著會有每個驅動程式和驅動程式版本的大小和內容各異的驅動程式特定元件。 因為此驅動程式相依性，所以在為它配置緩衝區之前，應用程式必須查詢驅動程式的正確大小，才是很重要的。

**若要對應用程式的本機列印設定進行變更，應用程式應該遵循下列步驟：**

1.  藉由呼叫 **DocumentProperties** ，並在 *fMode* 參數中指定零，取得完整 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)結構所需的位元組數目。
2.  為完整的 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) 結構配置記憶體。
3.  藉由呼叫 **DocumentProperties** 來取得目前的印表機設定。 將步驟2中配置的 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) 結構指標傳遞為 *pDevModeOutput* 參數，並指定 **DM \_ OUT \_ 緩衝區** 值。
4.  修改所傳回之 [**devmode**](/windows/win32/api/wingdi/ns-wingdi-devmodea)結構的適當成員，並藉由在 **DEVMODE** 的 **dmFields** 成員中設定對應的位，來指出哪些成員已變更。
5.  呼叫 **DocumentProperties** ，並將修改過的 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)結構傳回做 *為 pDevModeInput* 和 *pDevModeOutput* 參數，並同時指定在緩衝區和 **dm \_ 輸出 \_ 緩衝區** 值 **\_ 中 \_ 的 dm** ， (使用 OR 運算子) 來合併。第三次呼叫 **DocumentProperties** 所傳回的 **DEVMODE** 結構，可以當做 [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca)函式呼叫中的引數使用。

若要使用目前的印表機設定來建立印表機裝置內容的控制碼，您只需要呼叫 **DocumentProperties** 兩次，如上所述。 第一個呼叫會取得完整 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) 的大小，而第二個呼叫則會使用目前的印表機設定來初始化 **DEVMODE** 。 將初始化的 **DEVMODE** 傳遞給 [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) ，以取得印表機裝置內容的控制碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Winspool.drv (包含) 的 Windows。h </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Winspool.drv .lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv. winspool.drv</dt> </dl>                   |
| Unicode 與 ANSI 名稱<br/>   | **DocumentPropertiesW** (Unicode) 和 **DocumentPropertiesA** (ANSI) <br/>                           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 函式](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AdvancedDocumentProperties**](advanceddocumentproperties.md)
</dt> <dt>

[**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca)
</dt> <dt>

[**版**](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> </dl>

 

