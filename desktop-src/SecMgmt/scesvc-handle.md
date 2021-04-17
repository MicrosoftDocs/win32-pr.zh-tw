---
description: SCESVC \_ 控制碼資料類型是由安全性設定工具集所提供的不透明控制碼。
ms.assetid: 478d7d4b-7983-4247-b8be-2e2cd3327533
title: 'SCESVC_HANDLE (Scesvc) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09fbc115326361e4cbfe1152361a70a36007a302
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511166"
---
# <a name="scesvc_handle"></a>SCESVC \_ 控制碼

**SCESVC \_ 控制碼** 資料類型是由安全性設定工具集所提供的不透明控制碼。 [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata)和 [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo)介面的方法會使用它，在 [安全性設定] 嵌入式管理單元和嵌入式管理單元擴充功能之間傳遞資訊。


```C++
typedef PVOID SCESVC_HANDLE;
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Scesvc。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata)
</dt> <dt>

[**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo)
</dt> </dl>

 

 




