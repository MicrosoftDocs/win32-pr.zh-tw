---
description: PRINTPROCESSOR \_ CAPS \_ 1 結構是在 .pdata 變數所指定的緩衝區中，GetPrinterData 函式所傳回之印表機功能資訊的格式。
ms.assetid: 43c568ff-ccc9-4873-b159-ede09b4a7e51
title: 'PRINTPROCESSOR_CAPS_1 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTPROCESSOR_CAPS_1
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: d057914ef9a77c7a545817b205f919afa66fdd3bc154363f7e33a9a5ba43c446
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119824788"
---
# <a name="printprocessor_caps_1-structure"></a>PRINTPROCESSOR \_ CAPS \_ 1 結構

**PRINTPROCESSOR \_ CAPS \_ 1** 結構是在 *.pdata* 變數所指定的緩衝區中， [**GetPrinterData**](getprinterdata.md)函式所傳回之印表機功能資訊的格式。

## <a name="syntax"></a>語法


```C++
typedef struct _PRINTPROCESSOR_CAPS_1 {
  DWORD dwLevel;
  DWORD dwNupOptions;
  DWORD dwPageOrderFlags;
  DWORD dwNumberOfCopies;
} PRINTPROCESSOR_CAPS_1, *PPRINTPROCESSOR_CAPS_1;
```



## <a name="members"></a>成員

<dl> <dt>

**dwLevel**
</dt> <dd>

結構的版本號碼。 此值必須是1。

</dd> <dt>

**dwNupOptions**
</dt> <dd>

位元遮罩，代表印表機可在實體頁面上列印的各種檔頁面數目。 最不重要的位代表每個頁面1個檔頁面，下一個位代表每頁2份檔頁面等等。 例如，0x0000810B 表示印表機支援每個實體頁面1、2、4、9和16份檔頁面。

</dd> <dt>

**dwPageOrderFlags**
</dt> <dd>

列印頁面的順序。 此值可以是一般 \_ 列印、反向 \_ 列印或手冊 \_ 列印。

</dd> <dt>

**dwNumberOfCopies**
</dt> <dd>

印表機可以處理的最大複本數目。

</dd> </dl>

## <a name="remarks"></a>備註

所有結構成員的值都是由 [**GetPrintProcessorCapabilities**](/windows-hardware/drivers/ddi/content/winsplp/nf-winsplp-getprintprocessorcapabilities)函式所提供，此函數記載于 Windows 驅動程式套件 (WDK) 中。

當應用程式呼叫 [**GetPrinterData**](getprinterdata.md)，以 [](/windows-hardware/drivers/ddi/content/winsplp/nf-winsplp-getprintprocessorcapabilities) PrintProcCaps datatype 的格式指定值名稱 \_ **（其中 *datatype* 是輸入資料類型的名稱）時，多工緩衝處理器會呼叫列印處理器的 GetPrintProcessorCapabilities 函式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>winspool.drv (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 結構](printing-and-print-spooler-structures.md)
</dt> <dt>

[**GetPrinterData**](getprinterdata.md)
</dt> </dl>

 

