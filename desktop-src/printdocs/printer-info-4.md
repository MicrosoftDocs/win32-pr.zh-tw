---
description: 印表機 \_ 資訊 \_ 4 結構會指定一般印表機資訊。您可以使用此結構來取得 >enumprinters 呼叫的最短印表機資訊。
ms.assetid: 81bd0eab-dc1e-4cf1-8f63-3686f1711c1f
title: 'PRINTER_INFO_4 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_4
- _PRINTER_INFO_4A
- _PRINTER_INFO_4W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 3ba6e372b495c47dd92e61e51ba6487e6d9c2c0aca924bf6ed3a092ba0816820
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119446988"
---
# <a name="printer_info_4-structure"></a>印表機 \_ 資訊 \_ 4 結構

**印表機 \_ 資訊 \_ 4** 結構會指定一般印表機資訊。

您可以使用此結構來取得 [**>enumprinters**](enumprinters.md)呼叫的最短印表機資訊。 這種呼叫可讓您快速且輕鬆地取出系統上所有本機安裝印表機的名稱和屬性，以及使用者已建立的所有遠端印表機連線。

## <a name="syntax"></a>語法


```C++
typedef struct _PRINTER_INFO_4 {
  LPTSTR pPrinterName;
  LPTSTR pServerName;
  DWORD  Attributes;
} PRINTER_INFO_4, *PPRINTER_INFO_4;
```



## <a name="members"></a>成員

<dl> <dt>

**pPrinterName**
</dt> <dd>

以 null 結束的字串指標，指定印表機 (本機或遠端) 的名稱。

</dd> <dt>

**pServerName**
</dt> <dd>

以 null 結束的字串指標，這是伺服器的名稱。

</dd> <dt>

**屬性**
</dt> <dd>

指定傳回之資料的相關資訊。



| 值                       | 意義                          |
|-----------------------------|----------------------------------|
| \_本機印表機屬性 \_   | 印表機是本機印表機。  |
| 印表機 \_ 屬性 \_ 網路 | 印表機是遠端印表機。 |



 

</dd> </dl>

## <a name="remarks"></a>備註

**印表機 \_ 資訊 \_ 4** 結構提供簡單且極快速的方式來抓取本機電腦上安裝的印表機名稱，以及使用者已建立的遠端連線。 使用 **印表機 \_ 資訊 \_ 4** 資料結構呼叫 [**>enumprinters**](enumprinters.md)時，該函式會查詢登錄中的指定資訊，然後立即傳回。 與其他層級的 **印表機 \_ 資訊 \_ xxx** 資料結構一起呼叫時，這與 **>enumprinters** 的行為不同。 尤其是，使用層級 2 (**印表機 \_ 資訊 \_ 2** ) 資料結構來呼叫 **>enumprinters** 時，它會在每個遠端連線上執行 **OpenPrinter** 呼叫。 如果遠端連線已關閉，或遠端伺服器已不存在，或遠端印表機已不存在，則函式必須等待 RPC 超時，並導致 **OpenPrinter** 呼叫失敗。 這可能需要一段時間。 傳遞 **印表機 \_ 資訊 \_ 4** 結構，可讓應用程式取出最少的必要資訊; 如果需要更詳細的資訊，則可以進行後續的 **EnumPrinter** 層級2呼叫。

**屬性** 也可以包含在 [**印表機 \_ 資訊 \_ 2**] 的 [**屬性**] 欄位中定義的值。

某些印表機設定（例如，某些非 Windows 式列印伺服器的印表機連線）可能會同時傳回 **印表機 \_ 屬性 \_ 本機** 和 **印表機 \_ 屬性 \_ 網路**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>winspool.drv (包含 Windows .h) </dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **\_ 印表機 \_ 資訊 \_ 4W** (Unicode) 和 **\_ 印表機 \_ 資訊 \_ 4a** (ANSI) <br/>                           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 結構](printing-and-print-spooler-structures.md)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**>enumprinters**](enumprinters.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**印表機 \_ 資訊 \_ 1**](printer-info-1.md)
</dt> <dt>

[**印表機 \_ 資訊 \_ 2**](printer-info-2.md)
</dt> <dt>

[**印表機 \_ 資訊 \_ 3**](printer-info-3.md)
</dt> </dl>

 

 




