---
description: 印表機 \_ 資訊 \_ 7 結構會指定目錄服務印表機資訊。
ms.assetid: 9443855e-df7d-41a1-a0df-5649a97b2915
title: 'PRINTER_INFO_7 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_7
- _PRINTER_INFO_7A
- _PRINTER_INFO_7W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: c8ba37176bb970883533be1e0ddcc47a09b164bf48767442f75096828c9bce5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117867764"
---
# <a name="printer_info_7-structure"></a>印表機 \_ 資訊 \_ 7 結構

**印表機 \_ 資訊 \_ 7** 結構會指定目錄服務印表機資訊。 您可以使用此結構搭配 [**SetPrinter**](setprinter.md) 函式，在目錄服務中發佈印表機的資料 (ds) ，或從 ds 更新或移除印表機的已發佈資料。 使用此結構搭配 [**GetPrinter**](getprinter.md) 函式來判斷是否已在 DS 中發佈印表機。

## <a name="syntax"></a>語法


```C++
typedef struct _PRINTER_INFO_7 {
  LPTSTR pszObjectGUID;
  DWORD  dwAction;
} PRINTER_INFO_7, *PPRINTER_INFO_7;
```



## <a name="members"></a>成員

<dl> <dt>

**pszObjectGUID**
</dt> <dd>

以 null 結束的字串指標，其中包含與已發行的印表機相關聯之目錄服務列印佇列物件的 GUID。 使用 [**GetPrinter**](getprinter.md) 函式來取得此 GUID。

在呼叫 [**SetPrinter**](setprinter.md)之前，請將 **PszObjectGUID** 設定為 **Null**。

</dd> <dt>

**dwAction**
</dt> <dd>

指出 [**SetPrinter**](setprinter.md) 函式執行的動作。 若為 [**GetPrinter**](getprinter.md) 函數，這個成員會指出指定的印表機是否已發行。 這個成員可以是下列值的組合。



| 值                                                                                                                                                                                                                                     | 意義                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DSPRINT_PENDING"></span><span id="dsprint_pending"></span><dl> <dt>**DSPRINT \_暫**</dt>止的 <dt>0x80000000</dt> </dl>       | [**GetPrinter**](getprinter.md)：表示系統正在嘗試完成 [**SetPrinter**](setprinter.md) 呼叫所啟動的發行或取消發行作業。<br/> [**SetPrinter**](setprinter.md)：此值無效。 <br/>                                                |
| <span id="DSPRINT_PUBLISH"></span><span id="dsprint_publish"></span><dl> <dt>**DSPRINT \_發佈**</dt> <dt>0x00000001</dt> </dl>       | [**SetPrinter**](setprinter.md)：在 DS 中發佈印表機的資料。<br/> [**GetPrinter**](getprinter.md)：表示印表機已發佈。 <br/>                                                                                                                                      |
| <span id="DSPRINT_REPUBLISH"></span><span id="dsprint_republish"></span><dl> <dt>**DSPRINT \_重新發佈**</dt> <dt>0x00000008</dt> </dl> | [**SetPrinter**](setprinter.md)：印表機的 DS 資料已解除發佈，然後再次發佈，重新整理已發佈印表機中的所有屬性。 重新發佈也會變更已發行之印表機的 GUID。<br/> [**GetPrinter**](getprinter.md)：絕不會傳回這個值。 <br/> |
| <span id="DSPRINT_UNPUBLISH"></span><span id="dsprint_unpublish"></span><dl> <dt>**DSPRINT \_取消**</dt>發行 <dt>0x00000004</dt> </dl> | [**SetPrinter**](setprinter.md)：從 DS 移除印表機的已發佈資料。<br/> [**GetPrinter**](getprinter.md)：指出未發佈印表機。 <br/>                                                                                                                        |
| <span id="DSPRINT_UPDATE"></span><span id="dsprint_update"></span><dl> <dt>**DSPRINT \_UPDATE**</dt> <dt>0x00000002</dt> </dl>          | [**SetPrinter**](setprinter.md)：更新 DS 中的印表機已發佈資料。<br/> [**GetPrinter**](getprinter.md)：絕不會傳回這個值。 <br/>                                                                                                                                        |



 

</dd> </dl>

## <a name="remarks"></a>備註

[**SetPrinter**](setprinter.md)呼叫中使用 **印表機資訊 \_ \_ 7** 結構，將印表機資訊發佈到目錄服務。 已發佈的資料包含指定之印表機的所有值和資料，可在 SPLDS 多工 \_ 緩衝處理器 \_ 金鑰、SPLDS \_ 驅動程式 \_ 金鑰或 SETPRINTERDATAEX 所建立的 SPLDS \_ 使用者 \_ 金鑰[](setprinterdataex.md)金鑰下找到。

若為 [**SetPrinter**](setprinter.md)，則應該將 *PszObjectGUID* 設定為 **Null**。 針對 [**GetPrinter**](getprinter.md)， *pszObjectGUID* 會傳回與已發佈印表機相關聯之目錄服務列印佇列物件的 GUID。 您可以使用此 GUID 搭配 Active Directory Services 介面， (ADSI) 方法來取出印表機的已發佈資料。 不過，建議用來取得已發佈資料的方法是呼叫 [**GetPrinterDataEx**](getprinterdataex.md) 函數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>winspool.drv (包含 Windows .h) </dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **\_ 印表機 \_ 資訊 \_ 7W** (Unicode) 和 **\_ 印表機 \_ 資訊 \_ 7A** (ANSI) <br/>                           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 結構](printing-and-print-spooler-structures.md)
</dt> </dl>

 

 




