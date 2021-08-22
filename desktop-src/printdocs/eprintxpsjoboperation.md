---
description: 指定 XPS 列印工作是否在幕後處理或轉譯階段。
ms.assetid: 14871d29-59e4-45a2-9697-12550c58396c
title: 'EPrintXPSJobOperation 列舉 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EPrintXPSJobOperation
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 44f1f7ed80cd1de071633de37c5f0e91e913841388754a65c0194665bd3084de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971537"
---
# <a name="eprintxpsjoboperation-enumeration"></a>EPrintXPSJobOperation 列舉

指定 XPS 列印工作是否在幕後處理或轉譯階段。

## <a name="syntax"></a>Syntax


```C++
typedef enum tagEPrintXPSJobOperation { 
  kJobProduction,
  kJobConsumption
} EPrintXPSJobOperation;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="kJobProduction"></span><span id="kjobproduction"></span><span id="KJOBPRODUCTION"></span>**kJobProduction**
</dt> <dd>

XPS 工作為幕後處理。

</dd> <dt>

<span id="kJobConsumption"></span><span id="kjobconsumption"></span><span id="KJOBCONSUMPTION"></span>**kJobConsumption**
</dt> <dd>

XPS 工作正在呈現。

</dd> </dl>

## <a name="remarks"></a>備註

這個列舉主要是用來做為 [**ReportJobProcessingProgress**](reportjobprocessingprogress.md) 函式的參數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                            |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>winspool.drv (包含 Windows .h) </dt> </dl> |



 

 




