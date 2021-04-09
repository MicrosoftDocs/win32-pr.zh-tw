---
title: 'RPC_STATUS (Rpcdce) '
description: 資料類型 RPC \_ 狀態代表平臺特定的狀態碼類型。
ms.assetid: 0f929916-f3aa-477f-9c61-742f3fbbab29
keywords:
- RPC_STATUS
- RPC_STATUS
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 066022ce33676caadcf25a6814f3b4974701998e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025062"
---
# <a name="rpc_status"></a>RPC \_ 狀態

資料類型 **RPC \_ 狀態** 代表平臺特定的狀態碼類型。


```C++
typedef long RPC_STATUS;
typedef unsigned short RPC_STATUS;
```



## <a name="remarks"></a>備註

**Rpc \_ 狀態** 類型是由大部分 rpc 函式傳回，而且屬於 [**rpc \_ 物件 \_ INQ \_ FN**](/windows/desktop/api/Rpcdce/nc-rpcdce-rpc_object_inq_fn)函數類型定義的一部分。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                |
| 標頭<br/>                   | <dl> <dt>Rpcdce (包含 Rpc) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**RPC \_ 物件 \_ INQ \_ FN**](/windows/desktop/api/Rpcdce/nc-rpcdce-rpc_object_inq_fn)
</dt> </dl>

 

 





