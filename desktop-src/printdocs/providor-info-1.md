---
description: PROVIDOR \_ INFO \_ 1 結構會識別列印提供者。
ms.assetid: 0eff115a-b3d2-4c8f-b820-46e7f62dd295
title: 'PROVIDOR_INFO_1 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROVIDOR_INFO_1
- _PROVIDOR_INFO_1A
- _PROVIDOR_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 4f9e7015382ef34f4582c4772e148059c4ed01de9e81da5af71bc0849df26f15
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120091698"
---
# <a name="providor_info_1-structure"></a>PROVIDOR \_ INFO \_ 1 結構

**PROVIDOR \_ INFO \_ 1** 結構會識別列印提供者。

## <a name="syntax"></a>語法


```C++
typedef struct _PROVIDOR_INFO_1 {
  LPTSTR pName;
  LPTSTR pEnvironment;
  LPTSTR pDLLName;
} PROVIDOR_INFO_1, *PPROVIDOR_INFO_1;
```



## <a name="members"></a>成員

<dl> <dt>

**pName**
</dt> <dd>

以 null 結束的字串指標，該字串是列印提供者的名稱。

</dd> <dt>

**pEnvironment**
</dt> <dd>

以 null 結束的環境字串指標，指定環境：提供者動態連結程式庫 (DLL) 是設計用來執行。

</dd> <dt>

**pDLLName**
</dt> <dd>

以 null 結束的字串指標，這是提供者 .dll 的名稱。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>winspool.drv (包含 Windows .h) </dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **\_ PROVIDOR \_ Info \_ 1W** (Unicode) 和 **\_ PROVIDOR \_ info \_ 1a** (ANSI) <br/>                         |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 結構](printing-and-print-spooler-structures.md)
</dt> <dt>

[**AddPrintProvidor**](addprintprovidor.md)
</dt> </dl>

 

 




