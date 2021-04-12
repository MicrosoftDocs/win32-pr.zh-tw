---
description: SCE \_ 列舉 \_ 內容資料類型是由安全性設定工具集所提供的不透明控制碼。 PFSCE \_ QUERY INFO 函數會使用它 \_ 來流覽安全性資料庫。
ms.assetid: 05629c49-e36b-4045-93d0-d0f4bc09b08a
title: 'SCE_ENUMERATION_CONTEXT (Scesvc) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e380f6f99d68ad63199c3b82f5aa1e5ace8ddf0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318223"
---
# <a name="sce_enumeration_context"></a>SCE \_ 列舉 \_ 內容

**SCE \_ 列舉 \_ 內容** 資料類型是由安全性設定工具集所提供的不透明控制碼。 [**PFSCE \_ QUERY \_ INFO**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info)函數會使用它來流覽安全性資料庫。


```C++
typedef ULONG SCE_ENUMERATION_CONTEXT, *PSCE_ENUMERATION_CONTEXT;
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
</dt> </dl>

 

