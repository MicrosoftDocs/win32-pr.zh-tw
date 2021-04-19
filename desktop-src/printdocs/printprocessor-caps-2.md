---
description: 代表印表機功能資訊。
ms.assetid: 70120739-a4e0-4b87-ac7a-40a42fb509ee
title: 'PRINTPROCESSOR_CAPS_2 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTPROCESSOR_CAPS_2
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 1847ffa1912a8638476ce80dfbdb71c40fc376d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984643"
---
# <a name="printprocessor_caps_2-structure"></a>PRINTPROCESSOR \_ CAPS \_ 2 結構

代表印表機功能資訊。

## <a name="syntax"></a>語法


```C++
typedef struct _PRINTPROCESSOR_CAPS_2 {
  DWORD dwLevel;
  DWORD dwNupOptions;
  DWORD dwPageOrderFlags;
  DWORD dwNumberOfCopies;
  DWORD dwNupDirectionCaps;
  DWORD dwNupBorderCaps;
  DWORD dwBookletHandlingCaps;
  DWORD dwDuplexHandlingCaps;
  DWORD dwScalingCaps;
} PRINTPROCESSOR_CAPS_2, *PPRINTPROCESSOR_CAPS_2;
```



## <a name="members"></a>成員

<dl> <dt>

**dwLevel**
</dt> <dd>

值，指出結構的版本號碼。

</dd> <dt>

**dwNupOptions**
</dt> <dd>

位元遮罩，代表印表機可在實體工作表的一端列印的各種檔頁面數目。 最不重要的位代表每一端的一個檔頁面，下一個位代表每一端的2個檔頁面等等。 例如，0x0000810B 指出印表機每個實體端支援1、2、4、9和16份檔頁面。

</dd> <dt>

**dwPageOrderFlags**
</dt> <dd>

旗標值，指出列印頁面的順序。 它可以是 **一般 \_ 列印**、 **反向 \_ 列印** 或 **手冊 \_ 列印**。

</dd> <dt>

**dwNumberOfCopies**
</dt> <dd>

印表機可以處理的最大複本數目。

</dd> <dt>

**dwNupDirectionCaps**
</dt> <dd>

當多個檔頁面列印在紙張紙的同一側時，可使用的模式。 可能的旗標如下：



| 值                     | 意義                                                                                             |
|---------------------------|-----------------------------------------------------------------------------------------------------|
| 向 \_ \_ 下 PPCAPS \_ | 頁面會由右至左顯示于資料列中，每個後續的資料列在其前置項下方。                 |
| \_向下 PPCAPS 到 \_ \_ 右邊 | 頁面會顯示在資料行中，從上到下，每個後續的資料行都在其前置項右邊。 |
| \_向 \_ \_ 下 PPCAPS  | 頁面會從左至右出現在資料列中，每個後續的資料列在其前置項下方。                 |
| \_向下 PPCAPS 至 \_ \_ 左方  | 頁面會出現在從上到下的資料行中，每個後續的資料行都會出現在其前身的左邊。  |



 

</dd> <dt>

**dwNupBorderCaps**
</dt> <dd>

只能是 PPCAPS \_ 框線 \_ 列印，表示當多個檔頁面列印在實體工作表的一側時，可以告知印表機是否要在每個檔頁面的可成像區域周圍列印框線。

</dd> <dt>

**dwBookletHandlingCaps**
</dt> <dd>

只能 PPCAPS \_ 手冊 \_ EDGE，指出印表機可以列印手冊樣式。

</dd> <dt>**dwDuplexHandlingCaps**</dt> <dd> 

| 值                                         | 意義                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ \_ \_ \_ 反向 \_ 雙工 PPCAPS 反轉頁面  | 以反向順序和雙工方式進行列印時，處理器可以列印每一對頁面的順序，而不是依順序4、3、2、1來列印，而是會列印順序3、4、1、2。                                                                                                       |
| PPCAPS \_ 不要 \_ 傳送 \_ 額外 \_ \_ 的頁面給 \_ 雙工 | 當雙工時，當有奇數的檔頁面時，可以通知列印處理器不要傳送額外的頁面。 處理器會盡可能發揮最大的價值，但如果防止額外的空白頁面造成不適當的輸出，可能仍會傳送額外的頁面。 |



 

</dd> <dt>

**dwScalingCaps**
</dt> <dd>

只能 PPCAPS \_ 正方形 \_ 調整，表示印表機可以調整頁面影像。

</dd> </dl>

## <a name="remarks"></a>備註

所有結構成員的值都是由 Windows 驅動程式套件中記載的 **GetPrintProcessorCapabilities** 函數所提供。

當應用程式呼叫 [**GetPrinterData**](getprinterdata.md)時，多工緩衝處理器會呼叫列印處理器的 **GetPrintProcessorCapabilities** 函式，並指定具有 **\_ PrintProcCaps**_datatype_ 格式的值名稱，其中 *datatype* 是輸入資料類型的名稱。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Winspool.drv (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 結構](printing-and-print-spooler-structures.md)
</dt> <dt>

[**GetPrinterData**](getprinterdata.md)
</dt> </dl>

 

 




