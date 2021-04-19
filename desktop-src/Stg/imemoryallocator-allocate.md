---
title: IMemoryAllocator 配置方法
description: 當函數將 SERIALIZEDPROPERTYVALUE 資料類型轉換成 PROPVARIANT 資料類型時，配置方法會為 StgConvertPropertyToVariant 函數配置記憶體。
ms.assetid: aa9c9308-fb55-405c-901a-9d5abfac5395
keywords:
- 配置方法結構化儲存體
- 配置方法結構化儲存體、IMemoryAllocator 介面
- IMemoryAllocator 介面結構化儲存體，配置方法
topic_type:
- apiref
api_name:
- IMemoryAllocator.Allocate
api_location:
- Ole32.lib
- Ole32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7ee4b220e1c1e14ceed685e9b2adc694a44d2e4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967310"
---
# <a name="imemoryallocatorallocate-method"></a>IMemoryAllocator：： Allocate 方法

當函數將 **SERIALIZEDPROPERTYVALUE** 資料類型轉換成 **PROPVARIANT** 資料類型時，配置方法會為 [**StgConvertPropertyToVariant**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant)函數 **配置** 記憶體。

## <a name="syntax"></a>語法


```C++
virtual void* Allocate(
  [in] ULONG cbSize
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*cbSize* \[在\]
</dt> <dd>

指定要配置的記憶體大小。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 程式庫<br/>                  | <dl> <dt>Ole32.lib .lib</dt> </dl> |



 

