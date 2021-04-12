---
title: IMemoryAllocator 類別
description: 由 StgConvertPropertyToVariant 函式的記憶體配置器所執行。
ms.assetid: a0735b62-5ed3-42df-a320-b58c742645a8
keywords:
- IMemoryAllocator 類別結構化儲存體
- IMemoryAllocator 類別結構化儲存體，描述
topic_type:
- apiref
api_name:
- IMemoryAllocator
api_location:
- Ole32.lib
- Ole32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 421162fd0ee6228f1dbae03eeb52e5643b0e0b15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384765"
---
# <a name="imemoryallocator-class"></a>IMemoryAllocator 類別

**IMemoryAllocator** 類別是由 [**StgConvertPropertyToVariant**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant)函數的記憶體配置器所執行。

## <a name="methods"></a>方法



| 名稱                                                     | 描述                                                                                                                                                                                                        |
|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**分配**](imemoryallocator-allocate.md)<br/> | 當函數將 **SERIALIZEDPROPERTYVALUE** 資料類型轉換成 **PROPVARIANT** 資料類型時，為 [**StgConvertPropertyToVariant**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant)函數配置記憶體。<br/> |
| [**免費**](/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-initialize)<br/>        | 釋放由 [**配置方法配置**](imemoryallocator-allocate.md) 的記憶體。<br/>                                                                                                                 |



 

## <a name="remarks"></a>備註

只有 [**StgConvertPropertyToVariant**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant) 函式會使用這個類別。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 程式庫<br/>                  | <dl> <dt>Ole32.lib .lib</dt> </dl> |



 

