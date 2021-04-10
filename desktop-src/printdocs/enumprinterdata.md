---
description: EnumPrinterData 函式會列舉指定印表機的設定資料。
ms.assetid: 0a4c8436-46fe-4e21-8d55-c5031a3d1b38
title: 'EnumPrinterData 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrinterData
- EnumPrinterDataA
- EnumPrinterDataW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: d7c175b0c90853a592e0ff979095d41432c16b38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192599"
---
# <a name="enumprinterdata-function"></a>EnumPrinterData 函式

**EnumPrinterData** 函式會列舉指定印表機的設定資料。

若要在單一呼叫中取出設定資料，請使用 [**EnumPrinterDataEx**](enumprinterdataex.md) 函數。

## <a name="syntax"></a>語法


```C++
DWORD EnumPrinterData(
  _In_  HANDLE  hPrinter,
  _In_  DWORD   dwIndex,
  _Out_ LPTSTR  pValueName,
  _In_  DWORD   cbValueName,
  _Out_ LPDWORD pcbValueName,
  _Out_ LPDWORD pType,
  _Out_ LPBYTE  pData,
  _In_  DWORD   cbData,
  _Out_ LPDWORD pcbData
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hPrinter* \[在\]
</dt> <dd>

要取得其設定資料之印表機的控制碼。 使用 [**OpenPrinter**](openprinter.md) 或 [**interactivesession.addprinter**](addprinter.md) 函式來取出印表機控制碼。

</dd> <dt>

*dwIndex* \[在\]
</dt> <dd>

索引值，指定要取出的設定資料值。

針對指定的印表機控制碼，將此參數設定為零，以進行第一次的 **EnumPrinterData** 呼叫。 然後，將參數遞增一次，以用於後續涉及相同印表機的呼叫，直到函式傳回錯誤的 \_ \_ 專案為止 \_ 。 如需詳細資訊，請參閱下列備註一節。

如果您使用 *cbValueName* 和 *cbData* 參數描述中所述的技術來取得適當的緩衝區大小值，在第一次呼叫指定的印表機控制碼的 **EnumPrinterData** 時，將這些參數設定為零，就 *不會對* 該呼叫造成影響。 在下一次呼叫 **EnumPrinterData** 時，將 *dwIndex* 設定為零，以啟動實際的列舉程式。

設定資料值未排序。 新的值會有任意的索引。 這表示 **EnumPrinterData** 函數可能會以任何順序傳回值。

</dd> <dt>

*pValueName* \[擴展\]
</dt> <dd>

緩衝區的指標，此緩衝區會接收設定資料值的名稱，包括終止的 null 字元。

</dd> <dt>

*cbValueName* \[在\]
</dt> <dd>

*PValueName* 所指向之緩衝區的大小（以位元組為單位）。

如果您想要讓作業系統提供適當的緩衝區大小，請將此參數和 *cbData* 參數設定為零，以在第一次呼叫指定的印表機控制碼時使用 **EnumPrinterData** 。 當函式傳回時， *pcbValueName* 所指向的變數將包含夠大的緩衝區大小，以成功列舉印表機的所有設定資料值名稱。

</dd> <dt>

*pcbValueName* \[擴展\]
</dt> <dd>

變數的指標，此變數會接收儲存在 *pValueName* 所指向之緩衝區中的位元組數目。

</dd> <dt>

*pType* \[擴展\]
</dt> <dd>

變數的指標，此變數會接收程式碼，指出儲存在指定值中的資料類型。 如需可能的類型代碼清單，請參閱登錄 [數值型別](/windows/desktop/SysInfo/registry-value-types)。 如果不需要類型程式碼，則 *pType* 參數可以是 **Null** 。

</dd> <dt>

*.pdata* \[擴展\]
</dt> <dd>

接收設定資料值的緩衝區指標。

如果不需要設定資料值，則這個參數可以是 **Null** 。

</dd> <dt>

*cbData* \[在\]
</dt> <dd>

*.Pdata* 所指向之緩衝區的大小（以位元組為單位）。

如果您想要讓作業系統提供適當的緩衝區大小，請將此參數和 *cbValueName* 參數設定為零，以在第一次呼叫指定的印表機控制碼時使用 **EnumPrinterData** 。 當函式傳回時， *pcbData* 所指向的變數將包含夠大的緩衝區大小，以成功列舉印表機的所有設定資料值名稱。

</dd> <dt>

*pcbData* \[擴展\]
</dt> <dd>

變數的指標，此變數會接收儲存在 *.pdata* 所指向之緩衝區中的位元組數目。

如果 *.pdata* 為 **null**，則這個參數可以是 **null** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為「錯誤 \_ 成功」。

如果函式失敗，則傳回值為系統錯誤碼。

\_ \_ \_ 如果沒有更多的設定資料值要抓取指定的印表機控制碼，此函數會傳回錯誤的專案。

## <a name="remarks"></a>備註

> [!Note]  
> 這是封鎖或同步函式，可能不會立即傳回。 此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。 從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。

 

**EnumPrinterData** 會透過 [**SetPrinterData**](setprinterdata.md) 函式來抓取印表機設定資料集。 印表機的設定資料是由一組命名的和具類型的值所組成。 **EnumPrinterData** 函式會在您每次呼叫時取得其中一個值，以及其名稱和類型程式碼。 連續多次呼叫 **EnumPrinterData** 函數，以取得印表機的所有設定資料值。

印表機設定資料會儲存在登錄中。 列舉印表機設定資料時，您應該避免呼叫可能會變更該資料的登錄功能。

如果您想要讓作業系統提供適當的緩衝區大小，請先呼叫 **EnumPrinterData** ，並將 *cbValueName* 和 *cbData* 參數設定為零，如稍早在參數區段中所述。 此呼叫的 *dwIndex* 值並不重要。 當函式傳回時， \* *pcbValueName* 和 \* *pcbData* 將包含夠大的緩衝區大小，以列舉印表機的所有設定資料值名稱和值。 在下一個呼叫中，配置值名稱和資料緩衝區，將 *cbValueName* 和 *cbData* 設定為所配置緩衝區的大小（以位元組為單位），並將 *dwIndex* 設定為零。 之後，繼續呼叫 **EnumPrinterData** 函式，每次遞增 *dwIndex* 一次，直到函式傳回錯誤的 \_ 專案 \_ 為止 \_ 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Winspool.drv (包含) 的 Windows。h </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Winspool.drv .lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv. winspool.drv</dt> </dl>                   |
| Unicode 與 ANSI 名稱<br/>   | **EnumPrinterDataW** (Unicode) 和 **EnumPrinterDataA** (ANSI) <br/>                                 |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 函式](printing-and-print-spooler-functions.md)
</dt> <dt>

[**DeletePrinterData**](deleteprinterdata.md)
</dt> <dt>

[**EnumPrinterDataEx**](enumprinterdataex.md)
</dt> <dt>

[**GetPrinterData**](getprinterdata.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> <dt>

[**SetPrinterData**](setprinterdata.md)
</dt> </dl>

 

