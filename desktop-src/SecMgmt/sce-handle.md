---
description: SCE \_ 控制碼資料類型是由安全性設定工具集所提供的不透明控制碼。 PFSCE \_ 查詢 \_ 資訊和 PFSCE 設定資訊支援函式會使用它 \_ \_ 來傳遞附件和安全性資料庫之間的資訊。
ms.assetid: 8db91e6f-b31e-40c6-a158-b4b3b00ba0c0
title: 'SCE_HANDLE (Scesvc) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fef21dbe03d97dfa14537d5df132ba3cb222643
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112657"
---
# <a name="sce_handle"></a>SCE \_ 把手

**SCE \_ 控制碼** 資料類型是由安全性設定工具集所提供的不透明控制碼。 [**PFSCE \_ 查詢 \_ 資訊**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info)和 [**PFSCE \_ 設定 \_ 資訊**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info)支援函式會使用它來傳遞附件和安全性資料庫之間的資訊。


```C++
typedef PVOID SCE_HANDLE;
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Scesvc。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**PFSCE \_ 查詢 \_ 資訊**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info)
</dt> <dt>

[**PFSCE \_ 設定 \_ 資訊**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info)
</dt> </dl>

 

