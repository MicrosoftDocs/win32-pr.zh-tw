---
title: 'RPC_IF_HANDLE (Rpcdce) '
description: '\_如果 \_ 處理資料類型宣告介面控制碼，則為 RPC。'
ms.assetid: a85f3a44-7cdf-421f-a1e4-c67a9dd0c54d
keywords:
- RPC_IF_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4652fbd08c583ad0a33638e52face9569e6ff701cb6dc2b775c7060134b60437
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118926437"
---
# <a name="rpc_if_handle"></a>RPC \_ IF \_ 控制碼

**\_ 如果 \_ 處理** 資料類型宣告介面控制碼，則為 RPC。


```C++
typedef void __RPC_FAR* RPC_IF_HANDLE;
```



## <a name="remarks"></a>備註

RPC 執行時間程式庫會使用介面控制碼來存取介面規格資料結構。 MIDL 編譯器會自動從每個 IDL 檔案建立介面規格資料結構，並在 \_ 介面規格的控制碼中建立 RPC 型別的全域變數 \_ 。

MIDL 編譯器會在針對介面產生的每個標頭檔中包含介面控制碼。 需要介面規格做為參數的函式會顯示 RPC 的資料類型（ **\_ 如果是 \_ 控制碼**）。 每個介面控制碼名稱的形式如下：

-   *if-name* \_用戶端) 的 ClientIfHandle (
-   *if-name* \_ServerIfHandle 伺服器) 的 (

*If-name* 部分指定 IDL 檔案中的介面識別碼。

例如：

hello \_ ClientIfHandle

hello \_ ServerIfHandle

> [!Note]  
> 介面控制碼名稱的最大長度是31個字元。

 

因為名稱的 " \_ ClientIfHandle" 和 " \_ ServerIfHandle" 部分需要15個字元，所以 *name* 元素的長度不能超過16個字元。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                |
| 標頭<br/>                   | <dl> <dt>Rpcdce (包含 Rpc) </dt> </dl> |



 

 





