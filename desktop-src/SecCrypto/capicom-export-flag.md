---
description: CAPICOM \_ 匯出 \_ 旗標列舉型別會定義是否忽略任何私用金鑰匯出錯誤。
ms.assetid: 12e6862b-5c73-4e45-8829-8086048e94f3
title: 'CAPICOM_EXPORT_FLAG 列舉 (Capicom) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_EXPORT_FLAG
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: fe99b1123ae35083e5c59df37234821efd2db208
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990617"
---
# <a name="capicom_export_flag-enumeration"></a>CAPICOM \_ 匯出 \_ 旗標列舉

**CAPICOM \_ 匯出 \_ 旗** 標列舉型別會定義是否忽略任何私用金鑰匯出錯誤。

## <a name="members"></a>成員



| member                                                            | 描述                                               | 值 |
|-------------------------------------------------------------------|-----------------------------------------------------------|-------|
| **CAPICOM \_ 匯出 \_ 預設值**                                      | 不會忽略任何私用金鑰匯出錯誤。<br/> | 0     |
| **CAPICOM \_ 匯出 \_ 略 \_ 過 \_ 私密金鑰 \_ 不可 \_ 匯出的 \_ 錯誤** | 系統會忽略任何私用金鑰匯出錯誤。<br/>     | 1     |



## <a name="remarks"></a>備註

\_ \_ 下列方法會使用 CAPICOM 匯出旗標列舉類型：

-   [**憑證。儲存**](certificates-save.md)

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|--------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                |
| 標頭<br/>          | <dl> <dt>Capicom</dt> </dl> |



 

 




