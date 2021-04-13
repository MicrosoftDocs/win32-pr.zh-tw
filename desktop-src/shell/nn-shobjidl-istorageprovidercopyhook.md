---
description: 定義方法，此方法會決定是否允許 Shell 移動、複製、刪除或重新命名雲端提供者的同步根中的資料夾。
title: IStorageProviderCopyHook 介面
ms.topic: reference
ms.date: 11/11/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- IStorageProviderCopyHook
api_type:
- COM
api_location:
- shobjidl.h
ms.openlocfilehash: 52f2a7fb7c8d7b37fc27fd1e91c93d716bc92086
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384402"
---
# <a name="istorageprovidercopyhook-interface"></a>IStorageProviderCopyHook 介面

公開方法，這個方法會判斷是否允許 Shell 移動、複製、刪除或重新命名雲端提供者的同步根中的資料夾。

## <a name="members"></a>成員

**IStorageProviderCopyHook** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **IStorageProviderCopyHook** 也有下列類型的成員：

- [方法](#methods)

### <a name="methods"></a>方法

**IStorageProviderCopyHook** 介面具有這些方法。



| 方法                                           | 描述                                                                                               |
|:-------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [**CopyCallback**](nf-shobjidl-istorageprovidercopyhook-copycallback.md)               |  決定是否允許 Shell 移動、複製、刪除或重新命名雲端提供者的同步根中的資料夾。                                                           |


## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端 | Windows 10 Insider Preview 組建19624                                                |
| 標頭<br/>                   | shobjidl.h。h   |
