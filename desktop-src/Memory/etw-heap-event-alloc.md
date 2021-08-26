---
description: 堆積配置作業的記憶體管理追蹤事件。
ms.assetid: 572DEC3B-F909-45E5-849F-707AA62F2F5E
title: 'ETW_HEAP_EVENT_ALLOC (Ntwmi 的事件) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ETW_HEAP_EVENT_ALLOC
api_type:
- HeaderDef
api_location:
- ntwmi.h
ms.openlocfilehash: 111c9268cb6ad174dc79323a9b867923e6264428f939caeae7089685e62f4318
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963198"
---
# <a name="etw_heap_event_alloc-event"></a>ETW \_ 堆積 \_ 事件 \_ 分配事件

**ETW \_ 堆積 \_ 事件 \_ 分配** 事件是堆積配置作業的記憶體管理追蹤事件。


```C++
typedef struct ETW_HEAP_EVENT_ALLOC
```



## <a name="parameters"></a>參數

<dl> <dt>

*HeapHandle* 
</dt> <dd>

配置記憶體之堆積的控制碼。 這是在配置記憶體時，處理傳遞至 [**AllocateHeap**](/previous-versions/windows/desktop/legacy/aa374721(v=vs.85)) 函式的應用程式的堆積。

</dd> <dt>

*大小* 
</dt> <dd>

從堆積配置的大小（以位元組為單位）。

</dd> <dt>

*位址* 
</dt> <dd>

已配置之記憶體的位址。

</dd> <dt>

*來源* 
</dt> <dd>

配置器用於堆積配置的記憶體來源。

下表列出 *ntetw .h* 標頭檔中所定義之 *Source* 參數的可能值：



| 值                                                                                                                                                                                                                                                                               | 意義                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="MEMORY_FROM_LOOKASIDE"></span><span id="memory_from_lookaside"></span><dl> <dt>**記憶體 \_從 \_ 對應**</dt> <dt>1</dt> </dl>                                       | 對應清單中的記憶體。<br/>                                   |
| <span id="MEMORY_FROM_LOWFRAG"></span><span id="memory_from_lowfrag"></span><dl> <dt>**記憶體 \_從 \_ LOWFRAG**</dt> <dt>2</dt> </dl>                                             | 來自低片段堆積的記憶體。<br/>                           |
| <span id="MEMORY_FROM_MAINPATH"></span><span id="memory_from_mainpath"></span><dl> <dt>**記憶體 \_從 \_ MAINPATH**</dt> <dt>3</dt> </dl>                                          | 主要程式碼路徑中的記憶體。<br/>                                       |
| <span id="MEMORY_FROM_SLOWPATH____________________"></span><span id="memory_from_slowpath____________________"></span><dl> <dt> **\_ \_ SLOWPATH 4 的記憶體**</dt> <dt></dt> </dl> | 來自慢速路徑的記憶體。<br/>                                            |
| <span id="MEMORY_FROM_INVALID"></span><span id="memory_from_invalid"></span><dl> <dt>**記憶體 \_從 \_ 不正確**</dt> <dt>5</dt> </dl>                                             | 不正確記憶體。<br/>                                        |
| <span id="MEMORY_FROM_SEGMENT_HEAP"></span><span id="memory_from_segment_heap"></span><dl> <dt>**記憶體 \_從 \_ 區段 \_ 堆積**</dt> <dt>6</dt> </dl>                             | 此值已保留供日後使用，且永遠不會傳回。<br/> |



 

</dd> </dl>

## <a name="remarks"></a>備註

**ETW \_ 堆積 \_ 事件 \_ 分配** 事件會記錄在所有堆積配置上。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/>                            |
| 標頭<br/>                   | <dl> <dt>Ntwmi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[記憶體管理追蹤事件](memory-management-tracing-events.md)
</dt> </dl>

 

 
