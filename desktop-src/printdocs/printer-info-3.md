---
description: 印表機 \_ 資訊 \_ 3 結構會指定印表機安全性資訊。
ms.assetid: 527d635d-2d75-4b56-bab7-e95c9919a8fb
title: 'PRINTER_INFO_3 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_3
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: c6b9bc249921b3247f5df898c2810d735dc1a75c8e643e965b3fd249d9496f78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117867923"
---
# <a name="printer_info_3-structure"></a>印表機 \_ 資訊 \_ 3 結構

**印表機 \_ 資訊 \_ 3** 結構會指定印表機安全性資訊。

## <a name="syntax"></a>語法


```C++
typedef struct _PRINTER_INFO_3 {
  PSECURITY_DESCRIPTOR pSecurityDescriptor;
} PRINTER_INFO_3, *PPRINTER_INFO_3;
```



## <a name="members"></a>成員

<dl> <dt>

**pSecurityDescriptor**
</dt> <dd>

[**安全 \_ 描述項**](/windows/desktop/api/winnt/ns-winnt-security_descriptor)結構的指標，指定印表機的安全性資訊。

</dd> </dl>

## <a name="remarks"></a>備註

**印表機 \_ 資訊 \_ 3** 結構可讓應用程式取得和設定印表機的安全描述項。 即使它缺少特定的印表機權限，呼叫者仍可能這麼做，只要它具有 [**SetPrinter**](setprinter.md) 和 [**GetPrinter**](getprinter.md)中所述的標準許可權即可。 因此，應用程式可能會暫時拒絕印表機的所有存取，同時允許印表機的擁有者存取印表機的任意 ACL。

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

[**SetPrinter**](setprinter.md)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**印表機 \_ 資訊 \_ 1**](printer-info-1.md)
</dt> <dt>

[**印表機 \_ 資訊 \_ 2**](printer-info-2.md)
</dt> <dt>

[**印表機 \_ 資訊 \_ 4**](printer-info-4.md)
</dt> <dt>

[**安全 \_ 描述項**](/windows/desktop/api/winnt/ns-winnt-security_descriptor)
</dt> </dl>

 

