---
title: WMDMDATETIME 結構
description: WMDMDATETIME 結構包含一天的日期和時間。
ms.assetid: 47f3994d-66c6-47e4-803d-0c98c70eccc8
keywords:
- WMDMDATETIME 結構 windows Media 裝置管理員
- PWMDMDATETIME 結構指標 windows Media 裝置管理員
topic_type:
- apiref
api_name:
- WMDMDATETIME
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07acf706aa63a21edd27fb2ac206db3039249055
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999090"
---
# <a name="wmdmdatetime-structure"></a>WMDMDATETIME 結構

**WMDMDATETIME** 結構包含一天的日期和時間。

## <a name="syntax"></a>語法


```C++
typedef struct _WMDMDATETIME {
  WORD wYear;
  WORD wMonth;
  WORD wDay;
  WORD wHour;
  WORD wMinute;
  WORD wSecond;
} WMDMDATETIME, *PWMDMDATETIME;
```



## <a name="members"></a>成員

<dl> <dt>

**Daylightdate.wyear**
</dt> <dd>

包含四位數年份的單字。

</dd> <dt>

**wMonth**
</dt> <dd>

包含月份 (1-12) 的單字。

</dd> <dt>

**wDay**
</dt> <dd>

包含當月日期的單字 (1-31) 。

</dd> <dt>

**wHour**
</dt> <dd>

包含小時 (0-23) 的單字。

</dd> <dt>

**wMinute**
</dt> <dd>

包含分鐘 (0-59) 的單字。

</dd> <dt>

**wSecond**
</dt> <dd>

包含第二個 (0-59) 的單字。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wmdm .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMDSPStorage：： GetDate**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getdate)
</dt> <dt>

[**IWMDMStorage：： GetDate**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getdate)
</dt> <dt>

[**WMDMRIGHTS**](wmdmrights.md)
</dt> <dt>

[**結構**](structures.md)
</dt> </dl>

 

 





