---
title: IMemoryAllocator Free 方法
description: Free 方法會釋出配置方法所配置的記憶體。
ms.assetid: 41f81cba-4431-4ff7-ac84-8ff5bea71b65
keywords:
- 自由方法結構化儲存體
- 自由方法結構化儲存體、IMemoryAllocator 介面
- IMemoryAllocator 介面結構化儲存體，免費方法
topic_type:
- apiref
api_name:
- IMemoryAllocator.Free
api_location:
- Ole32.lib
- Ole32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c07731f60aba7d847c79467b2b2c166b363d807
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024694"
---
# <a name="imemoryallocatorfree-method"></a>IMemoryAllocator：： Free 方法

**Free** 方法會釋出配置方法所 [**配置**](imemoryallocator-allocate.md)的記憶體。

## <a name="syntax"></a>語法


```C++
virtual void Free(
   void* pv
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*光伏* 
</dt> <dd>

要釋放之記憶體的指標。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 程式庫<br/>                  | <dl> <dt>Ole32.lib .lib</dt> </dl> |



 

 





